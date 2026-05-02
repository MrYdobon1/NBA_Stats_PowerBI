# NBA_Stats_PowerBI
NBA Stats Dashboard using Power BI

This dashboard displays basic NBA stats such as Points, Rebounds, Assists, Steals, and Blocks, along with Advanced Basketball stats including Usage Rate (USG%), True Shooting% (TS%), Efficiency Value (EFF), and Assist-to-Turnover Ratio (AST/TOV). This dashboard consists of three pages, Team Stats, Player Profile, and League Leaders.

The data used consists of statistics from the 2025–2026 regular season. The data was retrieved from the NBA’s official website, using the API Client Package from https://github.com/swar/nba_api. The data retrieval process was performed using Python. Afterward, the data underwent a cleaning process in Python (converting date formats, removing unnecessary columns), then it was exported to PostgreSQL (defining data types, merging multiple tables), and finally to Power BI (creating conditional columns, defining relationships between tables).

1. Team Stats
<img width="4150" height="2400" alt="nba_analytics_page-0002" src="https://github.com/user-attachments/assets/ed9d9cb3-2a1e-4fd0-910c-c899f0051d6b" />

Team stats include per-game statistics for a team, along with the rank for each statistic calculated using DAX. It also includes a player roster with basic information, as well as the top 3 leaders for statistics such as Points, Rebounds, and Assists, displayed using a Clustered bar Chart. This page also includes a dropdown-style slicer for selecting teams.

2. Player Profile
<img width="4150" height="2400" alt="nba_analytics3_page-0001" src="https://github.com/user-attachments/assets/1b612b6c-ac08-4ae6-b7f5-ad01dcce7e30" />

This page displays the profiles and statistics for each player. Points, Rebounds, Assists, Steals, Blocks, and Minutes are displayed using Card. Field Goal%, 2-Point Field Goal%, 3-Point Field Goal%, Free Throw%, True Shooting%, and Plus-Minus are displayed using Gauge Chart, where the red line on the Gauge Chart represents the league average calculated using DAX. At the bottom, there are three Scatter Chart showing the USG% to TS% ratio, the EFF Value to USG% ratio, and the AST-to-TOV ratio.

True Shooting% is calculated using DAX with the following formula:
<img width="295" height="83" alt="image" src="https://github.com/user-attachments/assets/399182dc-843e-42a2-88dd-3590dde7402e" />

Usage Rate is calculated using DAX with the following formula:
<img width="1045" height="202" alt="image" src="https://github.com/user-attachments/assets/f101cd82-d639-4412-91a4-f0742e93081c" />

At first, I wanted to use the Player Efficiency Rating (PER), but since that formula was too complicated, I ended up using a simpler formula, which is EFF. EFF is calculated using DAX with the following formula:
<img width="617" height="70" alt="image" src="https://github.com/user-attachments/assets/e30ac169-abb1-44cb-b078-5bcfe48d0503" />

AST-to-TOV ratio is calculated using DAX with the following formula:
<img width="263" height="62" alt="image" src="https://github.com/user-attachments/assets/4d8376b4-db16-487a-b048-cafb78b805f3" />

4. League Leaders
<img width="4150" height="2400" alt="nba_analytics_page-0001" src="https://github.com/user-attachments/assets/2d9005a7-b2d8-416f-82cb-49ec28385c58" />

League Leaders lists the top 3 players in key statistics such as Points, Rebounds, Assists, Blocks, 3-Pointers Made, and Steals. The data is calculated using DAX to generate per-game statistics for each player.




