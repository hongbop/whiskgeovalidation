# whiskgeovalidation

This program validates the geolocation accuracy of MERSI and other whiskbroom scanners. 

The usage example is
`
..\WhiskGeolocation\bin\WhiskGeoValidation.exe ..\WhiskGeolocation\share\FY3D_MERSI2_QKM_Config.xml .\FY3D_MERSI_GBAL_L1_20220803_1230_0250M_MS.HDF .\FY3D_MERSI_GBAL_L1_20220803_1230_0250M_MS_GEO.H5
`
Three parameters are required. The first is the configure file, the second is the hdf5 file with the earth observation dataset, and the third is the hdf5 file with the geolocation field. This program would generate an EVA hdf5 file. The dataset `/Data/CKPs` contains very dense conjugate points, which could be used to validate the geolocation field.

The [WhiskGeolocation.tar.gz](https://github.com/hongbop/whiskgeovalidation/releases/tag/v0.1) has three sub-directories: bin, share, and data. The bin directory contains the exe and dlls for windows. The share directory contains the configure file, which is `FY3D_MERSI2_QKM_Config.xml`. In the configure file, the DOM and DEM need to be modified for your dataset. In our example, they are in the data directory. The `GLT` in `Rectification_Config` needs to be modified for your own dataset.

The geolocation fields are also provided as examples, which can be downloaded from release [MERSI2.tar.gz](https://github.com/hongbop/whiskgeovalidation/releases/tag/v0.1). The original image datas are required, which can be download from [NSMC](http://satellite.nsmc.org.cn/PortalSite/Data/Satellite.aspx?SatelliteCode=FY3D&SeriesCode=FY3X&InstrumentTypeCode=MERSI&currentculture=en-US).
