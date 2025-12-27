# Deposit Slips

*Browser-Based Deposit Slip Generator*

A browser-based application for generating accurate, print-ready bank deposit slips from imported deposit data.

This project is conceptually inspired by long-standing desktop tools such as QSlip, which demonstrated that precise layout control and repeatable workflows are more important than deep accounting integrations for this problem space

## Purpose

Banks still require deposit slips that match specific physical layouts. Accounting systems rarely produce printouts that align correctly with these slips.

This application exists to solve one problem well:

Take structured deposit data and produce a correctly aligned deposit slip PDF that can be printed on plain paper or aligned with a pre-printed slip.

## MVP Scope

The MVP is intentionally limited to validate the core workflow.

### Included in MVP

**Deposit Data**

- Upload a CSV file containing deposit line items
- Manual entry and editing of deposits
- Support for:
   - Checks
   - Cash
   - Coin
   - Cash back
- Validation of calculated totals

**Slip Format**
- Single, user-defined slip format
- Fixed paper size
- Single-sided layout
- Numeric positioning using inch-based measurements
- Font and font size selection
- Live preview of rendered output

**Output**
- Print-ready PDF generation
- Plain paper printing
- Overflow handling by page break

**Persistence**
- Save and reload:
   - Deposits
   - Slip formats
- All data stored per user account

## Roadmap Snapshot
### Phase 2
- Drag-and-drop layout editor
- Background image support
- Import presets
- Customer list memory
- Multi-format support

### Phase 3
- Duplex printing logic
- Printer profiles
- Accounting system integrations
- Shared format libraries
- Audit logging
