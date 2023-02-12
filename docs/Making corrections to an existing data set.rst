==========================================
Making corrections to an existing data set
==========================================

------------------------------------------
Correcting Metadata and Description Only
------------------------------------------

The metadata associated with an existing data set in a MatD3 database instance can be edited by users with administrator privileges, using the admin interface of that database instance.

------------------------------------------
Correcting actual data
------------------------------------------

The MatD3 database software does not actually allow one to directly edit the data stored in a given data set. This is by design. A data set that is retroactively edited would introduce a reproducibility issue since we do not have a log that remembers such edits and their version history. Even if we did, the complexity of such a system would be significant.

Rather, the recommended approach to making corrections is to actually create a new data set that includes the corrected data. If needed, a comment can be added in the new data set that explains the situation and indicates that the updated data set is to be preferred over the previous one (and why).

Additionally, it is possible to delete an incorrect data set - obviously, deletions should only be done after careful verification.
