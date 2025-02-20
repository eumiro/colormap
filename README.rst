#############################
COLORMAP documentation
#############################


Please see : http://colormap.readthedocs.io/ for an up-to-date documentation.

.. image:: https://badge.fury.io/py/colormap.svg
    :target: https://pypi.python.org/pypi/colormap

.. image:: https://github.com/cokelaer/colormap/actions/workflows/ci.yml/badge.svg?branch=master
    :target: https://github.com/cokelaer/colormap/actions/workflows/ci.yml

.. image:: https://coveralls.io/repos/cokelaer/colormap/badge.png?branch=master
    :target: https://coveralls.io/r/cokelaer/colormap?branch=master


:version: Python 3.7, 3.8, 3.9, 3.10
:contributions: Please join https://github.com/cokelaer/colormap
:issues: Please use https://github.com/cokelaer/colormap/issues
:notebook: Please see https://github.com/cokelaer/colormap/tree/master/notebooks



What is it ?
################

**colormap** package provides simple utilities to convert colors between
RGB, HEX, HLS, HUV and a class to easily build colormaps for matplotlib. All
matplotlib colormaps and some R colormaps are available altogether. The
plot_colormap method (see below) is handy to quickly pick up a colormaps and
the test_colormap is useful to see test a new colormap.


Installation
###################

::

    pip install colormap

Example
##########

* Create your own colormap from red to green colors with intermediate color as
  whitish (diverging map from red to green)::

      c = Colormap()
      mycmap = c.cmap( {'red':[1,1,0], 'green':[0,1,.39], 'blue':[0,1,0]})
      cmap = c.test_colormap(mycmap)

* Even simpler if the colormap is linear::

      c = Colormap()
      mycmap = c.cmap_linear('red', 'white', 'green(w3c)')
      cmap = c.test_colormap(mycmap)

.. image:: http://colormap.readthedocs.io/en/latest/_images/index-1.png
    :width: 50%
    :align: center

* check out the available colormaps::

      c = Colormap()
      c.plot_colormap('diverging')

.. image:: http://colormap.readthedocs.io/en/latest/_images/colormaps.png
    :width: 50%
    :align: center

See online documentation for details: http://colormap.readthedocs.io/

changelog
#########

========= ================================================================================
Version   Description
========= ================================================================================
1.0.5     * remove Python3.6 and added Python3.10 to CI action
          * Fix issue in setup reported in https://github.com/cokelaer/colormap/pull/14
          * add requirements in MANIFEST
          * applied black on all files
========= ================================================================================
