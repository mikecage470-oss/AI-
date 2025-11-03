# 🧠 Quantum Concierge Services - AI Automation Workflow

Complete AI-powered automation system for government contracting bid management, vendor sourcing, quote submission, PO tracking, and invoice automation.

## 📋 Table of Contents
- [Overview](#overview)
- [Features](#features)
- [Project Structure](#project-structure)
- [Installation](#installation)
- [Configuration](#configuration)
- [Usage](#usage)
- [Phases](#phases)

## 🎯 Overview

This system automates the entire government contracting workflow from bid discovery to invoice generation, saving time and increasing efficiency for Quantum Concierge Services.

## ✨ Features

### Phase 1: Bid Hunting + Vendor Sourcing
- **Automated Bid Hunting**: Daily scanning of SAM.gov and procurement portals
- **AI Summarization**: Plain English summaries of solicitations
- **Vendor Sourcing**: Automatic vendor matching and quote requests
- **Email Automation**: Auto-drafted vendor communications

### Phase 2: Quote Submission
- Auto-fill bid forms (PDF/Excel)
- Automatic profit margin calculation (8-10%)
- Submission package generation

### Phase 3: PO Tracking & Fulfillment
- Award notification monitoring
- Automatic PO generation
- Delivery tracking

### Phase 4: Invoice Automation
- Auto-generate branded invoices
- Automatic invoice delivery

## 📁 Project Structure

```
AI-/
├── config/
│   ├── __init__.py
│   └── settings.py
├── src/
│   ├── __init__.py
│   ├── phase1_bid_hunting/
│   │   ├── __init__.py
│   │   ├── bid_scraper.py
│   │   ├── ai_summarizer.py
│   │   └── dashboard_manager.py
│   ├── phase1_vendor_sourcing/
│   │   ├── __init__.py
│   │   ├── vendor_database.py
│   │   ├── email_handler.py
│   │   └── quote_parser.py
│   ├── phase2_quote_submission/
│   ├── phase3_po_tracking/
│   └── phase4_invoicing/
├── data/
│   └── vendors.json
├── templates/
│   ├── email_templates/
│   └── invoice_templates/
├── logs/
├── .env.example
├── .gitignore
├── requirements.txt
└── README.md
```

## 🚀 Installation

### Prerequisites
- Python 3.9+
- OpenAI API key
- Google Cloud Project (for Sheets & Gmail API)
- SAM.gov API access (optional)

### Setup

1. Clone the repository:
```bash
git clone https://github.com/mikecage470-oss/AI-.git
cd AI-
```

2. Create virtual environment:
```bash
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
```

3. Install dependencies:
```bash
pip install -r requirements.txt
```

4. Configure environment variables:
```bash
cp .env.example .env
# Edit .env with your API keys and settings
```

5. Set up Google Cloud credentials:
- Create a project in Google Cloud Console
- Enable Google Sheets API and Gmail API
- Download credentials JSON and save to `config/google_credentials.json`

## ⚙️ Configuration

Edit `.env` file with your credentials:

```env
# OpenAI
OPENAI_API_KEY=your_openai_key_here

# Google Sheets
GOOGLE_SHEETS_ID=your_sheet_id_here

# Gmail
GMAIL_ADDRESS=your_email@example.com

# Company Info
COMPANY_NAME=Quantum Concierge Services
PROFIT_MARGIN=0.10
```

## 📖 Usage

### Phase 1: Bid Hunting

Run daily bid scraper:
```bash
python -m src.phase1_bid_hunting.bid_scraper
```

### Phase 1: Vendor Sourcing

Process vendor quotes:
```bash
python -m src.phase1_vendor_sourcing.vendor_database
```

## 🔄 Phases

### ✅ Phase 1: Bid Hunting + Vendor Sourcing (In Progress)
- [x] Project structure
- [x] Bid scraper framework
- [x] AI summarization
- [x] Dashboard integration
- [x] Vendor database
- [x] Email automation

### 🔲 Phase 2: Quote Submission
- [ ] PDF form filler
- [ ] Margin calculator
- [ ] Package generator

### 🔲 Phase 3: PO Tracking
- [ ] Award monitor
- [ ] PO generator
- [ ] Delivery tracker

### 🔲 Phase 4: Invoice Automation
- [ ] Invoice generator
- [ ] Auto-emailer

## 🤝 Contributing

This is a private project for Quantum Concierge Services.

## 📄 License

Proprietary - All Rights Reserved

## 📧 Contact

For questions or support, contact mikecage470-oss

---

**Built with ❤️ for Quantum Concierge Services**