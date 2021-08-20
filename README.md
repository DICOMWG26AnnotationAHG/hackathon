# DICOM WG-26 WSI Annotation Hackathon

A virtual [Hackathon](https://en.wikipedia.org/wiki/Hackathon) for collaborative development and testing of software for the generation, exchange, and use of whole slide image (WSI) annotations in DICOM SEG, ANN, or SR format, in which anyone (vendors, academics, and individuals) can participate freely and openly.


## Venue

The event will be held virtually over the internet from Monday, September 27, 2021 to Friday, October 15, 2021.
Interoperability demonstrations will be conducted between Monday, October 11, 2021 and Friday, October 15, 2021 (exact dates and times will be scheduled with participants via email after registration).
A working prototype should be available by Monday, October 11, 2021 to allow for interoperability demonstrations to start on time.
A final summary session and panel discussion will take place live at the [Pathology Visions 2021](https://digitalpathologyassociation.org/pathology-visions-conference) conference in Las Vegas on Tuesday, October 19, 2021 9:45-10:30 AM PDT.


## Registration

If you would like to participate in the Hackathon, please fill out and submit [this form](https://docs.google.com/forms/d/e/1FAIpQLSclKQmFd8_LWazuvbO6B_N4eMoOZekV6XSX6GXQ7T-EP0TuNw/viewform?usp=sf_link) before Monday, September 24, 2021.


## Background and motivation

Over the last years, DICOM Working Group 26 Pathology (WG-26) held several [Digital Pathology Connectathons](http://dicom.nema.org/dicom/dicomwsi/Connectathon/index.html) to test interoperability between whole slide image (WSI) acquisition, management, and display systems from different vendors.
The Connectathons were focused on the exchange and display of DICOM VL Whole Slide Microscopy Image data sets over network using [DICOMweb RESTful services](https://www.dicomstandard.org/dicomweb/).
These events have been instrumental in evaluating the practicability of the standard and in demonstrating its ability to enable interoperability between different whole slide imaging systems.
DICOM WG-26 now considers these parts of the standard mature for production use and will work closely with the Integrating the Healthcare Enterprise (IHE) Pathology and Laboratory Medicine (PaLM) domain to evaluate the interoperability between whole slide imaging and laboratory information systems as part of the [Digital Pathology Workflow - Image Acquisition (DPIA)](https://www.ihe.net/uploadedFiles/Documents/PaLM/IHE_PaLM_Suppl_DPIA.pdf).

DICOM WG-26 itself has directed its attention to the standardization of image annotations and analysis results in the context of artificial intelligence (AI) and machine learning (ML).
To this end, it has formed the WSI Annotation Ad-Hoc Group (AHG), which is tasked with overseeing these standard development efforts.
With rapid technological developments in AI/ML, the AHG has recognized the need to speed up the standard development lifecycle to enable standard-based image analysis workflows.
For participation at Connectathons, vendors are expected to provide a standard-compliant prototype or product, which requires significant upfront software development efforts and thereby places a high bar for participation.
In turn, vendors expect the standard to be mature enough for implementation to justify development investments.
To streamline the standard development process and to encourage early trial implementation and testing, the AHG has decided to take a more agile development approach by hosting Hackathon events.
The goal of Hackathons is to establish a proof of concept through experimentation and development in the pre-competitive space, and to attract additional stakeholders from academia and government to inform and guide the standard and product development process.
The Hackathon is intended for the practical evaluation of standard mechanisms for the communication of slide microscopy image annotations between different digital pathology systems, including image display, management, and analysis systems.

## Scope

The Hackathon will be focused on the communication of WSI region of interest (ROI) annotations as raster graphics (segmentation bitmaps) or vector graphics (geometric contours defined by spatial coordinates) as well as measurements or qualitative evaluations derived thereof between image display, management, and analysis systems.

### Systems

For the Hackathon, we consider two types of systems:

- **Image display systems**: Slide microscopy image viewers with annotation capabilities that enable users to draw and review annotations.
- **Image analysis systems**: ML models in training or evaluation mode that either use annotations as ground truth labels for supervised learning during model training or generate annotations during model inference, respectively.

Each system may take on the role of an annotation producer or consumer:

 - **Producer**: Creates annotations for a given image.
 - **Consumer**: Parses and interprets annotations together with the corresponding source image.

### Use cases

The Hackathon focuses on the following two computational pathology use cases:

- ML model **development**: Annotations are manually drawn by a pathologist via an image display system and processed by an image analysis system to be used as labels for model training.
- ML model **deployment**: Annotations are automatically generated by an image analysis system upon model inference and visualized via an image display system for review by a pathologist.

![Systems and intersystem communication of images and image annotations](etc/interoperability.png)


## FAQs

### Who can participate?

The event is open to any party interested in collaborative software development in the field of digital and computational pathology.
We encourage participation of different stakeholder groups from academia, government, and industry.

### What will I need to bring?

All you need is a computer and an internet connection.

### What will be provided?

#### Data sets

For an overview of available DICOM studies containing DICOM VL Whole Slide Microscopy Image instances, please refer to the [data.md](data.md) document.

#### Services

For an overview of available DICOMweb origin servers, please refer to the [servers.md](servers.md) document.

### Are there any costs?

Participation in the Hackathon is free of charge.
There will be a panel discussion at the Path Visions 2021 conference, but you are not required to register for the conference to take part in the Hackathon.


### Required system capabilities

- **Image display system** (viewer)
    * **Producer** (drawing):
        + Manual drawing of annotations on images by a person via a graphical user interface
        + Storage of annotations over network
    * **Consumer** (review):
        + Query and retrieval of annotations over network
        + Visualization of annotations on corresponding source images via graphical user interface

- **Image analysis system** (ML model)
    * **Producer** (inference):
        + Automatic generation of annotations for a given image by an algorithm
        + Storage of annotations over network
    * **Consumer** (training):
        + Retrieval of annotations over network
        + Parsing and interpretation of annotations

### Modalities and Information Object Definitions

Encoding of user-drawn or machine-generated annotations derived from [VL Whole Slide Microscopy Image](http://dicom.nema.org/medical/dicom/current/output/chtml/part03/sect_A.32.8.html) instances using one of the following Information Object Definitions (IODs) defined in Part 3 of the DICOM standard:

- Segmentation (SEG) images:
    * [Segmentation](http://dicom.nema.org/medical/dicom/current/output/chtml/part03/sect_A.51.html)
- Annotation (ANN) instances:
    * [Microscopy Bulk Simple Annotations](http://dicom.nema.org/medical/dicom/current/output/chtml/part03/sect_A.87.html)
- Structured Report (SR) documents (using template [TID 1500 "Measurement Report"](http://dicom.nema.org/medical/dicom/current/output/chtml/part16/chapter_A.html#sect_TID_1500)):
    * [Comprehensive SR](http://dicom.nema.org/medical/dicom/current/output/chtml/part03/sect_A.35.3.html) with image regions encoded as Spatial Coordinates (SCOORD)
    * [Comprehensive 3D SR](http://dicom.nema.org/medical/dicom/current/output/chtml/part03/sect_A.35.13.html) with image regions encoded as 3D Spatial Coordinates (SCOORD3D)

#### Regions of Interest

Each region of interest (ROI) annotation shall consist of graphic data (raster graphic in case of SEG or vector graphic in case of ANN and SR) that spatially define the annotated image region and descriptive metadata that semantically define the annotated concept.

- **SEG**:
    * **Graphic data** (raster): Attribute ``Pixel Data`` of the [Image Pixel Module](http://dicom.nema.org/medical/dicom/current/output/chtml/part03/sect_C.7.6.3.html)
    * **Descriptive metadata**: Attribute ``Segmented Property Type Code Sequence`` of the [Segmentation Image Module](http://dicom.nema.org/medical/dicom/current/output/chtml/part03/sect_C.8.20.2.html)

- **ANN**:
    * **Graphic data** (vector): Attribute ``Point Coordinates Data`` or ``Double Point Coordinates Data`` of the [Microscopy Bulk Simple Annotations Module](http://dicom.nema.org/medical/dicom/current/output/chtml/part03/sect_C.37.html#sect_C.37.1.2)
    * **Descriptive metadata**: Attribute ``Annotation Property Type Code Sequence`` of the [Microscopy Bulk Simple Annotations Module](http://dicom.nema.org/medical/dicom/current/output/chtml/part03/sect_C.37.html#sect_C.37.1.2).

- **SR** (using template [TID 1410 "Planar ROI Measurements and Qualitative Evaluations"](http://dicom.nema.org/medical/dicom/current/output/chtml/part16/chapter_A.html#sect_TID_1410)):
    * **Graphic data** (vector): Attribute ``Graphic Data`` of the [Spatial Coordinates Macro](http://dicom.nema.org/medical/dicom/current/output/chtml/part03/sect_C.18.6.html) or [3D Spatial Coordinates Macro](http://dicom.nema.org/medical/dicom/current/output/chtml/part03/sect_C.18.9.html) using SR Content Item with name ``(111030, DCM, "Image Region")`` and value type ``SCOORD`` or ``SCOORD3D``, respectively
    * **Descriptive metadata**: Attribute ``Concept Code Sequence`` of the [Content Item Macro](http://dicom.nema.org/medical/dicom/current/output/chtml/part03/sect_10.2.html) using SR Content Item with name ``(121071, DCM, "Finding")`` and value type ``CODE``


#### Coded Concepts

The descriptive metadata represent [coded entry data](http://dicom.nema.org/medical/dicom/current/output/chtml/part03/chapter_8.html) and they are encoded using Code Sequence atttributes of the [Code Sequence Macro](http://dicom.nema.org/medical/dicom/current/output/chtml/part03/sect_8.8.html).
As part of the Hackathon, participants shall use [coding scheme](http://dicom.nema.org/medical/dicom/current/output/chtml/part16/chapter_8.html#para_9cada316-7eaa-4bc6-9fe4-bac5852564f9) ``SCT`` ([SNOMED CT](https://www.snomed.org/)) for coding.

The value of attributes ``Segmented Property Category Code Sequence`` and ``Annotation Property Category Code Sequence`` (in case of SEG and ANN) shall be ``(91723000, SCT, "Anatomical structure")`` from context group [CID 7150 "Segmentation Property Categories"](http://dicom.nema.org/medical/dicom/current/output/chtml/part16/sect_CID_7150.html).

The value of attributes ``Segmented Property Type Code Sequence`` and ``Annotation Property Type Code Sequence`` (in case of SEG and ANN) as well as of attribute ``Concept Code Sequence`` of SR Content Item with concept name ``(121071, DCM, "Finding")`` (in case of SR) shall be children of one of the following concepts:

- ``(85756007, SCT, "Body tissue structure")`` (see [SNOMED browser](https://browser.ihtsdotools.org/?perspective=full&conceptId1=85756007&edition=MAIN/2021-07-31&release=&languages=en))
- ``(4421005, SCT, "Cell structure")`` (see [SNOMED browser](https://browser.ihtsdotools.org/?perspective=full&conceptId1=4421005&edition=MAIN/2021-07-31&release=&languages=en))
- ``(122453002, SCT, "Intercellular anatomical structure")`` (see [SNOMED browser](https://browser.ihtsdotools.org/?perspective=full&conceptId1=122453002&edition=MAIN/2021-07-31&release=&languages=en))

Note that these concepts are not (yet) part of context group [CID 7192 "Anatomical Structure Segmentation Property Types"](http://dicom.nema.org/medical/dicom/current/output/chtml/part16/sect_CID_7192.html), which currently lacks codes for microanatomic regions relevant in the context of digital pathology.
A goal of the Hackathon is to identify relevant codes for inclusion into the context group.

### Services

Communication of annotations over network using the following [DICOMweb RESTful Web Services](http://dicom.nema.org/medical/dicom/current/output/chtml/part18/chapter_7.html#sect_7.1.2) defined in Part 18 of the DICOM standard:

- [Store transaction](http://dicom.nema.org/medical/dicom/current/output/chtml/part18/sect_10.5.html) (STOW-RS)
- [Search transaction](http://dicom.nema.org/medical/dicom/current/output/chtml/part18/sect_10.6.html) (QIDO-RS)
- [Retrieve transaction](http://dicom.nema.org/medical/dicom/current/output/chtml/part18/sect_10.4.html) (WADO-RS)


## Evaluation

Interoperability of a participant's software will be reviewed by a panel of experts (members of DICOM WG-26) with experience in DICOM and digital pathology based on live demonstration of the software.
Participants are expected to demonstrate the capabilities described above for a set of provided SM instances during a video conference via screen sharing.
Please note, however, that participants are **not** expected to provide or share the actual software and do **not** have to reveal any implementation details.
The focus of the Hackathon is on establishing interoperability with other systems based on the DICOM standard.

### Producer

Reviewers will assess the SEG, ANN, or SR instances generated by the system and test whether they can be parsed and interpreted by established open-source DICOM software tools.
Further, reviewers will determine whether the annotations reference the corresponding source SM images and whether annotations and images can be correctly overlaid.

### Consumer

Reviewers will assess whether the system can parse and interpret a curated set of SEG, ANN, and SR instances.
In addition, reviewers will ask participants to demonstrate whether the system can parse and interpret any SEG, ANN, or SR instances generated by participating producers.

#### Image Display System

Participants are expected to demo the capabilities of the system via a graphical user interface.
Reviewers will assess whether both the graphic data as well as the descriptive metadata are correctly displayed.

#### Image Analysis System

Participants may demo the capabilities of the system via a graphical user interface, a command line interface, or an application programming interface.
For example, participants may execute a program via the command line and the system may print the graphic data and descriptive metadata to the standard output stream or write the information to a log file.


## Disclaimers

We abide by the [DICOM anti-trust rules](ftp://medical.nema.org/medical/Dicom/Geninfo/AntitrustRules.docx).

### Data privacy

Participants shall respect patient privacy and all materials used in the Hackathon, whether provided by the organizers or the participants, shall be free of any Individually Identifiable Information.
In particular, all DICOM data sets shall either contain dummy data or be fully de-identified in compliance with the [Application Level Confidentiality Profile](http://dicom.nema.org/medical/dicom/current/output/chtml/part15/chapter_E.html) defined in Part 15 of the DICOM standard.
It is the responsibility of participants to comply with patient privacy rules and regulations under US and EU law.


## Data use

Any data participants contribute to the Hackathon (e.g., store in one of the provided image management systems) shall be made available to anyone under the [CCO](https://creativecommons.org/share-your-work/public-domain/cc0/) license.
The data will subsequently be available to anyone for free and can be reused without restrictions, including for commercial purposes.

Software used by participants during the Hackathon (image display and analysis systems) may be open source or close source.
Participants are **not** obligated to provide access to software or underlying source code.


## Supporters

- Computational Pathology, Massachusetts General Hospital (MGH)
- Digital Pathology Association (DPA)
- European Society of Digital and Integrative Pathology (ESDIP)
- National Cancer Institute (NCI) Imaging Data Commons (IDC)
- Alliance for Digital Pathology
- Neagen
- J4Care
- Google Cloud Healthcare & Life Sciences
