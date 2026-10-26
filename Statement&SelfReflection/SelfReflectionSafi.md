# Safi Ullah — Statement and Self-Reflection

## Motion and location analysis

In this assignment, my main part was to figure out which clusters may not have
originally been from the Milky Way galaxy and instead may have been absorbed
when other smaller galaxies were absorbed into the Milky Way. The way I was
supposed to do this was through the longitude versus position versus motion
analysis for the clusters, and I used the Harris Part 1.csv and Harris Part
3.csv.

My coding was fairly simple. As a rule, I always make sure that all of my code
is modular, self-contained, and easy to understand. We started by loading the
Harris tables and checking everything was all right—the shape, the repeated
stuff, and the columns—and comparing the ID sets to make sure nothing was
missing or duplicated. Then I joined Part 1 and Part 3 using the same IDs and
made sure that the final number of clusters was still 157.

Then we made a first plot of motion against longitude to give us a general idea
of how they were distributed. We only plotted the values that had both
longitude and motion, which were 143. The other 14 were missing either one or
both, so we checked them. We found that none were missing longitude, but all
were missing v_LSR.

I divided the galactic longitude into six portions and, for each portion,
calculated the average v_LSR value, the spread, and the count. Then we took the
highest 10% of v_LSR values by magnitude and varied the cutoff between 5%,
10%, and 15%. We plotted all the clusters in grey and highlighted the ones
meeting the 10% cutoff, then exported the values.

## What I learned

For my assigned section, I learned how to work with real-world data, because
real-world data isn't an abstract representation of a perfect model. It's
messy. There are missing values and duplicated values, and at the end of the
day, there is no perfect first rule that differentiates between something
that meets a criterion and something that misses it.

For example, we had 157 values, but only 143 of them had both longitude and
motion. The other 14 did not, so we could not use them. We cannot make a proper
conclusion about any of those 14 from these measurements, because we do not
have enough values, and that's how it is in the real world.

Additionally, there wasn't a clearly defined rule for what the cutoff should
be, so I decided on 10%. I varied it to 5% and 15% to see which values
survived and which were taken out. This helped me see which outliers were
stronger across cutoffs and which depended on the 10% value. I did not choose
it because of a universal law. In real-world analysis, you have to make a
decision and justify it, which is what I did here.

Additionally, you can make observations and analyse them, but you cannot be
100% certain from this alone. For example, the 10% cutoff gave us a group of
clusters, but this only tells us about their motion away from or towards the
Sun. It does not give us their full paths around the Milky Way, and it does
not prove that they came from another galaxy. This motion and longitude may
be worth investigating, but they are not a hard, conclusive rule. We need to
use the age and metallicity analysis alongside them.

## Age and metallicity analysis

I was also partly responsible for the age and metallicity analysis, mainly
because the teammate responsible for that part got sick, although she did
substantial work on the Harris Part II plots too.

First, we were having trouble fetching the Harris data file from a link. I
downloaded the .dat file manually, but it was not a normal CSV: its columns
were laid out with fixed spacing, and missing entries needed to be handled
carefully. So I made the extractHarrisPartII notebook to read that layout and
export Harris Part II as a CSV. We then used that CSV in Aditi's notebook
instead of fetching the file from the internet.

The final age-metallicity analysis was still left, and since we were close to
the deadline, I took it upon myself to finish it. I loaded Daniel's combined
table, checked its rows and columns, and previewed the age and metallicity
values. Then I plotted age against metallicity for van den Berg and Krause to
get a first visual impression of which points might be unusual. But a visual
check was not enough.

I had already written a backup analysis using the original age datasets, so I
built a bridge in Aditi's notebook to use Daniel's combined table with the
same analysis. That bridge gives the age and metallicity columns shared names,
keeps their source labels, and keeps separate measurements separate rather
than averaging them.

After looking at the plot, we used a clear screening rule. Within each data
source, we compared a cluster's age with the median age of other clusters
whose metallicity was within 0.25 of its own. We only assessed it if it had at
least four such neighbours, and flagged it if its age differed from their
median by at least 2 billion years. Otherwise, we left it unassessed or
unflagged as appropriate.

The 0.25 range and 2-billion-year limit were choices for making a shortlist,
not universal laws. I explained why they were reasonable starting points and
repeated the check with different ranges and age limits. That told us which
flags stayed when the settings changed and which depended more heavily on
our choices. We then compared the shortlisted clusters' measurements,
especially where the two sources gave different ages, before interpreting
the flags. Finally, we exported all the age-check results to a CSV so we
could compare them with the movement results.

## What I learned from the age analysis

I learned that looking at a graph and deciding what seems unusual is not
precise enough by itself. Some points I noticed visually were flagged by the
rule, but I missed others, and some I thought were unusual were not flagged.
The mathematical rule gave us a consistent way to make the comparison, even
though the exact limits were still our choices rather than proven boundaries.

The amount of available data also mattered. If a cluster had fewer than four
similar-metallicity neighbours, we did not have enough for our chosen
comparison, so we left it unassessed. The sources sometimes gave different
ages for the same cluster as well. That brought me back to the same lesson
as the movement work: real-world data is messy and incomplete. Trying
different cutoffs helped us see how stable the shortlist was, but even a
stable flag does not prove where a cluster formed.

## Coordination and leadership

Perhaps the hardest part of this assignment was figuring out the
coordination. I was the coordinator and took on an administrative role, and
we ran into some significant issues.

One of our partners got sick, and I think we underestimated how much that
would affect the schedule. She still attended meetings, put in effort, and
did substantial work. However, I had to finish the remaining age-metallicity
analysis one day before submission. I learned that, no matter how well you
plan, being transparent about setbacks and accounting for them is as
important as making the initial plan.

From now on, I think I should be more helpful towards people and try to
understand why progress has stalled. If it is something outside their
control, I should be more open to offering help. At the same time, I should
have tracked progress more closely, set a clearer roadmap and firmer internal
deadlines, and prepared fallbacks if those deadlines were not met.

Daniel completed most of his work very well. At that stage, the remaining
step was exporting the combined table so the rest of the analysis could
use it.
