# Safi Ullah -- Week 2

## Assigned Task

- Investigate the behaviour of the Milky way clusters.
- Identify the position and velocity measurements in the datasets for the GAlactic rotation
- Determine how the motions of the the clusters could be compared with the bulk cluster population
- Develop a way to find the dynamically unusal clusters such that u can defend it in data analysis
- Then we compare the dynamic and the behaviour of clusters to the age-metallicity data.

## Relevant Datasets and Columns

### Harris Catalogue Part 1

The columns mean the following for the Harris Part 1:

- **ID**
  - **Meaning:** Primary cluster identifier
  - **Unit:** no unit

- **Name**
  - **Meaning:** Common Name
  - **Unit:** no unit

- **RA**
  - **Meaning:** Right Ascension, imagine a sky wrapping the earth around in a ball, the RA is equivalent to the latitude
  - **Unit:** hours minutes seconds

- **DEC**
  - **Meaning:** Equal to the longitude
  - **Unit:** degrees, arcminutes arcseconds

- **L**
  - **Meaning:** Galactic longitude, direction around plane of the milky way
  - **Unit:** degress

- **B**
  - **Meaning:** Galatic Latitude, angle above or below the Galactic plane
  - **Unit:** degrees

- **R_SUN**
  - **Meaning:** 3d distance from sun to cluster
  - **Unit:** KPCs

- **R_gc**
  - **Meaning:** 3d distance from galactic centre to cluster
  - **Unit:** KPCs

- **X**
  - **Meaning:** Sun centred distance component pointing to Galactic centre
  - **Unit:** KPCs

- **Y**
  - **Meaning:** Sun centred distance component pointing in direction of the centre
  - **Unit:** KPCs

- **Z**
  - **Meaning:** above galactic disk
  - **Unit:** KPCs

Now, at an initial glance, the most likely relevant fields seem to be the following:

1. ID: essential for matching to the informaiton in the Harris Part III.
2. L: Galactic longitude influences how we percieve the velocity pattern of the clusters movement,
   depending on where it is we might percieve it to be moving different in direction
3. B: Shows how far above or below the cluster lies in the galactic plane, and it also affects how motion
   is projected on our line of sight
4. X, Y, Z: Help us find position depending on location

Secondary Relevant:

1. R_gc: useful for comparing inner and outer clusters and seeing if dynamic behaviour changes with distance
2. R_sun: useful for distance context

Tertieray fields:

RA and DEC: can help us locate clusters on sky but it is not that useful since we already have the
galactic coordinate system

Name: who cares about this?

### Harris Catalogue Part III

## How we physically interpret the data

## Research Questions

## Proposed Methodology

## Dependencies and Team Coordination

## Tasks before Week 3
