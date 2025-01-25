# SRTR

SRTR Research Projects 

# Data forms of interest 

# General 

1. DONOR_DECEASED: All Deceased Donor Information 

2. DONOR DISPOSITION: This file contains the organ dispositions for each organ for each recovered deceased donor.

There potentially 11 different "organs" from a donor given the 16 different possible ways of recovering organs. See the variable "DON_ORG" for the list.

There are 7 different possible dispositions for each organ type. The variable "DON_DISPOSITION" contains this value.

3. FOL_IMMUNO: Data about immunosupression medications being given a transplant recipient durint the follow up period associated with them. One record per med, merge to the various TRF SAFs by key 'TRR_FOL_ID'.


4. HIST_OPO_TXC: History of affiliation of Organ Procurement Organizations with Transplant Centers.

5. IMMUNO: Data about immunosupression medications being given a transplant recipient at the time of transplant

6. INSTITUTION: Data of all the institutions. Link with center code/ center type combination

7. MALIG: Malignancies during the Follow up period. Merge with the various TXF SAFs by key 'TRR_FOL_ID'

8. REC_HISTO: This file contains one record for the recipient histocompatability lab results for each transplant performed. Merge with file ALLORG.REC_HISTO_XMAT by key, REC_HISTO_TX_ID. Merge to the appropriate transplant record by key, REC_HISTO_TX_ID.



10.  TREATMENT: This file contains treatment data for each De Nova Solid tumor reported on the ALLORG.MALIG record. Merge by key, MALIG_ID.


# HEART AND LUNGS 

1. CAND_THOR: The candidates table includes persons who are registered on the OPTN waiting list as well as additional candidates who have received a living donor organ, even if they have never been placed on the waiting list. The vast majority of candidate information comes from the candidate registration and waiting list information collected by the OPTN. Presents information about candidates during the time they are waiting to receive an organ.

Contains one record per registration; if a person is registered on more than one center's waiting list, he or she is multiply included.

Link by px_id to transplants (TX file) that are a direct result of this registration.






   
   






