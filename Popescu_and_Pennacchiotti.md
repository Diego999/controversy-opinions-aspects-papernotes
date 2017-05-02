# Detecting Controversial Events from Twitter

This paper addresses the task of identifying controversial events using Twitter and presents 3 regression models.
They model the controversial event dtection task as supervised learning and they analyze each snapshot (s=(entity e, delta t, set of tweets related to e)).

## Direct model

Estimating the controversy score cont(s) in a single step using regression model.

## Two-step pipeline model

The event detection classification model selects event snapshots from the set S. 
The controversy detection regression model assess the level of controversy cont(s) for snapshosts

## Two-step belnded model

A soft variant of the pipeline model 