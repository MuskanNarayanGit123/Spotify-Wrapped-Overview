# 🎼 Music by the Numbers: Spotify Wrapped Analysis  


## 🎯 Project Objective:

To create a personalized Spotify Wrapped dashboard that provides a comprehensive view of the user's listening habits over the years. The dashboard will showcase trends in listening behavior by year, month, weekday, and time of day, while also highlighting personal music preferences, such as favorite artists, tracks, and albums. The goal is to deliver an engaging, data-driven summary of the user's unique music journey.

## 🛢 Dataset:

The data for this project is sourced from the Maven Analytics website and can be accessed via the following link:
[Maven Music Challenge](https://mavenanalytics.io/challenges/maven-music-challenge/e161353d-9967-4297-869c-505de168e610)

It contains two CSV files:

1. **spotify_data_dictionary:** A reference file describing the dataset's columns.
2. **spotify_history:** The primary dataset used in this project.

The spotify_history file includes detailed information such as:

- spotify_track_uri: Unique identifier for each track.
- ts: Timestamp (in UTC).
- platform: Platform used for streaming the track.
- ms_played: Playback duration in milliseconds.
- track_name: Name of the track.
- artist_name: Artist of the track.
- album_name: Album of the track.
- reason_start: Reason the track started playing.
- reason_end: Reason the track stopped playing.
- shuffle: Shuffle status (True/False).
- skipped: Skipped status (True/False).

The analysis covers data from 2013 to 2024, offering valuable insights into listening habits and personal music preferences.

## 🧹️ Data Cleaning Steps:

#### Removed Noisy Tracks:

- Filtered out tracks with a playback duration of ≤30 seconds, as they indicate minimal interaction and primarily add noise, skewing the results.

#### Ensured Consistency:

- Used Power Query to clean and standardize the data for further processing.

## 📊 Data Preparation Steps:

#### Extracted Playback Duration:

- From the ms_played column, created two new columns to extract playback duration in seconds and minutes for easier analysis.

#### Extracted and Organized Dates:

- Extracted the date from the ts (timestamp) column and created a separate Date column for time-based analysis.

#### Created a Calendar Table:

- Built a calendar table in Power Query with the following fields:

  - Year, Date, Month Name, Month (for sorting), Weekdays, and Weekday Sort (for sorting), Month_name_short (for specific visual), Week_Name_full (for specific visual).

#### Generated Unique Track Identifiers:

- Created a calculated column in DAX to generate a unique_uri_track column, ensuring accurate identification of tracks with the same title but different identifiers.

#### Added Daytype Classification:

- Created a calculated column in the calendar table using DAX to classify dates as weekday or weekend for time-based analysis.

#### Time Period Categorization:

- Created a calculated column in DAX to determine the time of day from the timestamp, enabling the identification of the most active time periods.

## 📑 Report Inclusions

This repository showcases a Power BI report hosted on the Power BI Service, along with its underlying data model. Below are pdfs of the report and the data model for a quick preview:

- [Data Model](https://github.com/Joyeta16/Spotify-Wrapped-Overview/blob/main/Spotify%20Data%20Model.pdf)
- [Spotify Wrapped Dashboard](https://github.com/Joyeta16/Spotify-Wrapped-Overview/blob/main/Spotify%20Dashboard.pdf)


## 💡 Key Insights

### Overall Listening Trends:

#### Engagement Growth and Decline:

- Initial engagement with Spotify was low in 2013 and 2014, with significant growth starting in 2015.

- Listening activity peaked in 2020 with 54.77K minutes, likely influenced by lifestyle changes during the pandemic.

- A gradual decline in activity is observed from 2022 onward.  

#### Device Preferences:

- Most listening was done on Android (90.9% of total time). However, Windows was the primary platform in 2013 and 2014.

### Year-Specific Highlights:  

#### 2013–2014 (Early Activity):

- **2013:** July saw the highest activity (226.28 minutes), with Saturday nights being the most active time. Top artist: John Mayer.

- **2014:** January stood out (61.84 minutes), with Thursday evenings being the peak listening time. Artists were varied with no clear favorite.

#### 2015–2019 (Growth Years):

- **2015:** A significant increase in activity, peaking in August (1.23K minutes). Saturdays and nighttime listening were most prominent.

- **2016–2019:** Nighttime listening remained consistent, with favorite days shifting each year.

- The Beatles became the dominant artist from 2016 onward.

#### 2020–2024 (Peak and Decline):

- **2020:** Marked the highest overall engagement, with April being the top month (7.01K minutes). Fridays and nighttime were the most active. Favorite artists included The Killers and The Beatles.

- **2021:** Showcased the most diverse exploration of artists(1.48K), albums(2.45K), and unique tracks(4.72K), with January seeing the highest activity (6.74K minutes).

- **2022–2024:** A gradual decline in listening is evident. Fridays and nighttime continued to dominate, with The Beatles remaining a top choice.

### Recurring Patterns:

#### Time Preferences:

- Nighttime consistently emerged as the favorite time for streaming music across all years.

#### Day Preferences:

- Fridays were the most active day starting from 2018, with some variations in earlier years.

#### Artist and Track Dominance:

- The Beatles consistently ranked as the favorite artist from 2016 onward, with occasional competition in specific years. Similarly, ‘Ode To The Mets’ stood out as the most-played track over the years, reflecting a strong personal connection.  

## 🛠️ Tools

- Data Visualization: Power BI
- Data Cleaning and Transformation: Power Query
- Data Analysis: DAX

## 📎 Links
🌐 [Linkedin Post](https://www.linkedin.com/feed/update/urn:li:activity:7288082253304188928/)  
📊 [Live Dashboard](https://app.powerbi.com/view?r=eyJrIjoiMzIxOGQzZTctMzU3Zi00N2JlLWFiYzUtODA2YmI5OWE5NjFjIiwidCI6ImM2ZTU0OWIzLTVmNDUtNDAzMi1hYWU5LWQ0MjQ0ZGM1YjJjNCJ9)

## 🧠 Skills Gained

- Applied data cleaning and transformation techniques using Power Query and DAX.

- Conducted time-based analysis by creating calendar tables and utilizing date functions.

- Designed user-centric Power BI dashboards to visualize personalized insights effectively.

- Gained a deeper understanding of personalized marketing metrics and their impact on user engagement and sentiments.

---


