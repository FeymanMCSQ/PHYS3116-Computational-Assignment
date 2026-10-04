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
  - **Meaning:** Right Ascension, imagine a sky wrapping the earth around in a ball, the RA is equivalent to the longitude
  - **Unit:** hours minutes seconds

- **DEC**
  - **Meaning:** Equal to the latitude
  - **Unit:** degrees, arcminutes arcseconds

- **L**
  - **Meaning:** Galactic longitude, direction around plane of the milky way
  - **Unit:** degress

- **B**
  - **Meaning:** Galatic Latitude, angle above or below the Galactic plane
  - **Unit:** degrees

- **R_Sun**
  - **Meaning:** 3d distance from sun to cluster
  - **Unit:** KPCs

- **R_gc**
  - **Meaning:** 3d distance from galactic centre to cluster
  - **Unit:** KPCs

- **X**
  - **Meaning:** Sun centred distance component pointing to Galactic centre
  - **Unit:** KPCs

- **Y**
  - **Meaning:** Sun centred distance component pointing in direction of Galactic rotation
  - **Unit:** KPCs

- **Z**
  - **Meaning:** above or below galactic disk
  - **Unit:** KPCs

Now, at an initial glance, the most likely relevant fields seem to be the following:

1. ID: essential for matching to the informaiton in the Harris Part III.
2. L: Galactic longitude influences how we percieve the velocity pattern of the clusters movement,
   depending on where it is we might percieve it to be moving different in direction
3. B: Shows the angle above or below the galactic plane, and it also affects how motion
   is projected on our line of sight
4. X, Y, Z: Help us find position depending on location

Secondary Relevant:

1. R_gc: useful for comparing inner and outer clusters and seeing if dynamic behaviour changes with distance
2. R_Sun: useful for distance context

Tertieray fields:

RA and DEC: can help us locate clusters on sky but it is not that useful since we already have the
galactic coordinate system

Name: who cares about this?

### Harris Catalogue Part III

The Harris Part III columns are these:

1. **ID:** Primary cluster identifier, not unit

2. **v_r:** how quickly the whole cluster is moving away from the sun. Positive means away, negative means toward us. km/s

3. **v_r_e:** uncertainty in the measurement. Unit: km/s

4. **v_LSR:** The cluster's toward-or-away speed compared with a local reference that follows the average movement near the Sun. The Sun has its own extra movement relative to that reference, and v_LSR adjusts for it.

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
cluster on a 3D map. Then v_LSR tells u whether that cluster is moving toward or away compared with
the local reference near the Sun.

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

1. How does a cluster measured movement change depending on where it is?
2. WHich clusters stand out compared with clustes in similar locations
3. Are those differences convincing once we check whether uncertain the measurements are?
4. DO the clusters that stand out in movments also stand out in Aditi's age and metallicity work
5. What can we reasonably say about where those clusters formed, and what extra measurements would
   we need to be certain.

## Proposed Methodology

1. Connect the two Harris tables using ID: This gives each cluster its location from Part I and its movement
   measurement from Part III. Daniel is preparing the combined data and I will check that the columns I
   need match correctly

2. CHeck whether the clusters have usable measurements. Nate any misssing speeds and check for obvious
   mistakes before making graphs.

3. Make a first graph of v_LSR against L. This lets us see whether the measured movement changes as you
   look in different directions around the milky way, We can also use B, Z or R_gc to see whether location
   affects what u observe.

4. Describe how most clusters behave: look from a broad trend, if there is one. Do NOT assume in advance
   that they need to follow the same movement.

5. Identify possible unusual clusters: we choose a clear rule for how far a cluster must differ from the
   broad trend, then check the uncertainty of its measured speed using v_r_e. Record why each was flagged.

6. Compare my list with Aditis: See whether any cluster stands out in both movement and age-metallicity

7. Explain the limits. THese speeds show only movement toward or away along our viewing direction. They
   cannot, by themselves give us a clusters full path or prove where it formed.

## Dependencies and Team Coordination

Daniel: He is combining the catalogues. I need the cluster ID, position, movement columns matched correctly. I will start working on Harris Part I and III while he works on the full combined file. When
his file is ready, check a few cluster rows against the original CSVs.

Aditi: SHe is looking at clusters age and metallicity. Once we have canditate lists, we compare the IDs.

Me: share my graphs, my flagged clustes, and short reason for each choice. Also tell the team which clusters had missing or uncrertain measurements.

Whole team: Agree on what "unusual" means and how cautiously to describe an accreted cluster.
