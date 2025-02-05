# SRTR


# Practicum Title: Primary Graft Dysfunction Following Heart Transplantation from Donation After Circulatory Death versus Donation After Brain Death: An Analysis of the Scientific Registry of Transplant Recipients

# Background and public health relevance
Primary graft dysfunction (PGD) is the leading cause of early mortality within the first 30 days
after heart transplantation, resulting in poor post-transplant outcomes and significant challenges
for patient care. Although the International Society for Heart and Lung Transplantation (ISHLT)
has developed a consensus-based classification system for PGD, transplant centers continue to
refine its definition to improve clinical application and standardization. Reported PGD incidence
varies widely, ranging from 2.3% to 28.2% in single-center studies, reflecting variability in
definitions and practices. As the use of hearts donated after circulatory death (DCD) grows to
address organ shortages, concerns have emerged regarding increased risks of PGD in this donor
category, particularly in centers newly adopting DCD protocols. However, limited data currently
exist to substantiate these associations. Understanding the incidence, outcomes, and potential
risks of PGD in DCD versus donation after brain death (DBD) hearts is essential to improving
patient outcomes and guiding the safe and effective expansion of the donor pool.



# Specific aims/hypotheses

Specific Aim 1: To compare the incidence and severity of primary graft dysfunction (PGD)
between heart transplant recipients who received hearts from donation after circulatory death
(DCD) and donation after brain death (DBD).
Hypothesis: Heart transplant recipients of DCD hearts have a higher incidence and severity of
PGD compared to recipients of DBD hearts.

Specific Aim 2: To evaluate the short-term and long-term outcomes of heart transplant recipients
with PGD, stratified by DCD and DBD donor status.
Hypothesis: Recipients with PGD following transplantation from DCD hearts experience worse
short-term and long-term outcomes compared to those receiving DBD hearts.

Specific Aim 3: To identify factors that mediate or modify the risk of PGD in DCD versus DBD
heart transplants, such as donor characteristics, ischemic time, and center experience.
Hypothesis: Differences in ischemic time and center experience significantly influence the risk of
PGD in DCD heart recipients compared to DBD recipients.

![Presentation_PGD](Articles/presentation_proposal_PGD.pdf) 
![FOL_IMMUN](Articles/presentation_proposal_PGD.pdf) 


# Data forms of interest 
![FOL_IMMUN](Data_dic_pict/SAFsLinkingDiagram.png) 
Data dictionary online: https://www.srtr.org/requesting-srtr-data/saf-data-dictionary/

# General 

1. DONOR_DECEASED: All Deceased Donor Information
 
   ![FOL_IMMUN](Data_dic_pict/DONOR_DECEASED1.png)
      ![FOL_IMMUN](Data_dic_pict/DONOR_DECEASED2.png)
      ![FOL_IMMUN](Data_dic_pict/DONOR_DECEASED3.png)
       ![FOL_IMMUN](Data_dic_pict/DONOR_DECEASED4.png)
      ![FOL_IMMUN](Data_dic_pict/DONOR_DECEASED5.png)
      ![FOL_IMMUN](Data_dic_pict/DONOR_DECEASED6.png)



3. DONOR DISPOSITION: This file contains the organ dispositions for each organ for each recovered deceased donor.

  ![FOL_IMMUN](Data_dic_pict/DONOR_DISPOSITION.png) 
  
There potentially 11 different "organs" from a donor given the 16 different possible ways of recovering organs. See the variable "DON_ORG" for the list.

There are 7 different possible dispositions for each organ type. The variable "DON_DISPOSITION" contains this value.

3. FOL_IMMUNO: Data about immunosupression medications being given a transplant recipient durint the follow up period associated with them. One record per med, merge to the various TRF SAFs by key 'TRR_FOL_ID'.
   
![FOL_IMMUN](Data_dic_pict/FOL_IMMUN.png)

4. HIST_OPO_TXC: History of affiliation of Organ Procurement Organizations with Transplant Centers.
   ![FOL_IMMUN](Data_dic_pict/HIST_OPO_TXC.png)

5. IMMUNO: Data about immunosupression medications being given a transplant recipient at the time of transplant
   ![FOL_IMMUN](Data_dic_pict/IMMUNO.png)

6. INSTITUTION: Data of all the institutions. Link with center code/ center type combination
    ![FOL_IMMUN](Data_dic_pict/INSTITUTION.png)

7. MALIG: Malignancies during the Follow up period. Merge with the various TXF SAFs by key 'TRR_FOL_ID'
    ![FOL_IMMUN](Data_dic_pict/MALIG1.png)
      ![FOL_IMMUN](Data_dic_pict/MALIG3.png)

8. REC_HISTO: This file contains one record for the recipient histocompatability lab results for each transplant performed. Merge with file ALLORG.REC_HISTO_XMAT by key, REC_HISTO_TX_ID. Merge to the appropriate transplant record by key, REC_HISTO_TX_ID.
    ![FOL_IMMUN](Data_dic_pict/REC_HISTO1.png)
     ![FOL_IMMUN](Data_dic_pict/REC_HISTO2.png)
     ![FOL_IMMUN](Data_dic_pict/REC_HISTO3.png)



9.  TREATMENT: This file contains treatment data for each De Nova Solid tumor reported on the ALLORG.MALIG record. Merge by key, MALIG_ID.
    ![FOL_IMMUN](Data_dic_pict/TREATMENT.png)


# HEART 

1. CAND_THOR: The candidates table includes persons who are registered on the OPTN waiting list as well as additional candidates who have received a living donor organ, even if they have never been placed on the waiting list. The vast majority of candidate information comes from the candidate registration and waiting list information collected by the OPTN. Presents information about candidates during the time they are waiting to receive an organ.

Contains one record per registration; if a person is registered on more than one center's waiting list, he or she is multiply included.

Link by px_id to transplants (TX file) that are a direct result of this registration.
![CAND_THOR1](Data_dic_pict/CAND_THOR1.png)
![FOL_IMMUN](Data_dic_pict/CAND_THOR2.png)
![FOL_IMMUN](Data_dic_pict/CAND_THOR3.png)
![FOL_IMMUN](Data_dic_pict/CAND_THOR4.png) 

	
2. STATHIST_THOR
For each registration on the waiting list, at least one record exists in the STATHIST (status history) table. This table records characteristics that may change during the course of waiting list tenure, such as medical urgency status or model for end-stage liver disease (MELD) score for liver candidates. Each record in this table is associated with a time at which those characteristics began and ended.

The STATHIST table is created by examining histories of changes to the operational waiting list, recording all changes that involve these variables of interest, and augmenting this file with non-overlapping start- and end-dates for the span of each set of characteristics.
![FOL_IMMUN](Data_dic_pict/STATHIST_THOR.png) 

Link to the CAND file by wl_id.

3. STATJUST_HR1A
![FOL_IMMUN](Data_dic_pict/STATJUST_HR1A.png)
![FOL_IMMUN](Data_dic_pict/STATJUST_HR2A.png)
![FOL_IMMUN](Data_dic_pict/STATJUST_HR3A.png)
![FOL_IMMUN](Data_dic_pict/STATJUST_HR4A.png)
![FOL_IMMUN](Data_dic_pict/STATJUST_HR5A.png) 

5. STATJUST_HR1B
![FOL_IMMUN](Data_dic_pict/STATJUST_HR1B.png) 


7. TXF_HR
For each transplant, a record at 1 year and then annually, post transplant until the recipient is re-transplanted, dies, or is lost to followup.

Information from the Transplant Recipient Followup (TRF) form, including characteristics of the patient at the time of followup and during the period since the transplant (1 yr) or last followup (all others). The variable TFL_FOL_CD indicates which followup period the record represents.

If the record shows TFL_IMMUNO = Y, immunosuppresion data for the followup period is available in LIIN.FOL_IMMUNO, linked by key, TRR_FOL_ID. If the record shows TFL_MALIG = Y, malignancy data diagnosed during the followup period is available in ALLORG.MALIG, linked by key, TRR_FOL_ID.

Link to transplant records (TX_org) using trr_id.
![FOL_IMMUN](Data_dic_pict/TXF_HR1.png) 
![FOL_IMMUN](Data_dic_pict/TXF_HR2.png) 
![FOL_IMMUN](Data_dic_pict/TXF_HR3.png) 

6. TX_HR
One record per transplant.

Information from the Transplant Recipient Registration (TRR) form, including characteristics of the patient at the time of transplant and the transplant operation itself. For ease of analysis, characteristics of the donor are added, as well as donor-recipient interactions, such as calculated HLA mismatch scores, blood compatibilities, and whether the organ was "shared," based on the relationship between the organ procurement organization (OPO) recovering the organ and the transplant center.

The TX table also includes summarized information from the transplant follow-ups, such as patient status information from the last transplant follow-up filed, to enable survival analyses.

Link to follow-up records (TXF_org) using trr_id. Link to CAND files using px_id. Link to donor records using don_id.

![FOL_IMMUN](Data_dic_pict/TX_HR1.png) 
![FOL_IMMUN](Data_dic_pict/TX_HR2.png) 
![FOL_IMMUN](Data_dic_pict/TX_HR3.png) 
![FOL_IMMUN](Data_dic_pict/TX_HR4.png) 
![FOL_IMMUN](Data_dic_pict/TX_HR5.png) 
![FOL_IMMUN](Data_dic_pict/TX_HR6.png) 
![FOL_IMMUN](Data_dic_pict/TX_HR7.png) 





   
   






