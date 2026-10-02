# IMDB OTT Platforms Movie Dashboard

## 📌 Project Overview

**IMDB OTT Platforms Movie Dashboard** is an interactive **Power BI data visualization and analytics project** created to explore OTT content, movies, TV shows, genres, ratings, release trends, platform distribution, and Tamil cinema releases.

The project combines broad OTT-platform analysis with a focused **Tamil Movie Dataset for 2024–2025**. It presents the information through multiple themed dashboards and interactive filters so that users can explore content trends from different perspectives.

The project includes dedicated dashboard views inspired by major OTT platforms such as **Netflix, Prime Video, and Disney+ Hotstar**, along with Tamil cinema analysis and a consolidated OTT Master dashboard.

---

## 🎯 Project Objectives

The main objectives of this project are:

- Analyze movie and TV-show content across OTT platforms.
- Compare content distribution between platforms.
- Explore genre-wise content availability.
- Analyze movie and TV-show release trends over time.
- Study IMDb rating patterns.
- Identify highly rated content.
- Analyze runtime and content duration.
- Explore country-wise content distribution.
- Analyze Tamil movies and web series released during 2024–2025.
- Compare OTT platforms for Tamil content.
- Present business-friendly insights using interactive Power BI dashboards.

---

## 🛠️ Tools & Technologies

| Tool / Technology | Purpose |
|---|---|
| **Power BI Desktop** | Dashboard development and visualization |
| **Power Query** | Data cleaning and transformation |
| **DAX** | Measures, KPIs and analytical calculations |
| **Excel / CSV** | Data storage and preparation |
| **Data Modeling** | Relationships and analytical structure |
| **Data Visualization** | Interactive charts and dashboard storytelling |

---

## 📊 Dashboard Pages

### 1. Netflix Dashboard

The Netflix dashboard provides an overview of Netflix-style OTT content analysis.

Key visuals include:

- Total Content
- Number of Movies
- Number of TV Shows
- Average Runtime
- Release Year filter
- Content distribution by type
- Content by release year
- Top countries by content
- Genre distribution
- Average running time by rating
  
---

### 2. Prime Video Dashboard

The Prime Video dashboard focuses on content trends, genres and ratings.

Key visuals include:

- Total Titles
- Total Genres
- Total Directors
- Release year analysis
- Genre-wise total shows
- Rating-wise content distribution
- Movies vs TV Shows
- Longest-duration movies
- TV shows with the highest number of seasons

---

### 3. Disney+ Hotstar Dashboard

This dashboard provides an overview of movies and TV shows with genre and age-rating analysis.

Key visuals include:

- Total Movies
- Total Genres
- Average Duration
- Average Release Year
- Total TV Shows
- Age-rating segmentation
- Movie vs TV content distribution
- Top genres
- Genre and age-rating filters

---

### 4. Tamil Movie Dashboard – 2024 & 2025

This page focuses specifically on Tamil cinema content.

Key KPIs include:

- Total Movies
- Total Titles
- Total Web Series
- Highest IMDb Rating
- Number of OTT Platforms

Key analysis:

- OTT platform distribution
- Average IMDb rating by platform
- Top-rated movies
- Content details
- Genre distribution
- Release-year analysis

---

### 5. Tamil Movie Trend Analysis

This page provides additional analysis for Tamil movies and web series released during 2024–2025.

Key visuals include:

- Movies by release quarter
- Average box office by year and certification
- Release year vs IMDb rating
- Movie and web-series release trends
- IMDb rating slicer
- Release-year analysis
  
---

### 6. OTT Master Dashboard

The final dashboard provides a consolidated view of OTT content.

Key KPIs and visuals include:

- Total Content
- Total Platforms
- Content by Platform
- Average Rating
- Genre Diversity
- Genre distribution across platforms
- Top 10 genres by content
- Top 10 highest-rated content
- Platform and genre filters
- Release-year range

---

## 🔍 Major Analytical Areas

### Content Analysis

The dashboards compare:

- Movies
- TV Shows
- Web Series
- Total titles/content

### Platform Analysis

The project analyzes content across platforms such as:

- Amazon Prime
- Netflix
- Hotstar
- ZEE5
- Aha Tamil
- Sun NXT
- SonyLIV
- Simply South

### Genre Analysis

The project explores genres such as:

- Drama
- Comedy
- Action
- Romance
- Documentary
- Kids
- Reality
- Horror
- Thriller
- Suspense

### Rating Analysis

The dashboards provide analysis using:

- IMDb ratings
- Age ratings
- Certification categories
- Average rating
- Highest-rated content

### Time-Series Analysis

Release-year analysis is used to understand how content volume changes over time.

The Tamil cinema section additionally analyzes:

- 2024 vs 2025
- Release quarters
- Release trends
- IMDB rating by release year

---

## 🎛️ Interactive Filters

The dashboard uses interactive slicers and filters such as:

- Release Year
- Genre
- Rating
- Platform Type
- Content Type
- Age Rating
- IMDb Rating

These filters allow users to drill down into specific segments of the dataset.

---

## 📐 Data Modeling

The project uses Power BI data modeling concepts to organize content and analytical dimensions.

A suitable star-schema design for the consolidated dashboard can be represented as:

```text
                    Dim Platform
                         |
                         |
Dim Genre ------ Fact OTT Content ------ Dim Type
                         |
                         |
                    Dim Year
                         |
                         |
                    Dim Rating
```

### Fact Table

**Fact OTT Content**

Typical analytical fields include:

- Title
- Platform
- Genre
- Type
- Release Year
- IMDb Rating
- Runtime
- Country
- Rating / Certification

### Dimension Tables

**Dim Platform**
- Platform ID
- Platform Name

**Dim Genre**
- Genre ID
- Genre Name

**Dim Type**
- Type ID
- Content Type

**Dim Year**
- Year ID
- Release Year

**Dim Rating**
- Rating ID
- Rating / Certification

---

## 🧮 Example DAX Measures

The project can use measures such as:

```DAX
Total Content =
COUNTROWS('OTT Master')
```

```DAX
Total Movies =
CALCULATE(
    COUNTROWS('OTT Master'),
    'OTT Master'[Type] = "Movie"
)
```

```DAX
Total TV Shows =
CALCULATE(
    COUNTROWS('OTT Master'),
    'OTT Master'[Type] = "TV Show"
)
```

```DAX
Average IMDb Rating =
AVERAGE('OTT Master'[IMDB Rating])
```

```DAX
Highest IMDb Rating =
MAX('OTT Master'[IMDB Rating])
```

```DAX
Total Platforms =
DISTINCTCOUNT('OTT Master'[Platform Type])
```

> Column and table names should be adjusted to match the exact names in the `.pbix` file.

---

## 🧹 Data Preparation

The general data preparation workflow is:

```text
Raw Dataset
     ↓
Import into Power BI
     ↓
Power Query
     ↓
Remove duplicates
     ↓
Handle missing values
     ↓
Correct data types
     ↓
Standardize categories
     ↓
Create calculated columns where required
     ↓
Create relationships
     ↓
Create DAX measures
     ↓
Build visualizations
     ↓
Add slicers and interactions
     ↓
Dashboard formatting
```

---

## 📈 Key Dashboard Insights

The dashboard is designed to help users answer questions such as:

1. Which OTT platforms contain the most content?
2. How is content distributed between movies and TV shows?
3. Which genres contain the largest amount of content?
4. How have releases changed over the years?
5. Which titles have the highest IMDb ratings?
6. Which platforms have higher average ratings?
7. How does content vary by country?
8. Which ratings are most common?
9. How does Tamil movie content differ between 2024 and 2025?
10. Which OTT platforms distribute Tamil content?
11. Which genres dominate Tamil cinema releases?
12. How do IMDb ratings vary by release year?

---



## 💡 Skills Demonstrated

This project demonstrates practical skills in:

- Power BI
- Power Query
- DAX
- Data Cleaning
- Data Transformation
- Data Modeling
- Star Schema
- KPI Development
- Data Visualization
- Interactive Dashboard Design
- Time-Series Analysis
- Exploratory Data Analysis
- Business Intelligence

---

## 📷 Dashboard Preview

The `Screenshots` contains the complete dashboard screenshots for quick viewing without opening Power BI.
 
---

## 👩‍💻 Author

**Rekha N**

**Project:** IMDB OTT Platforms Movie Dashboard
