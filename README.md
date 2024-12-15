🌍 COVID-19 Analysis Using SQL
🚨 The Pandemic That Shook the World
The COVID-19 pandemic was a serious global event that claimed countless lives and brought economies to a standstill. This project dives deep into exploring COVID-19 data using SQL, applying data analysis techniques to uncover trends in cases, deaths, and vaccinations. 🧑‍💻

📅 Data Used
Timeframe: 24th February 2020 to 30th April 2021
Source: Our World in Data
🔍 What's Inside?
The dataset has been split into two categories for simplicity:

CovidDeaths - Focused on cases and deaths 💀
CovidVaccinations - Highlighting vaccinations and tests 💉
SQL queries were run using Microsoft SQL Server Management Studio to analyze and visualize the pandemic's impact.

🛠️ Queries & Insights
Query 1: Daily Trends in India 🇮🇳
Objective: Get daily total cases, deaths, and the percentage death rate for India.
Snippet:

sql
Copy code
SELECT Date, 
       TotalCases, 
       TotalDeaths, 
       (TotalDeaths * 100.0 / TotalCases) AS PercentageDeathRate
FROM CovidDeaths
WHERE Country = 'India';
🎯 Insight: India recorded a high number of cases but maintained a lower death rate compared to global trends.

Query 2: Global Impact 🌍
Objective: Show country-wise population, total cases, total deaths, and the percentages of population infected and dead.
Snippet:

sql
Copy code
SELECT Country, 
       Population, 
       TotalCases, 
       TotalDeaths, 
       (TotalCases * 100.0 / Population) AS PercentagePopulationInfected,
       (TotalDeaths * 100.0 / Population) AS PercentagePopulationDead
FROM CovidDeaths;
💡 Findings:

Top 3 countries with the highest cases:
USA: ~32M cases and ~500K deaths
India: ~19M cases
Brazil: Significant numbers follow.
Query 3: Vaccination Stats 💉
Objective: Analyze country-wise population, total cases, total vaccinations, and the vaccination rate.
Snippet:

sql
Copy code
SELECT Country, 
       Population, 
       TotalCases, 
       TotalVaccinations, 
       (TotalVaccinations * 100.0 / Population) AS VaccinationPercentage
FROM CovidVaccinations;
✨ Observation: Vaccination campaigns ramped up globally by early 2021, with developed nations leading the way.

📊 Highlights & Results
SQL allowed us to break down massive datasets into insightful chunks.
The pandemic’s numbers tell a somber tale, yet also show the global effort in fighting back with vaccinations. 🌟
📁 Repo Contents
SQL Queries: Explore the exact scripts used for analysis.
Sample Results: Screenshots showcasing query results.
Dataset Link: COVID-19 Data
✍️ Final Words
This project served as a stepping stone in applying SQL to solve real-world problems. While this analysis scratches the surface, there’s potential for deeper insights. 💡 If you have ideas, feel free to fork and contribute! 🚀

❤️ Contribute
Found this useful? Star ⭐ the repo and share your insights!
