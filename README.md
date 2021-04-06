# DICOM WG-26 WSI Annotation Hackathon

A virtual [Hackathon](https://en.wikipedia.org/wiki/Hackathon) for collaborative development and testing of software for the generation, exchange, and use of whole slide image (WSI) annotations in DICOM SR, SEG or Sup 222 format, in which anyone (vendors, academics and individuals) can participate freely and openly.

The event will be held virtually over the internet and coordinated via this repository.
It will start May 1st 2021 and end with a grand finale at the [European Congress on Digital Pathology (ECDP)](https://www.ecdp2021.org/) June 15th-18th, 2021.
There will be opportunities at the ECDP conference to demo software and present results to an international audience of experts in digital and computational pathology.


## Background and motivation

Over the last years, DICOM Working Group 26 Pathology (WG-26) held several Connectathons to test interoperability between whole slide image (WSI) acquisition, management, and display systems from different vendors.
The Connectathons were focused on the exchange and display of DICOM VL Whole Slide Microscopy Image data sets over network using DICOM RESTful Web Services.
These events have been instrumental in evaluating the practicability of the standard and in demonstrating its ability to enable interoperability between different whole slide imaging systems.
DICOM WG-26 now considers these parts of the standard mature for production use and will work closely with the Integrating the Healthcare Enterprise (IHE) Pathology and Laboratory Medicine (PaLM) domain to evaluate the interoperability between whole slide imaging and laboratory information systems as part of the [Digital Pathology Workflow - Image Acquisition (DPIA)](https://www.ihe.net/uploadedFiles/Documents/PaLM/IHE_PaLM_Suppl_DPIA.pdf).

DICOM WG-26 itself will direct its attention to the standardization of image annotations and analysis results in the context of artificial intelligence (AI) and machine learning (ML).
To this end, it has formed the WSI Annotation Ad-Hoc Group (AHG), which is tasked with overseeing these standard development efforts.
With rapid technological developments in AI/ML, the AHG has recognized the need to speed up the standard development lifecycle to enable standard-based image analysis workflows.
For participation at Connectathons, vendors are expected to provide a standard-compliant prototype or product, which requires significant upfront software development efforts and thereby places a high bar for participation.
In turn, vendors expect the standard to be mature enough for implementation to justify development investments.
To streamline the standard development process and to encourage early trial implementation and testing, the AHG proposes to take a more agile development approach by hosting Hackathon events.
The goal of Hackathons is to establish a proof of concept through experimentation and development in the pre-competitive space, and to attract additional stakeholders from academia and government to inform and guide the standard and product development process.
The Hackathon is intended for the practical evaluation of existing standard mechanisms as well as new proposed mechanisms that may be introduced to the standard.


## Scope

The first Hackathon will be focused on the standardization of WSI region of interest (ROI) annotations as raster graphics (segmentation bitmaps) or vector graphics (geometric contours defined by spatial coordinates) as well as measurements or qualitative evaluations derived thereof.

### Modalities, Information Entities, and Information Object Definitions

Encoding of user-drawn or machine-generated annotations derived from [VL Whole Slide Microscopy Image](http://dicom.nema.org/medical/dicom/current/output/chtml/part03/sect_A.32.8.html) instances using one of the following Information Object Definitions (IODs) defined in Part 3 of the DICOM standard:

- Structured Report (SR) documents:
    * [Comprehensive SR](http://dicom.nema.org/medical/dicom/current/output/chtml/part03/sect_A.35.3.html)
    * [Comprehensive 3D SR](http://dicom.nema.org/medical/dicom/current/output/chtml/part03/sect_A.35.13.html)
- Segmentation (SEG) images:
    * [Segmentation](http://dicom.nema.org/medical/dicom/current/output/chtml/part03/sect_A.51.html)

In addition, encoding of bulk annotations in Annotation (ANN) instances as proposed via [Supplement 222](ftp://medical.nema.org/MEDICAL/Dicom/Supps/LB/sup222_lb_WSIAnnotations.pdf).

### Services

Communication of annotations over network using the following [RESTful Web Services](http://dicom.nema.org/medical/dicom/current/output/chtml/part18/chapter_7.html#sect_7.1.2) defined in Part 18 of the DICOM standard:

- [Store transaction](http://dicom.nema.org/medical/dicom/current/output/chtml/part18/sect_10.5.html) (STOW-RS)
- [Search transaction](http://dicom.nema.org/medical/dicom/current/output/chtml/part18/sect_10.6.html) (QIDO-RS)
- [Retrieve transaction](http://dicom.nema.org/medical/dicom/current/output/chtml/part18/sect_10.4.html) (WADO-RS)

### Actors and use cases

- Image management systems
    * Storage, query and retrieval of annotations via RESTful Web Services
- Image display systems
    * Drawing of annotations
    * Visualization of annotations
- Image analysis systems
    * Reading and parsing of annotations for model training
    * Creation of annotations upon model inference
- Legacy conversion systems
    * Transformation of annotations from proprietary format into standard DICOM format


## FAQs

### Who can participate?

The event is open to any party interested in collaborative software development in the field of digital and computational pathology.
We encourage participation of different stakeholder groups from academia, government, and industry.

### What's in it for me?

A subset of projects will be selected for presentation at the final session at the ECDP conference and awarded a prize.
In addition, participants will be invited to become coauthors of a summary report publication.

### What will I need to bring?

All you need is a computer and an internet connection.

### What will be provided?

Data sets:

- DICOM Slide Microscopy (SM) images
- DICOM Segmentation (SEG) images
- DICOM Structured Report (SR) documents

Information technology resources:

- Image management systems with DICOMweb interface for data storage, query, and retrieval
- Limited number of cloud virtual machine (VM) instances for hosting Jupyter notebooks, web-based viewers, or image management systems.

### Are there any costs?

Participation in the Hackathon is free of charge; you and other participants will learn from your efforts and advance the work of annotations in the field of whole slide imaging.
There will be a summary session at ECDP 2021 with more details to be provided.
You are not required to participate in the summary session to take part in the Hackathon.
Participation in the summary session does require registration for ECDP 2021 and the associated costs.

### Where can I sign up?

There is no official registration process.
If you would like to participate in the Hackathon, you can either propose a new project by creating a pull request using the "Project proposal" template ([link](https://github.com/DICOMWG26AnnotationAHG/hackathon/issues/new?assignees=&labels=&template=project-proposal-template.md&title=%5BPROJECT%5D)) or join one of the existing projects.
You can search for proposed projects under the `Pull requests` tab ([link](https://github.com/DICOMWG26AnnotationAHG/hackathon/labels/project%20proposal)).
If you like a particular project, upvote the pull request using the 👍️ emoji.

While there is in principle no restriction on the number of participants per project or the total number of projects, we have only a limited number of meetup areas at the final at the ECDP conference.
Therefore, a subset of projects will be selected by the DICOM WG-26 AHG for presentation at ECDP.
Selection criteria will include standard conformance, clinical relevance, popularity, and status of the project.

### What should I work on?

The world is your oyster!
What you work on during the event is entirely up to you, as long as it is related to WSI annotations in DICOM format.
While we realize that great software solutions exists for handling annotations in proprietary formats, this event is driven by and focused on the use and further development of the DICOM standard.

### How can I ask questions or get help?

Start a discussion under the `Discussions` tab ([link](https://github.com/DICOMWG26AnnotationAHG/hackathon/discussions)).


## Disclaimers

We abide by the [DICOM anti-trust rules](ftp://medical.nema.org/medical/Dicom/Geninfo/AntitrustRules.docx).

### Data privacy

Participants shall respect patient privacy and all materials used in the Hackathon, whether provided by the organizers or the participants, shall be free of any Individually Identifiable Information.
In particular, all DICOM data sets shall either contain dummy data or be fully de-identified in compliance with the [Application Level Confidentiality Profile](http://dicom.nema.org/medical/dicom/current/output/chtml/part15/chapter_E.html) defined in Part 15 of the DICOM standard.
It is the responsibility of participants to comply with patient privacy rules and regulations under US and EU law.


## Data use

Any data participants contribute to the Hackathon (e.g., store in one of the provided image management systems) shall be made available to anyone under the [CCO](https://creativecommons.org/share-your-work/public-domain/cc0/) license.
The data will subsequently be available to anyone for free and can be reused without restrictions, including for commercial purposes.

Software used by participants during the Hackathon (display systems, analysis systems, etc.) may be open source or close source.
Participants are **not** obligated to provide access to software or underlying source code.


## Supporters

- Computational Pathology, Massachusetts General Hospital
- Digital Pathology Association (DPA)
- European Society of Digital and Integrative Pathology (ESDIP)
- Alliance for Digital Pathology
- Neagen
- J4Care
- Google Cloud Healthcare
