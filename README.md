# CTI Newsletter Quick Job

This project collects recent cybersecurity articles from Feedly, ranks the top items by impact and relevance, and generates a Word newsletter for cyber threat intelligence monitoring.

## What It Produces

- Top 4 ranked articles from the last 18 hours.
- Article summaries for a general cybersecurity audience.
- Extracted CVEs.
- Inferred MITRE ATT&CK IDs.
- Targeted systems.
- Exploitation prerequisites.
- A `.docx` newsletter and JSON report.

## Deployment Package

Download the EC2 deployment package from:

- `dist/cti-newsletter-aws-ec2.zip`

Unzip it on the EC2 instance, then follow `deploy/aws-ec2/README.md` inside the package.

## Local Quick Run

```powershell
$env:FEEDLY_API_KEY="your_feedly_token"
.\quick_jobs\run_last18h_cti_newsletter.ps1
```

## Important

Do not commit real API keys. Use `.env` on the target host.
