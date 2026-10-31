---
name: content-calendar
description: Build a realistic posting calendar from a stock of ready videos and platform rules. Use when the user lists finished videos, asks what to post today or this week, wants a schedule for one or more accounts, or needs to spread a video stock across days without burning out the audience or the stock. Works in WIB by default for Indonesian creators.
---

# Content Calendar

A calendar is a promise the creator can actually keep. Schedule from the stock that exists, not from videos that are "almost done". A smaller schedule that ships beats an ambitious one that collapses in three days.

## Inputs to collect first

- The video stock: list of finished videos with a one-line description each (required).
- Platforms and accounts, and how many posts per day each one takes.
- Fixed rules from the user: posting times, series that must stay together, products that must not repeat back-to-back.

If the user gives a stock count instead of a list, plan by count and label slots by theme, not by invented video titles.

## Planning rules

1. **Pace the stock.** Spread the stock across the requested horizon evenly. If the stock runs out before the horizon ends, say exactly which day it runs out and what that day onward looks like. Never silently double-post the same video to fill a gap.
2. **Rotate, do not repeat.** The same product or topic does not appear on the same account two slots in a row. Alternate categories so the feed feels varied.
3. **Anchor slots to behavior.** Default anchor times for Indonesian audiences, when the user has no fixed times: morning commute 06:00-08:00, lunch 12:00-13:00, evening prime 19:00-21:00 WIB. User-fixed times always override these defaults.
4. **Series stay in order.** Episodes of a series post in sequence, one per slot, never two episodes of the same series in one day unless the user asks for a binge drop.
5. **Front-load strength.** Put the strongest video in the highest-traffic slot of each day; use weaker stock in secondary slots. Ask the user to mark their strongest videos if it is not obvious.

## Output format

A day-by-day table: date, time (with timezone), platform/account, video, and one short note column for anything the user must prepare (a product link, a thumbnail, a basket check). After the table:

- Stock remaining after the plan
- The first day the stock runs dry, if it does
- Any rule from the user that could not be honored, stated plainly

## Rules

- Dates must be real: verify the weekday matches the date before presenting the plan.
- Never schedule in the past relative to the user's timezone.
- If two user rules conflict (for example, a fixed daily count and a stock too small for the horizon), surface the conflict and offer the two resolutions instead of picking silently.
