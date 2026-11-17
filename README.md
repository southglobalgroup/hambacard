# hambacard
Patient-held clinic record in a QR code, so a person's medicines, allergies and refill date travel with them across clinics and borders.

# HambaCard
A clinic record that travels with the patient, inside a QR code.

**Live app:** https://southglobalgroup.github.io/hambacard/

**Try a ready-made card:** [Nomsa's HambaCard](https://southglobalgroup.github.io/hambacard/#n=Nomsa+Dlamini&d=1972-03-14&c=Hypertension%2C+Type+2+diabetes&m=Amlodipine+10mg+daily%2C+Metformin+500mg+twice+daily&a=Penicillin&r=BP+150%2F95&f=2026-11-05&l=Khayelitsha+CHC)

## The problem
Across Africa, people move for work: from Cape Town to the Eastern Cape every December, miners from Lesotho and Mozambique, truck drivers crossing borders. Their clinic file stays behind. At the next clinic nobody knows their medicines, their allergies or when they last collected treatment, and treatment breaks.

## What it does
1. A nurse fills in a short form and taps **Make HambaCard**.
2. A QR code appears. The patient saves it to their phone.
3. At any other clinic, any phone camera scans it. The card opens with allergies in red, the medicines, and a warning if the refill is overdue.

## How it works
The patient's details live inside the link, after the `#`. Browsers never send that part to a server, so there is no database and no backend. The QR code is the record. The whole app is one HTML file on GitHub Pages.

## How to run
Open the live link on any phone or computer. No install, no sign-up.

## How we kept tokens low
- One HTML file: no framework, no build step, no backend, so there was less code for Copilot to write.
- Copilot Chat in Ask mode only, never agent mode. 2 messages built the whole app.
- When something broke, we found the exact cause first and gave Copilot a one-line fix instead of asking it to debug.

## Status
Working prototype. Next: PIN encryption, clinic-signed cards, offline mode, and a pilot at one clinic.
