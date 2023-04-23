# data-science_baseball

If we want to find out (or anywyay make an argument for) who the best and worst players are in the history of Major League Baseball, how shall we proceed?

We can pick our favorite stats -- say batting average (BA) for hitters and walks + hits per inning pitched (WHIP) for pitchers.

But we can't simply rank players by these statistics and expect to get good results, because some players will have artificially high or low values of these statistics simply due to very limited playing records.

To address this, a Bayesian approach is taken: Start by assuming that every player is average. For hitters this means assuming a 0.260 BA; for pitchers this means assuming a 1.67 WHIP. This will serve as our *prior*.

Then use the weight of a player's career statistics to update our probabilities in the normal Bayesian way. In the case of hitting, we can treat it like a Beta-Binomial model. In the case of pitching, we can treat it like a Gamma-Poisson model.

Even after setting our priors as percentages or probabilities, we still have the task of setting how many at-bats or innings pitched to assume. The analysis explores this issue, checking to see which players come out on top (or bottom) depending on what numbers we choose, and asking how many at-bats or innings pitched would be an appropriate number to draw our conclusions about the best and worst hitters and pitchers in the history of Major League Baseball.

For hitters, we find the best to be Ty Cobb and the worst to be Bill Bergen.

For pitchers, we eliminate pitchers before 1900 and then further distinguish between starters and relievers. We then find the best starter to be Addie Joss and the worst to be Dick Weik. We find the best reliever to be Koji Uehara and the worst to be Stu Flythe. 
