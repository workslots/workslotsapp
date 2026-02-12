# WorkSlots

WorkSlots is a lightweight, single-page web app that lets you **define recurring work shift types and visually plan your schedule** on a monthly calendar — then sync everything directly to Google Calendar with one click.

## The Problem

If you work irregular shifts, rotating schedules, or freelance hours, keeping your calendar up to date is tedious. You end up manually creating the same kinds of events over and over, picking colors, setting times — for every single day.

## The Solution

WorkSlots flips the workflow: you define your shift types once (name, start time, end time, color), then simply click on calendar days to stamp them in. When you're happy with the month, hit **Sync Current Month** and all your slots are pushed to Google Calendar as real events.

## Why Google Calendar Integration Matters

Because WorkSlots syncs to Google Calendar, your schedule becomes instantly **shareable**. Google Calendar has built-in sharing — you can share the WorkSlots calendar with your partner, family, friends, or coworkers. They'll always know when you're working without having to ask.

This is especially useful for:

- **Couples** — share your work schedule so your partner can plan around it, coordinate meal times, or know when you'll be home.
- **Friends** — let friends see your free time so you can make plans without the back-and-forth.
- **Coworkers or teams** — give colleagues visibility into your availability without manually updating a separate system.
- **Caregivers and families** — keep family members informed about your shifts for childcare handoffs or shared responsibilities.

Since it's a native Google Calendar, shared people see updates in real time on any device — phone, tablet, or desktop — with no extra app to install.

## How It Works

1. **Connect your Google account** — click "Connect Google" and authorize WorkSlots to manage a dedicated calendar.
2. **Define your slot types** — create shift definitions like "Morning Shift (06:00–14:00)" or "Deep Work (09:00–12:00)", each with a name, time range, and color from Google Calendar's palette.
3. **Plan your month** — click any day on the calendar to assign one of your slot types. Click again to change or clear it.
4. **Sync to Google Calendar** — hit "Sync Current Month" to push all your assignments as color-coded events. WorkSlots only touches events it created, so your other calendar entries are safe.
5. **Navigate months** — use the arrow buttons to move between months. When you switch months, existing synced slots are loaded back automatically.

## Features

- **Zero setup** — no build step, no framework, no server. Just open `index.html` in a browser.
- **Dedicated calendar** — WorkSlots automatically creates and manages its own Google Calendar, keeping your work slots separate and organized.
- **Slot type definitions** — define as many shift types as you need, each with custom name, start/end times, and color.
- **Color-coded events** — uses Google Calendar's native event color palette so your slots look great everywhere.
- **Two-way awareness** — synced events load back when you revisit a month, so you always see your current state.
- **Dark mode** — toggle between light and dark themes; your preference is remembered.
- **Responsive layout** — works on desktop and mobile screens.
- **Dev mode** — append `?dev` to the URL to test the UI with mock data, no Google account needed.

## Tech Stack

- Single HTML file with inline CSS and JavaScript
- [Tailwind CSS](https://tailwindcss.com/) via CDN
- [Google Identity Services](https://developers.google.com/identity) for OAuth 2.0
- [Google Calendar API](https://developers.google.com/calendar) for event management
- [Inter](https://fonts.google.com/specimen/Inter) font via Google Fonts

## Getting Started

1. Clone the repository:
   ```bash
   git clone https://github.com/your-username/workslotsapp.git
   ```
2. Open `index.html` in your browser. That's it — no install, no build.
3. Click **Connect Google** to authenticate and start planning.

To try the UI without a Google account, open `index.html?dev` instead.

## How Data Is Stored

- **Slot type definitions** are stored in the description field of the dedicated WorkSlots Google Calendar, so they persist across devices and sessions.
- **Schedule assignments** (which slot goes on which day) are stored as Google Calendar events with a private extended property that identifies them as WorkSlots-managed.
- **Nothing is stored in localStorage** except your theme preference (light/dark). There is no backend server.

## License

MIT
