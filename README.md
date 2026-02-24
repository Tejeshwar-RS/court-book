# CourtBook — Indoor Sports Scheduling and Management System

A frontend-only court booking web application built with plain HTML, CSS, and JavaScript. No frameworks, no backend, no database.

---

## Overview

CourtBook allows facility managers or front-desk staff to view court availability, make bookings, track time slots, and calculate session costs — all within a single HTML file.

---

## Features

- View all courts with live Available / Booked status
- Hourly rate displayed per court
- Book a court by selecting player name, court, date, start time, and end time
- Live cost preview calculated from duration and court rate before confirming
- Overlap detection prevents double-booking the same court at the same time
- Bookings table with court, player, date, time range, duration, and total amount
- Cancel any booking directly from the table
- Live summary panel showing total courts, available count, booked count, bookings today, and estimated daily revenue
- Responsive layout for desktop and mobile

---

## Courts and Pricing

| Court   | Sport        | Rate (Rs./hr) |
|---------|--------------|---------------|
| Court A | Badminton    | 200           |
| Court B | Badminton    | 220           |
| Court C | Basketball   | 450           |
| Court D | Squash       | 350           |
| Court E | Table Tennis | 250           |
| Court F | Volleyball   | 300           |

Prices are placeholders and can be edited in the `courts` array inside the `<script>` tag.

---

## Usage

1. Open `index.html` in any modern browser
2. View court availability on the cards at the top
3. Click "Book This Court" on a card or manually select a court in the form
4. Enter player name, date, start time, and end time
5. Review the live cost estimate that appears below the time fields
6. Click "Confirm Booking" to finalize
7. The booking appears in the table below and the court status updates immediately
8. To cancel a booking, click the "Cancel" button on the corresponding table row

---

## File Structure

```
index.html   — complete application, single file
README.md               — this file
```

---

## Technical Notes

- All state is managed in memory via a JavaScript array; data resets on page reload
- No external JavaScript libraries or frameworks are used
- Google Fonts (DM Sans, DM Mono) are loaded via CDN; the app requires an internet connection for correct typography
- Cost is calculated as: `ceil((duration in minutes / 60) * hourly rate)`
- Overlap check compares start and end times as strings in HH:MM format

---

## Customization

- To add or remove courts, edit the `courts` array in the `<script>` tag
- To change a court rate, update the `rate` property on the corresponding court object
- To change the color scheme, update the CSS variables under `:root` at the top of the `<style>` block

---

## Browser Support

Works in all modern browsers: Chrome, Firefox, Edge, Safari.
