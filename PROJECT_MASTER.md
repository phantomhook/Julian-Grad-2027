Project Title: Julian's Regis University Graduation Celebration 2027
Graduation: Regis University (Denver, CO) — Undergraduate
Brand Identity: Navy (#002D72) + Gold (#8A704C) — Regis University colors. Clean, modern, celebratory.
Scope: A phased digital experience moving from "Save the Date" to a full RSVP/Menu + Weekend Guide site for ~15 guests.
Stack: GitHub Pages (hosting/code), Mobile-first Tailwind CSS, single index.html.

*important... commencement is Sunday, May 2, 2027 at 10:00 AM at Boettcher Commons, Regis University
*important... dinner is Saturday, May 1, 2027 at 6:30 PM at Farmers Union, 1780 Wynkoop St, Denver, CO 80202
*important... host is TBD — set HOST_NAME constant when confirmed
*important... footer reads "To Julian with California Love"

## URLs
- Live Site:  https://phantomhook.github.io/Julian-Grad-2027/
- GitHub Repo: https://github.com/phantomhook/Julian-Grad-2027

## Deploy
From your Julian-Grad-2027 folder in Terminal:
  bash deploy.sh "your message here"

## Feature Flags (in index.html script section)

| Flag | Default | Purpose |
|------|---------|---------|
| RSVP_ENABLED | false | Shows/hides RSVP & Menu tab |
| GUIDE_ENABLED | false | Shows/hides Weekend Guide tab |
| LIVESTREAM_URL | '' | Set to URL to convert placeholder into livestream link |
| HOST_NAME | '' | Set to host name for dinner card |
| RSVP_DEADLINE | 'TBD' | Set to date string like "April 15, 2027" |

## Phases

Phase 1: Save the Date Landing Page ✅ BUILT
- Navy + Gold Regis theme, Tailwind CSS
- Hero with Julian's photo, "Regis University Class of 2027"
- Event Details tab (active): Commencement card + Dinner card
- Add to Calendar: Google Calendar + Apple/Outlook (.ics) for BOTH events
- Livestream placeholder (auto-converts to link when URL set)
- Host line placeholder (auto-updates when HOST_NAME set)
- Footer: "To Julian with California Love"
- Weekend Guide + RSVP tabs grayed out with "Coming Soon" tooltip

Phase 2: Weekend Guide
- Flip GUIDE_ENABLED = true
- Hotels: AC Hotel, Source Hotel, Kimpton Monaco — with direction links
- Saturday Activity Guide: 3 collapsible accordion packages
  - Relaxed & Scenic (Botanic Gardens → Cherry Creek → Union Station)
  - Adventure & Outdoors (Red Rocks → Morrison → RiNo)
  - Mix & Match (modular cards: parks, culture, city, wow add-on)

Phase 3: RSVP & Menu
- Flip RSVP_ENABLED = true
- Set RSVP_DEADLINE to actual date
- Formspree endpoint: https://formspree.io/f/xpqjoqpk (shared with JAGgrad — timestamped + subject line differentiated)
- Form collects: contact name, email, additional guests, dietary notes
- Hidden _timestamp field for submission tracking
- Hidden _subject field: "Julian Grad 2027 - New RSVP"
- Success message shown after submit
- Add menu image when available

Phase 4: Pre-Event Updates
- Set LIVESTREAM_URL when available
- Set HOST_NAME when confirmed
- Add any last-minute details

## RSVP Submissions
- Log in at formspree.io → Submissions tab
- Julian Grad submissions identified by subject line "Julian Grad 2027 - New RSVP" and timestamp
- View, download CSV, or share from there

## Hotels
- AC Hotel by Marriott Denver Downtown – 750 15th Street, Denver, CO 80202
- The Source Hotel + Market Hall – 3330 Brighton Boulevard, Denver, CO 80216
- Kimpton Hotel Monaco Denver – 1717 Champa Street, Denver, CO 80202
