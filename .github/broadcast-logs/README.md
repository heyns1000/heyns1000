# Broadcast Logs Directory

This directory contains historical logs of all ecosystem broadcasts.

Each broadcast creates a timestamped log file with:
- Broadcast ID
- Message content
- Target repositories
- Distribution status
- Links to workflow runs

## Log Format

Files are named: `broadcast-[YYYYMMDD-HHMMSS]-[run_id].md`

Example: `broadcast-20260105-144523-1234567890.md`

## Retention Policy

Logs are kept indefinitely for audit and tracking purposes. They help:
- Track communication history
- Debug distribution issues
- Provide accountability
- Enable trend analysis

## Usage

These logs are automatically created by the `ecosystem-broadcast.yml` workflow and should not be manually edited.
