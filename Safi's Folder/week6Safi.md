# Safi — Week 6

## Overview

My Week 6 contribution was significant. It was mostly about coordinating and patching everything together so the different parts could work properly together.

## Daniel's merged data

For Daniel's part, I helped make the merged datasets readily usable for the analysis. Daniel had done the merging; the main thing left was to export the table to an actual `master.csv` file instead of just printing it out. I wrote the code to do that.

I also verified the data: all 157 Harris IDs were present, the age coverage counts were printed, and I corrected some misleading labels on the NGC-only graphs.

## Harris Part II preparation

For Aditi's work, I downloaded the original Harris catalogue because her notebook was trying to fetch it every time it ran, and that kept giving us errors. I added a preprocessing notebook that extracted Harris Part II into a CSV, so we could use the local file instead of the internet-fetched one.

## Age–metallicity work after Week 6

I then worked on the age–metallicity analysis. Aditi had done significant work on that, but I filled in and patched the holes. My work involved setting up the cutoff values, checking different windows, finding which clusters were flagged across the settings, exporting those values, and using them to finish the work.

This age–metallicity analysis happened after midnight at the end of Sunday in Week 6, so it belongs to Week 7.
