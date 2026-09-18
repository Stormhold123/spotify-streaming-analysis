# Spotify Streaming History Analysis

Do we actually explore new music, or just keep replaying the same favorites on repeat?

This project analyzes Spotify streaming history to answer:
- Do they mostly replay favorite artists, or explore new ones?
- When during the day do they listen the most?
- Which songs get played the most — and which get skipped the most?
- How have the top artists shifted between 2023 and 2024?

## Dashboard



![Power BI Dashboard](powerbi/BI%20Dashboard_page-0001.jpg)



*Full interactive version available by opening the `.pbix` file in [Power BI Desktop](https://powerbi.microsoft.com/desktop/) (free) — filters and cross-highlighting are fully functional.*

### Excel Prototype



![Plays by Time of Day](Excel/Time%20of%20plays.png)




![Share of Total Plays](Excel/Share%20of%20plays.png)




![Share of Artists](Excel/Share%20of%20artists.png)




![Top Most Played Songs & Skip Rate](Excel/Skipped%20songs%20and%20skip%20rate.png)




![Top 10 Artists: 2023 vs 2024](Excel/Top%2010%20Artists%20by%20year.png)



## Data

Raw Spotify streaming history export.

Raw dataset: [`data/Spotify Streaming History raw file.zip`](data/Spotify%20Streaming%20History%20raw%20file.zip)

## Process

1. Prototyped the visuals in Excel first, using pivot tables to explore plays by time of day, skip rates, and artist trends year-over-year — see [`Excel/Spotify.xlsb`](Excel/Spotify.xlsb)
2. Rebuilt and combined the visuals into a single Power BI dashboard, adding cross-filtering between charts so selecting a time-of-day segment or artist updates the other visuals
3. Built a "Replayed Favourites vs Explored a Little" classification to separate listening behavior by play volume vs. by number of distinct artists

Power BI file: [`powerbi/BiSpotify.pbix`](powerbi/BiSpotify.pbix)

## Key Findings

- **Listening skews heavily nocturnal** — Night accounts for the largest share of plays (~690K), followed closely by Evening (~670K), with Morning the quietest period (~165K)
- **Plays are dominated by a small circle of favorites**: 98% of total plays come from replayed favorite artists, despite those artists making up only 17% of all distinct artists listened to — the other 83% of artists were "explored a little" and rarely returned to
- **Skip rate doesn't track with popularity** — "Concerning Hobbits" had a mid-range play count but the highest skip count of any top track, while heavily played songs like "Ode To The Mets" and "In the Blood" were rarely skipped
- **Artist rankings shifted noticeably year over year** — The Beatles and The Killers remained top artists in both years but saw play counts drop from 2023 to 2024, while ABBA and John Mayer saw sharp increases, with ABBA's plays growing 20x

## Tools

Excel · Power BI

---
Data via personal Spotify streaming history export.
