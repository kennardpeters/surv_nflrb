# surv_nflrb
Survival Analysis of NFL Running Backs. More info to come. A function of Data Science at UCSB.

This README file is subject to change.

General idea: Collect data on NFL RBs, career metrics, physical measures, accolade status, (MVP, All-Pro, etc.) and most importantly, whether or not the player in question is indeed retired.
This is the main challenge of this project. We will need to devise a systematic method of collecting very specific data from a large quantity of pages on the internet. 

We already have access to the following covariate values after a quick piecemeal CSV scrape off of pro-football-reference.com: Year drafted, Round Drafted, Pick number in draft, Position (HB or FB),Age when drafted, Team, Start year, End year (2016 if not retired), AP1 (First Team All-Pro Selections), Pro Bowl selections, Years spent as primary starter for team, Weighted Career Approximate Value (an advanced metric regarding a player's worth, weighing his better seasons more heavily than his worse ones), Games played, Games started, Career Rush Att, Career Rush Yds, Career Rush TD, Career Receptions, Career Receiving Yds, Career Receiving TD, College Team.

These existing data may be enough for a satisfactory survival analysis. However, I would like for this one to consider physical attributes of the players, as this must have some sort of effect on career length for runningbacks. You don't see 5'9 180-pounders make it in the NFL, unless, perhaps, they are lightning-quick; in addition to height or weight, I would like to see if there is any relationship between early retirement and measured 40-yard dash times from the NFL Combine, which is a showcase of aspiring NFL players' raw physical skills.

This "extra yard" that we are pursuing in terms of scraping Wikipedia/nflcombineresults.com is not an easy task. I have a simple database in the form of an excel file containing all of the covariate levels for each player. We will need to find a way to collect height/weight and 40 yard dash times (as well as any other measures from the NFL combine) and then store it in the columns adjacent to that player's existing data. I am in the process of figuring out how to do this, and am unsure if we should move forward with Python or start learning some SQL. 

I believe this to be a valuable lesson in data science: scraping the internet for data, with **precision.** If we can accomplish this, we should get wasted together, because we will be more or less teaching ourselves how to do this, and this is certainly a marketable skill in the world of data science. It will not be easy, but this is the true challenge of the project. Survival analysis is incredibly easy in comparison.

After the data collection process, we will load the dataset into R to perform analysis, primarily employing the survival library. We will create Kaplan Meier estimates and build a Cox Proportional Hazards model using our dataset. The Cox PH model is unintelligible to a layman in survival analysis but we can present hazard ratios (the output parameters of the model) visually to really wow our readers. We will become very, very familiar with plotting in R and building other visual aids. As time permits, we may build predictive models, or run other analyses which pique our curiousity.

Thanks for reading!!!! (-: