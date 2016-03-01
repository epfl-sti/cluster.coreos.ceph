# Ceph on EPFL-STI CoreOS clusters

TODO: we have no idea what we are doing.

## ceph-osd

We just run ceph-osd.service everywhere (`Global=true` in `[X-Fleet]`)

## ceph-mon

+ We need a quorum of ceph-mon@
+ Apparently, insertions Just Work; when fleet migrates a mon however, we are
  supposed to clean up after it:<pre>docker exec -it ceph-mon ceph mon remove c08.ne.cloud.epfl.ch</pre>
