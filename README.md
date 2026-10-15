# Koinonia Ride — Proof of Concept

Passenger transport app for Koinonia prayer meetings in Abuja.
Pilot: Daughters of Abraham (DOA), Kado → then Chida Event Centre, Utako → Koinonia Abuja → Koinonia Global.

## What the POC does
| Feature | Where in the app |
|---|---|
| Member registration (default home destination, emergency contact, consent, security tag KR-####) | Members |
| Vehicle registration — hired buses, kekes, personal cars (driver, plate, seats, condition, route) | Vehicles |
| Route plan — corridors along major roads, assign vehicles per session, map | Routes & Map |
| Seat reservation on buses/kekes with live seat grid | Book & Share |
| Ride share — car owners opt in/out per session, set seats (never above the car's limit), approve/decline riders | Book & Share |
| Location check-in (GPS geofence around DOA / Chida) + auto-allocation to bus → ride share → waitlist | Today |
| Destination override for one session (default stays home) | Today |
| Security brief / manifest with emergency contacts — share to WhatsApp or print | Security |
| End-of-trip report per vehicle + session summary on close | Security / Today |
| Partnerships & welfare giving ledger vs monthly running-cost target | Giving |
| Export / import / reset data, adjust meeting-point coordinates and geofence | Settings |

## Host on GitHub Pages (5 minutes)
1. Create a new public repository on GitHub, e.g. `koinonia-ride`.
2. Upload `index.html` (and this README) to the repository root → **Commit changes**.
3. Go to **Settings → Pages** → Source: *Deploy from a branch* → Branch: `main` / `(root)` → **Save**.
4. After about a minute the app is live at `https://<your-username>.github.io/koinonia-ride/`.

GitHub Pages serves over HTTPS, which phones require for the location check-in to work.

## Before the demo
- Open **Settings**, stand at the DOA gate, tap **Use my location** → **Save settings**. The seeded coordinates are approximate.
- Use **Simulate: at DOA** when demoing away from the venue.
- **Settings → Reset to demo data** restores the sample members, vehicles and bookings.

## Known POC limits (addressed in the full build)
- Data lives in each browser's local storage — devices don't share data. Use Export/Import to move it. The full build adds a cloud database, phone-number login and roles.
- Allocation is rule-based (geofence + destination-to-corridor match + seat availability). Route optimisation and demand prediction come later.
- No SMS/push notifications or online payments yet; giving records transfers and pledges.
- All names and phone numbers in the demo data are fictitious.
