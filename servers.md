# Origin servers

Each origin server exposes a [DICOMweb](https://www.dicomstandard.org/dicomweb/) RESTful application programming interface (API) and provides the search (QIDO-RS), retrieve (WADO-RS), and store (STOW-RS) transactions of the [Studies Service](http://dicom.nema.org/medical/dicom/current/output/chtml/part18/chapter_10.html).

## Google Cloud Healthcare API

The [Google Cloud Healthcare API](https://cloud.google.com/healthcare) generally requires users to authenticate and authorize an application to access the data stored in a DICOM store via the DICOMweb RESTful API.
To enable public access during the Hackathon event, we set up a reverse proxy server in front of the DICOM store in an [Imaging Data Commons (IDC) cloud environment](https://learn.canceridc.dev/).

### DICOMweb Studies Service Base URI

```none
https://idc-external-006.uc.r.appspot.com
```

### DICOM conformance statement

https://cloud.google.com/healthcare/docs/dicom
