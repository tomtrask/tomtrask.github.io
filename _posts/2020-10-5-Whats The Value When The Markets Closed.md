---
layout: post
title: What's the Value When The Market's Closed?
---

I've been sampling the Betfair 2020 Presidential race market since 2020-7-4.
That's approximately the date Kanye West entered the race and that's the reason
I started monitoring the conte market. Friday, 2020-10-1, when I went to sample
that market, betfair said the market was suspended. My question is simply, what
happens to the price when the market is suspended? I'm not asking how bets are
settled, I assume the market will re-open (in much the same way that the NYSE
and other equities markets re-opened after 9/11). I'm simply asking what we
should expect to happen while the market is closed?

Consider other markets and somewhat
This is an update, mostly, on a project I've been working on wherein I sample
the betfair odds on the "USA - Presidential Election 2020". My curiosity to
date has me collecting daily prices since about 2020-07-04, approximately daily,
approximately 6-9AM Pacific. I'm reading and transcribing this data from the
betfair site and then running an ever evolving notebook of pandas/matplotlib
code on the results. As some may know, that market closed Friday morning,
2020-10-02 and reopened Monday afternoon. The question today is simply what
happens to the price between samples? Is that process different if the market
is open? My initial answers were "uncertainty creeps into the price" and "yes"
but I've changed my mind somewhat.

I want to make a case that exponential moving average (EMA) gives me a sense of
how reliable a market price is when the market is closed. Further I want to
posit that the half life for that EMA is dependent on the volatility of the
iten in question on the scale of the price is sampled.

Let me walk through that with some examples:

* stock prices I expect to open within a very small percentage on any day of
where they closed the prior day
* milk or eggs in the grocery market I expect to be within a few cents of where
they were last time I went to that same store
* gasoline, I can sample whenever I see a gas station on the street. For this
commodity, I do need to factor out zip code maybe and species of gas station.

I should clarify
And already I've painted myself into a corner but I'm going to snap my fingers
and be out of it. By "market's closed" I mean, *mostly* that I'm not watching,
I'm not polling the price. I may look at the price of AMZN on the stock market
in the morning and again when the market closes but

I think the only time we know the value of an asset (e.g. a bet) is
immediately after the asset is bought or sold. Before that transaction and after
that transaction, the value of the asset is unknown. We have some confidence
that the value is the same as or near the previous transaction valuation. We
could assume that the price will open tomorrow at the same price it closed
today. We could assume it will open within the single day volatility with 95%
probability (one day in 20, the price will be up or down "a lot" tomorrow
morning). Consider milk. In my life it's a fairly volatile priced commodity
that I see the price of since I can only store a week's supply in my fridge.
And maybe, since I only buy it weekly or less frequently, let's expand our
timeframe. I don't see the price of milk daily but I do see the price of milk
when I go to a store in which I might buy it (e.g. Trader Joe's, Safeway,
rarely Target, sometimes Smart & Final, never 7-11 or other convenience store).
And while I might or might not buy milk or even notice the price at TJs, I do,
quite frequently, pass by the egg case and note the price of a dozen large eggs
and that can act as a proxy for milk. The prices of both go up or down at the
same times and both seem to be positively correlated to the price of a gallon
of gasoline (which I can price by driving past a gas station).

