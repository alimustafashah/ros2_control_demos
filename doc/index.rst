==================
ros2_control Demos
==================

.. image:: https://github.com/ros-controls/ros2_control_demos/workflows/CI/badge.svg?branch=master
           :target: https://github.com/ros-controls/ros2_control_demos/actions?query=workflow%3ACI
.. image:: https://github.com/ros-controls/ros2_control_demos/workflows/Linters/badge.svg?branch=master
           :target: https://github.com/ros-controls/ros2_control_demos/actions?query=workflow%3ALinters
.. image:: https://github.com/ros-controls/ros2_control_demos/workflows/Coverage/badge.svg?branch=master
           :target: https://github.com/ros-controls/ros2_control_demos/actions?query=workflow%3ACoverage
.. image:: https://img.shields.io/badge/License-Apache%202.0-blue.svg
           :target: https://opensource.org/licenses/Apache-2.0


This repository provides templates for the development of ros2_control-enabled robots and a simple simulations to demonstrate and prove ros2_control concepts.

=====
Goals
=====

===========
Description
===========

===========
Quick Hints
===========

=================
Build from source
=================

=================================
Getting Started with ros2_control
=================================

=======================
Starting example robots
=======================


==============================
Controlles and moving hardware
==============================

======
Result
======
Independently from the controller you should see how the example's output changes. Look for the following lines

   .. code-block:: shell

           [RRBotSystemPositionOnlyHardware]: Got state 0.0 for joint 0!
           [RRBotSystemPositionOnlyHardware]: Got state 0.0 for joint 1!

If you echo the /joint_states or /dynamic_joint_states topics you should also get similar values.

   .. code-block:: shell

           ros2 topic echo /joint_states
           ros2 topic echo /dynamic_joint_states
           
You should also see the RRbot moving in rviz2.
