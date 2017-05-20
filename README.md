# mongodb_update
Scripts to update a MongoDB cluster to a different version.

The intent here is to provide a set of scripts that can perform a rolling update of a mongodb cluster.  The way that this is achieved is by delivering to each MongoDB node a script that will idenitfy that nodes role, then query the cluster to determine when is the right time to update the binaries and restart any MongoDB processes, based on that node's role in the cluster.  The delivery mechanism at this time is puppet for which a puppet class is provided.
