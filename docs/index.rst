.. toolShelf documentation master file, created by
   sphinx-quickstart on Thu Apr 20 13:34:05 2023.
   You can adapt this file completely to your liking, but it should at least
   contain the root `toctree` directive.

toolShelf documentation
=====================================

.. toctree::
   :maxdepth: 2
   :caption: Contents:

	granule

Indices and tables
==================

* :ref:`genindex`
* :ref:`modindex`
* :ref:`search`

Class Granule

=======

Classes for IS2 data granules


.. py:class:: granule(hFile, short_name)

	This class will unpack the data from a downloaded granule in .h5 format
	
	:param hFile: path to granule
	:type hFile: string
	:param short_name: data product short name (e.g., 'ATL03')
	:type short_name: string
	
	:ivar product: data product short name
	:type product: string
	:ivar tracks: available ground tracks ('gt1l', 'gt1r', 'gt2l', 'gt2r', 'gt3l', 'gt3r')
	:type tracks: list
	:ivar alt: elevation data (either profile ('ATL06') or photon cloud ('ATL03'))
	:type alt: list
	:ivar lat: data point latitudes
	:type lat: list
	:ivar lon: data point longitudes
	:type lon: list
	
	..versionadded:: 0.1.0

	..versionchanged:: 0.1.0
	
.. py:class:: gt(alt, lon, lat)
	
	Inverted class structure in which data are organized according to their ground track. A later version will likely pick one of these organizations and stick with it.

	Identical subclasses are initialized by granule for all ground tracks ('gt[1|2|3][l|r]')

	:param alt: elevation data (either profile ('ATL06') or photon cloud ('ATL03'))
	:type alt: list
	:param lat: data point latitudes
	:type lat: list
	:param lon: data point longitudes
	:type lon: list
	
