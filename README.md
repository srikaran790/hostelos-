# HostelOS

A hostel management prototype that replaces paper outpass registers with an online workflow.

**Live demo:** add your GitHub Pages link here

## What it does
- **Student:** requests an outpass, sees a one-time code once approved, raises complaints.
- **Warden:** approves or rejects requests, sees who is inside or outside, tracks overdue returns, manages complaints, reads the activity log.
- **Guard:** enters the student's code at the gate to record exit, then return (late returns are flagged).

Exit and return times are recorded only. HostelOS does not track live location.

## How the outpass works
1. Student submits a request (status: pending).
2. Warden approves (status: approved) and a six-digit code is generated.
3. Guard verifies the code at exit (status: out) and a new code is generated.
4. Guard verifies the new code at return (status: returned, late if after the due time).

## Prototype vs planned
| Built now | Planned |
|---|---|
| Plain HTML, CSS, JavaScript | React front end |
| Data in browser localStorage | Node.js API and MongoDB |
| Role switcher | Real login for each role |
| Code shown on screen | SMS or push delivery, expiry, attempt limits |

## Run it
Open `index.html` in any browser. No install needed.

## Documentation
Data flow diagrams and UML diagrams (made in Sparx Enterprise Architect) are in the `docs/` folder.
