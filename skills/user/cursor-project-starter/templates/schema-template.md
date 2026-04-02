# 🗃️ Database & Schema Reference
## Project: {{PROJECT_NAME}}

---

## Overview

**Database/Storage:** {{DATABASE_TECHNOLOGY}}
**ORM / Access Layer:** {{ORM_OR_ACCESS_METHOD}}
**Total entities/tables/collections:** {{COUNT}}

---

## Table/Collection 1: {{ENTITY_1_NAME}}

**Purpose:** {{PURPOSE}}
**Access pattern:** {{HOW_ITS_QUERIED}}

| # | Field Name | Data Type | Source | Notes |
|---|---|---|---|---|
| 1 | {{FIELD}} | {{TYPE}} | {{SOURCE}} | {{NOTES}} |
| 2 | {{FIELD}} | {{TYPE}} | {{SOURCE}} | {{NOTES}} |

---

## Table/Collection 2: {{ENTITY_2_NAME}}

**Purpose:** {{PURPOSE}}

| # | Field Name | Data Type | Source | Notes |
|---|---|---|---|---|
| 1 | {{FIELD}} | {{TYPE}} | {{SOURCE}} | {{NOTES}} |

<!-- Repeat for each entity -->

---

## Data Validation Rules

### {{FIELD_1}} Validation
```
{{VALIDATION_LOGIC}}
```

### {{FIELD_2}} Validation
```
{{VALIDATION_LOGIC}}
```

---

## Indexing / Query Strategy

- **Primary lookup:** {{HOW_TO_LOOK_UP_PRIMARY_KEY}}
- **Common query:** {{COMMON_QUERY_PATTERN}}
- **Performance tip:** {{OPTIMIZATION_ADVICE}}

---

## Relationships

| Entity A | Relationship | Entity B | Via |
|---|---|---|---|
| {{ENTITY_A}} | one-to-many | {{ENTITY_B}} | {{FOREIGN_KEY}} |

---

## Backup / Migration Strategy

{{BACKUP_APPROACH}}
