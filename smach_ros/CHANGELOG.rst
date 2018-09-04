^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
Changelog for package smach_ros
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Forthcoming
-----------
* changed maintainer for local version
* Merge pull request `#5 <https://github.com/strands-project/executive_smach/issues/5>`_ from ros/indigo-devel
  Import upstream
* 2.0.1
* changelog 2.0.1
* Merge pull request `#48 <https://github.com/strands-project/executive_smach/issues/48>`_ from 130s/i/update_ci4
  [indigo-devel] Sync to master branch. Update CI conf to enable ROS IJKL
* [test] More pep8 enforced.
* [package.xml] Update maintainer.
* make rostest in CMakeLists optional (`ros/rosdistro#3010 <https://github.com/ros/rosdistro/issues/3010>`_)
* change MonitorState and document its behavior
* increment n_checks only *after* checking
  otherwise, setting max_checks=1 results in a MonitorState that returns the 'valid' outcome for any message
* Specify queue sizes for introspection publishers
* tests: adding test for actionlib timeout
* packaging: switching to format 2
* Using correct timeout
* SimpleActionState will no longer wait forever
  for a missing ActionServer
* Contributors: Isaac I.Y. Saito, Jonathan Bohren, Loy, Lukas Bulwahn, Marc Hanheide, Nick Hawes, Nils Berg, contradict

2.0.1 (2015-04-27)
------------------
* updated changelogs
* fixing monitor state callback args and adding unit test for monitor state that modifies userdata
* Merge pull request `#32 <https://github.com/strands-project/executive_smach/issues/32>`_ from T045T/patch-1
  make ServiceState more robust to termination while waiting for service
* make ServiceState more robust to termination while waiting for service
* 2.0.0
* Updating changelogs
* smach_ros: Adding rostests to cmakelists
* Merging changes, resolving conflicts, from strands-project (@cburbridge)
* cleaning up and removing rosbuild support
* merging groovy and hydro
* Fixing `#28 <https://github.com/strands-project/executive_smach/issues/28>`_ which was introduced by python3 changes
  Introduced in fdf99b1f3674dada7f22ca2636addb596c3294eb
* Listing available goal slots in case of specifying wrong ones
* Merge pull request `#4 <https://github.com/strands-project/executive_smach/issues/4>`_ from strands-project/groovy-devel
  merging our changes to groovy-devel into hydro-devel
* Merge pull request `#3 <https://github.com/strands-project/executive_smach/issues/3>`_ from cburbridge/chris/groovy-devel
  Thread synchronization in concurrence
* Merge pull request `#27 <https://github.com/strands-project/executive_smach/issues/27>`_ from felix-kolbe/groovy-devel
  Syntax errors, documentation improvements, Exception base class and more
* Fixing `#28 <https://github.com/strands-project/executive_smach/issues/28>`_ which was introduced by python3 changes
  Introduced in fdf99b1f3674dada7f22ca2636addb596c3294eb
* Fix syntax errors, doc typos and indentations glitches
* Merge pull request `#24 <https://github.com/strands-project/executive_smach/issues/24>`_ from SeveQ/hydro-devel
  Listing available goal slots in case of specifying wrong ones
* Merge pull request `#23 <https://github.com/strands-project/executive_smach/issues/23>`_ from bgromov/fix/monitor_state
  [MonitorState] Make exception handler more verbose
* if monitor state prempted before executing, return.
* Adding event for thread synchronization in concurrence and using event not condition in monitor state
* Listing available goal slots in case of specifying wrong ones
* [MonitorState] Make exception handler more verbose
* Merge pull request `#1 <https://github.com/strands-project/executive_smach/issues/1>`_ from BFALacerda/groovy-devel
  edited monitor state to allow input and output keys
* edited monitor state to allow input and output keys
* Contributors: BFALacerda, Boris Gromov, Bruno Lacerda, Chris Burbridge, Felix Kolbe, Hendrik Wiese, Jonathan Bohren, Marc Hanheide, Nils Berg, cburbridge

1.3.1 (2013-07-22)
------------------
* updating changelogs
* adding changelogs
* Merge pull request `#20 <https://github.com/strands-project/executive_smach/issues/20>`_ from meyerj/hydro-devel
  Missing package.xml and other catkin-generated files in binary packages
* added missing catkin_package() calls in CMakeLists.txt files of packages smach and smach_ros
* Updating maintainer name
* Contributors: Johannes Meyer, Jonathan Bohren

1.3.0 (2013-04-16)
------------------
* adding setup.py files
* adding setup.py files
* updates for simultaneous python3 and python2.7 compatibility
  updates for simultaneous python3 and python2.7 compatibility
  fixes to ensure no api changes between 2.7 and 3.x
* fixing test dep
* merging new version conflict
* Making this a hybrid buildsystem compatible with both ROS fuerte and ROS groovy
* Merge pull request `#4 <https://github.com/strands-project/executive_smach/issues/4>`_ from jbohren/groovy-devel
  fixing unit tests, adding introspection unit test
* Merge pull request `#3 <https://github.com/strands-project/executive_smach/issues/3>`_ from jbohren/master
  Fixing unit tests
* fixing unit tests, adding introspection unit test
* Merge branch 'fuerte-devel'
* fixing unit tests, adding introspection unit test
* cleaning up some other stuff in service state
* fixing service state output keys bug
* temporary fix to error spewage in action_server_wrapper due to missing feedback key in userdata
* removing patch for get/setstate.  Necessary due to genmsg refactoring
* patch to fix publishing of userdata in action server wrapper. `#5033 <https://github.com/strands-project/executive_smach/issues/5033>`_. Thanks to jbrindza
* merge
* Adding rosdoc export to smach_ros
* fix deprecated imoport of header `#4912 <https://github.com/strands-project/executive_smach/issues/4912>`_, fix package name in load_manifest
* mark doc reviewed
* api doc for smach_ros
* these packages have been api reviewed
* add description for smach_ros
* Removing bad deps
* No longer needed
* use smach messages instead of executive python messages
* import from https://code.ros.org/svn/wg-ros-pkg/branches/jbohren/executive_smach, which is the restructured code from the executive_python stack
* Contributors: Bhaskara Marthi, Jonathan Bohren, Ken Conley, Wim Meeussen, jbohren, wim
