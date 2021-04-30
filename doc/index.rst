==================
ros2_control Demos
==================

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



========
 HAL-CGP
========


.. image:: https://badge.fury.io/py/hal-cgp.svg
    :target: https://badge.fury.io/py/hal-cgp
.. image:: https://img.shields.io/badge/python-3.6-red.svg
	   :target: https://www.python.org/downloads/release/python-369/
.. image:: https://img.shields.io/badge/python-3.7-red.svg
	   :target: https://www.python.org/
.. image:: https://img.shields.io/badge/python-3.8-red.svg
	   :target: https://www.python.org/
.. image:: https://img.shields.io/badge/License-GPLv3-blue.svg
	   :target: https://www.gnu.org/licenses/old-licenses/gpl-3.0.html
.. image:: https://github.com/Happy-Algorithms-League/hal-cgp/actions/workflows/tests.yaml/badge.svg
	   :target: https://github.com/Happy-Algorithms-League/hal-cgp/actions/workflows/tests.yaml
.. image:: http://www.mypy-lang.org/static/mypy_badge.svg
	   :target: http://mypy-lang.org/
.. image:: https://img.shields.io/badge/code%20style-black-000000.svg
	   :target: https://github.com/psf/black
.. image:: https://coveralls.io/repos/github/Happy-Algorithms-League/python-gp/badge.svg?branch=master
	   :target: https://coveralls.io/github/Happy-Algorithms-League/python-gp?branch=master
.. image:: https://readthedocs.org/projects/ansicolortags/badge/?version=latest
	   :target: https://happy-algorithms-league.github.io/hal-cgp/

Cartesian genetic programming (CGP) in pure Python.

hal-cgp is an extensible pure Python library implementing Cartesian genetic programming to represent, mutate and evaluate populations of individuals encoding symbolic expressions targeting applications with computationally expensive fitness evaluations. It supports the translation from a CGP genotype, a two-dimensional Cartesian graph, into the corresponding phenotype, a computational graph implementing a particular mathematical expression. These computational graphs can be
exported as pure Python functions, NumPy-compatible functions (Walt et al., 2011), SymPy expressions (Meurer et al., 2017) or PyTorch modules (Paszke et al., 2019).

The library implements a mu + lambda evolution strategy (Beyer and Schwefel, 2002) to evolve a population of individuals to optimize an objective function.

Design decisions/use cases
==========================

We designed hal-cgp for optimization problems in which individual fitness evaluations are computationally expensive. The library is hence not optimized for high performance, but rather puts ease of use and extensibility first. Furthermore we take steps to reduce the number of redundant fitness evaluations, for example by avoiding reevaluating parents at the beginning of each episode and providing a convenient decorator to cache results on disk. If for your use case individual fitness evaluations are fast and the performance of the library itself becomes a relevant factor, you may want to check out https://github.com/darioizzo/dcgp or http://www.cgplibrary.co.uk/files2/About-txt.html.


.. image-start
   
.. image:: ./cgp-sketch.png
   :width: 600
   :alt: CGP Sketch
	 
Figure from Jordan, Schmidt, Senn & Petrovici, "Evolving to learn: discovering interpretable plasticity rules for spiking networks", arxiv:2005.14149_.

.. _arxiv:2005.14149: https://arxiv.org/abs/2005.14149

.. image-end

.. long-description-end

.. installation-start
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

