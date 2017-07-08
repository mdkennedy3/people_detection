^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
Changelog for package face_detector
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

1.0.12 (2017-07-08)
-------------------
* changelogs
* changed maintainer
* Added id to shown image (`#43 <https://github.com/lcas/people_detection/issues/43>`_)
  * added id to shown image
  * added capability to switch on/off face id display
* Update hardcoded location of opencv
  Version changed to 3.2.0, unfortunately we need to hardcode the
  location for now.
* [face_detector][test common] Use newly introduced publishtest.
  Since the publish rate of the detected face varies every second because one of the persons in the bag file is moving, [publishtest](http://wiki.ros.org/rostest/Nodes#publishtest) should suit the best in this case.
  [face_detector][test common] Enable substitution in rosparam tag.
* [test] Cleaner namespace assignment.
  [face_detector][test common] Fix warning in .launch format.
  Fix namespace in testcases.
  Increase retry. .bag-based perceptional tests are hard to deterministic, so it makes sense to do this.
  Set param use_sim_time.
  [face_detector][test] hztest can be used for measureing no publishment. hzerror is not needed in that case.
  [face_detector][test] Specify test name. Pass all args.
  [face_detector][test] pass_all_args might require all args kept out of include tag.
  [face_detector][test] Specify test-name.
  [face_detector][test] Disable all tests other than rgbd. I couldn't figure out how to use launches other than face_detector.rgbdlaunch, after hours of trial on local machine. I leave that up to someone else.
  [face_detector][test] Detection using rgbd works with this config.
  [face_detector][test] Shorter test duration (bag files are less than 7 seconds).
  [face_detector][test] Shorter test_duration. We only need a second or so as long as we can confirm the designated topic is being published.
  [face_detector][test] rosbag play with clock and loop option.
* [face_detector] an obtuse fix to hardcoded path for Xenial with OpenCV 3.1.0.
* [test] Missing dependency.
* [test] Missing dependency.
* Contributors: Alessandro Francescon, Isaac I.Y. Saito, Karl D. Hansen, Marc Hanheide

* changed maintainer
* Added id to shown image (`#43 <https://github.com/lcas/people_detection/issues/43>`_)
  * added id to shown image
  * added capability to switch on/off face id display
* Update hardcoded location of opencv
  Version changed to 3.2.0, unfortunately we need to hardcode the
  location for now.
* [face_detector][test common] Use newly introduced publishtest.
  Since the publish rate of the detected face varies every second because one of the persons in the bag file is moving, [publishtest](http://wiki.ros.org/rostest/Nodes#publishtest) should suit the best in this case.
  [face_detector][test common] Enable substitution in rosparam tag.
* [test] Cleaner namespace assignment.
  [face_detector][test common] Fix warning in .launch format.
  Fix namespace in testcases.
  Increase retry. .bag-based perceptional tests are hard to deterministic, so it makes sense to do this.
  Set param use_sim_time.
  [face_detector][test] hztest can be used for measureing no publishment. hzerror is not needed in that case.
  [face_detector][test] Specify test name. Pass all args.
  [face_detector][test] pass_all_args might require all args kept out of include tag.
  [face_detector][test] Specify test-name.
  [face_detector][test] Disable all tests other than rgbd. I couldn't figure out how to use launches other than face_detector.rgbdlaunch, after hours of trial on local machine. I leave that up to someone else.
  [face_detector][test] Detection using rgbd works with this config.
  [face_detector][test] Shorter test duration (bag files are less than 7 seconds).
  [face_detector][test] Shorter test_duration. We only need a second or so as long as we can confirm the designated topic is being published.
  [face_detector][test] rosbag play with clock and loop option.
* [face_detector] an obtuse fix to hardcoded path for Xenial with OpenCV 3.1.0.
* [test] Missing dependency.
* [test] Missing dependency.
* Contributors: Alessandro Francescon, Isaac I.Y. Saito, Karl D. Hansen, Marc Hanheide

1.0.9 (2015-09-01)
------------------
* Install missing param directory: face_detector.rgbd.launch fails due to the `param` folder.
* Contributors: Isaac I.Y. Saito

1.0.8 (2014-12-10)
------------------
* cleanup formatting with astyle (supersedes `#18 <https://github.com/wg-perception/people/issues/18>`_)
* centrally reference cascade from standalone opencv (addresses `#15 <https://github.com/wg-perception/people/issues/15>`_)
* Contributors: Dan Lazewatsky

1.0.3 (2014-03-01)
------------------
* fix message generation
* Contributors: Dan Lazewatsky

1.0.2 (2014-02-28)
------------------
* update to properly generate messages
* Contributors: Dan Lazewatsky

1.0.1 (2014-02-27)
------------------
* update some remappings to deal with the changed openni message api
* convert 16FC1 depth images to 32FC1 and scale to get meters
* switch constants to defines to get rid of linker issues for catkin switch
* catkinizing
* Contributors: Dan Lazewatsky
