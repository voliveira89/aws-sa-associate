# Cross Region Replication

* To allow for cross region replication, the both source and target buckets must have versioning enabled
* When cross region replication is enabled, all existing objects in the bucket are not copied over to replica site. Only updates to existing objects and newer objects are replicated over. All previous versions of the updated objects are replicated
* Permissions are also replicated from one bucket to another
* Transitive replications do not work. E.g. if you set up bucket C to replicate content from bucket B which replicates content from bucket A – Changes made to bucket A will not get propagated to C. You will need to manually upload content to bucket B to trigger replication to C.
* Delete markers are replicated
* If you delete source replication bucket objects, they are deleted from replica target bucket too. When you delete a Delete marker or version from source, that action is not replicated

