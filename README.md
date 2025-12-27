# Deposit Slips

Generate bank deposit slips from managed accounts and print them on plain paper. Small, open-source tool for businesses and bookkeepers to create customizable, bank-friendly deposit slips (PDF or direct to printer) using managed account data.

## Key features
- Create deposit slips from one or more managed accounts
- Export to PDF, print to any system printer, or save as images
- Configurable slip templates (paper size, margins, fonts, bank logo)
- Batch processing and combined slips for multiple accounts
- CSV/JSON import and simple account management
- Preview mode with alignment guides for regular paper printing
- CLI and web UI for automated and manual workflows
- Audit log and optional encryption for stored account data

## Screenshot
(Replace with actual images in /docs)
![preview-placeholder](docs/preview.png)

## Quick start

Requirements
- Node.js 18+ or Python 3.10+ (project contains both web + CLI implementations; pick one)
- Docker (optional)

Local (Node) example
1. Clone:
    git clone https://github.com/your-org/deposit-slips.git
2. Install:
    cd deposit-slips && npm install
3. Start dev server:
    npm run dev
4. Open http://localhost:3000 and add managed accounts, create a slip, then Export → PDF or Print.

CLI example
- Create slip from CSV:
  deposit-slips create --input accounts.csv --template "standard" --output deposit.pdf
- Print directly (Linux/CUPS):
  deposit-slips print --input accounts.csv --printer "HP-Laser"

Docker
- Build:
  docker build -t deposit-slips .
- Run:
  docker run -p 3000:3000 -v $(pwd)/data:/app/data deposit-slips

## Templates & Printing
- Templates defined in /templates as JSON + HTML/CSS
- Adjust paper size, margins, logo, and alignment guides
- Preview uses a calibration mode to help align with your printer’s printable area
- Save templates and share across team installations

## Managed accounts
- Store multiple accounts with metadata (bank name, routing, account number, nickname)
- Import from CSV/JSON or connect to accounting exports
- Optionally encrypt account store with a passphrase (local-only; no cloud by default)

## Security & Privacy
- Data stored locally by default
- Optional encryption for stored account data (AES-256)
- No phone-home telemetry unless explicitly enabled
- Review configuration in /config for defaults and allowed export formats

## Contributing
- See CONTRIBUTING.md for guidelines
- Open issues and PRs welcome (tests and template samples encouraged)
- Use branch naming: feature/*, fix/*, docs/*

## License
MIT — see LICENSE

## Contact
Issues: https://github.com/your-org/deposit-slips/issues
Pull requests: welcome

Replace placeholders (repo URL, screenshots, templates) with your project assets before publishing.