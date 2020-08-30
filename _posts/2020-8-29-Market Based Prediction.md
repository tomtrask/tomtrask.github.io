---
layout: post
title: Market Based Predictions
---

As I write this,
[betfair](https://www.betfair.com/exchange/plus/en/politics-betting-2378961)
(Not available in all countries, sorry) gives Biden odds of 1.92 (back all)
or 1.93 (lay all) to be the next POTUS. It gives odds of 2.12 (back all) or
2.14 (lay all) for Trump to be the next POTUS. This amounts to implied
probabilities of 52.1% to back vs 51.8% to lay Biden. Likewise those
probabilities for Trump are 47.2% and 46.7%.

What does that mean and why would I care?

Let's start from the top.

### Odds, back bets, lay bets, implied probability

Odds on betting sites are stated as a relationship between a bet amount and
the winnings or payout that result when the bet proposition is established to
be true. Winnings are the amount you win (seems obvious but hang on), payout
is the winnings plus your bet. Betfair bets work somewhat like a horse race
ticket. With a horse race ticket you give the person behind the counter some
fixed amount and announce your bet. The fixed amount when I used to listen to
the race results from Los Alamitos on KNX was \$2 and the payouts were always
something bigger than that. The odds given above are what is known as _decimal
odds_ and they are the amount you would win if a horse race style ticket cost
\$1. There are other ways to express odds. _Fractional odds_ is common.
Fractional odds are simply the winnings divided by the bet expressed usually as
a pure fraction. _American odds_ on the other hand are the winnings one would
get on a \$100 bet, if positive, or the negative amount of money one would have
to bet to win \$100 if negative. Decimal odds have the advantage that their
reciprocal is exactly the _implied probability_. Implied probability is an
estimate of probability of the proposition happening. That actual probability
is the reason I'm writing this. This table shows the relationship between the
different odds and implied probability for the above propositions:


| Odds Type           | Biden, Back | Biden, Lay | Trump, Back | Trump, Lay |
|---------------------|:-----------:|:----------:|:-----------:|:----------:|
| Decimal             |     1.92    |    1.93    |     2.12    |    2.14    |
| Implied Probability |    52.1%    |    51.8%   |    47.2%    |    46.7%   |
| Fractional          |    11/12    |    13/14   |     10/9    |     8/7    |
| American            |     -109    |    -108    |     111     |     114    |


So what's a back and lay bet? A back bet is a bet that the condition will be
true at the conclusion of the bet. A lay bet is a bet that the condition will
be false. One way to think of back vs lay is that you are betting the prop
or you're taking the house side of the prop. The odds on back and lay bets are
always back odds in the same sense that the loan interest you talk about when
you take out a loan or buy a CD is the interest rate being paid, whether you
are borrowing money from the bank or lending them money. Since betfair is a
market the back and lay numbers are, in fact, unmet bids. Specifically a
bettor wants to back Biden if they can get 1.93 (and if somebody wants to
accept those odds, they can buy a lay bet on Biden. Likewise some bettor wants
to lay odds on Biden at 1.92. If somebody wants to take 1.92, they can. I
always want to say the two odds, back and lay, are like a bid and ask but it's
not quite that simple. They're both ask prices but not for the side you'd think.
The back bet odds is the ask of somebody wanting to do a lay bet and vice versa.
The bet is only completed when somebody bids that much. In the case of the
back bet, that means taking lower odds than you'd like. In the case of the
lay bet, that means paying higher odds than you'd like.

So let's put this together a little bit differently. In that last table I
showed the odds _as given_ in betfair - back, lay, decimal odds within a couple
percent of each other. Let's instead look at what either side has to put on
the table to win a fixed amount, say \$1000. We expect that an exhaustive set
of bets for a given proposition (say, back and lay Biden) would cost over
\$1000.  I once thought that back Biden and back Trump was exhaustive but it
isn't, more
on this later. But let's see:

| Metric              | Biden, Back | Biden, Lay | Trump, Back | Trump, Lay |
|---------------------|-------------|------------|-------------|------------|
| Decimal Odds        |     1.92    |    1.93    |     2.12    |    2.14    |
| Implied Probability |    52.1%    |    51.8%   |    47.2%    |    46.7%   |
| Probability of Win  |    52.1%    |    48.2%   |    47.2%    |    53.3%   |
| Cosf of \$1K bet    |     \$521   |     \$482  |     \$472   |     \$533  |

So as we expected, if we back and lay Trump, it will cost \$1005 and we'll only
win \$1000 so we would never bet that combination. Likewise {back, lay} Biden.

But what about back Biden and Trump? That costs us \$993 and seems to yield a
payout of \$1000 regardless of which candidate wins. Yes, today this 0.7% win
is not worth the cost. While it seems at first blush to be a risk free bet - in
the last 58 elections the winner has always been one of the two major party
candidates - it seems imprudent to call an election of two candidates that are
both older than Ron Reagan in his first election a certainty. I don't know who
said it, I read recently and want to credit Pascal but what I read was that
if an event doesn't occur in N trials, compute the odds as if two additional
trials had been performed, one succeeding and one failing, just like the prior
N trials. So the odds against are (N+1)/(N+2) and more importantly the
probability of success is distributed as B(1, N+1).

And that is really the point of all this. We have a bet that is maybe 59/60
(98.3%) likely to win (betting on both candidates) but the implied probability
of that bet is 99.3%. A rational actor would never place that bet.

### A Comparison

On 2020-7-4 that same table looked like this:

| Metric              | Biden, Back | Biden, Lay | Trump, Back | Trump, Lay |
|---------------------|-------------|------------|-------------|------------|
| Decimal Odds        |     1.73    |    1.74    |     2.76    |    2.80    |
| Implied Probability |    57.8%    |    57.5%   |    36.2%    |    35.7%   |
| Probability of Win  |    57.8%    |    42.5%   |    36.2%    |    64.3%   |
| Cosf of \$1K bet    |     \$578   |     \$425  |     \$362   |     \$643  |

So a hypothetical bet to back both Biden and Trump costs $940 and yields $1000.
If our stake is $1000 and we presume that either winning is a 98.3% likely win,
Kelly suggests we should bet \$721. And of course, like all Kelly bets a
rational gambler scoffs at that huge number and adjusts it downward but still
on July 4, there was reasonable bet to be made on this race. Today there is not.

My question is and always has been what is the probability of either man
winning? Why, when I expect the winner to be one of these two and therefore for
the sum of both implied probabilities to be about 1 or maybe a bit higher, was
the sum so much less than 1? And why did the odds move from 3/2 in favor of
Biden to essentially a coin flip today? Can any of these market driven odds
be trusted?

There's more to this than a single post but for now I've got to drop
it and go do some chores.

