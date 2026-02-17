# ADAS AI System — Article 12 Logging Schema Template
Version 1.0 | LXD Advisory | EU AI Act Compliance

## System Information
- System Name: [e.g. Lane Keeping Assist v2.3]
- Risk Classification: High-Risk (Annex III, Point 3)
- OEM/Provider: [Company name]
- Schema Owner: [Name, role]
- Last Updated: [Date]

## Article 12 Compliance Mapping

### 12.1 — Automatic Logging Enabled
[ ] Logging is automatically triggered during operation
[ ] No manual intervention required to initiate logging
Infrastructure note: [eSIM/ACSP configuration reference]

### 12.2 — Event Types Logged
[ ] Model input data (sensor feeds, environmental data)
[ ] Model output / decision (action recommended or taken)
[ ] Confidence scores and uncertainty flags
[ ] Human override events
[ ] System failures and fallback events
[ ] OTA deployment events

### 12.3 — Log Format Specification
| Field | Data Type | Format | Example |
|-------|-----------|--------|---------|
| timestamp | datetime | ISO 8601 | 2026-01-15T09:23:41Z |
| system_id | string | UUID | adas-lka-v2-003 |
| input_hash | string | SHA256 | a3f9... |
| output_decision | enum | [assist/override/neutral] | assist |
| confidence_score | float | 0.00–1.00 | 0.94 |
| human_override | boolean | true/false | false |
| session_id | string | UUID | sess-20260115-... |

### 12.4 — Retrieval Capability
[ ] Logs retrievable within 48 hours of request
[ ] Export format: [JSON / CSV / XML]
[ ] Retrieval process documented at: [link/location]

## Article 19 Log Control

### Retention
- Minimum retention period: [X months/years]
- Archival location: [Infrastructure reference]
- Deletion policy: [Procedure]

### Access Control
- Access restricted to: [Roles]
- Access audit trail: [Yes/No — system]
- Last access review: [Date]

### Integrity Protection
- Tamper protection method: [Technical description]
- Integrity verification: [Hash/signature approach]

## Audit Defense Summary
[2-3 sentences explaining how this logging setup 
satisfies Article 12 and 19 requirements in plain language 
understandable to a non-technical regulator]# adas-logging-schema-template
