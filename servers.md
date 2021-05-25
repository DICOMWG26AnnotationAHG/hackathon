# Origin servers

Each origin server exposes a [DICOMweb](https://www.dicomstandard.org/dicomweb/) RESTful application programming interface (API) and provides the search (QIDO-RS), retrieve (WADO-RS), and store (STOW-RS) transactions of the [Studies Service](http://dicom.nema.org/medical/dicom/current/output/chtml/part18/chapter_10.html).

## J4Care DCM4CHE

The [J4Care DCM4CHE](https://www.j4care.com/) archive.

### DICOMweb Studies Service Base URI

```none
https://test.j4care.com:8443/dcm4chee-arc/aets/DCM4CHEE/rs
```

### DICOM conformance statement

https://www.j4care.com/sites/default/files/2017-02/j4care-cs.pdf

## Neagen neaLink

The [Neagen neaLink](http://www.neagen.com/digital-pathology.php) archive

### DICOMweb Studies Service Base URI

```none
https://cloud.neagen.com/ilp
```

Note that this origin server exposes each of the transactions of the DICOMweb Studies Service at a different path prefix:

* Search transaction (QIDO-RS): https://cloud.neagen.com/ilp/qrs
* Retrieve transaction (WADO-RS): https://cloud.neagen.com/ilp/wrs
* Store transaction (STOW-RS): https://cloud.neagen.com/ilp/stowrs

### DICOM conformance statement


## Google Cloud Healthcare API

The [Google Cloud Healthcare API](https://cloud.google.com/healthcare) generally requires users to authenticate and authorize an application to access the data stored in a DICOM store via the DICOMweb RESTful API.
To enable public access during the Hackathon event, we set up a reverse proxy server in front of the DICOMweb API in an [Imaging Data Commons (IDC) cloud environment](https://learn.canceridc.dev/).

### DICOMweb Studies Service Base URI

```none
https://idc-external-006.uc.r.appspot.com
```

### DICOM conformance statement

https://cloud.google.com/healthcare/docs/dicom
