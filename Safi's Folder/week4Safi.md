# Safi - Week 4

## Movement analysis

First of all, we continued from the Week 3 work, where we merged Harris Parts I and III. Of the 157 clusters in that merge, 14 had no `v_LSR` measurement, which left 143 for the movement check. We compared their movement with Galactic longitude and divided the longitude into six 60-degree sections. The section averages changed across the sky, but the individual speeds overlapped a lot, so we couldn't earnestly say that the graph showed two clean groups.

Then we made a movement shortlist by flagging the highest 10% of absolute `v_LSR` values: basically, clusters with very large measured speeds towards or away from us. That put the cutoff at 214.72 km/s and flagged 15 clusters. We didn't treat 10% as a hard rule, though. We also tried 5% and 15%, which flagged 8 and 22 clusters. This helped us see which names survived a stricter cutoff and which only just made the list. This is a speed shortlist, not a list of proven origins.

## Age and metallicity analysis

I also did an age and metallicity analysis, which was originally assigned to a teammate. I made this as a backup; it isn't supposed to replace my teammate's work. It's there in case there are issues with whether they can deliver their work in time. For this, I used van den Berg's 55 measurements and Krause's 61 measurements. I checked the columns, matched their IDs, and kept the two sources labelled instead of just averaging their values, because some values differed. That gave me 116 measurements, not 116 different clusters, because some clusters appeared in both sources. I plotted age against metallicity so I could see the measurements from both sources.

Next, I made an age shortlist. For each measurement, I compared its age with the middle age of other clusters from the same source whose metallicity was within 0.25 of its `FeH` value. I required at least four other clusters and an age difference of at least 2 billion years from their middle age. This first rule flagged four measurements belonging to three clusters: NGC 1851, NGC 6171, and Pal 12. Pal 12 appeared twice because both sources flagged it; the other two were flagged in only one source each.

I then tested whether the age flags were fragile. I changed the metallicity range and age cutoff across five settings to see whether the same clusters kept standing out or depended on my choices. Krause's NGC 1851 and Pal 12 stayed flagged across all five settings. Van den Berg's Pal 12 stayed flagged across four, while NGC 6171 depended more on the rule. I also checked the original rows and compared ages between sources. Pal 12's age estimates were similar, while NGC 1851's differed substantially. Krause's table doesn't provide an age-error field, so I couldn't use these tables alone to declare one estimate more accurate than the other.

## Comparing both results

I connected the two analyses by exporting a CSV from each notebook and matching the clusters by ID in a separate comparison notebook. NGC 1851 was the only cluster flagged in both. Pal 12 and NGC 6171 had age flags but not movement flags. Seven movement-flagged clusters had a usable age comparison but no age flag, and another seven had no usable age comparison. None of the age-flagged clusters lacked a movement measurement. I kept "checked and not flagged" separate from "couldn't fairly check."

## Checks and commits

I reran the notebooks, saved the results, and committed the work.
