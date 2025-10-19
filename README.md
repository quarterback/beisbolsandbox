# OOTP Advanced Administrative Dashboard Guide

## Overview

The OOTP Advanced Dashboard is designed to quickly parse your player roster data and generate actionable strategic insights about your team composition, depth, strengths, and weaknesses. It identifies roster inefficiencies and provides recommendations for mid-season adjustments.

---

## Getting Started

### Step 1: Export Your Data

From OOTP, export your roster data as CSV:

**Batting Data:**
- Navigate to: Players → Batting Stats (or Player Ratings)
- Select all players or filter by team
- Export as CSV
- Include columns: player_id, team_id, position, and all batting_ratings columns (contact, power, gap, eye, strikeouts, etc.)

**Pitching Data:**
- Navigate to: Players → Pitching Stats (or Player Ratings)
- Export as CSV
- Include columns: player_id, team_id, role (starter/reliever/closer), and all pitching_ratings columns (stuff, movement, control, etc.)

### Step 2: Upload to Dashboard

You have **two options:**

**Option A: Drag & Drop (Easy!)**
1. Open the dashboard in your browser
2. Drag your CSV file(s) directly onto the upload area
3. You can upload multiple files at once
4. Click "Analyze" button

**Option B: Click to Browse**
1. Open the dashboard
2. Click the upload box
3. Select one or multiple CSV files from your computer
4. Click "Analyze"

**Option C: Manual Paste (If needed)**
1. Open the dashboard
2. Paste CSV text into the textarea below the upload area
3. Click "Analyze Data"

### Step 3: View Results

The dashboard instantly analyzes and displays:
- Roster depth breakdown
- Critical warnings (in red)
- Key observations and opportunities
- Position-by-position or role-by-role analysis

---

## Understanding the Analysis

### Key Metrics (Top Row)

**Batting Roster:**
- **Avg Contact**: Overall contact ability (20-50 scale). 25+ is above average.
- **Avg Power**: Overall power rating (20-50 scale). 30+ indicates power presence.
- **Avg Speed**: Running speed rating (25-70 scale).

**Pitching Roster:**
- **Avg Stuff**: Fastball quality/stuff (20-50 scale). 30+ is quality starter material.
- **Avg Control**: Control and command (20-50 scale). 35+ is excellent.
- **Rotation Composition**: Number of starters vs. bullpen arms.

### Roster Depth Section

Shows your position-by-position (or role-by-role) breakdown:

**Batting:**
- Positions: C, 1B, 2B, 3B, SS, LF, CF, RF, DH
- Shows: Number of players, average contact, average power
- **What to look for:** Gaps in depth, weak positions with only 1-2 qualified players

**Pitching:**
- Roles: Starter, Reliever, Closer, Long Relief
- Shows: Number of pitchers, average stuff, average control
- **What to look for:** Insufficient starter depth (need 4-5), weak reliever corps

### Critical Warnings ⚠️

Red-highlighted warnings indicate roster issues that require attention:
- "Offensive power below average" = weak lineup for run production
- "Insufficient starter depth" = rotation vulnerability to injury
- "High walk rates projected" = poor pitching control

### Key Observations

Green insights about your roster:
- Rotation/bullpen composition details
- Overall roster athleticism
- Development opportunities
- Competitive positioning

### Opportunities 🔧

Yellow recommendations for mid-season adjustments:
- "Weak lineup depth at: SS, 2B" = target trade acquisitions at these positions
- "Insufficient starting pitcher depth" = call up prospects or trade for help
- "Limited speed on roster" = adjust offensive strategy to power/contact focus

---

## How to Use This for Season Assessment

### Pre-Trade Deadline (Mid-Season)

1. **Identify Weaknesses:** Look at the Warnings section - these are your pain points
2. **Spot Depth Gaps:** The Roster Depth grid shows where you have only 1-2 options
3. **Target Positions:** The Opportunities section lists specific positions to upgrade
4. **Make Trades:** Use identified weaknesses to research trade market needs

**Example:** If you see "Weak lineup depth at: SS - only 2 players, avg contact 18", you know SS is a priority acquisition target.

### Lineup Optimization

1. **Efficiency Detection:** Check average contact/power ratings by position
2. **Right Spots:** Place high-contact players in leadoff/2-hole, power bats in middle
3. **Bench Alignment:** Identify depth players who should platoon or rotate

### Rotation Management

1. **Starter Count:** If you have only 3 starters, you're one injury away from trouble
2. **Stuff/Control:** Compare average stuff ratings to league (25-30 is average)
3. **Bullpen Role:** Reliever/Closer distinction affects usage patterns

---

## Advanced Interpretation

### Reading Position Profiles

**High Contact (25+), Low Power (<25):** Contact hitter - good for average, on-base focus
**Low Contact (<25), High Power (30+):** Power hitter - vulnerable to strikeouts but drives runs
**Balanced (20+/20+):** Well-rounded player - most valuable profile

### Reading Pitching Profiles

**High Stuff (30+), High Control (35+):** Ace-tier starter
**High Stuff (30+), Low Control (30-):** Power arm with command issues - strikeouts but walks
**Low Stuff (20-), High Control (35+):** Finesse pitcher - rely on contact management
**Both Low (<25):** Prospect or depth/relief only

### Interpreting Warnings vs Opportunities

**Warnings:** Immediate threats to competitiveness
- "Offensive power below average" = You'll lose 1v1 power battles
- "Control issues" = ERA will be higher, more inherited runners score

**Opportunities:** Actionable improvements
- "Weak SS depth" = Find SS prospects in farm or trade targets
- "Limited speed" = Build around contact/power, not stolen bases

---

## Monthly/Quarterly Usage

### Month 1 (April): Baseline Assessment
- Establish current roster strength
- Identify your team identity (power, speed, contact, pitching-heavy, etc.)
- Note positions to monitor for injuries

### Month 3 (June): Mid-Season Check-in
- Re-run the analysis after trades/callups
- Update roster composition
- Reassess playoff contention based on depth

### Month 6 (September): Deadline Retrospective
- Did you successfully address identified weaknesses?
- What unexpected issues emerged?
- Document lessons for next season

---

## CSV Format Requirements

**Required Columns for Batting:**
- `player_id` (unique identifier)
- `team_id` (which team owns player)
- `position` (1=C, 2=1B, 3=2B, 4=3B, 5=SS, 6=LF, 7=CF, 8=RF, 9=DH)
- `batting_ratings_overall_contact` (20-50 scale)
- `batting_ratings_overall_power` (20-50 scale)
- `running_ratings_speed` (25-70 scale)

**Required Columns for Pitching:**
- `player_id`
- `team_id`
- `role` (11=Starter, 12=Reliever, 13=Closer, 10=Long Relief)
- `pitching_ratings_overall_stuff` (20-50 scale)
- `pitching_ratings_overall_control` (20-50 scale)
- `pitching_ratings_misc_velocity` (optional, velocity rating)

The dashboard is flexible - include any columns you want, but these core ones enable deep analysis.

---

## Troubleshooting

**"Could not parse CSV data"**
- Check that your first row contains headers (column names)
- Verify no blank lines between header and data
- Ensure proper comma separation (not tabs or semicolons)

**"No insights generated"**
- You may have very few players (need 10+)
- Or your player stats are all zero/empty
- Check that the CSV includes rating columns, not just player names

**Dashboard shows "0" for all metrics**
- Your CSV may not include the stat columns the dashboard looks for
- Verify column names match expected format (e.g., "batting_ratings_overall_contact")

---

## Tips & Tricks

1. **Separate by Level:** Analyze MLB, AAA, AA separately - each tells a different story
2. **Before/After Trades:** Run analysis before and after major roster moves to validate
3. **Prospect Pool:** Export your farm system separately to identify hidden gems
4. **Trade Deadline Prep:** Generate reports before negotiating - know your needs precisely
5. **League Comparison:** If league data available, compare your average stats to league average

---

## Next Steps

- **Version 2 Coming:** Multi-season trend analysis
- **Integration:** Connect directly to OOTP game files (beta)
- **League Context:** Automatic comparison to league-wide stats
- **AI Insights:** Claude-powered strategic recommendations

---

## Questions or Feature Requests?

The dashboard currently handles:
- ✅ Batting roster analysis
- ✅ Pitching roster analysis
- ✅ Depth charting by position/role
- ✅ Weakness identification
- ✅ Trade target recommendations

Future versions will add:
- 🔄 Contract/salary analysis
- 🔄 Prospect evaluation
- 🔄 Trade value calculations
- 🔄 League-wide comparison
- 🔄 Season projection models

Enjoy analyzing your team!
