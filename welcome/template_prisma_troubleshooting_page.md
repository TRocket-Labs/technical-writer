# Template: Troubleshooting Guide

> **Template:** Troubleshooting Guide  
> **Based on:** [Troubleshooting Prisma Migrate](https://www.prisma.io/docs/orm/prisma-migrate/workflows/troubleshooting)

---

This template helps you write a troubleshooting page that organizes issues by specific problem → causes → fix. It's based on how Prisma structures their Migrate troubleshooting guide, scoping each page to a single environment and linking out for alternatives.

---

# **Troubleshooting**

{One sentence describing the scope of this troubleshooting page and the environment it applies to. Example: "Troubleshooting issues with {Feature} in a development environment."}

{Link to alternative paths if this page doesn't apply. e.g. "For production-focused troubleshooting, see: [Production Troubleshooting Guide]".}

> **Note:** {Optional explicit out-of-scope warning. e.g. "This guide does not apply to [Exception Case]. See [Alternative Tool] instead."}

---

## **{Specific Issue Name e.g., Handling history conflicts}**

{Definition of what the issue actually is in one sentence. Example: "A {Issue Name} occurs when there are discrepancies between X and Y."}

### **Causes of {Issue Name}**

{List bullet points of why this happens. Focus heavily on actions the user might have taken or environmental factors.}
- {Cause 1}
- {Cause 2}

> **Caution:** {High-risk action warning: What they SHOULD NOT do when debugging this state, e.g. "Never manually delete X."}

### **Fixing {Issue Name}**

{Provide the exact resolution or what the system will do to help them fix it.}

{If it's an automated fix: Explain the system behavior expectation, e.g. "If the system detects this conflict, the CLI will prompt you to reset..."}

{If manual steps: Provide the exact CLI commands or code to run.}
```bash
{Command}
```

### **Related resources** _(optional)_

{Link to related documentation, alternative approaches, or deeper-dive guides.}

- Link to {resource title}
- Link to {resource title}

---

## **{Another Specific Issue Name}**

{Definition of what the issue actually is in one sentence.}

### **Causes of {Issue}**
- {Cause 1}

### **Fixing {Issue}**
{Exact steps or commands.}

### **Related resources** _(optional)_

- Link to {resource title}

---

ℹ️ _**Pattern Note:** This template scopes each troubleshooting page to a single environment and structures each issue as Problem → Causes → Fix. This makes it easy for users to find the exact issue they're dealing with and follow a direct path to the resolution._
