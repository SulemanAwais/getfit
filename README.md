<div align="center">

<img src="icon-512.png" width="96" alt="getfit icon">

# getfit

**Commit to the routine. Ship the abs.**

For busy professional Muslims who want to transform their body in 3 months and be in shape before Eid.<br>
An 87 KB, zero-dependency PWA that builds the whole day around the five prayers, a full-time job and the gym, and turns it into a streak.

<br>

![size](https://img.shields.io/badge/size-87_KB-FF6B35?style=flat-square&labelColor=0F1012)
![deps](https://img.shields.io/badge/dependencies-0-FFC24A?style=flat-square&labelColor=0F1012)
![pwa](https://img.shields.io/badge/PWA-installable_·_offline-E8437A?style=flat-square&labelColor=0F1012)
![tz](https://img.shields.io/badge/runs_on-PKT-8F9297?style=flat-square&labelColor=0F1012)

<br>

<img src="assets/strip.png" width="100%" alt="Maghrib under a shader sunset, the journey torso, and the night ring">

<sub>Maghrib at sunset &nbsp;·&nbsp; the journey torso &nbsp;·&nbsp; the ring at night</sub>

</div>

<br>

## The idea

You have a 9-to-6 job, five prayers to make at the masjid, and a body you want to change before Eid. There's no room for a plan that ignores any of them.

**getfit** is built around the day a working Muslim actually has. Salah anchors the schedule; the gym, work, study and meals fit between the prayers. Every part of the day becomes a small commit with a deadline. The app scores it and shows the result two ways: how consistent you were today, and how far you are into the 3-month journey.

A cut fails on the days you don't notice slipping. This makes every slip visible the same day.

```
Nov 10 ────────────── 90-day cut ─────────────── Feb 7 │ Ramadan ── Mar 7 │ Eid
71.3 kg                                         ~61 kg │           59 kg  │ in shape
```

<br>

## What's on the screen

<table>
<tr>
<td width="50%" valign="top">

### A sky that keeps time
The header is a live **WebGL shader** that follows Pakistan time, whatever the phone's zone says. The sun sits where it really is over Lahore, so dawn, noon, the Maghrib sunset and the night sky happen on screen when they happen outside. The moon shows its true phase, clouds drift, stars twinkle, and the masjid skyline lights its windows after dark. No WebGL? It falls back to a CSS sky.

### The day ring
One arc per window, with the five prayers drawn thick because they anchor the day. The live window burns and drifts embers; done windows glow; missed ones go red. A hand marks exactly where you are in the day.

</td>
<td width="50%" valign="top">

### The journey
Swipe the sky to see a torso that slims as the cut goes on: love handles shrink, the belly flattens, and **six abs fill with molten colour one by one**, top pair first. Full at a 75 average over 90 days. Every morning it replays yesterday's points pouring in.

### The moon chain
Every day to Eid is a disc showing **that night's moon**, tinted by the day's score. Three dark moons count down to Ramadan. Every day scoring 60+ extends the streak.

</td>
</tr>
</table>

<br>

## The rules

| Window | Weight | Rule |
|---|:-:|---|
| Fajr | ×3 | Masjid full, at home half. Locks 1 h after close. Sunday allows qaza at half |
| Zuhr · Asr · Maghrib | ×3 | Masjid full, at home half. Lock after 1 h |
| Juma | ×3 | Friday. Masjid only, on time only |
| Isha | ×3 | Masjid only, on time only |
| Stop work by 7:45 | ×1 | Mon–Fri |
| Phone down, into bed | ×2 | Sun–Thu nights |

Salah is marked **after** praying: the button unlocks 10 minutes into the window. At 9 pm a *Close the day* sheet catches anything left unmarked.

Plus daily checks: three clean meals, snack on plan, water in two tiers, workouts (5 a week, any split, any day) and abs (2 a week), steps (full at 11k, zero under 8k) and study hours.

### The fitness four
11k+ steps · a workout (or an allowed rest day) · 3 clean meals · 3.25 L+ water. Miss three of the four and the day is **red**. Two red days in a row puts a one-tap *Message the coach* button on the screen, with the message already written.

> **Thursday check-in.** Weight, eight tape measurements and progress photos by **9:00 am**. Miss it and the whole day scores zero.

```
day score = points earned ÷ points possible × 100
late ×0.6 · at home ×0.5 · qaza ×0.5 · snack over plan −1 · water not logged −1
```

<br>

## Trends

<img src="assets/trends.png" width="280" align="right" alt="Trends screen">

- **Weekly report card**, graded every Thursday, with the weakest windows named
- **Weight vs plan**, daily weigh-ins and their 7-day average against the line to 59 kg
- **Measurements**, latest value and change against each of the last four Thursdays, green toward the goal, red away from it, plus the full dated log
- **Day score**, daily bars against the 60 line
- **Salah**, masjid on time, late, at home, qaza, missed, per prayer
- **Training by week**, with no-skip misses in red
- **Study, steps and sleep** against target

<br clear="right">

## Built with

Nothing. One `index.html` with inline CSS, inline SVG and vanilla JS, a 10-line service worker, and a manifest. Data lives in the phone's `localStorage`; nothing is sent anywhere.

| | |
|---|---|
| Sky | One fragment shader, sun position computed for Lahore, mean lunar phase |
| Skyline, ring, torso, moon chain | Hand-built SVG, recomputed per render |
| Embers and bursts | One `<canvas>`, paused when the tab is hidden |
| Time | `Intl.DateTimeFormat` pinned to `Asia/Karachi` |
| Offline | Service worker, network first, cache fallback |
| Motion | Respects `prefers-reduced-motion` |

<br>

## Install it as an app

It's a website that installs like an app: own icon, full screen, no browser bar, works offline.

**Android (Chrome)**
1. Open **[sulemanawais.github.io/getfit](https://sulemanawais.github.io/getfit/)**
2. Tap **⋮** → **Add to Home screen** → **Install**
3. Open it from the new **ABS** icon

**iPhone (Safari)**
1. Open the same link in **Safari**
2. Tap **Share** → **Add to Home Screen** → **Add**

**Keep your data safe.** Everything lives on your phone. Settings → **Copy backup** every Thursday after the weigh-in, and paste it somewhere you trust. Restore pastes it back.

<br>

<div align="center">
<sub>Three months, five prayers a day, one goal: in shape by Eid. Fork it and make it yours.</sub>
</div>
