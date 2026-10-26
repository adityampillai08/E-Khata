# E-KHATA — Digital Credit Ledger for Kirana Stores

**Trust captured in a snap.**

E-KHATA is a collaborative hackathon project that digitises the traditional *khata* system used by neighbourhood kirana stores. It provides a shopkeeper-facing dashboard and a customer-facing ledger experience for managing credit, tracking outstanding amounts, and recording transactions.

🌐 **Live Demo:** [ekhata-gamma.vercel.app](https://ekhata-gamma.vercel.app/)

💻 **Team Project Repository:** [jemankalita/E-KHATA](https://github.com/jemankalita/E-KHATA)

## Overview

Traditional kirana stores often track customer credit using handwritten notebooks. E-KHATA explores how this process can be digitised through a simpler, mobile-friendly interface that connects shopkeepers with their customers' khata records.

The application includes separate shopkeeper and customer experiences, a running credit ledger, bill-photo OCR, QR-based workflows, and a prototype RFID interaction flow.

## Technical Highlights

**E-KHATA is an interactive application, not simply a static collection of UI screens.** Its interface includes application state and ledger-related workflows that respond to user interactions.

- **Dynamic ledger interface:** displays credit-related information such as outstanding balances, transaction details, and due dates.
- **Running balance:** ledger information reflects the application's transaction workflow rather than treating every displayed amount as an unrelated UI element.
- **Bill digitisation:** uses OCR to extract information from receipt images, allowing the user to review the extracted items before posting them to a khata.
- **QR-based workflow:** generates QR codes for shopkeeper-side account interactions.
- **Voice feedback:** supports spoken transaction-amount confirmation through an API proxy and ElevenLabs text-to-speech, with a local fallback when the external service is unavailable.
- **Demo environment:** includes preloaded demonstration data and a reset option for testing the intended workflows.

## Technology Stack

| Layer | Technologies |
|---|---|
| Frontend framework | React 19 |
| Programming language | TypeScript |
| Build tool and development server | Vite |
| Styling | Tailwind CSS v4 |
| UI components | Radix UI |
| Animations and motion | Motion, Framer Motion |
| Notifications | Sonner |
| QR generation | `qrcode.react` |
| QR decoding | `jsqr` |
| OCR | Tesseract.js |
| Backend/API functionality | API routes, including a server-side voice proxy |
| Data integration | Supabase client and schema/migration resources; optional configuration |
| Voice synthesis | ElevenLabs Text-to-Speech |
| Web deployment | Vercel |
| Android packaging | Capacitor 8 |

The stack is based on the dependencies, configuration files, and technical documentation in the team's repository.

## How the Application Works

### 1. Shopkeeper workflow

The shopkeeper can access the dashboard, work with khata-related information, create QR codes, and add bill information to a customer's account.

### 2. OCR-based bill digitisation

The shopkeeper can photograph or upload a receipt. Tesseract.js is used for OCR processing, after which the extracted line items can be reviewed and corrected before being posted to the khata. Manual item entry remains available when a photograph cannot be read reliably.

### 3. Customer ledger

The customer-facing interface presents khata information, including the running balance and settlement-related details.

### 4. QR and RFID prototype workflows

The application includes shopkeeper-side QR generation and a customer-side RFID prototype using Web NFC where supported, with USB RFID-wedge input as an alternative. These interactions demonstrate ways to reduce manual identification and data entry.

### 5. Voice confirmation

A server-side API proxy connects the application to ElevenLabs text-to-speech for spoken confirmation of a posted amount. A local fallback is available when the external voice service is not configured.

## My Contributions

My primary focus was **UI/UX direction, visual identity, and user-facing workflows**, alongside contributions to QR scanning, OCR bill digitisation, and product-scanning functionality.

### 1. Visual Identity and Branding

- Designed the E-KHATA logo.
- Contributed to the project's visual identity and overall design direction.
- Helped establish a recognisable identity around trust and simplicity in digital credit management.

### 2. UI/UX and Interaction Design

- Shaped the UI/UX direction around the needs of kirana shopkeepers and customers.
- Proposed familiar consumer-app patterns inspired by products such as Zomato, Blinkit, and Amazon rather than a conventional, complicated business dashboard.
- Developed detailed design guidance for navigation, customer cards, search, transaction flows, and prominent balance information.
- Emphasised mobile-friendly layouts, accessible typography, visible labels, icon-based status indicators, and clear information hierarchy.
- Suggested simplified forms, step-by-step interactions, and clear confirmation states to reduce friction for users who may be unfamiliar with digital tools.

### 3. OCR Bill-Digitisation Workflow

- Contributed to the workflow for converting physical receipts into digital khata entries.
- Focused on the user journey from capturing or uploading a bill to reviewing extracted information before posting it.
- Helped make the bill-entry process more practical and reduce repetitive manual input.

### 4. QR Scanning and Account Workflows

- Contributed to QR-related functionality and its integration into the user-facing workflow.
- Focused on making scanning and account interactions intuitive within the broader khata experience.

### 5. Product-Scanning Workflow

- Contributed to the product-scanning workflow intended to reduce manual product-information entry.
- Helped shape how scanning fits into the overall user experience.

### 6. Design Research

I used visual and interaction references to help communicate the intended interface and experience:

- [Anime.js](https://animejs.com/) — animation inspiration.
- [Motion](https://motion.dev/) — interface motion and transitions.
- [Uiverse](https://uiverse.io/) — UI component inspiration.
- [Pexels](https://www.pexels.com/) — visual assets.
- [SVG Backgrounds](https://www.svgbackgrounds.com/) — background design references.
- [3Dicons](https://3dicons.co/) — icon references.
- [Rive](https://rive.app/) — interactive animation inspiration.

### 7. Collaborative Development

The project was developed collaboratively with my hackathon teammates. We used design references, detailed prompts, iterative feedback, and Cursor as an AI-assisted development tool during implementation.

My main focus was shaping the user experience and visual direction, along with contributions to the QR, OCR, and product-scanning workflows.

This repository is a portfolio entry documenting my contributions. The linked team repository contains the collaborative project's implementation.

## Design Philosophy

**Simplicity:** prioritise common khata tasks over complex navigation.

**Accessibility:** make information easy to read and actions easy to understand.

**Practicality:** design around real shopkeeper and customer workflows, rather than building a purely visual prototype.

**Clarity:** present balances and transaction information in a way that helps users understand the state of their khata.

## Development and Testing

The team repository includes scripts for local development, testing, and production builds.

```bash
npm install
npm run dev
npm test
npm run build
```

The application is built with Vite and TypeScript. The repository also includes Capacitor configuration for packaging the web application as an Android application.

Some functionality, including voice synthesis and optional data integrations, depends on environment configuration. See the team repository for the implementation and setup details.

## Future Scope

Potential future improvements include:

- **UPI integration:** supporting more convenient digital payment and settlement workflows.
- **Dedicated mobile application:** extending the experience beyond the browser-based application.
- **Real-time synchronisation:** keeping customer and shopkeeper views aligned across devices.
- **Reminders and overdue tracking:** helping shopkeepers follow up on outstanding balances.
- **Offline RFID workflows:** supporting interactions when network connectivity is unavailable.

These are future development goals and should not be interpreted as features already completed in the current prototype.

## Project Links

- 🌐 **Live Demo:** [E-KHATA](https://ekhata-gamma.vercel.app/)
- 💻 **Team Project Repository:** [View source code and implementation](https://github.com/jemankalita/E-KHATA)

---

*E-KHATA was developed collaboratively during a hackathon. This portfolio entry highlights my contributions to the project while linking to the team's implementation.*
