# PHYS3116 Computational Assessment

## What this project does

Okay, so this project is part of the PHYS3116 assessment. We used several
datasets to screen Milky Way globular clusters using movement, age, and
metallicity evidence, then compare the results.

Some clusters may have formed in smaller galaxies that were later absorbed
by the Milky Way. We do not know which clusters those are from these tables
alone. We look for clusters that stand out from the others and are worth a
closer look, not claim that a flag proves their origin.

We do two analyses: age versus metallicity, and galactic longitude versus
movement towards or away from the Sun. Then we check which clusters are
flagged by both.

## What to run

Run these notebooks in this order:

1. `Aditi's folder/extractHarrisPartII.ipynb` reads `mwgc.dat.txt` and
   converts Harris Part II into `HarrisPartII.csv`.
2. `Daniel's Folder/mergerCode.ipynb` combines the catalogues and saves
   `master.csv`.
3. `Safi's Folder/safisCode.ipynb` does the longitude and movement analysis
   and saves `movement_checked.csv`.
4. `Aditi's folder/plots.ipynb` makes the Harris Part II plots, then runs
   the age-metallicity analysis and saves `age_checked.csv`.
5. `Safi's Folder/holistic_work.ipynb` compares the saved movement and age
   results. It prints the clusters flagged by both, as well as cases where
   one result was not flagged or could not be assessed.

## How to run them

You need Python and Jupyter with pandas, NumPy, and Matplotlib. Run each
notebook with its working directory set to its own folder, because the
file paths in the code are relative to that folder.

## Where to look

Our individual folders contain the notebooks and week-by-week notes about
what we did. The `meetings` folder has our meeting notes, including what
we had done and what we planned to do next. Our individual reflections
give an overview of our contributions and what we learned.

## Other notebooks

`Safi's Folder/ageMetallicityBackup.ipynb` is a backup age-metallicity
analysis and is not needed for the main run. `Aditi's folder/Aditiscode.ipynb`
is an older data-loading notebook; the working analysis is in
`Aditi's folder/plots.ipynb`.
