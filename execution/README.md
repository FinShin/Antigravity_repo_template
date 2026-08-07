# Execution Tools (Layer 3: Deterministic Code)

Python scripts that handle API calls, data processing, file operations, and database interactions deterministically.

## Guidelines
- Scripts should be clean, modular, testable, and well-commented.
- Read configuration and secrets from environment variables (defined in `.env`).
- Never perform intermediate work outside `.tmp/` directory.
