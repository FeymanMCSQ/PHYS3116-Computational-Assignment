# Assigned Tasks
- Identify both supplied datasets and find the important columns in each
- Identify the cluster name/ID fields and determine how the datasets can be matched
- Start a joint python script for loading, checking and merging the datasets.
- Commit both the code and the brief documentation found on github.
# Datasets and Column Definitions
## Harris Catalogue Part I(https://physics.mcmaster.ca/~harris/mwgc.dat)

Key to columns:
1. Cluster identification number
2. Other commonly used cluster name
3. Right ascension (epoch J2000)
4. Declination (epoch J2000)
5. Galactic longitude (degrees)
6. Galactic latitude (degrees)
7. Distance from Sun (kiloparsecs)
8. Distance from Galactic center (kpc), assuming R_0=8.0 kpc
9. Galactic distance component X (points toward Galactic center)
10. Galactic distance component Y (direction of Galactic rotation)
11. Galactic distance component Z (toward North Galactic Pole)

Note: 9-11 - in kiloparsecs, in a Sun-centered coordinate system

## Harris Catalogue Part III
            Part III:  Velocities and Structural Parameters

Key to columns:
1. Cluster identification
2. Heliocentric radial velocity (km/s)
3. Observational (internal) uncertainty in radial velocity
4. Radial velocity relative to Solar neighborhood LSR
5. Central velocity dispersion sig_v (km/s)
6. Observational (internal) uncertainty in velocity dispersion
7. King-model central concentration, c = log(r_t/r_c); a 'c' denotes a core-collapsed cluster
8. Core radius in arcmin
9. Half-light radius in arcmin
10. Central surface brightness, V magnitudes per square arcsecond
11. Central luminosity density, log_10(Solar luminosities per cubic parsec)
12. Core relaxation time t(r_c), in log_10(years)
13. Median relaxation time t(r_h), in log_10(years)

## van de Berg et.al (2013) (https://mast.stsci.edu/search/ui/#/hst/results?proposal_id=10775)
1. Cluster Identification (does not include "NGC" compared to Harris)
2. Name
3. FeH (metallicity)
4. Age
5. Uncertainty on age estimate
6. Method (V or H)
7. Figs (reference to figure number)
8. Range (range for age estimate)
9. HBtype (horizontal branch morphology index, where a cluster's stars sit on the horizontal branch of the HR diagram)
10. Distance from the Galactic centre (kpc) (overlaps with Harris's R_gc - can crosscheck)
11. Absolute visual magnitude (measure of cluster's total luminosity)
12. Central Escape Velocity
13. log of the central velocity dispersion

## Krause21
1. Class
2. Name
3. Alternative Name
4. Stellar Mass
5. Half light radius (where half the cluster's light is contained)
6. C5?
7. Age
8. Metallicity

# Methodology
1. Merge Harris I and Harris III together using ID
2. Fill in information about Age and FeH, with vandeBerg (primary source) and Krause21 (secondary source), and keep the source of the age tracked
3. NON-NGC Harris clusters - flag, and keep in full table with NaNs
4. Analysing information - use only relevant clusters that have all information available.
