---
title:  "Game Theory and Oligopolies"
date:   2020-12-20 11:53:59 +0000
draft: false
images: []

lightgallery: true

toc:
  auto: false

categories: [ECONOMICS]
tags: [oligopolies]
---

When examining Oligopolies we often use the kinked demand curve to show how firms might face a dual demand curve (i.e. elastic and inelastic) for its product based on the likely reactions of other firms to a change in its price.  Game Theory can also be used by economists to gain a more detailed understanding of how oligopolies might operate in their market.

<!--more-->

## 1.0 Game Theory and Oligopolies

John Forbes Nash was renowned for his work in game theory, winning the Nobel Prize for Economics in 1994.  The film clip of **A Beautiful Mind** – the bar scene – illustrates the need to think about the response of others where it highlights **interdependence**. Interdependence is vital for understanding oligopoly theory – that firms react to decisions made by other firms.

{{< youtube 2d_dtTZQyUM >}}
<br>

Game Theory is in short, the study of how individuals (or organisations) apply strategy to achieve an outcome which is to their benefit — namely, a pay-off.  One of the criticisms of the kinked demand curve used in Oligopoly theory is that it does not take into account the interdependence between firms.  Game Theory looks at this interdependence in much more detail.  Game Theory considers the strategic interaction when one player's decision depends on what the other player does.  What the opponent does also depends on what s/he thinks the first player will do.

A game consists of:
1. Players
2. Strategies
3. Payoffs

## 2.0 Dominant Strategy

When considering Game Theory one of the first steps is to identify the dominant strategy.

{{< admonition info >}}
A **dominant strategy** occurs when there is an optimal choice of strategy for each player no matter what the other does.
{{< /admonition >}}

In fact, there are two types of dominance.  A **strictly dominant strategy** is that strategy that always provides greater utility (i.e. satisfaction) to a player, no matter what the other player's strategy is.  A **weakly dominant strategy** is that strategy that provides at least the same utility for all the other player’s strategies, and strictly greater for some strategy.

### 2.1 Strictly Dominant Strategy

Let's consider a dominant strategy, using the **prisoner's dilemma** which is the most famous example of game theory.

In the matrix below there are two prisoners who have committed a crime together and have been arrested.  Each prisoner knows there is enough evidence to convict them.  However, they have each been offered a deal.  If they confess and implicate their fellow prisoner they will get a reduced sentence but their fellow prisoner will get a more severe sentence.  They cannot collude.  The consequences of confessing or not confessing for Prisoner 1 is shown in green.  For Prisoner 2 the alternatives are shown in red.

\
![Prisoners Dilemma](/posts/1-game-theory-and-oligopolies/prisoner-dilemma.png "Prisoner's Dilemma")


Prisoner 1's perspective:

- If Prisoner 2 confesses, Prisoner 1 should **confess** - 8 years is better than 10 years.
- If Prisoner 2 does not confess, Prisoner 1 should still **confess** - 0 years is better than 1 year.

Prisoner 1 has a **dominant strategy** to **confess** since no matter what Prisoner 2 does the *optimal choice* for Prisoner 1 is to confess.

Prisoner 2's perspective:

- If Prisoner 1 confesses, Prisoner 2 should **confess** - 8 years is better than 10 years.
- If Prisoner 1 does not confess, Prisoner 2 should still confess - 0 years is better than 1 year.

Prisoner 2 has a **dominant strategy** to **confess** since no matter what Prisoner 1 does the *optimal choice* for Prisoner 2 is to confess.

### 2.2 Weakly Dominant Strategy

Let's now look at a **weakly dominant strategy**.  For this example we will consider a game show which ran in the UK from 2007 to 2009.  It was called **Golden Balls** and was hosted by Jasper Carrot.  In the final round of the game each contestant is given a set of two balls, one each marked "Split" and "Steal," and must secretly choose one to indicate their intentions after looking inside to confirm which is which.  There is obviously a sum of money involved.

- If both choose Split, they each receive half the jackpot.
- If one chooses Steal and the other chooses Split, the Steal
contestant wins the entire jackpot and the Split contestant leaves with
nothing.
- If both choose Steal, neither contestant wins any money.

If we assume that the jackpot is £2,000 then we can show this in the following matrix:

\
![Golden Balls](/posts/1-game-theory-and-oligopolies/golden-balls1.png "Golden Balls")

Player 1's perspective:

- If player 2 plays share, player 1 should play steal.
- If player 2 plays steal, it does not matter what player 1 does. S/he will end up with £0.

We could say that for player 1 the **weakly dominant strategy it to steal.**

Player 2's perspective:

- If player 1 plays share, player 2 should play steal.
- If player 1 plays steal, it does not matter what player 2 does. S/he will end up with £0.

Again, we would say that for player 2 the **weakly dominant strategy is to steal.**

We will come back to these two examples when we look at the Nash Equilibrium.

## 3.0 Nash Equilibrium

Nash Equilibrium is an important idea in game theory ... 

{{< admonition info >}}
A **Nash Equilibrium** describes any situation where all the participants in a game are pursuing their best possible strategy given the strategies of all the other participants.   It is where there is no incentive to deviate from their initial strategy. 
{{< /admonition >}}

The Nash Equilibrium seems similar to a dominant strategy.  However, with a Nash equilibrium we are looking at each quadrant within the payoff matrix and the looking at the payoff combinations to see if there is an equilibrium which we will naturally gravitate towards.

### 3.1 Example 1

Consider the Prisoner Dilemma example from above.

\
![Prisoner's Dilemna](/posts/1-game-theory-and-oligopolies/prisoner-dilemma.png "Prisoner's Dilemma")


***Top left quadrant:***

- If Prisoner 2 confesses is there any benefit of Prisoner 1 changing strategy and not confessing?  No, because he will end up with 10 years in prison.  We know this anyway because it is the dominant strategy.

- If Prisoner 1 confesses is there any benefit for  Prisoner 2 changing strategy and not confessing?  No, because he will end up with 10 years in prison.

This would **represent a Nash Equilibrium** because there is not benefit for either player changing strategy given the strategy the other player is playing.

***Bottom right quadrant:***

- If Prisoner 2 does not confess is there any benefit of Prisoner 1 changing his/her strategy and confessing?  Yes, there is because s/he will end up with no prison sentence instead of 1 year.

- If Prisoner 1 does not confess is there any benefit of Prisoner 2 changing his/her strategy and confessing?  Yes, there is a benefit of changing strategy because s/he will also end up with no prison sentence.

As a result this quadrant would **not represent a Nash Equilibrium** since there is a benefit for each of them to deviate from their initial strategy to not confess.

***Top right quadrant:***

- If Prisoner 2 does not confess is there any benefit of Prisoner 1 changing his/her strategy and not confessing?  No, there is not a benefit because s/he will end up with 1 year in prison instead of being set free.

- If Prisoner 1 confesses is there any benefit of Prisoner 2 changing his/her strategy and confessing?  Yes, there is a benefit of changing strategy because s/he will also end up with 8 years instead of the current 10 years.

Again this quadrant would **not represent a Nash Equilibrium** since Prisoner 2 could benefit by deviating from the initial strategy of not confessing to confessing.

***Bottom left quadrant:***

- If Prisoner 2 confesses is there any benefit of Prisoner 1 changing his/her strategy and confessing?  Yes, there is a benefit because s/he will end up with 8 years in prison instead of 10 years.

- If Prisoner 1 does not confess is there any benefit of Prisoner 2 changing his/her strategy and not confessing?  No, there is no benefit of changing strategy because s/he will also end up with 1 year instead of being set free by confessing

Again this quadrant would **not represent a Nash Equilibrium** since  Prisoner 1 could benefit from the initial strategy by moving from not confessing to confessing.

### 3.2 Example 2

In this example let's consider an **oligopoly** situation where there are two businesses - Business A and Business B.  The two choices are that they can offer their product for a high price of £2 or a low price of £1.50.  Each pricing decision will lead to a certain amount of profit.  The matrix showing this is:

\
![Game Theory - Oligopoly](/posts/1-game-theory-and-oligopolies/oligopoly.png "Game Theory - Oligopoly")


The dominant strategy for Business A is to charge a low price.  The dominant strategy for Business B is to charge a low price.  The Nash Equilibrium lies where there are two underlined numbers, i.e. the bottom right quadrant.  This Nash Equilibrium can last in the long term.  If this is a long term situation then there will be **price rigidity** (which links back to the kinked demand curve) in the market since there is no incentive to change.  If firms do decide to compete it will be on non-price factors such as:

- branding
- advertising
- quality of products
- quality of service

Interestingly the Nash Equilibrium is not the best option for both firms combined.   If both firms were to charge £2 then this would give a higher profit - a total of £12m rather than £4m in the Nash Equilibrium.

If firms could break this interdependence and **collude** then there is a way that these firms could earn higher profits, i.e. top left quadrant.  This could involve forming a **cartel**.  This also shows that even when there is collusion there is still an **incentive to cheat** and undercut and earn £8m.  Therefore, in the long-run collusion may not last.

### 3.3 Example 3

As a final example let's go back to the **Golden Balls** scenario.  Rather than using monetary values we will use percentages:

\
![Golden Balls](/posts/1-game-theory-and-oligopolies/golden-balls2.png "Golden Balls")

As mentioned above each player has a weakly dominant strategy, which is to choose to steal.  This can be seen by underlined %'s.   In the above matrix there are three Nash Equilibrium!

\
![Golden Balls](/posts/1-game-theory-and-oligopolies/golden-balls3.png "Golden Balls")

In each of these three Nash Equilibrium outcomes a player cannot do better on his or her own by changing his or her strategy.  Notice that offering to share is not a good option.  The game was set up so that all the choices that players are making is pulling them towards the Nash Equilibrium of steal.

Watch the following episode from Golden Balls to see what can happen...


{{< youtube S0qjK3TWZE8 >}}
<br>

A result of a split (top left quadrant) is unusual. How did Nick manage to get to this position with Abraham?  It is possible that Nick knew something about Game Theory because he changed the game; he changed the payoff matrix.  

Nick consistently said that he was going to steal.  He adopted a strategy that no matter what Abraham was going to walk away with nothing. He reiterated it so many times that Abraham believed it.  The strategy was unusual in that most contestants would claim that they would share.  The payoff matrix was changed by Nick so that he eliminated the left-hand side of the payoff matrix.

\
![Golden Balls](/posts/1-game-theory-and-oligopolies/golden-balls4.png "Golden Balls")

Abraham is now looking at a situation where he gets zero if he steals or splits.  However, Nick also said that he would split all the money that he receives.  There was no contractual obligation for Nick to share, but he kept telling Abraham that he would share.  For Abraham there was no benefit in going for steal but there was a small possibility that Nick **would share** his winnings.  The rational choice for Abraham is to go for a split, hoping that there might be some money shared.  This is what Abraham did... and they ended up in the unlikely top left position of the quadrant!

## 4.0 Final Words

We have seen situations where there is one Nash Equilibrium and also multiple Nash Equilibrium.  There can also be games where there is no Nash Equilibrium.  An example of a game that has no Nash Equilibrium is shown in the table below.

\
![No Nash Equilibrium](/posts/1-game-theory-and-oligopolies/no-nash-eqm.png "No Nash Equilibrium")



If the players end up in the **top left quadrant**, player B would want to switch to Right. If they end up in the **top right quadrant** player A wants to switch to Bottom. Furthermore, if they end up in the **bottom left quadrant** player A would rather have taken Top, and if they end up in the **bottom right quadrant** player B would be better off choosing Left. There is no dominant strategy and none of the four options is a Nash equilibrium.
