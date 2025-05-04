# 🏟️ Barcelona Champions League 2024–2025 Stats (Scraping Project)

This repository contains datasets scraped from **FBref.com** representing **Barcelona's performance** in the **2024–2025 UEFA Champions League** season. The data includes detailed stats for each player and match across multiple aspects like shooting, passing, defending, goalkeeping, and more.


## 📁 Dataset Contents

The dataset was collected by scraping FBref’s publicly available tables using Python and Playwright. The following tables were extracted:

| Filename | Description |
|----------|-------------|
| `Standard_Stats_2024-2025_Barcelona:_Champions_League.csv` | Basic stats per player (games, goals, assists, etc.) |
| `Scores_&_Fixtures_2024-2025_Barcelona:_Champions_League.csv` | Match results and dates |
| `Goalkeeping_2024-2025_Barcelona:_Champions_League.csv` | Core goalkeeping stats |
| `Advanced_Goalkeeping_2024-2025_Barcelona:_Champions_League.csv` | Deeper goalkeeping analysis |
| `Shooting_2024-2025_Barcelona:_Champions_League.csv` | Shot types, distance, goals |
| `Passing_2024-2025_Barcelona:_Champions_League.csv` | Total passes, key passes |
| `Pass_Types_2024-2025_Barcelona:_Champions_League.csv` | Breakdown of pass types |
| `Goal_and_Shot_Creation_2024-2025_Barcelona:_Champions_League.csv` | Offensive contribution |
| `Defensive_Actions_2024-2025_Barcelona:_Champions_League.csv` | Tackles, interceptions |
| `Possession_2024-2025_Barcelona:_Champions_League.csv` | Ball retention & dribbles |
| `Playing_Time_2024-2025_Barcelona:_Champions_League.csv` | Minutes, starts, substitutions |
| `Miscellaneous_Stats_2024-2025_Barcelona:_Champions_League.csv` | Other stats like fouls, cards |
| `League_phase,_Champions_League.csv` | Champions League group/phase info |

---


## 📌 Column Descriptions

> Each section below will explain the columns in the raw `.csv` files for better readability and use in analysis.

<details>
<summary><strong>Standard Stats</strong></summary>

| Column | Description |
|--------|-------------|
| `Player` | Name of the player |
| `Nation` | Nationality — derived in order: senior international, youth level, Wikipedia citizenship, or birthplace |
| `Pos` | Position(s) played (e.g., GK, CB, MF, FW). Includes detailed roles like AM, DM, LB, etc. |
| `Age` | Age in years-days as of the season start (August 1 for winter leagues) |
| `MP` | Matches Played |
| `Starts` | Matches Started |
| `Min` | Minutes Played |
| `90s` | 90s Played — Minutes / 90 |
| `Gls` | Goals Scored |
| `Ast` | Assists |
| `G+A` | Goals + Assists |
| `G-PK` | Non-Penalty Goals |
| `PK` | Penalties Scored |
| `PKatt` | Penalty Attempts |
| `CrdY` | Yellow Cards |
| `CrdR` | Red Cards |
| `xG` | Expected Goals (incl. penalties) — Provided by Opta |
| `npxG` | Non-Penalty xG |
| `xAG` | Expected Assisted Goals |
| `npxG+xAG` | Total of non-penalty xG and xAG |
| `PrgC` | Progressive Carries |
| `PrgP` | Progressive Passes |
| `PrgR` | Progressive Passes Received |
| `Gls/90` | Goals per 90 minutes |
| `Ast/90` | Assists per 90 minutes |
| `G+A/90` | Goals + Assists per 90 minutes |
| `G-PK/90` | Non-Penalty Goals per 90 minutes |
| `G+A-PK/90` | (G+A) minus PKs per 90 minutes |
| `xG/90` | Expected Goals per 90 |
| `xAG/90` | Expected Assisted Goals per 90 |
| `xG+xAG/90` | xG + xAG per 90 |
| `npxG/90` | Non-Penalty xG per 90 |
| `npxG+xAG/90` | Non-Penalty xG + xAG per 90 |
| `Matches` | Number of Matches in dataset |

</details>

<details>
<summary><strong>Scores & Fixtures</strong></summary>

| Column | Description |
|--------|-------------|
| `Date` | Local match date |
| `Time` | Local venue time (24-hour) |
| `Round` | Competition phase (e.g. Group Stage, Quarterfinals) |
| `Day` | Day of the week |
| `Venue` | Stadium or ground |
| `Result` | Match result (e.g. W, D, L) |
| `GF` | Goals For |
| `GA` | Goals Against |
| `Opponent` | Opposing team |
| `xG` | Expected Goals scored |
| `xGA` | Expected Goals conceded |
| `Poss` | Possession percentage |
| `Attendance` | Match attendance |
| `Captain` | Team captain for the match |
| `Formation` | Starting formation |
| `Opp Formation` | Opponent's formation |
| `Referee` | Match official |
| `Match Report` | Link to official match report |
| `Notes` | Additional match notes |

</details>
<details>
<summary><strong>Goalkeeping</strong></summary>

| Column | Description |
|--------|-------------|
| `Player` | Player |
| `Nation` | Nationality of the player.<br>First, we check our records in international play at senior level.<br>Then youth level.<br>Then citizenship presented on wikipedia.<br>Finally, we use their birthplace when available. |
| `Pos` | <strong>Position</strong><br>Position most commonly played by the player<br>GK - Goalkeepers<br>DF - Defenders<br>MF - Midfielders<br>FW - Forwards<br>FB - Fullbacks<br>LB - Left Backs<br>RB - Right Backs<br>CB - Center Backs<br>DM - Defensive Midfielders<br>CM - Central Midfielders<br>LM - Left Midfielders<br>RM - Right Midfielders<br>WM - Wide Midfielders<br>LW - Left Wingers<br>RW - Right Wingers<br>AM - Attacking Midfielders |
| `Age` | <strong>Current age</strong><br>Age at season start<br>Given on August 1 for winter leagues<br>and February 1 for summer leagues. |
| `MP` | <strong>Matches Played</strong><br>Matches Played by the player or squad |
| `Starts` | Game or games started by player |
| `Min` | <strong>Minutes</strong> |
| `90s` | <strong>90s Played</strong><br>Minutes played divided by 90 |
| `GA` | <strong>Goals Against</strong> |
| `GA90` | <strong>Goals Against/90</strong><br>Goals Against per 90 minutes |
| `SoTA` | <strong>Shots on Target Against</strong> |
| `Saves` | Saves |
| `Save%` | <strong>Save Percentage</strong><br>(Shots on Target Against - Goals Against) / Shots on Target Against<br>Note: does not include penalty kicks |
| `W` | <strong>Wins</strong> |
| `D` | <strong>Draws</strong> |
| `L` | <strong>Losses</strong> |
| `CS` | <strong>Clean Sheets</strong><br>Full matches by goalkeeper where no goals are allowed. |
| `CS%` | <strong>Clean Sheet Percentage</strong><br>Percentage of matches that result in clean sheets. |
| `PKatt` | <strong>Penalty Kicks Attempted</strong> |
| `PKA` | <strong>Penalty Kicks Allowed</strong> |
| `PKsv` | <strong>Penalty Kicks Saved</strong> |
| `PKm` | <strong>Penalty Kicks Missed</strong> |
| `Save%` | <strong>Save% (Penalty Kicks)</strong><br>Penalty Save Percentage<br>Penalty Kick Goals Against / Penalty Kick Attempts<br>Penalty shots that miss the target are not included |
| `Matches` | Matches |

</details>

<details>
<summary><strong>Advanced Goalkeeping</strong></summary>

| Column | Description |
|--------|-------------|
| `Player` | Player |
| `Nation` | Nationality of the player.<br>First, we check our records in international play at senior level.<br>Then youth level.<br>Then citizenship presented on wikipedia.<br>Finally, we use their birthplace when available. |
| `Pos` | <strong>Position</strong><br>Position most commonly played by the player<br>GK - Goalkeepers<br>DF - Defenders<br>MF - Midfielders<br>FW - Forwards<br>FB - Fullbacks<br>LB - Left Backs<br>RB - Right Backs<br>CB - Center Backs<br>DM - Defensive Midfielders<br>CM - Central Midfielders<br>LM - Left Midfielders<br>RM - Right Midfielders<br>WM - Wide Midfielders<br>LW - Left Wingers<br>RW - Right Wingers<br>AM - Attacking Midfielders |
| `Age` | <strong>Current age</strong><br>Age at season start<br>Given on August 1 for winter leagues<br>and February 1 for summer leagues. |
| `90s` | <strong>90s Played</strong><br>Minutes played divided by 90 |
| `GA` | <strong>Goals Against</strong> |
| `PKA` | <strong>Penalty Kicks Allowed</strong> |
| `FK` | <strong>Free Kick Goals Against</strong> |
| `CK` | <strong>Corner Kick Goals Against</strong> |
| `OG` | <strong>Own Goals Scored Against Goalkeeper</strong> |
| `PSxG` | <strong>Post-Shot Expected Goals</strong><br>Expected goals based on how likely the goalkeeper is to save the shot<br>Includes penalties, excludes shootouts<br>Provided by Opta |
| `PSxG/SoT` | Post-Shot Expected Goals per Shot on Target<br>Not including penalty kicks<br>Higher = harder shots to stop<br>Provided by Opta |
| `PSxG+/-` | <strong>PSxG-GA</strong><br>PSxG minus Goals Allowed<br>Positive = better performance or luck |
| `/90` | <strong>PSxG-GA/90</strong><br>Same as above, per 90 minutes |
| `Cmp` | <strong>Passes Completed (Launched)</strong><br>Passes longer than 40 yards |
| `Att` | <strong>Passes Attempted (Launched)</strong><br>Passes longer than 40 yards |
| `Cmp%` | <strong>Pass Completion % (Launched)</strong> |
| `Att (GK)` | <strong>Passes Attempted (GK)</strong><br>Not including goal kicks |
| `Thr` | <strong>Throws Attempted</strong> |
| `Launch%` | <strong>Launch %</strong><br>% of non-goal-kick passes over 40 yards |
| `AvgLen` | <strong>Average Pass Length</strong><br>In yards, excluding goal kicks |
| `Att` | <strong>Goal Kicks Attempted</strong> |
| `Launch%` | <strong>Launch % (Goal Kicks)</strong><br>% of goal kicks longer than 40 yards |
| `AvgLen` | <strong>Average Length of Goal Kicks</strong><br>In yards |
| `Opp` | <strong>Crosses Faced</strong><br>Opponent's crosses into penalty area |
| `Stp` | <strong>Crosses Stopped</strong> |
| `Stp%` | <strong>Crosses Stopped %</strong> |
| `#OPA` | <strong>Defensive Actions Outside Penalty Area</strong> |
| `#OPA/90` | Per 90 minutes |
| `AvgDist` | <strong>Avg. Distance of Defensive Actions</strong><br>From goal, in yards |
| `Matches` | Matches |

</details>
<details>
<summary><strong>Shooting</strong></summary>

| Column | Description |
|--------|-------------|
| `Player` | Player |
| `Nation` | Nationality of the player. First, we check our records in international play at senior level. Then youth level. Then citizenship presented on Wikipedia. Finally, we use their birthplace when available. |
| `Pos` | <strong>Position</strong><br>Position most commonly played by the player<br>GK - Goalkeepers<br>DF - Defenders<br>MF - Midfielders<br>FW - Forwards<br>FB - Fullbacks<br>LB - Left Backs<br>RB - Right Backs<br>CB - Center Backs<br>DM - Defensive Midfielders<br>CM - Central Midfielders<br>LM - Left Midfielders<br>RM - Right Midfielders<br>WM - Wide Midfielders<br>LW - Left Wingers<br>RW - Right Wingers<br>AM - Attacking Midfielders |
| `Age` | <strong>Current age</strong><br>Age at season start. Given on August 1 for winter leagues and February 1 for summer leagues. |
| `90s` | <strong>90s Played</strong><br>Minutes played divided by 90. |
| `Gls` | <strong>Goals</strong><br>Goals scored or allowed. |
| `Sh` | <strong>Shots Total</strong><br>Shots Total (does not include penalty kicks). |
| `SoT` | <strong>Shots on Target</strong><br>Shots on Target (note: shots on target do not include penalty kicks). |
| `SoT%` | <strong>Shots on Target %</strong><br>Percentage of shots that are on target. Minimum .395 shots per squad game to qualify as a leader. Note: Shots on target do not include penalty kicks. |
| `Sh/90` | <strong>Shots Total/90</strong><br>Shots total per 90 minutes. Minimum 30 minutes played per squad game to qualify as a leader. |
| `SoT/90` | <strong>Shots on target/90</strong><br>Shots on target per 90 minutes. Minimum 30 minutes played per squad game to qualify as a leader. Note: Shots on target do not include penalty kicks. |
| `G/Sh` | <strong>Goals/Shot</strong><br>Goals per shot. Minimum .395 shots per squad game to qualify as a leader. |
| `G/SoT` | <strong>Goals/Shot on Target</strong><br>Goals per shot on target. Minimum .111 shots on target per squad game to qualify as a leader. Note: Shots on target do not include penalty kicks. |
| `Dist` | <strong>Average Shot Distance</strong><br>Average distance, in yards, from goal of all shots taken. Minimum .395 shots per squad game to qualify as a leader. Does not include penalty kicks. |
| `FK` | <strong>Shots from Free Kicks</strong><br>Shots from Free Kicks. |
| `PK` | <strong>Penalty Kicks Made</strong><br>Penalty Kicks Made. |
| `PKatt` | <strong>Penalty Kicks Attempted</strong><br>Penalty Kicks Attempted. |
| `xG` | <strong>xG: Expected Goals</strong><br>Expected Goals. xG totals include penalty kicks, but do not include penalty shootouts (unless otherwise noted). An underline indicates there is a match that is missing data, but will be updated when available. |
| `npxG` | <strong>npxG: Non-Penalty xG</strong><br>Non-Penalty Expected Goals. An underline indicates there is a match that is missing data, but will be updated when available. |
| `npxG/Sh` | <strong>npxG/Shot</strong><br>Non-Penalty Expected Goals per shot. An underline indicates there is a match that is missing data, but will be updated when available. Minimum .395 shots per squad game to qualify as a leader. |
| `G-xG` | <strong>Goals - xG</strong><br>Goals minus Expected Goals. xG totals include penalty kicks, but do not include penalty shootouts (unless otherwise noted). An underline indicates there is a match that is missing data, but will be updated when available. |
| `np:G-xG` | <strong>Non-Penalty Goals - npxG</strong><br>Non-Penalty Goals minus Non-Penalty Expected Goals. xG totals include penalty kicks, but do not include penalty shootouts (unless otherwise noted). An underline indicates there is a match that is missing data, but will be updated when available. |
| `Matches` | Matches |

</details>

<details>
<summary><strong>Passing </strong></summary>

| Column | Description |
|--------|-------------|
| `Player` | Player |
| `Nation` | Nationality of the player. First, we check our records in international play at senior level. Then youth level. Then citizenship presented on Wikipedia. Finally, we use their birthplace when available. |
| `Pos` | <strong>Position</strong><br>Position most commonly played by the player<br>GK - Goalkeepers<br>DF - Defenders<br>MF - Midfielders<br>FW - Forwards<br>FB - Fullbacks<br>LB - Left Backs<br>RB - Right Backs<br>CB - Center Backs<br>DM - Defensive Midfielders<br>CM - Central Midfielders<br>LM - Left Midfielders<br>RM - Right Midfielders<br>WM - Wide Midfielders<br>LW - Left Wingers<br>RW - Right Wingers<br>AM - Attacking Midfielders |
| `Age` | <strong>Current age</strong><br>Age at season start. Given on August 1 for winter leagues and February 1 for summer leagues. |
| `90s` | <strong>90s Played</strong><br>Minutes played divided by 90. |
| `Cmp` | <strong>Passes Completed</strong><br>Passes Completed. Includes live ball passes (including crosses) as well as corner kicks, throw-ins, free kicks and goal kicks. |
| `Att` | <strong>Passes Attempted</strong><br>Passes Attempted. Includes live ball passes (including crosses) as well as corner kicks, throw-ins, free kicks and goal kicks. |
| `Cmp%` | <strong>Pass Completion %</strong><br>Pass Completion Percentage. Minimum 30 minutes played per squad game to qualify as a leader. Includes live ball passes (including crosses) as well as corner kicks, throw-ins, free kicks and goal kicks. |
| `TotDist` | <strong>Total Passing Distance</strong><br>Total distance, in yards, that completed passes have traveled in any direction. |
| `PrgDist` | <strong>Progressive Passing Distance</strong><br>Total distance, in yards, that completed passes have traveled towards the opponent's goal. Passes away from the opponent's goal are counted as zero progressive yards. |
| `Cmp (Short)` | <strong>Passes Completed (Short)</strong><br>Passes completed between 5 and 15 yards. |
| `Att (Short)` | <strong>Passes Attempted (Short)</strong><br>Passes attempted between 5 and 15 yards. |
| `Cmp% (Short)` | <strong>Pass Completion % (Short)</strong><br>Pass Completion Percentage for passes between 5 and 15 yards. Minimum 30 minutes played per squad game to qualify as a leader. |
| `Cmp (Medium)` | <strong>Passes Completed (Medium)</strong><br>Passes completed between 15 and 30 yards. |
| `Att (Medium)` | <strong>Passes Attempted (Medium)</strong><br>Passes attempted between 15 and 30 yards. |
| `Cmp% (Medium)` | <strong>Pass Completion % (Medium)</strong><br>Pass Completion Percentage for passes between 15 and 30 yards. Minimum 30 minutes played per squad game to qualify as a leader. |
| `Cmp (Long)` | <strong>Passes Completed (Long)</strong><br>Passes completed longer than 30 yards. |
| `Att (Long)` | <strong>Passes Attempted (Long)</strong><br>Passes attempted longer than 30 yards. |
| `Cmp% (Long)` | <strong>Pass Completion % (Long)</strong><br>Pass Completion Percentage for passes longer than 30 yards. Minimum 30 minutes played per squad game to qualify as a leader. |
| `Ast` | <strong>Assists</strong><br>Assists. |
| `xAG` | <strong>xAG: Exp. Assisted Goals</strong><br>Expected Assisted Goals. xG which follows a pass that assists a shot. |
| `xA` | <strong>xA: Expected Assists</strong><br>Expected Assists. The likelihood each completed pass becomes a goal assist given the pass type, phase of play, location, and distance. |
| `A-xAG` | <strong>Assists - xAG</strong><br>Assists minus Expected Goals Assisted. |
| `KP` | <strong>Key Passes</strong><br>Passes that directly lead to a shot (assisted shots). |
| `1/3` | <strong>Passes into Final Third</strong><br>Completed passes that enter the 1/3 of the pitch closest to the goal. |
| `PPA` | <strong>Passes into Penalty Area</strong><br>Completed passes into the 18-yard box. |
| `CrsPA` | <strong>Crosses into Penalty Area</strong><br>Completed crosses into the 18-yard box. |
| `PrgP` | <strong>Progressive Passes</strong><br>Completed passes that move the ball towards the opponent's goal line at least 10 yards from its furthest point in the last six passes, or any completed pass into the penalty area. Excludes passes from the defending 40% of the pitch. |
| `Matches` | Matches |

</details>
<details>
<summary><strong>Defensive Actions</strong></summary>

| Column | Description |
|--------|-------------|
| `Player` | Player |
| `Nation` | Nationality of the player.<br>First, we check our records in international play at senior level.<br>Then youth level.<br>Then citizenship presented on wikipedia.<br>Finally, we use their birthplace when available. |
| `Pos` | Position most commonly played by the player<br>GK - Goalkeepers<br>DF - Defenders<br>MF - Midfielders<br>FW - Forwards<br>FB - Fullbacks<br>LB - Left Backs<br>RB - Right Backs<br>CB - Center Backs<br>DM - Defensive Midfielders<br>CM - Central Midfielders<br>LM - Left Midfielders<br>RM - Right Midfielders<br>WM - Wide Midfielders<br>LW - Left Wingers<br>RW - Right Wingers<br>AM - Attacking Midfielders |
| `Age` | Current age<br>Age at season start<br>Given on August 1 for winter leagues<br>and February 1 for summer leagues. |
| `90s` | 90s Played<br>Minutes played divided by 90 |
| `Tkl` | Tackles<br>Number of players tackled |
| `TklW` | Tackles Won<br>Tackles in which the tackler's team won possession of the ball |
| `Def 3rd` | Tackles (Def 3rd)<br>Tackles in defensive 1/3 |
| `Mid 3rd` | Tackles (Mid 3rd)<br>Tackles in middle 1/3 |
| `Att 3rd` | Tackles (Att 3rd)<br>Tackles in attacking 1/3 |
| `Dribblers Tackled` | Number of dribblers tackled |
| `Att` | Dribbles Challenged<br>Number of unsuccessful challenges plus number of dribblers tackled |
| `Tkl%` | % of Dribblers Tackled<br>Percentage of dribblers tackled<br>Dribblers tackled divided by number of attempts to challenge an opposing dribbler<br>Minimum .625 dribblers challenged per squad game to qualify as a leader |
| `Lost` | Challenges Lost<br>Number of unsuccessful attempts to challenge a dribbling player |
| `Blocks` | Number of times blocking the ball by standing in its path |
| `Sh` | Shots Blocked<br>Number of times blocking a shot by standing in its path |
| `Pass` | Passes Blocked<br>Number of times blocking a pass by standing in its path |
| `Int` | Interceptions<br>Interceptions |
| `Tkl+Int` | Number of players tackled plus number of interceptions |
| `Clr` | Clearances<br>Clearances |
| `Err` | Errors<br>Mistakes leading to an opponent's shot |
| `Matches` | Matches |
</details>

<details>
<summary><strong>Possession</strong></summary>

| Column | Description |
|--------|-------------|
| `Player` | Player |
| `Nation` | Nationality of the player.<br>First, we check our records in international play at senior level.<br>Then youth level.<br>Then citizenship presented on wikipedia.<br>Finally, we use their birthplace when available. |
| `Pos` | Position most commonly played by the player<br>GK - Goalkeepers<br>DF - Defenders<br>MF - Midfielders<br>FW - Forwards<br>FB - Fullbacks<br>LB - Left Backs<br>RB - Right Backs<br>CB - Center Backs<br>DM - Defensive Midfielders<br>CM - Central Midfielders<br>LM - Left Midfielders<br>RM - Right Midfielders<br>WM - Wide Midfielders<br>LW - Left Wingers<br>RW - Right Wingers<br>AM - Attacking Midfielders |
| `Age` | Current age<br>Age at season start<br>Given on August 1 for winter leagues<br>and February 1 for summer leagues. |
| `90s` | 90s Played<br>Minutes played divided by 90 |
| `Touches` | Number of times a player touched the ball. Note: Receiving a pass, then dribbling, then sending a pass counts as one touch |
| `Def Pen` | Touches (Def Pen)<br>Touches in defensive penalty area |
| `Def 3rd` | Touches (Def 3rd)<br>Touches in defensive 1/3 |
| `Mid 3rd` | Touches (Mid 3rd)<br>Touches in middle 1/3 |
| `Att 3rd` | Touches (Att 3rd)<br>Touches in attacking 1/3 |
| `Att Pen` | Touches (Att Pen)<br>Touches in attacking penalty area |
| `Live` | Touches (Live-Ball)<br>Live-ball touches. Does not include corner kicks, free kicks, throw-ins, kick-offs, goal kicks or penalty kicks |
| `Att` | Take-Ons Attempted<br>Number of attempts to take on defenders while dribbling |
| `Succ` | Successful Take-Ons<br>Number of defenders taken on successfully, by dribbling past them<br>Unsuccessful take-ons include attempts where the dribbler retained possession but was unable to get past the defender |
| `Succ%` | Successful Take-On %<br>Percentage of Take-Ons Completed Successfully<br>Unsuccessful take-ons include attempts where the dribbler retained possession but was unable to get past the defender<br>Minimum .5 take-ons per squad game to qualify as a leader |
| `Tkld` | Times Tackled During Take-On<br>Number of times tackled by a defender during a take-on attempt |
| `Tkld%` | Tackled During Take-On Percentage<br>Percentage of time tackled by a defender during a take-on attempt<br>Minimum .5 take-ons per squad game to qualify as a leader |
| `Carries` | Number of times the player controlled the ball with their feet |
| `TotDist` | Total Carrying Distance<br>Total distance, in yards, a player moved the ball while controlling it with their feet, in any direction |
| `PrgDist` | Progressive Carrying Distance<br>Total distance, in yards, a player moved the ball while controlling it with their feet towards the opponent's goal |
| `PrgC` | Progressive Carries<br>Carries that move the ball towards the opponent's goal line at least 10 yards from its furthest point in the last six passes, or any carry into the penalty area. Excludes carries which end in the defending 50% of the pitch |
| `1/3` | Carries into Final Third<br>Carries that enter the 1/3 of the pitch closest to the goal |
| `CPA` | Carries into Penalty Area<br>Carries into the 18-yard box |
| `Mis` | Miscontrols<br>Number of times a player failed when attempting to gain control of a ball |
| `Dis` | Dispossessed<br>Number of times a player loses control of the ball after being tackled by an opposing player. Does not include attempted take-ons |
| `Rec` | Passes Received<br>Number of times a player successfully received a pass |
| `PrgR` | Progressive Passes Received<br>Completed passes that move the ball towards the opponent's goal line at least 10 yards from its furthest point in the last six passes, or any completed pass into the penalty area. Excludes passes from the defending 40% of the pitch |
| `Matches` | Matches |
</details>
<details>
<summary><strong>Playing Time</strong></summary>

| Column  | Description |
|---------|-------------|
| `Player` | Player |
| `Nation` | Nationality of the player.<br>First, we check our records in international play at senior level.<br>Then youth level.<br>Then citizenship presented on Wikipedia.<br>Finally, we use their birthplace when available. |
| `Pos` | <strong>Position</strong><br>Position most commonly played by the player<br>GK - Goalkeepers<br>DF - Defenders<br>MF - Midfielders<br>FW - Forwards<br>FB - Fullbacks<br>LB - Left Backs<br>RB - Right Backs<br>CB - Center Backs<br>DM - Defensive Midfielders<br>CM - Central Midfielders<br>LM - Left Midfielders<br>RM - Right Midfielders<br>WM - Wide Midfielders<br>LW - Left Wingers<br>RW - Right Wingers<br>AM - Attacking Midfielders |
| `Age` | <strong>Current age</strong><br>Age at season start<br>Given on August 1 for winter leagues<br>and February 1 for summer leagues. |
| `MP` | <strong>Matches Played</strong><br>Matches Played by the player or squad |
| `Min` | <strong>Minutes</strong><br>Minutes played by the player |
| `Mn/MP` | <strong>Minutes Per Match Played</strong><br>Minutes per match played |
| `Min%` | <strong>Percentage of Squad Minutes Played</strong><br>Percentage of minutes played by the player compared to the team's total minutes played |
| `90s` | <strong>90s Played</strong><br>Minutes played divided by 90 |
| `Starts` | Game or games started by player |
| `Mn/Start` | <strong>Minutes Per Match Started</strong><br>Minutes per match started |
| `Compl` | <strong>Complete Matches Played</strong><br>Complete matches played |
| `Subs` | <strong>Substitute Appearances</strong><br>Games as a substitute |
| `Mn/Sub` | <strong>Minutes Per Substitution</strong><br>Minutes per substitution |
| `unSub` | <strong>Matches as Unused Sub</strong><br>Games as an unused substitute |
| `PPM` | <strong>Points per Match</strong><br>Average number of points earned by the team from matches in which the player appeared |
| `onG` | <strong>Goals Scored (on pitch)</strong><br>Goals scored by team while on pitch |
| `onGA` | <strong>Goals Allowed (on pitch)</strong><br>Goals allowed by team while on pitch |
| `+/-` | <strong>Plus/Minus</strong><br>Goals scored minus goals allowed by the team while the player was on the pitch |
| `+/-90` | <strong>Plus/Minus/90</strong><br>Goals scored minus goals allowed by the team per 90 minutes played |
| `On-Off` | <strong>Plus/Minus Net per 90 Minutes</strong><br>Net goals per 90 minutes played |
| `onxG` | <strong>xG (on pitch)</strong><br>Expected goals by team while on pitch |
| `onxGA` | <strong>xGA (on pitch)</strong><br>Expected goals allowed by team while on pitch |
| `xG+/-` | <strong>xG Plus/Minus</strong><br>Expected goals scored minus expected goals allowed while on pitch |
| `xG+/-90` | <strong>xG Plus/Minus/90</strong><br>Expected goals scored minus expected goals allowed per 90 minutes played |
| `On-Off` | <strong>xG On-Off</strong><br>Net expected goals per 90 minutes played by the team while the player was on the pitch minus the team's net expected goals when the player was off |
| `Matches` | Matches |

</details>
<details>
<summary><strong>Miscellaneous</strong></summary>

| Column  | Description |
|---------|-------------|
| `Player` | Player |
| `Nation` | Nationality of the player.<br>First, we check our records in international play at senior level.<br>Then youth level.<br>Then citizenship presented on Wikipedia.<br>Finally, we use their birthplace when available. |
| `Pos` | <strong>Position</strong><br>Position most commonly played by the player<br>GK - Goalkeepers<br>DF - Defenders<br>MF - Midfielders<br>FW - Forwards<br>FB - Fullbacks<br>LB - Left Backs<br>RB - Right Backs<br>CB - Center Backs<br>DM - Defensive Midfielders<br>CM - Central Midfielders<br>LM - Left Midfielders<br>RM - Right Midfielders<br>WM - Wide Midfielders<br>LW - Left Wingers<br>RW - Right Wingers<br>AM - Attacking Midfielders |
| `Age` | <strong>Current age</strong><br>Age at season start<br>Given on August 1 for winter leagues<br>and February 1 for summer leagues. |
| `90s` | <strong>90s Played</strong><br>Minutes played divided by 90 |
| `CrdY` | <strong>Yellow Cards</strong><br>Yellow Cards |
| `CrdR` | <strong>Red Cards</strong><br>Red Cards |
| `2CrdY` | <strong>Second Yellow Card</strong><br>Second Yellow Card |
| `Fls` | <strong>Fouls Committed</strong><br>Fouls Committed |
| `Fld` | <strong>Fouls Drawn</strong><br>Fouls Drawn |
| `Off` | <strong>Offsides</strong><br>Offsides |
| `Crs` | <strong>Crosses</strong><br>Crosses |
| `Int` | <strong>Interceptions</strong><br>Interceptions |
| `TklW` | <strong>Tackles Won</strong><br>Tackles in which the tackler's team won possession of the ball |
| `PKwon` | <strong>Penalty Kicks Won</strong><br>Penalty Kicks Won |
| `PKcon` | <strong>Penalty Kicks Conceded</strong><br>Penalty Kicks Conceded |
| `OG` | <strong>Own Goals</strong><br>Own Goals |
| `Recov` | <strong>Ball Recoveries</strong><br>Number of loose balls recovered |
| `Won` | <strong>Aerials Won</strong><br>Aerials Won |
| `Lost` | <strong>Aerials Lost</strong><br>Aerials Lost |
| `Won%` | <strong>% of Aerials Won</strong><br>Percentage of aerials won |
| `Matches` | Matches |

</details>
<details>
<summary><strong>League Phase, Champions League</strong></summary>

| Column  | Description |
|---------|-------------|
| `Rk` | <strong>Rank</strong><br>Squad finish in competition<br>Finish within the league or competition.<br>For knockout competitions may show final round reached.<br>Colors and arrows represent promotion/relegation or qualification for continental cups.<br>Trophy indicates team won league whether by playoffs or by leading the table.<br>Star indicates topped table in league USING another means of naming champion. |
| `Squad` | Squad |
| `MP` | <strong>Matches Played</strong><br>Matches Played by the player or squad |
| `W` | <strong>Wins</strong><br>Wins |
| `D` | <strong>Draws</strong><br>Draws |
| `L` | <strong>Losses</strong><br>Losses |
| `GF` | <strong>Goals For</strong><br>Goals For |
| `GA` | <strong>Goals Against</strong><br>Goals Against |
| `GD` | <strong>Goal Difference</strong><br>Goal Difference |
| `Pts` | <strong>Points</strong><br>Most leagues are ordered by points.<br>Three for a win and one for a draw. |
| `xG` | <strong>Expected Goals</strong><br>xG totals include penalty kicks, but do not include penalty shootouts (unless otherwise noted).<br>Provided by Opta.<br>An underline indicates there is a match that is missing data, but will be updated when available. |
| `xGA` | <strong>xG Allowed</strong><br><strong>Expected Goals Allowed</strong><br>xG totals include penalty kicks, but do not include penalty shootouts (unless otherwise noted).<br>Provided by Opta.<br>An underline indicates there is a match that is missing data, but will be updated when available. |
| `xGD` | <strong>xG Difference</strong><br><strong>Expected Goals Difference</strong><br>xG totals include penalty kicks, but do not include penalty shootouts (unless otherwise noted).<br>Provided by Opta.<br>An underline indicates there is a match that is missing data, but will be updated when available. |
| `xGD/90` | <strong>xG Difference/90</strong><br><strong>Expected Goals Difference per 90 Minutes</strong><br>xG totals include penalty kicks, but do not include penalty shootouts (unless otherwise noted).<br>Provided by Opta.<br>An underline indicates there is a match that is missing data, but will be updated when available. |
| `Notes` | Notes |

</details>


## 📦 How to Use

1. Clone this repository:
   ```bash
   git clone https://github.com/aliratel1/Fc-Barcelona-Champions-League-24-25-Stats.git
