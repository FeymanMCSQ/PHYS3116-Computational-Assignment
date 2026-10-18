VDB is the main age source, and Krause21 is an optional cross-check
# How the datasets match
1. ID formats: NGC 104 in Harris, NGC104 in Krause21 and 104 in VDB
2. method: pull out an integer NGC_number from each, and using NaN when there is none
3. used a left merge when merging tables: Harris is the base table and nothing gets dropped when merging

# Validation (todo)
- put the row counts, unmatched IDs and duplicate checks in a small table
- include the merge check (R_gc against R_G)

# Issues and Limitations
- 53 non-NGC clusters have no NGC_number
- there are 6 name-only rows (3 from VDB, 3 from Krause21) which are matchs by name and distance
  
