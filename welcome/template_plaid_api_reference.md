> **Template:** API Endpoint Reference Page  
> **Based on:** [Plaid's API Transactions Endpoint Reference](https://plaid.com/docs/api/products/transactions/)  
> **Why it works:** By linking triggered endpoints directly to their corresponding webhooks, Plaid closes the "action-to-feedback" loop on a single page. This removes the need for developers to search through separate sections to understand the full lifecycle of a single request.

---

# **{Endpoint Group Name}**

💡 _One sentence describing what this group of endpoints does, plus a link to the full implementation guide._

**Example:** "Use the Transactions endpoints to retrieve and manage transaction data from linked accounts. For implementation guidance, see the [Transactions guide](#)."

### **Endpoints**

💡 _List all related endpoints in this product area for quick navigation._

- `{METHOD} /v1/{resource}/{action}`
- `{METHOD} /v1/{resource}/{action}`
- `{METHOD} /v1/{resource}/{action}`

**Example from Plaid:**
- `POST /transactions/get`
- `POST /transactions/refresh`
- `POST /transactions/sync`

---

## **{Endpoint Path}**

`{METHOD} /v1/{resource}/{action}`

💡 _Start with the HTTP method and full endpoint path._

### **Versioning / Migration Notes** _(optional)_

💡 _If this endpoint replaces a deprecated one, state it here with a migration link._

> **Note:** This endpoint replaces the deprecated `/{old-endpoint}`. Migration guide available [here](#).

### **Supported Resource Types** _(optional)_

💡 _List which resource types or configurations this endpoint supports._

> Supported types: `{type_a}`, `{type_b}`, `{type_c}`

### **Code Example**

💡 _Include a working code snippet if there's a common implementation pattern._

**Example from Plaid:**

```javascript
const response = await plaidClient.transactionsGet({
  access_token: accessToken,
  start_date: '2024-01-01',
  end_date: '2024-01-31',
});
```

💡 _Reference any related webhooks._

See [{WEBHOOK_NAME}](#webhooks) webhook for async updates.

---

### **Request Fields**

💡 _List all request parameters with types, requirements, and descriptions._

**Example from Plaid:** `access_token` (string, required), `start_date` (string, required), `options.count` (integer, optional).

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `{field_name}` | {type} | {Yes/No} | {What this field does} |
| `{field_name}` | {type} | {Yes/No} | {What this field does} |
| `{options.field_name}` | {type} | {Yes/No} | {Nested option description}. Default: `{value}` |

---

### **Response Fields**

💡 _List all response fields with types and descriptions._

**Example from Plaid:** `accounts` (array), `transactions` (array), `total_transactions` (integer), `request_id` (string).

| Field | Type | Description |
|-------|------|-------------|
| `{field_name}` | {type} | {What this field contains} |
| `{field_name}` | {type} | {What this field contains} |
| `{nested.field_name}` | {type} | {Nested field description} |

---

### **Webhooks** _(if applicable)_

💡 _For each webhook related to this endpoint: explain when it fires + show a sample payload._

**Example from Plaid:** `TRANSACTIONS_REMOVED` fires when transactions are deleted from an account.

#### `{WEBHOOK_NAME}`

**When it fires:** {Describe the triggering event.}

**Sample Payload:**

```json
{
  "webhook_type": "{TYPE}",
  "webhook_code": "{CODE}",
  "{resource_id}": "{value}",
  "{field}": "{value}",
  "environment": "production"
}
```

---

ℹ️ _**Pattern Note:** Plaid structures each endpoint with a consistent flow: endpoint path → optional context (versioning, supported types) → code example → request/response tables → related webhooks. This "everything in one place" approach minimizes developer context-switching during integration._
