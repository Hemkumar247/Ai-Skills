# ⚙️ Technical Specification
## Project: {{PROJECT_NAME}}

---

## 1. Tech Stack

| Layer | Technology | Purpose |
|---|---|---|
| {{LAYER_1}} | {{TECH_1}} | {{PURPOSE_1}} |
| {{LAYER_2}} | {{TECH_2}} | {{PURPOSE_2}} |
| {{LAYER_3}} | {{TECH_3}} | {{PURPOSE_3}} |

---

## 2. System Architecture

```
{{ASCII_ARCHITECTURE_DIAGRAM}}
```

Describe each major component and how data flows between them.

---

## 3. Data Storage Structure

Describe each table / collection / model here at a high level.
(Full schema with column types is in schema.md)

### {{ENTITY_1}}
- Purpose: {{PURPOSE}}
- Key fields: {{FIELDS}}

### {{ENTITY_2}}
- Purpose: {{PURPOSE}}
- Key fields: {{FIELDS}}

---

## 4. Core Functions / Modules

### `{{FUNCTION_1_NAME}}({{PARAMS}})`
- **Purpose:** {{WHAT_IT_DOES}}
- **Input:** {{INPUT_DESCRIPTION}}
- **Output:** {{OUTPUT_DESCRIPTION}}
- **Side effects:** {{SIDE_EFFECTS}}

### `{{FUNCTION_2_NAME}}({{PARAMS}})`
- **Purpose:** {{WHAT_IT_DOES}}
- **Input:** {{INPUT_DESCRIPTION}}
- **Output:** {{OUTPUT_DESCRIPTION}}

<!-- Repeat for each major function -->

---

## 5. External API Configuration

### {{API_1_NAME}}
- Endpoint: `{{ENDPOINT}}`
- Auth: {{AUTH_METHOD}}
- Used for: {{USE_CASE}}
- Request format: {{FORMAT}}
- Response format: {{FORMAT}}

### {{API_2_NAME}}
- Endpoint: `{{ENDPOINT}}`
- Auth: {{AUTH_METHOD}}

---

## 6. Environment Variables / Secrets

| Key | Description |
|---|---|
| `{{ENV_VAR_1}}` | {{DESCRIPTION}} |
| `{{ENV_VAR_2}}` | {{DESCRIPTION}} |

Store in: {{WHERE_TO_STORE}} (e.g., `.env`, Script Properties, Secrets Manager)

---

## 7. Error Handling Strategy

{{DESCRIBE_ERROR_HANDLING_APPROACH}}

Standard pattern:
```{{LANGUAGE}}
{{ERROR_HANDLING_CODE_EXAMPLE}}
```
