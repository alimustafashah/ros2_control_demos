==================
ros2_control Demos
==================

============
Installation
============

You can install the latest relase via pip:

   .. code-block:: shell

      pip install hal-cgp


This library depends on some optional packages defined in `extra_requirements.txt`. These are necessary, for example, to compile an individual to a SymPy expression or a PyTorch class. You can install the extra requirements for full functionality of the library via:

   .. code-block:: shell

      pip install hal-cgp[extra]

You can also install individual extra requirements by specifying the package name (without version number) in square brackets, e.g., to install the `torch` dependency:

   .. code-block:: shell

      pip install hal-cgp[torch]


   .. code-block:: shell
   
      This repository provides templates for the development of ros2_control-enabled robots and a simple simulations to demonstrate and prove ros2_control concepts.

.. image:: https://github.com/ros-controls/ros2_control_demos/workflows/CI/badge.svg?branch=master
           :target: https://github.com/ros-controls/ros2_control_demos/actions?query=workflow%3ACI
.. image:: https://github.com/ros-controls/ros2_control_demos/workflows/Linters/badge.svg?branch=master
           :target: https://github.com/ros-controls/ros2_control_demos/actions?query=workflow%3ALinters
.. image:: https://github.com/ros-controls/ros2_control_demos/workflows/Coverage/badge.svg?branch=master
           :target: https://github.com/ros-controls/ros2_control_demos/actions?query=workflow%3ACoverage
.. image:: https://img.shields.io/badge/License-Apache%202.0-blue.svg
           :target: https://opensource.org/licenses/Apache-2.0



