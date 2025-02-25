---
layout: document
title: "Secure Development Handbook"
permalink: /guides/isms-guide-03/
---

# Enablis Secure Development Handbook

**Document ID**: ISMS-GUIDE-03  
**Version**: 1.0  
**Last Updated**: February 25, 2025  
**Owner**: Chief Technology Officer  
**Approved by**: Board of Directors

## 1. Introduction

### 1.1 Purpose

This Secure Development Handbook provides practical guidance for building secure applications and systems at Enablis. It offers actionable techniques, code examples, and best practices to help developers integrate security throughout the software development lifecycle.

### 1.2 How to Use This Handbook

This handbook is designed as a practical reference rather than policy documentation. It provides:

- Actionable security techniques with code examples
- Language-specific security guidance
- Practical approaches to common security challenges
- Tools and resources for implementation

Use this handbook as a reference during design, development, and testing phases. Apply the techniques that are relevant to your specific project needs while maintaining the security principles.

### 1.3 Security by Design Philosophy

At Enablis, we believe in building security in from the start, not bolting it on later. This means:

- Considering security requirements during initial design
- Including security activities in each development phase
- Making security a natural part of development, not a separate activity
- Automating security checks where possible
- Continuously improving our security approach

## 2. Secure Design Principles

### 2.1 Core Security Principles

#### 2.1.1 Defense in Depth

Implement multiple security controls so that if one fails, others will still provide protection.

**Examples:**

- Implement network security, application security, and data security
- Use input validation at multiple layers (client, API, database)
- Combine authentication, authorization, and audit controls

**Practical Implementation:**

```javascript
// Example: Multiple validation layers
// 1. Client-side validation (for user experience)
function validateClientSide(input) {
  if (!/^[a-zA-Z0-9]{5,20}$/.test(input)) {
    showError("Invalid format");
    return false;
  }
  return true;
}

// 2. API validation (for security)
function validateServerSide(input) {
  // Never trust client-side validation
  if (typeof input !== "string" || !/^[a-zA-Z0-9]{5,20}$/.test(input)) {
    return { valid: false, error: "Invalid format" };
  }
  return { valid: true };
}

// 3. Database parameterized query (for SQL injection protection)
// Using prepared statements with parameters
const query = "SELECT * FROM users WHERE username = ?";
database.execute(query, [sanitizedInput]);
```

#### 2.1.2 Least Privilege

Grant the minimum access necessary to perform a function.

**Examples:**

- Use read-only database access for reporting features
- Implement role-based access with fine-grained permissions
- Use time-limited elevated access for administrative functions

**Practical Implementation:**

```typescript
// Example: Role-based API access with fine-grained permissions
enum Permission {
  VIEW_RECORDS,
  CREATE_RECORDS,
  UPDATE_RECORDS,
  DELETE_RECORDS,
  ADMIN_FUNCTIONS,
}

function checkPermission(user: User, requiredPermission: Permission): boolean {
  return user.permissions.includes(requiredPermission);
}

// Usage in API endpoint
function updateRecord(user: User, recordId: string, data: any): void {
  if (!checkPermission(user, Permission.UPDATE_RECORDS)) {
    throw new Error("Unauthorized: Missing required permission");
  }

  // Proceed with update
  recordService.update(recordId, data);
}
```

#### 2.1.3 Secure Defaults

Make the default configuration secure, requiring explicit actions to reduce security.

**Examples:**

- Enable HTTPS by default
- Apply strict content security policies by default
- Start with restrictive permissions that must be explicitly loosened

**Practical Implementation:**

```typescript
// Example: Secure cookie defaults
function createSessionCookie(sessionId: string): Cookie {
  return {
    name: "session",
    value: sessionId,
    httpOnly: true, // Default: Not accessible via JavaScript
    secure: true, // Default: Only sent over HTTPS
    sameSite: "strict", // Default: Not sent in cross-site requests
    path: "/",
    maxAge: 3600, // Default: Expires in 1 hour
  };
}

// Explicit action needed to make less secure (not recommended)
function createLessSecureCookie(
  sessionId: string,
  options: Partial<Cookie>
): Cookie {
  // Requires explicit override, logged for security review
  logger.warn("Creating cookie with non-default security settings", {
    options,
  });
  return { ...createSessionCookie(sessionId), ...options };
}
```

#### 2.1.4 Fail Secure

When a system fails or encounters an error, it should default to a secure state.

**Examples:**

- Deny access when authentication systems are unavailable
- Reject transactions when validation fails
- Prevent file access when authorization checks encounter errors

**Practical Implementation:**

```java
// Example: Fail secure during authorization
public boolean hasAccess(User user, Resource resource) {
    try {
        // Attempt to check permissions
        return permissionService.checkAccess(user, resource);
    } catch (Exception e) {
        // Log the error
        logger.error("Error checking permissions", e);

        // Fail secure - deny access on error
        return false;
    }
}
```

### 2.2 Threat Modeling

#### 2.2.1 Simplified Threat Modeling

A lightweight approach to identify security risks:

1. **Identify assets**: What are you protecting?
2. **Create a system diagram**: How does data flow through the system?
3. **Identify threats**: What could go wrong?
4. **Mitigate risks**: How will you address the threats?
5. **Validate**: Did you miss anything?

**Practical Tips:**

- Focus on high-value assets and data flows
- Use the STRIDE framework to identify threat categories:
  - **S**poofing: Impersonating someone else
  - **T**ampering: Modifying data or code
  - **R**epudiation: Denying having performed an action
  - **I**nformation disclosure: Exposing sensitive information
  - **D**enial of service: Making a system unavailable
  - **E**levation of privilege: Gaining additional access

**Simplified Template:**

```
Asset: [Name]
Description: [Brief description]
Classification: [Public/Internal/Confidential]
Threats:
  1. [Threat description]
     - Impact: [High/Medium/Low]
     - Likelihood: [High/Medium/Low]
     - Mitigation: [How you'll address it]
  2. [Additional threats...]
```

#### 2.2.2 MACH Architecture Considerations

When working with MACH architecture (Microservices, API-first, Cloud-native, Headless), consider:

**Microservices Security:**

- Service-to-service authentication
- API gateway security
- Service boundary protection
- Distributed logging and monitoring

**API Security:**

- API authentication and authorization
- Input validation and output encoding
- Rate limiting and throttling
- API versioning security

**Cloud-Native Security:**

- Container security
- Serverless function security
- Cloud service configuration
- Infrastructure as code security

**Headless Security:**

- Frontend/backend separation security
- Cross-site scripting protection
- Content security policies
- Authentication token handling

## 3. Secure Coding Practices

### 3.1 Input Validation

#### 3.1.1 General Principles

- Validate all input regardless of source
- Use allowlist validation (define what's allowed) rather than blocklist (what's forbidden)
- Validate data type, length, format, and range
- Apply validation server-side (client-side is for UX only)
- Use structured data validation libraries when possible

**Practical Implementation:**

```typescript
// Example: Using a validation library (Zod)
import { z } from "zod";

// Define validation schema
const UserSchema = z.object({
  username: z
    .string()
    .min(5)
    .max(20)
    .regex(/^[a-zA-Z0-9]+$/),
  email: z.string().email(),
  age: z.number().int().min(18).max(120).optional(),
  role: z.enum(["user", "admin", "editor"]),
});

// Validate input with type safety
function processUserInput(input: unknown) {
  try {
    // This validates and provides type safety
    const user = UserSchema.parse(input);

    // If we get here, input is valid and typed
    saveUser(user);

    return { success: true };
  } catch (error) {
    if (error instanceof z.ZodError) {
      return {
        success: false,
        errors: error.errors.map((e) => ({
          field: e.path.join("."),
          message: e.message,
        })),
      };
    }
    throw error;
  }
}
```

#### 3.1.2 Input Sanitization

Sanitization is the process of cleaning or transforming input to make it safe:

**When to use:**

- When allowing HTML or markdown in user input
- Before displaying user-provided content
- When storing data that will be rendered later

**Practical Implementation:**

```javascript
// Example: Sanitizing HTML input using DOMPurify
import DOMPurify from "dompurify";

function sanitizeHtml(unsafeHtml) {
  // Only allow specific tags and attributes
  const config = {
    ALLOWED_TAGS: ["b", "i", "em", "strong", "a", "p", "ul", "ol", "li"],
    ALLOWED_ATTR: ["href", "title", "target"],
  };

  // Sanitize and return the safe HTML
  return DOMPurify.sanitize(unsafeHtml, config);
}

// Usage
const userComment = getUserInput();
const safeComment = sanitizeHtml(userComment);
document.getElementById("comments").innerHTML = safeComment;
```

### 3.2 Authentication and Authorization

#### 3.2.1 Authentication Best Practices

- Use multi-factor authentication where possible
- Implement secure password handling
- Use time-limited authentication tokens
- Implement secure session management
- Consider passwordless options where appropriate

**Practical Implementation:**

```typescript
// Example: Secure password handling
import * as bcrypt from "bcrypt";

async function hashPassword(password: string): Promise<string> {
  // Use a high cost factor for security (adjust based on performance needs)
  const saltRounds = 12;
  return await bcrypt.hash(password, saltRounds);
}

async function verifyPassword(
  password: string,
  hash: string
): Promise<boolean> {
  return await bcrypt.compare(password, hash);
}

// Example: Secure JWT token generation
import * as jwt from "jsonwebtoken";

function generateToken(userId: string, role: string): string {
  // Short expiration time for security
  return jwt.sign({ userId, role }, process.env.JWT_SECRET, {
    expiresIn: "1h",
    notBefore: 0, // Valid immediately
    audience: "api.enablis.co",
    issuer: "auth.enablis.co",
  });
}
```

#### 3.2.2 Authorization Patterns

- Implement role-based access control (RBAC)
- Consider attribute-based access control (ABAC) for complex scenarios
- Centralize authorization logic
- Validate authorization at each request
- Implement least privilege by default

**Practical Implementation:**

```typescript
// Example: Policy-based authorization
interface AuthorizationPolicy {
  canAccess(user: User, resource: Resource, action: string): boolean;
}

// Specific policies
class ProjectPolicy implements AuthorizationPolicy {
  canAccess(user: User, project: Project, action: string): boolean {
    switch (action) {
      case "view":
        return project.members.includes(user.id) || project.isPublic;
      case "edit":
        return project.members.includes(user.id) && user.role !== "viewer";
      case "delete":
        return project.ownerId === user.id || user.role === "admin";
      default:
        return false;
    }
  }
}

// Centralized authorization service
class AuthorizationService {
  private policies: Map<string, AuthorizationPolicy> = new Map();

  registerPolicy(resourceType: string, policy: AuthorizationPolicy): void {
    this.policies.set(resourceType, policy);
  }

  authorize(user: User, resource: any, action: string): boolean {
    const resourceType = resource.constructor.name;
    const policy = this.policies.get(resourceType);

    if (!policy) {
      logger.warn(`No policy found for ${resourceType}`);
      return false; // Fail secure
    }

    return policy.canAccess(user, resource, action);
  }
}

// Usage
const authService = new AuthorizationService();
authService.registerPolicy("Project", new ProjectPolicy());

// In API endpoint
function updateProject(user: User, projectId: string, data: any): void {
  const project = projectService.getProject(projectId);

  if (!authService.authorize(user, project, "edit")) {
    throw new Error("Unauthorized");
  }

  // Proceed with update
  projectService.update(projectId, data);
}
```

### 3.3 Data Protection

#### 3.3.1 Encryption Best Practices

- Use modern, standard encryption algorithms
- Don't implement custom encryption
- Use appropriate key management
- Implement encryption at rest and in transit
- Consider field-level encryption for sensitive data

**Practical Implementation:**

```typescript
// Example: Data encryption with Node.js crypto
import * as crypto from "crypto";

// Encryption helper
class Encryption {
  private algorithm = "aes-256-gcm";
  private keyLength = 32; // 256 bits
  private ivLength = 16; // 128 bits
  private tagLength = 16; // 128 bits

  // Encrypt data
  encrypt(text: string, key: Buffer): string {
    // Generate random initialization vector
    const iv = crypto.randomBytes(this.ivLength);

    // Create cipher
    const cipher = crypto.createCipheriv(this.algorithm, key, iv);

    // Encrypt data
    let encrypted = cipher.update(text, "utf8", "hex");
    encrypted += cipher.final("hex");

    // Get authentication tag
    const tag = cipher.getAuthTag();

    // Return iv + tag + encrypted data
    return iv.toString("hex") + ":" + tag.toString("hex") + ":" + encrypted;
  }

  // Decrypt data
  decrypt(encrypted: string, key: Buffer): string {
    // Split components
    const parts = encrypted.split(":");
    const iv = Buffer.from(parts[0], "hex");
    const tag = Buffer.from(parts[1], "hex");
    const ciphertext = parts[2];

    // Create decipher
    const decipher = crypto.createDecipheriv(this.algorithm, key, iv);
    decipher.setAuthTag(tag);

    // Decrypt data
    let decrypted = decipher.update(ciphertext, "hex", "utf8");
    decrypted += decipher.final("utf8");

    return decrypted;
  }

  // Generate a new encryption key
  generateKey(): Buffer {
    return crypto.randomBytes(this.keyLength);
  }
}
```

#### 3.3.2 Sensitive Data Handling

- Identify and classify sensitive data
- Minimize sensitive data collection and storage
- Implement appropriate access controls
- Apply data masking for display
- Consider data tokenization for storage

**Practical Implementation:**

```typescript
// Example: Data masking
function maskPII(data: string, type: "email" | "card" | "phone"): string {
  switch (type) {
    case "email":
      // Convert user@example.com to u**r@example.com
      const [username, domain] = data.split("@");
      const firstChar = username.charAt(0);
      const lastChar = username.charAt(username.length - 1);
      return `${firstChar}${"*".repeat(
        username.length - 2
      )}${lastChar}@${domain}`;

    case "card":
      // Convert 4111111111111111 to ************1111
      return data.replace(/\d(?=\d{4})/g, "*");

    case "phone":
      // Convert +1234567890 to +1******7890
      return data.replace(/(\+\d{1,3})(\d{6})(\d{4})/, "$1******$3");

    default:
      throw new Error(`Unsupported masking type: ${type}`);
  }
}

// Example: Tokenization service stub
class TokenizationService {
  private tokenStore = new Map<string, string>();

  tokenize(sensitiveData: string): string {
    // Generate a random token
    const token = crypto.randomBytes(16).toString("hex");

    // Store the mapping
    this.tokenStore.set(token, sensitiveData);

    return token;
  }

  detokenize(token: string): string | null {
    return this.tokenStore.get(token) || null;
  }
}
```

### 3.4 Error Handling and Logging

#### 3.4.1 Secure Error Handling

- Never expose sensitive information in error messages
- Implement different error handling for development and production
- Use generic error messages for users
- Log detailed errors for debugging
- Consider centralized error handling

**Practical Implementation:**

```typescript
// Example: Centralized error handling in Express
import { Request, Response, NextFunction } from "express";

// Custom error class with security classification
class AppError extends Error {
  constructor(
    public message: string,
    public statusCode: number = 500,
    public isOperational: boolean = true, // Operational errors are expected and can be handled
    public exposable: boolean = false // Whether error details can be exposed to users
  ) {
    super(message);
    Error.captureStackTrace(this, this.constructor);
  }
}

// Error handling middleware
function errorHandler(
  err: Error | AppError,
  req: Request,
  res: Response,
  next: NextFunction
) {
  // Default error
  let statusCode = 500;
  let message = "Something went wrong";
  let details = undefined;

  // Handle known AppError instances
  if (err instanceof AppError) {
    statusCode = err.statusCode;

    // Only expose details for exposable errors
    if (err.exposable) {
      message = err.message;
    }
  }

  // In development, provide more details
  if (process.env.NODE_ENV === "development") {
    details = {
      message: err.message,
      stack: err.stack,
      name: err.name,
    };
  }

  // Log error for internal debugging
  logger.error("Error caught in global handler", {
    url: req.url,
    method: req.method,
    statusCode,
    message: err.message,
    stack: err.stack,
    userId: req.user?.id,
  });

  // Send appropriate response
  res.status(statusCode).json({
    status: "error",
    message,
    details,
  });
}

// Usage in routes
app.get("/api/resource/:id", (req, res, next) => {
  try {
    // Resource not found - operational error, can be exposed
    if (!resource) {
      throw new AppError("Resource not found", 404, true, true);
    }

    // Database error - operational but not exposable
    if (dbError) {
      throw new AppError("Database error", 500, true, false);
    }

    res.json(resource);
  } catch (err) {
    next(err); // Pass to error handler
  }
});
```

#### 3.4.2 Secure Logging

- Never log sensitive data (passwords, tokens, PII)
- Implement appropriate log levels
- Structure logs for better analysis
- Secure log storage and transmission
- Consider log rotation and retention policies

**Practical Implementation:**

```typescript
// Example: Structured logging with sensitive data filtering
import * as winston from "winston";

// List of fields to redact
const SENSITIVE_FIELDS = [
  "password",
  "token",
  "apiKey",
  "secret",
  "creditCard",
  "ssn",
  "socialSecurity",
  "dob",
  "birthdate",
];

// Custom formatter to redact sensitive data
const redactSensitiveData = winston.format((info) => {
  // Create a deep copy of the log object
  const sanitized = JSON.parse(JSON.stringify(info));

  // Function to recursively redact fields
  function redact(obj: any) {
    for (const key in obj) {
      // Check if this key should be redacted
      if (
        SENSITIVE_FIELDS.some((field) =>
          key.toLowerCase().includes(field.toLowerCase())
        )
      ) {
        obj[key] = "[REDACTED]";
      }
      // Recurse into nested objects
      else if (obj[key] && typeof obj[key] === "object") {
        redact(obj[key]);
      }
    }
  }

  redact(sanitized);
  return sanitized;
});

// Create logger
const logger = winston.createLogger({
  level: process.env.LOG_LEVEL || "info",
  format: winston.format.combine(
    winston.format.timestamp(),
    redactSensitiveData(),
    winston.format.json()
  ),
  defaultMeta: { service: "api-service" },
  transports: [
    new winston.transports.Console(),
    new winston.transports.File({ filename: "error.log", level: "error" }),
    new winston.transports.File({ filename: "combined.log" }),
  ],
});

// Usage
logger.info("User logged in", {
  userId: "123",
  username: "johndoe",
  password: "should-be-redacted", // This will be redacted
  metadata: {
    creditCard: "4111111111111111", // This will be redacted too
    preferences: { theme: "dark" },
  },
});
```

### 3.5 API Security

#### 3.5.1 RESTful API Security

- Implement proper authentication and authorization
- Use HTTPS for all API endpoints
- Apply rate limiting and throttling
- Validate all input and sanitize output
- Implement proper error handling

**Practical Implementation:**

```typescript
// Example: API security middleware for Express
import rateLimit from "express-rate-limit";
import { expressjwt as jwt } from "express-jwt";
import helmet from "helmet";

// 1. Security headers
app.use(helmet());

// 2. Rate limiting
const apiLimiter = rateLimit({
  windowMs: 15 * 60 * 1000, // 15 minutes
  max: 100, // limit each IP to 100 requests per windowMs
  standardHeaders: true,
  legacyHeaders: false,
  message: { error: "Too many requests, please try again later" },
});

app.use("/api/", apiLimiter);

// 3. JWT Authentication
const authenticate = jwt({
  secret: process.env.JWT_SECRET,
  algorithms: ["HS256"],
  audience: "api.enablis.co",
  issuer: "auth.enablis.co",
});

// 4. Role-based authorization middleware
function authorize(requiredRole) {
  return (req, res, next) => {
    if (!req.auth || !req.auth.role) {
      return res.status(403).json({ error: "Forbidden" });
    }

    if (req.auth.role !== requiredRole && req.auth.role !== "admin") {
      return res.status(403).json({ error: "Insufficient permissions" });
    }

    next();
  };
}

// Apply middleware to routes
app.get(
  "/api/users",
  authenticate,
  authorize("manager"),
  usersController.getAll
);
```

#### 3.5.2 GraphQL Security

- Implement depth and complexity limits
- Apply query whitelisting for production
- Use persisted queries when possible
- Implement proper authorization at field level
- Consider batching and caching for performance

**Practical Implementation:**

```typescript
// Example: GraphQL security configuration with Apollo Server
import { ApolloServer } from "@apollo/server";
import { depthLimit } from "graphql-depth-limit";
import { createComplexityLimitRule } from "graphql-validation-complexity";

// 1. Create complexity limits
const complexityLimit = createComplexityLimitRule(1000, {
  scalarCost: 1,
  objectCost: 2,
  listFactor: 10,
});

// 2. Create Apollo Server with security configurations
const server = new ApolloServer({
  typeDefs,
  resolvers,
  validationRules: [
    depthLimit(5), // Limit query depth
    complexityLimit, // Limit query complexity
  ],
  formatError: (error) => {
    // Log the error internally
    logger.error("GraphQL error", error);

    // Return sanitized error to client
    return {
      message: error.message,
      path: error.path,
      // Don't expose internal details in production
      extensions:
        process.env.NODE_ENV === "development"
          ? error.extensions
          : { code: error.extensions?.code || "INTERNAL_ERROR" },
    };
  },
  plugins: [
    // Add plugin for logging and monitoring
    {
      async requestDidStart(ctx) {
        const { query, operationName, variables } = ctx.request;

        // Log sanitized request
        logger.info("GraphQL request", {
          operationName,
          variables: sanitizeVariables(variables),
          query: query?.substring(0, 1000), // Truncate long queries
        });

        return {
          async didEncounterErrors(ctx) {
            // Log errors
            logger.error("GraphQL errors", {
              operationName,
              errors: ctx.errors,
            });
          },
        };
      },
    },
  ],
});

// 3. Field-level authorization in resolvers
const resolvers = {
  Query: {
    project: async (_, { id }, context) => {
      const project = await projectService.findById(id);

      // Check permissions
      if (!authService.authorize(context.user, project, "view")) {
        throw new Error("Not authorized to view this project");
      }

      return project;
    },
  },
};
```

## 4. Common Vulnerability Prevention

### 4.1 Injection Prevention

#### 4.1.1 SQL Injection

SQL injection occurs when untrusted data is sent to an interpreter as part of a command or query.

**Prevention Techniques:**

- Use parameterized queries or prepared statements
- Implement ORM libraries with proper escaping
- Apply input validation
- Use stored procedures when appropriate
- Apply least privilege database accounts

**Practical Implementation:**

```typescript
// Example: Preventing SQL injection

// DON'T DO THIS - Vulnerable to SQL injection
function unsafeQuery(username) {
  const query = `SELECT * FROM users WHERE username = '${username}'`;
  return db.execute(query);
}

// DO THIS - Using parameterized queries
function safeQuery(username) {
  const query = `SELECT * FROM users WHERE username = ?`;
  return db.execute(query, [username]);
}

// OR THIS - Using an ORM (TypeORM example)
async function safeOrmQuery(username) {
  return await userRepository.findOne({
    where: { username },
  });
}
```

#### 4.1.2 NoSQL Injection

NoSQL injection targets databases like MongoDB through unvalidated input.

**Prevention Techniques:**

- Use parameterized queries
- Apply input validation and sanitization
- Avoid using string operations to build queries
- Use typed operators instead of interpolated strings
- Apply schema validation

**Practical Implementation:**

```typescript
// Example: Preventing NoSQL injection in MongoDB

// DON'T DO THIS - Vulnerable to NoSQL injection
function unsafeQuery(username, password) {
  const query = `
    this.collection.find({
      username: '${username}',
      password: '${password}'
    });
  `;
  eval(query); // NEVER use eval with user input
}

// DO THIS - Using parameterized queries
function safeQuery(username, password) {
  return this.collection.find({
    username: username, // Direct property assignment
    password: password,
  });
}

// EVEN BETTER - With input validation and type checks
function safestQuery(username, password) {
  if (typeof username !== "string" || typeof password !== "string") {
    throw new Error("Invalid input types");
  }

  // Input validation
  if (!/^[a-zA-Z0-9]{3,30}$/.test(username)) {
    throw new Error("Invalid username format");
  }

  return this.collection.find({
    username,
    password: hashPassword(password),
  });
}
```

#### 4.1.3 Command Injection

Command injection occurs when untrusted data is sent to a system shell.

**Prevention Techniques:**

- Avoid executing system commands when possible
- Use libraries/APIs instead of shell commands
- Apply strict input validation
- Use parameterized commands with arguments
- Implement allow lists for permitted commands

**Practical Implementation:**

```typescript
// Example: Preventing command injection

import { exec, execFile } from "child_process";

// DON'T DO THIS - Vulnerable to command injection
function unsafeCommand(fileName) {
  return new Promise((resolve, reject) => {
    exec(`ls -la ${fileName}`, (error, stdout, stderr) => {
      if (error) reject(error);
      else resolve(stdout);
    });
  });
}

// DO THIS - Using execFile with separate arguments
function safeCommand(fileName) {
  return new Promise((resolve, reject) => {
    execFile("ls", ["-la", fileName], (error, stdout, stderr) => {
      if (error) reject(error);
      else resolve(stdout);
    });
  });
}

// EVEN BETTER - Avoid shell commands entirely
function safestApproach(fileName) {
  const fs = require("fs");
  return fs.promises.stat(fileName); // Use native API instead
}
```

### 4.2 Cross-Site Scripting (XSS) Prevention

#### 4.2.1 XSS Types and Prevention

XSS allows attackers to inject client-side scripts into web pages viewed by others.

**Types of XSS:**

- **Reflected XSS**: Script comes from the current HTTP request
- **Stored XSS**: Script is stored on the server and delivered later
- **DOM-based XSS**: Vulnerability exists in client-side code

**Prevention Techniques:**

- Implement context-appropriate output encoding
- Use Content Security Policy (CSP)
- Apply input validation
- Use modern frameworks that automatically escape output
- Implement XSS filters

**Practical Implementation:**

```typescript
// Example: Output encoding

// Simple HTML encoding function
function encodeHTML(text: string): string {
  return text
    .replace(/&/g, '&amp;')
    .replace(/</g, '&lt;')
    .replace(/>/g, '&gt;')
    .replace(/"/g, '&quot;')
    .replace(/'/g, '&#039;');
}

// React automatically escapes variables in JSX
function ReactComponent({ userInput }) {
  // Safe by default - automatically escaped
  return <div>{userInput}</div>;

  // DANGEROUS -
```
