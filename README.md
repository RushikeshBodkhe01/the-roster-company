# The Roster Company

Rostering, payroll and compliance for small Irish retail. Trial demo for a single-site, ~12-person shop in the Dublin area.

Live demo: https://rushikeshbodkhe01.github.io/the-gem-roster/

## Background

I work weekends at a single-site retail business. The owner rosters ~12 staff every Sunday using paper and WhatsApp. I built this to replace that.

It handles three things Bizimply and similar tools don't do well for a small Irish retail business:

- Right-to-work expiry tracking (Stamp 2, Working Holiday, Stamp 1G)
- Demand forecast that uses live weather (a coastal business lives and dies by sunshine)
- Payroll output that drops straight into BrightPay with correct PRSI and USC bands

All staff in the demo are anonymised as Staff A through Staff N.

## What's in it

Auto-generated weekly roster, weighted by the 7-day Open-Meteo forecast. Click any cell to edit a shift.

Right-to-work tracker per staff member with a 30-day expiry warning.

Compliance checker that runs against the Organisation of Working Time Act 1997, the National Minimum Wage Act 2000, and the Employment Permits Acts after every change. Flags breaches of the 48-hour week, 11-hour daily rest, age-band minimum wage, and Stamp 2 20-hour term-time cap.

Payslip generator with PAYE, PRSI Class A1, USC bands, and the 23% employer uplift. Exports a BrightPay-ready CSV.

Shift swap marketplace, availability heatmap, weekly payroll summary, leave approvals.

## Stack

Next.js (App Router), React, Tailwind, Supabase for Postgres and auth, Claude API for shift suggestion logic and supplier email drafts, Open-Meteo for the forecast, Resend for sending payslips. Hosted on Vercel, demo on GitHub Pages.

## What it saves

Rough numbers from time-and-motion on my own shifts:

- Rostering: ~2 hours down to ~15 minutes a week
- Payroll prep: ~90 minutes down to ~10
- Right-to-work compliance: tracked properly instead of in someone's head

At roughly €18/hr manager rate that's around €2,500–€2,800 a year, plus avoiding one WRC fine which would dwarf that.

I haven't pitched this to the owner yet. That's the next conversation.

## What's next

SMS shift notifications, multi-store support if a second site opens, and eventually pushing PRSI returns straight to Revenue's ROS API. The plan is to keep building it for the trial client first, then offer it to one or two other Dublin SMEs.

## Why this exists

I'm an MSc Business Analytics grad from DCU job-hunting for Business Analyst and Data Analyst roles in Dublin. The fastest way I've found to learn what stakeholders actually need is to be the stakeholder.

Stamp 1G, work-authorised in Ireland until 2028.
