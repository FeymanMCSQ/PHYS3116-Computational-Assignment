VDB is the main age source, and Krause21 is an optional cross-check

# How the datasets match

1. ID formats: NGC 104 in Harris, NGC104 in Krause21 and 104 in VDB
2. method: pull out an integer NGC_number from each, and using NaN when there is none
3. used a left merge when merging tables: Harris is the base table and nothing gets dropped when merging

# Validation

-added a final master with 157 rows, 157 unique harris IDs, and zero repeated IDs
-vanderberg matches: 55; Krause matches: 61. All sources rows mappd after the checked name matches.
-52 clusters have ages from both sources; 93 have no age from either source. So, that leaves us 64 with at
least one age from one source.
-the earlier graph only uses 104 row NGC only table the final master retains all 157 clusters.

# Issues and Limitations

- 53 non-NGC clusters have no NGC_number
- there are 6 name-only rows (3 from VDB, 3 from Krause21) which are matchs by name and distance
- 93 clusters without age cannot be assessed without an age comparison
- matching distance is useful but not a perfect independant proof.
