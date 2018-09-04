^^^^^^^^^^^^^^^^^^^^^^^^^^^
Changelog for package smach
^^^^^^^^^^^^^^^^^^^^^^^^^^^

3.0.0 (2018-09-04)
------------------
* changed maintainer for local version
* Merge pull request `#5 <https://github.com/strands-project/executive_smach/issues/5>`_ from ros/indigo-devel
  Import upstream
* Merge pull request `#59 <https://github.com/strands-project/executive_smach/issues/59>`_ from josephcoombe/patch-2
  Update state.py Docstrings' @type descriptions
* Update state.py
  Change array -> list
  Change string -> str
* Merge pull request `#56 <https://github.com/strands-project/executive_smach/issues/56>`_ from cclauss/remove-set_shutdown_cb
  Typo set_shutdown_cb() --> set_shutdown_check()
* Typo set_shutdown_cb() --> set_shutdown_check()
* 2.0.1
* changelog 2.0.1
* Merge pull request `#48 <https://github.com/strands-project/executive_smach/issues/48>`_ from 130s/i/update_ci4
  [indigo-devel] Sync to master branch. Update CI conf to enable ROS IJKL
* [package.xml] Update maintainer.
* Contributors: Isaac I.Y. Saito, Joseph Coombe, Marc Hanheide, Nick Hawes, cclauss

2.0.1 (2015-04-27)
------------------
* updated changelogs
* Add timeout on termination child states.
  This is to handle cases where child states refuse to terminate. Providing a timeout value allows the concurrence to return that long after a termination event (preempt or child completion) has happened. If the argument is ommitted from the init method then the default behaviour (no timeout) is used.
* Added check for immediate preemption to Concurrence.
  This is necessary because a prior state may have failed to honour a preempt and thus it could be passed to us.
* 2.0.0
* Updating changelogs
* Merging changes, resolving conflicts, from strands-project (@cburbridge)
* cleaning up and removing rosbuild support
* merging groovy and hydro
* Merge pull request `#4 <https://github.com/strands-project/executive_smach/issues/4>`_ from strands-project/groovy-devel
  merging our changes to groovy-devel into hydro-devel
* Merge pull request `#3 <https://github.com/strands-project/executive_smach/issues/3>`_ from cburbridge/chris/groovy-devel
  Thread synchronization in concurrence
* Merge pull request `#27 <https://github.com/strands-project/executive_smach/issues/27>`_ from felix-kolbe/groovy-devel
  Syntax errors, documentation improvements, Exception base class and more
* Fix get_internal_edges returning list of tuples, not list of lists
* Remove old methods set_userdata
* Remove superfluous parent class declaration 'UserData' from 'Remapper'
* Add local error base class 'SmachError', extending Exception
* Fix syntax errors, doc typos and indentations glitches
* Merge pull request `#26 <https://github.com/strands-project/executive_smach/issues/26>`_ from orzechow/groovy-devel
  Fixed invalid exception type in concurrence.py
* Fixed invalid exception type in concurrence.py
* Checking threads have fully terminated before cleanup of outcomes dict
  This commit uses thread.isAlive() on each concurrent state runner to check for termination of all the threads before continuing. This is necessary as only checking that the outcome has been filled in does not mean the thread has completed; if the thread has not completed it may not yet have called the termination callback. If this loop exits before the termination callback of the last thread is called, then the callback will occasionally be sent an empty dictionary (when the main thread has got to line 305).
* cope with missed state termination notifications
  Concurrent states could terminate and notify _ready_event without the concurrence container realising, as it could be busy checking the outcome values. This makes the concurrency container get stuck on line 250. This commit adds a timeout to the wait to safely cope with missing notifications.
* Adding event for thread synchronization in concurrence and using event not condition in monitor state
* Contributors: Chris Burbridge, Felix Kolbe, Jonathan Bohren, Marc Hanheide, Nick Hawes, Piotr Orzechowski, cburbridge

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
* Merge pull request `#17 <https://github.com/strands-project/executive_smach/issues/17>`_ from jihoonl/patch-1
  correcting get_active_states()
* correcting get_active_states()
  It was missing 'for k' in the get_active_states.
  ```
  Traceback (most recent call last):
  File "/home/dwlee/rocon_ws/src/rocon_taskcoordinator/task_master/task_manager/scripts/cafe_manager.py", line 863, in <module>
  main()
  File "/home/dwlee/rocon_ws/src/rocon_taskcoordinator/task_master/task_manager/scripts/cafe_manager.py", line 850, in main
  sis.start()
  File "/home/dwlee/rocon_ws/src/executive_smach/smach_ros/src/smach_ros/introspection.py", line 274, in start
  self.construct(self._server_name, self._state, self._path)
  File "/home/dwlee/rocon_ws/src/executive_smach/smach_ros/src/smach_ros/introspection.py", line 295, in construct
  proxy._publish_status("Initial state")
  File "/home/dwlee/rocon_ws/src/executive_smach/smach_ros/src/smach_ros/introspection.py", line 220, in _publish_status
  self._container.get_active_states(),
  File "/home/dwlee/rocon_ws/src/executive_smach/smach/src/smach/concurrence.py", line 376, in get_active_states
  return [label for (label,outcome) in ((k,self._child_outcomes[k]) in self._child_outcomes) if outcome is None]
  NameError: global name 'k' is not defined
  ```
* adding setup.py files
* adding setup.py files
* updates for simultaneous python3 and python2.7 compatibility
  updates for simultaneous python3 and python2.7 compatibility
  fixes to ensure no api changes between 2.7 and 3.x
* merging new version conflict
* Making this a hybrid buildsystem compatible with both ROS fuerte and ROS groovy
* UserData remapper was calling a nonexistant function (typo)
* UserData remapper was calling a nonexistant function (typo)
* fix for double-preemption by miguelprada. `#5191 <https://github.com/strands-project/executive_smach/issues/5191>`_
* merge
* remove import roslib from util.py
* mark doc reviewed
* Renamed smach's logging module to log. `#4403 <https://github.com/strands-project/executive_smach/issues/4403>`_
* Fix logdebug message. Ticket 4343
* these packages have been api reviewed
* add description for smach
* import from https://code.ros.org/svn/wg-ros-pkg/branches/jbohren/executive_smach, which is the restructured code from the executive_python stack
* Contributors: Jihoon Lee, Jonathan Bohren, Wim Meeussen, blaise, wim
