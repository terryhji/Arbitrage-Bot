# Arbitrage Bet Finder

This project aims to find guaranteed profit opportunities over multiple sportsbook platforms. In one month of testing, 14% return on investment was yielded.

The project provides a general overview of the arbitrage bet finder. Due to containing sensitive information, the repository will not contain the source code.

### What is arbitraging? 

Arbitrage betting is the process of hedging two bets against each other to guarantee a profit. An easy explanation is the use of a one winner boxing match.

![](https://media.discordapp.net/attachments/287394739765116928/1203051053986353253/rWNdYTT.png?ex=65cfaf9a&is=65bd3a9a&hm=17e8ae560e4849477398f4e19d12cfd0f19aa07631efa3babbfed4ae44b22782&=&format=webp&quality=lossless)

If two different bookmakers provided you the odds of 1.50 and 3.00 for Boxer 1 and Boxer 2 respectively, betting $80 on Boxer 1 and $30 on Boxer 2 will yield a return of $120 non-dependent on who wins the match. As the total waged is $110 across the two different bookmakers, a guaranteed profit of $10 would be made. This is an example of arbitrage betting.

### How does it work?

The following program scrapes web data for sport categories such as NBA on multiple different sportsbooks where it then calculates whether there is an arbitrage opportunity or not. Profit % is calculated as 100 - arbitrage %.

![](https://media.discordapp.net/attachments/287705954454339584/1204030226946990102/image.png?ex=65d33f87&is=65c0ca87&hm=a06b8f34fa175a3d8329ed1263982701fb2c658dafd9b7adcbb4ffee98200cb8&=&format=webp&quality=lossless)

To improve visibility of the arbitrage opportunities, the data is sent through Discord API into its own dedicated server.

![](https://media.discordapp.net/attachments/287705954454339584/1204031089597743135/image.png?ex=65d34055&is=65c0cb55&hm=d97888d2b3c9fd3c12701032ee5364bb64f622a5897984c1886319cfadd7855c&=&format=webp&quality=lossless)

Separate team bet sizes are calculated by multiplying the arbitrage % of each bet by a randomly generated total bet size. This value is then multiplied by the odds and subtracted by the total amount hedged to calculate the total profit values on either team winning.

By reverse engineering the API of these sites, runtime can be improved by ~85% over conventional web scraping.

![image](https://github.com/terryhji/arbitragebot/assets/139197235/a2d6ab17-43cb-47e4-a7a7-89b283d6dee3)
![image](https://github.com/terryhji/arbitragebot/assets/139197235/867704d5-bdd5-4295-842d-62af4f1f928c)
