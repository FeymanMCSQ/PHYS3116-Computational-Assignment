## Research question

[INTRO]

Okay. So the purpose of this experiment was for us to find whether or not, if there were clusters in our current galaxy that were not originally part of our galaxy, right?

## Datasets

[DATA]

And the thing is, we were basically given, like, a few datasets. We were given Harris Part 1, Harris Part 3, Krause and van den Berg, right? Now the thing is, each of them contained, like, different values. Harris Part 1 contained the locations, Part 3 contained the movement measurements, while Krause and van den Berg contained, like, age and metallicity. So it was our job to, like, figure out what changes and what separates them.

## Movement analysis

[METHOD]

So first of all, we talked about the Harris Part 1 and the Harris Part 3, which contained the location and movement stuff. Now the thing is, at the end of the day, the choice of what qualifies as, like, a valid flagged cluster was the thing we chose ourselves, right?

So for the Harris one, we basically, like, matched the clusters and found out the clusters that had both, like, the galactic longitude and the movement measurement, right? And so it was our job to figure out what qualifies as, like, an outlier.

## Flagging rule

[CUTOFF]

So we basically took, like, the top 10% of absolute V underscore LSR values as outliers, and technically speaking, we could have also taken 5% and 15%, and we did check for specific clusters. We did check if, like, they were only, like, valid for, like, the 10%, or if they're also valid for the other percent. But we generally chose 10% as the cutoff point because it gave us enough flagged clusters to look at without flagging too many.

## What a flag means

[LIMITATION]

And when we found it, we basically found, like, a set of values that, like, were flagged, and it is necessary to keep in mind that, like, them being flagged did not prove they were from a different galaxy. It just basically, like, gave us an idea that these are sort of suspicious, so we might need to check them out.

## Fields used

[DATA DETAIL]

Right, so we had Harris Part 1 and Harris Part 3. Part 1 supplies us the L, which is the galactic longitude. Part 3 supplies us the V underscore LSR, which measures movement toward or away from us, after adjusting for the Sun's motion.

## Cutoff check

[SENSITIVITY]

We chose the top 10%. For this flag we use the absolute values, so it doesn't matter whether it's moving away from us or towards us. The original measurements still have that direction; the rule just looks at the size. The 10% is that it's just a flag. We chose the 5% and 15% checks were to see if, like, the flagging was dependent on our specific cutoff, or if it just, like, gets also flagged in other criterias.

## Result

[FIGURE / RESULTS]

143 clusters had usable measurements. The other 14 had, like, the V underscore LSR measurement missing; none were missing the galactic longitude. And out of the 143, 15 met the 10% rule. Once again, it is not established if it's actually from a different galaxy or not. It just gives us, like, more stuff to investigate further.
