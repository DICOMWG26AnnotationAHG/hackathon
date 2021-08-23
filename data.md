# Data collections

This document provides an overview of collections of DICOM data sets used for the Hackathon.
The data is available publicly at the [medical.nema.org FTP server](ftp://medical.nema.org/MEDICAL/Dicom/DataSets/WG26/).

## WG-26 Connectathons

Overview of data sets that were used at previous WG-26 Connectathons.
Note that some of the data sets have compliance issues that impeded interoperability during a Connectathon event.
These data sets were therefore not used in the Hackathon (indicated by values in column `Used`).
The remaining data sets are also not guaranteed to be fully compliant with the standard, but no compliance issues have been identified or reported so far.

Event  |  Used  |  Study Instance UID                                                |  Study Date  |  Study ID          |  Accession Number  |  Patient Name              |  Patient ID  |  Num Series  |  Num Instances
-------|--------|--------------------------------------------------------------------|--------------|--------------------|--------------------|----------------------------|--------------|--------------|---------------
PV 20 | yes | 2.16.840.1.113995.3.110.3.0.10118.2000002.278819.649182 | 20200731 | Steiner_40x_z1_Q | RTD-810--E-01-40 | Diagnostics^Roche^Tissue | 0010 | 1 | 8
PV 20 | yes | 2.16.840.1.113995.3.110.3.0.10118.2000002.198526.54628 | 20200731 | HE_Liver_40x_z1_ | RTD-428--Q-08-06 | Diagnostics^Roche^Tissue | 0010 | 1 | 8
PV 20 | yes | 2.16.840.1.113995.3.110.3.0.10118.2000002.301347.675574 | 20200731 | HE_Liver_20x_z1_ | RTD-538--X-01-40 | Diagnostics^Roche^Tissue | 0010 | 1 | 7
PV 20 | yes | 2.16.840.1.113995.3.110.3.0.10118.2000002.488964.707589 | 20200731 | TriChrome_Grn_20 | RTD-911--H-05-38 | Diagnostics^Roche^Tissue | 0010 | 1 | 8
PV 20 | yes | 2.25.292315917905782003007355414279734624434 | 20190104 | Case S | D19-1001 | Histech^Samantha | 1229631 | 1 | 13
PV 20 | yes | 2.25.31500298076180885870438326289639355558 | 20190105 | Case T | D19-1002 | Histech^Theresa | 1473843 | 1 | 26
PV 20 | yes | 2.25.261030824872518877931236952174606351723 | 20190214 | Case U | D19-1003 | Histech^Ulysses | 2588367 | 1 | 26
PV 20 | yes | 1.2.276.0.7230010.3.1.2.3376381013.14472.1601001847.138 | 20180904 | 100-00-0000 | D18-6001 | Patricia^Huron | 8528631 | 1 | 4
PV 20 | yes | 1.3.46.670589.45.1.1.4993912214784.1.5436.1538560373543 | 20181003 | | D18-1001 | Philips^Amy | 123456 | 1 | 9
PV 20 | yes | 1.3.46.670589.45.1.1.4993912214784.1.5436.1538560374871 | 20181003 | | D18-2001 | Philips^Bob | 234567 | 2 | 17
PV 20 | no | 1.3.46.670589.45.1.1.4993912214784.1.5436.1538560375246 | 20181003 | | D18-3001 | Philips^Chris | 345678 | 2 | 17
PV 20 | no | 1.2.276.0.7230010.3.1.2.3376381013.14472.1601001929.152 | 20180904 | 100-00-0001 | D18-6002 | Quinn^Huron | 1473695 | 1 | 5
PV 20 | no | 1.2.276.0.7230010.3.1.2.3376381013.14472.1601002049.169 | 20180904 | 100-00-0001 | D18-6002 | Quinn^Huron | 1473695 | 1 | 5
PV 20 | no | 1.2.276.0.7230010.3.1.2.3376381013.14472.1601002190.186 | 20180904 | 100-00-0002 | D18-6003 | Robert^Huron | 2581674 | 1 | 4
PV 20 | no | 1.2.276.0.7230010.3.1.2.3376381013.14472.1601002333.203 | 20180904 | 100-00-0002 | D18-6003 | Robert^Huron | 2581674 | 1 | 5
PV 20 | yes | 1.2.826.0.1.3680043.10.559.8890942384645890740091934032221187063 | 20200924 | 1 | 1234 | nference^patient | AKq32AMr | 1 | 10
PV 21 | yes | 2.25.269859997690759739055099378767846712697 | 20210527 | D2M_1S_1 | A20210527084753 | 3DHISTECH^Ureter | ID_20210527084753 | 1 | 477
PV 21 | yes | 2.25.184680854825166843735153744170994632843 | 20210527 | D1M_1S_1 | A20210527084050 | 3DHISTECH^SweatGland | ID_20210527084050 | 1 | 477
PV 21 | yes | 2.25.229657274315044610913259338298080404914 | 20210527 | D1M_17S_1 | A20210527083722 | 3DHISTECH^SmallIntestine | ID_20210527083722 | 1 | 477
PV 21 | yes | 2.25.2794218761846424444317355673683954585 | 20210527 | D2M_2S_1 | A20210527084809 | 3DHISTECH^Testis | ID_20210527084809 | 1 | 477
PV 21 | yes | 2.25.152217345222506078299137009424595786510 | 20210527 | D1M_2S_1 | A20210527084237 | 3DHISTECH^ThyroidCuboidalEpithelium | ID_20210527084237 | 1 | 477
PV 21 | yes | 2.25.97615948674928531317804325176666404677 | 20210527 | D1M_13S_1 | A20210527083316 | 3DHISTECH^SkinOfAbdomen | ID_20210527083316 | 1 | 477
PV 21 | yes | 2.25.281030634571568675050978511298247470490 | 20210527 | D1M_12S_1 | A20210527083253 | 3DHISTECH^Thyroid | ID_20210527083253 | 1 | 477
PV 21 | yes | 2.25.18791930072034659343691185074678777595 | 20210527 | D1M_15S_1 | A20210527083431 | 3DHISTECH^Stomach | ID_20210527083431 | 1 | 477
PV 21 | yes | 2.25.47279596615636500586797160883505973882 | 20210527 | D1M_11S_1 | A20210527083204 | 3DHISTECH^SkinAdipose | ID_20210527083204 | 1 | 477
 |PV 21 | yes | 2.25.44085228549373838680998495894195082939 | 20210527 | D1M_7S_1 | A20210527084705 | 3DHISTECH^SmoothMuscle | ID_20210527084705 | 1 | 477
PV 21 | yes | 2.25.312893125243388464042149748151386729952 | 20210527 | D1M_10S_1 | A20210527083053 | 3DHISTECH^Spleen | ID_20210527083053 | 1 | 477
