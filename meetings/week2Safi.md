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

The Harris Part III columns are these:

1. **ID:** Primary cluster identifier, not unit

2. **v_r:** how quickly the whole cluster is moving away from the sun. Positive means away, negative means toward us. km/s

3. **v_r_e:** uncertainty in the measurement. Unit: km/s

4. **v_LSR:** Another version of the cluster field toward or away from us. The sun is also kinda moving through the Milky. This movement affects the measurement. v_LSR kinda adjusts to like remove or mitigate the sun's effect.

   This makes it easy to compare it to other clusters. km/s.

5. **sig_v:** stars inside a cluster don't move at the same speed. this tells us how different their speeds are. A larger number means more spread out. unit km/s

6. **sig_v_e:** uncertainty in sig_v. it is also in km/s

7. **c:** describes how strongly the clusters stars are like packed in the centre. larger c, more packed, less c, more spread out. Unit: none

8. **r_c:** size of the clusters central area. Unit: arcminutes

9. **r_h:** the size of area containing half of clusters total light. Unit: arcminutes

10. **mu_V:** how bright the centre of the cluster is. Unit: V-band magnitudes per square arcsecond

11. **rho_0:** how much light is packed into the centre of the cluster. a large number means more light in a given amount of space. its logarithmic. Unit: log10 of solar luminosities per cubic parsec

12. **lg_tc:** estimate on how long it takes the stars near the centre to change and mix their movements through repeated gravitational interactions. Unit: log10 of years

13. **lg_th:** a similar time estimate, but measured across larger cluster. also logarithmic. Unit: log10 of years

The most likely relevant ones are _drum roll_:

1. ID: tells u which cluster the row is on to correspond with Part I.
2. v_LSR: the main movement measure u will compare across clusters
3. v_r_e: tells u how uncertain the measurement movement is. A surprising value needs a closer look if like the uncertainty is massive.

Secondary:

1. v_r: measurement from sun, useful for checking v_LSR.

Tertiary:

1. sig_v and sig_v_e: describes how stars inside cluster move and how uncertain that number is. Our
   main question is the movement of whole cluster.

2. c, r_c, r_h: describe how packed together or spread out the clusters stars are. describe its structure

3. mu_V and rho_0: describe the brightness and how tightly packed in centre. once again no info about
   movement.

4. lg_tc and lg_th: describe timescale for changes inside cluster. Do not measure the whole clusters
   movement.

## How we physically interpret the data

Okay, so each of the clusters tell us two different stories:

Part I: Where is it?
Part III: How does its movement appear from our position?

For example, L and B tell us which direction to look in the Milky Way while X,Y, and Z help us place the
cluster on a 3D map. Then v_LSR tells u whether that cluster is appearing to be moving away from us after
we adjust for the sun's movement.

like imagine being in a side of a circle and people walk around the circle, technically from your POV they could be moving away or towards you even if they are walking in the same circular path. v_LSR thus does not
tell us how the cluster is behaving, we gotta consider where the cluster is as well.

So our question is:

When we compare clusters in different places, is there a broad way that most of them appear to move? Are
any noticeably different from cluster in comparable places

There are two things to also keep in mind:

1. v_LSR gives only the toward or away part of a clusters movement. It does not tell u its full path
   around its Milky Way.

2. An unusual measurement makes a cluster worth investigating, does not tell us if its from another galaxy
   or not.

## Research Questions

## Proposed Methodology

## Dependencies and Team Coordination

## Tasks before Week 3
