
**Find players. Join pickup games. Get on the field.**

SportsMatch removes the friction between wanting to play sports and actually getting on the field. Users find pickup games near them, see who is going, join in one tap, and connect with players in their area.

> "I am not guessing who this platform is for — I am who this is for."
> — Owen Eiler, Co-Founder

---

## What It Does

- **Browse games** — see upcoming pickup games nearby with sport, time, location, and spots left
- **Join instantly** — one tap to join or leave a game, no group chats needed
- **See who is going** — view player profiles, bios, skill levels, and mutual friends before you commit
- **Create games** — host your own pickup game with a full address, max players, and notes
- **Friends** — send and accept friend requests, message friends directly
- **Game chat** — group messaging thread inside every game
- **Gear coordination** — let teammates know what you are bringing (goals, balls, cones, etc.)
- **Calendar** — add any game to Apple Calendar or Google Calendar
- **Maps** — get directions via Apple Maps or Google Maps directly from the game detail
- **Notifications** — email alerts for new games and when a game is almost full

---

## Tech Stack

| Layer | Technology |
|---|---|
| Frontend | React 18 (via Babel CDN), Tailwind CSS |
| Backend | Supabase (Postgres + Realtime) |
| Auth | Custom email/password via Supabase users table |
| Maps | Apple Maps, Google Maps (deep links) |
| Calendar | .ics download, Google Calendar link |
| Notifications | SendGrid (email) via Supabase notifications table |
| Hosting | GitHub Pages |
| Fonts | Syne (headings), DM Sans (body) |

---

## Database Tables

| Table | Purpose |
|---|---|
| `users` | Player profiles, sports, availability, friends list |
| `games` | Pickup games with players array and gear map |
| `friend_requests` | Pending, accepted, and declined friend requests |
| `game_messages` | Group chat messages per game |
| `private_messages` | Direct messages between two users |
| `notifications` | Email notification queue for SendGrid |

---

## Design System

| Token | Value |
|---|---|
| Primary | #16a34a (dark green) |
| Accent | #f97316 (orange) |
| Background | #f8fafc |
| Text | #0f172a |
| Heading font | Syne 700/800 |
| Body font | DM Sans 400/500/600 |

Mobile-first, light mode only. Max-width 480px on mobile. Full dashboard layout on desktop (768px+).

---

## Sports Supported

Soccer, Basketball, Tennis, Volleyball, Beach Volleyball, Pickleball, Ultimate Frisbee, Running, Golf, Baseball, Softball, Cycling

---

## Current Status

Early beta — Santa Barbara, CA

Focused on getting real users to play real games. Not yet monetizing.

Next milestones:
- 10 users who have played a game found on SportsMatch
- 50 users before expanding to Cornell University
- Communities feature (venue-based) once 50+ users are active

---

## Founders

**Owen Eiler** — Co-Founder. Incoming D1 Soccer player at Cornell University, Class of 2031. Based in Santa Barbara, CA.

**Paolo Shamshiri** — Co-Founder.

---

## Feedback

Beta testers can submit feedback at the SportsMatch Feedback Form linked in the app.

---

## Local Development

This is a single HTML file. No build step required.

1. Clone the repo
2. Open index.html — must be served over HTTP, not opened as a local file
3. Use Live Server in VS Code, or push to GitHub Pages

Supabase credentials are in the file. RLS is disabled for beta.
