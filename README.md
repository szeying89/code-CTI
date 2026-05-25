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

## Local Quick Run

```powershell
$env:FEEDLY_API_KEY="your_feedly_token"
.\quick_jobs\run_last18h_cti_newsletter.ps1
```

## AWS EC2 Deployment

Use the deployment package instructions in:

- `deploy/aws-ec2/README.md`

The EC2 installer creates a Python virtual environment, installs dependencies, adds a runner script, and registers an optional systemd timer.

## Important

Do not commit real API keys. Use `.env` on the target host.
