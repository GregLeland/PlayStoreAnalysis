<h1>Google Play Store Analysis</h1>

Link to PowerPoint Presentation:

<a href="https://docs.google.com/presentation/d/1DsUauIwIGu0gwG0U3uTcGyBi1iW1_dQFDqjJTgGixDA/edit?usp=sharing">Google Play Store Analysis Presentation</a>

<h2>The Scenario:</h2>

I was hired as a consultant by a small startup game production company that has a limited budget to spend on their first Android mobile game. To maximize the return on their investment, they want to know what type of game to develop, and how much they should charge to maximize profit (via paid downloads).

<h2>Hypothesis:</h2>

If they develop a game in a specific category, at a specific price point, they will have the best chance at maximizing their ROI. 

<h2>Primary Questions</h2>
<ul>
 <li>Is there an optimal game category (Arcade, Action, Racing, Simulation, etc)?</li>
 <li>Is there an optimal price point?</li>
 <li>Does the game’s rating score have an impact on the game’s success?</li>
</ul>

<h2>The process:</h2>

1. Install the Play Scraper library.

2. Create a loop that would find the top 25 paid games in all gaming categories on the Google Play Store.

3. Take the app/game ID’s from the top 25 games in each gaming category and pull the following information:
<ul>
<li>The game’s title</li>
<li>The game’s rating</li>
<li>The amount of reviews for each game</li>
<li>The price of each game</li>
<li>The approximate amount of installations/purchases each game has</li>
<li>The game’s developer</li>
<li>The link to the game on the play store for reference</li>
</ul>

I then took all the information and put it into multiple data frames for analysis

<h2>Hurdles</h2>

<h3>Challenges 1 & 2:</h3>
The majority of mobile  games are free. They make revenue via ads and ‘microtransactions’ (a.k.a. in-game purchases). Because we don’t have access to the data on revenue generated from free games, I was limited to coming to conclusions based on available information for paid games.

Google doesn’t have an official API to get the information from the Play Store directly,  which made things a bit difficult. 

<h3>The Solution:</h3>
I got lucky and found a Python library on PyPi.org called, “Play Scraper”. It functions as an API, and combs through the Google Play Store’s website by using variables in Python. Luckily, it was able to get enough information to deliver a plausible conclusion to my theoretical employer.

<h3>Challenge 3:</h3>
Limited information on the Google Play Store made it impossible to get an exact download amount for each game.

<h3>The Solution:</h3>
Because the Google Play Store gives an approximate number of downloads (in 5k, 10k, 50k, 100k,  500k, 1M, & 10M increments), I was able to use the ‘number of installations’ as the source for generating approximate revenue for each game. This data was good enough to be directionally accurate and I was able to continue with my analysis.


<h2>Initial Findings:</h2>

1.	There was a significant outlier among the games, which, by itself, contributed to more than double of any other CATEGORY. This outlier was Minecraft, which had a total revenue of over $69,000,000. I decided to make Minecraft its own category to compare it with the rest of the data instead of excluding it completely because there is a possibility that any game could experience a similar phenomenon.
2.	The highest grossing category was Action games.
3.	The highest grossing price point was $4.99

<h2>Conclusion:</h2>

Based on the available information, if the mobile gaming company develops their first game in the ‘Action’ or ‘Arcade’ categories at a price point of $2.99 or $4.99,  they are likely to have a better chance of maximizing their ROI. Also, based on the available data and the strong correlation of reviews to revenue, it would benefit them to encourange users to review the game.
