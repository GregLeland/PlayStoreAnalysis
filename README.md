Link to PowerPoint Presentation:

<a href="https://docs.google.com/presentation/d/1DsUauIwIGu0gwG0U3uTcGyBi1iW1_dQFDqjJTgGixDA/edit?usp=sharing">Google Play Store Analysis Presentation</a>

###Our Scenario:

I was hired as a consultant by a small startup game production company that has a limited budget to spend on their first Android mobile game. To maximize the return on their investment, they want to know what type of game to develop, and how much they should charge to maximize profit (via paid downloads).

Hypothesis:

If they develop a game in a specific category, at a specific price point,  they will have the best chance at maximizing their ROI. 

Our process:

Google doesn’t have an API to get the information from the Play Store directly, which made things a bit difficult. However, we got lucky and found a Python library on PyPi called, “Play Scraper”. It functions as an API, and combs through the Google Play Store by using variables in Python. Luckily, it was able to get the detailed game information that we needed to deliver a conclusion to our ‘employers’.

Steps we took:

1. Installed the Play Scraper library.

2. I created a loop that would find the top 25 paid games in all gaming categories on the Google Play Store.

3. I took the app/game ID’s from the top 25 games in each gaming category and pulled the following information for my research:
<ul>
<li>The game’s title</li>
<li>The game’s rating</li>
<li>The amount of reviews for each game</li>
<li>The price of each game</li>
<li>The approximate amount of installations/purchases each game has</li>
<li>The game’s developer</li>
<li>The link to the game on the play store for reference</li>
<li>I then took all the information and put it into multiple data frames for analysis</li>
</ul>
4.	We then took all the information and put it into a data frame so we could access it and answer the following questions:

a.	What is the optimal game category (Arcade, Action, Racing, Simulation, etc)?
b.	What is the optimal price point?
c.	Does the game’s rating score have an impact on the game’s success?

Challenges 1 & 2:
The majority of mobile  games are free. They make revenue via ads and ‘microtransactions’ (a.k.a. in-game purchases). Because we don’t have access to the data on revenue generated from free games, I was limited to coming to conclusions based on available information for paid games.

Google doesn’t have an official API to get the information from the Play Store directly,  which made things a bit difficult. 

The Solution:
I got lucky and found a Python library on PyPi.org called, “Play Scraper”. It functions as an API, and combs through the Google Play Store’s website by using variables in Python. Luckily, it was able to get enough information to deliver a plausible conclusion to my theoretical employer.

Challenge 3:
Limited information on the Google Play Store made it impossible to get an exact download amount for each game.

The Solution:
Because the Google Play Store gives an approximate number of downloads (in 5k, 10k, 50k, 100k,  500k, 1M, & 10M increments), I was able to use the ‘number of installations’ as the source for generating approximate revenue for each game. This data was good enough to be directionally accurate and I was able to continue with my analysis.


Our findings:

1.	We were surprised to find that there was a significant outlier among the games, which, by itself, contributed to more than double of any other CATEGORY. This outlier was Minecraft, which had a total revenue of over $69,000,000. We then decided to make Minecraft its own category to compare it with the rest of the data instead of excluding it completely because there is a possibility that any game could experience a similar phenomenon.
2.	The highest grossing category was Action games.
3.	The highest grossing price point was $4.99

Our conclusion:

1.	The data showed that games in the Action category and $4.99 price point performed the best overall, and grossed the highest.
