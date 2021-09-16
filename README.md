# Sports Analytics - National Hockey League (NHL)

This repository contains data science toolkit codes to analyze National Hockey League (NHL) statistics. 

Please find the analyses documented here: [![Documentation](https://img.shields.io/badge/doc-latest-blue.svg)](https://justinjoliver.github.io/NHL-Analytics/)
, or in [Tableau Public](https://public.tableau.com/app/profile/justin.l.1253).

This is a selection of many ways to collect, compile, clean, analyze, model, and predict team and player (skaters and goalies) performances statistics. This repository does not claim any ownership of data and represents points of views of organizations or representations mentioned. All original codes (including generic and model algorithms) can be used freely with a proper citation to this repository.

## Data collection and clean up
- [x] Data scrap - using [BeautifulSoup](https://www.crummy.com/software/BeautifulSoup/) & [Selenium](https://selenium-python.readthedocs.io/) using Python
  - [x] Team - By season
  - [x] Team - By season, by game
  - [x] Skater - By season
  - [x] Skater - By season, by game
  - [x] Goalie - By season
  - [x] Goalie - By season, by game
- [x] Data scrape - Leveraging [http://statsapi.web.nhl.com](http://statsapi.web.nhl.com) (see [documentation](https://gitlab.com/dword4/nhlapi/-/blob/master/records-api.md))
  - [x] Player - Goalie & Skaer
  - [x] Live game data - By action
- [ ] Data join - merge relevant data
  - [ ] Player salary and salary cap from [hockey-reference.com](https://www.hockey-reference.com/friv/current_nhl_salaries.cgi), (annual)
  - [ ] (Private) NHL stadium foot traffic behaviors and demographics data (mobile / foot traffic data)
  - [ ] University of Michigan - Men's Ice Hockey [player statistics](https://statsarchive.ath.umich.edu/VS-IceHockey-M/ihockeystart.php)
- [ ] Data compilation & preliminary validations - using [Online Algorithm / Statistics](https://github.com/joshday/OnlineStats.jl) using julia and [PySpark](https://spark.apache.org/docs/latest/api/python/) using Python/Spark. to handle large / big data
  - [ ] Team abbreviation match and identifications
- [ ] Establish extract, transform, and load (ETL) structure

Web scraping portion of the code requires a careful consideration of followings,
* Define the web browser of your choice - the default one used by the code in this repository is Firefox
* Depending on the response time of the host website, users need to adjust explicit wait time for JavaScript table to load

## Example visualization 
1. Pythagorean Expectation [in Tableau Public](https://public.tableau.com/app/profile/justin.l.1253/viz/NHL-PythagoreanExpectation/Dashboard2)

## Other resources - Exercises
- Salary Cap: [Tracker](https://puckpedia.com/#salary-cap)
- NHL Hockey Reference: [Insights](https://www.hockeyzoneplus.com/)
- Articles - Christian Lee's [extensive analyses](https://medium.com/hockey-stats)
  - [R version of pulling data](https://medium.com/hockey-stats/how-to-scrape-nhl-com-dynamic-data-in-r-using-rvest-and-rselenium-ba3b5d87c728)
