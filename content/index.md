+++
date = "2017-03-10T11:25:12-05:00"
draft = false
title = "Dirty Dozen results using Strava times"
url = "index.html"
+++

This is a fun experiment with the Strava API to compare against the official Dirty Dozen results. There's a lot of interesting data available which this only begins to explore. I'm hoping to add some more analysis and additional ranking schemes later. 

Scoring
-------
The official Dirty Dozen scoring system is based on the order athletes reach the top of 13 designated hills. So, only riders in the lead pack are eligible to score points. Male competitors use a 10-point system (10 points for 1st, down to 1 point for 10th) and female competitors use a 5-point system (5 points for 1st, down to 1 point 5th). Competitors must finish all 13 hills to be ranked. The system is simple and, barring any unusual circumstances, provides a clear winner.

I’ve considered two scoring the systems based on Strava data, where instead of ranking athletes based on the time-of-day they reach the top of the hill, it is instead based on ***time from the bottom to the top of the hill***, i.e. a Strava segment. There are several advantages of using a Strava based approach. First, it does not matter where in the pack a rider begins, or even that they ride with the lead pack at all. There is no fighting for position in the pack, simply because it does not matter. Logistically, it makes collecting results super easy (all these results are generated automatically through the Strava API).

Obviously, there are some disadvantages of using Strava. Segment time are prone to GPS error, not all participants use Strava, and standings are unclear until all riders finish and upload their ride.

#### Points System
This is the classic points based system used by Danny Chew, with a couple small modifications. It’s possible for riders to tie on Strava, and when this occurs occurs, I’ve awarded both riders the number of points for the better position (e.g. if times for top 4 male riders are 45s, 49s, 46s, and 46s each rider gets 10, 7, 9 and 9 points, respectively). I did not require athletes to necessarily finish all the hills to be ranked, because many riders' Canton Ave segment is missing (the hill is quite short and GPS does not always pick it up).

