# picast.com

Separate website and hosting project for **picast.com**. This repository is intentionally separate from manualAI.

## Confirmed hosting target

- Provider: Amazon Lightsail
- Location: Frankfurt, AWS Region `eu-central-1`
- OS: Linux/Ubuntu
- Plan: 1 GB RAM, 2 vCPU, 40 GB SSD, 2 TB transfer
- Published list price checked on 2026-10-07: USD 7/month; taxes and any applicable overage may add cost

## Status

The repository is a scaffold only. The server has **not** been provisioned, the website source has not yet been added, and DNS has not been changed. Provisioning requires authorized AWS account access; deployment requires the actual picast.com source code; DNS cutover requires access to the domain's DNS provider.

## Structure

- `app/` — website source will go here or be integrated from the supplied source repository.
- `infrastructure/lightsail/` — Frankfurt server decisions and provisioning notes.
- `deploy/` — deployment instructions/scripts once the app stack and source are known.
- `docs/` — operational and DNS notes.

Never commit credentials, private keys, AWS tokens, or `.env` files. Use a secure secret manager for runtime secrets.
