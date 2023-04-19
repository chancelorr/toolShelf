toolshelf readme

toolshelf.py

Python library which unpacks IS2 data granules in the .h5 format
To install, find out where your python libraries are stored and put this file there

Classes:

	granule: data granule

		product: data product
		tracks: array of ground tracks, mostly to keep track of indices
			alt: height profile or photon heights
			lon/lat: locations of ATL03 photons or ATL06 points
		alts: alt indexed by track
		lons/lats: lon/lat indexed by track
(n.b., not efficient to store this info twice, but I don't know which format is more useful yet)

		

NSIDC.py

Python script to download subsetted IS2 data from NSIDC. Can readily download ATL03 (geolocated photons) or ATL06 (land ice height) data products, subsetted by date and bounding polygon



polygon.sh

Shell script to 