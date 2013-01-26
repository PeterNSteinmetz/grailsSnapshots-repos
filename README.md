grailsSnapshots-repos
=====================

This project is designed to make finding and using snapshots of Grails plugins simpler. 
It is currently at a startup stage for design of a mechanism to achieve this.

Ideal operation.
================

When complete we would like to have a system that operates something like the following:

* There is a grailsSnapshots declaration that can be used simply by adding 'grailsSnapshots()' to the repositories stanza.

* Dependencies on snapshops can be simply expressed in the plugins block.

* Snapshot releases will be stored in a central maven repository which the grailsSnapshots declaration refers to.

* Snapshot releases can be deployed to the central maven repository using the Release plugin and its publish-plugin command. 

* The main grails plugin portal will reflect the last several snapshots which have been released.

* Source code for the snapshot versions of plugins will be maintained in Github as a separate repository from the main line 
development for a plugin.

* All developers agreeing to a simply statement of goals will be allowed to commit to the source and to create
snapshot releases.

Practical Starting Point.
=========================

Achieving the ideal will take some time and effort. In order to get to this point, the practical plan is:

1. Use the existing Grails snapshot repository to store snapshots.

2. Source code for each plugin will be maintained in a separate Github repository. This repository will maintain a branch named
snapshot, which will contain the line of development resulting in the snapshot releases and will be tagged with 
subnumbering, so that it is possible to use particular snapshots. For example, snapshots for development of myplugin:1.2 
would be numbered like myplugin:1.2.1-SNAPSHOT, myplugin:1.2.2-SNAPSHOT.

3. This project will maintain a list of current snapshot plugins, pointers to their SCM, as well as appropriate dependencies
to be used to bring them into a project.

4. Snapshot developers will be members of this project and be granted access to the SCM for the individual plugins they may 
wish to work on as well as onto the Grails snapshot repository.

Moving Toward Ideal.
====================

In the event there is sufficient work on snapshots, work can commence on changes to achieve the ideal. These would include:

* Modifying the Release plugin to publish to the Grails snapshot repository.

* Modifying the website plugin portal to reflect the snapshot versions. 


