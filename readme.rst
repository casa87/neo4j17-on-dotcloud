Neo4J 1.7 On DotCloud (ALPHA)
=========================

This is an **ALPHA** (i.e., not production-ready) Neo4j stack for DotCloud.

based on https://raw.github.com/jpetazzo/neo4j-on-dotcloud-ALPHA

How It Works
------------

It retrieve Neo4j community edition tarball, unpacks it, and adds a little
bit of scaffolding (custom scripts) to run it under dotCloud.
The build is not totally dotCloud-compliant (it uses all the default build
options, instead of trying to setup the logs/data/etc. directories in the
proper place).

Again: **don't use this for production!**

Proper Neo4j support will come soon.


How To Use It (Standalone)
--------------------------

Just use our (un)patented Clone-And-DotCloud-Push method::

  
  dotcloud push  neo4j17-on-dotcloud

At the end of the push, the URL to the Neo4j administration interface
will be shown.


How To Use It (In Your App)
---------------------------

Add the ``dotcloud.yml`` supplied here to your own ``dotcloud.yml``,
and copy the ``neo4j`` directory to your repository as well. Push as
usual. Rejoice (but remember not to put any important stuff into
your Neo4j DB yet).


Authentication
--------------

Default authentication is located in ~/neo4j/conf/db-acl.properties
the default accounts are :

write:passwordwrite
readonly:passwordread

Please don't forget to change it