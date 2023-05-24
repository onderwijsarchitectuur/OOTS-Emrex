## Meeting-notes			Technical preparation OOTS-Emrex, April 17th 2023

Opening 

* Present: Michael Lieferath, Guido Bacherach, Gerald Groot Roessink
* Declined: Tor Fridell, Jan Joost Norder, Geir Vangen
*	Next meeting will be rescheduled because it’s a holiday in several countries
*	The technical en semantic meetings with EU (DG-Digit) will be combined.


Purpose for this (serial) meeting
* To understand the technical aspects of SDG/OOTS starting with the High Level Architecture (HLA)
* To find a solution (a bridge) where schools connected to Emrex adhere to SDG/OOTS
* And if possible without intermediary hubs in the dataflow 

Formal stuf from OOTS:
* digitalization of 21 public procedures including enrolment tertiary education
* Since June 2022: Implementing ACT OOP, standardizing cross border exchange (OOTS), with components at  EU and member state level. It also mentions Emrex en Eucaris as sectoral systems established (partionally) at EU-level. OOTS should be ready end 2023.
* Technical, semantic en other working groups with representation from the member states to work on Technical Design Documents (latest: https://ec.europa.eu/digital-building-blocks/wikis/display/TDD/1.+Once-Only+Technical+System+High+Level+Architecture+-+Q1+2023
* Question for Emrex representatives: Is there a line of communication between the national representative in the technical working group and Emrex? If not, should there be?

HLA, OOTS Requirements (initial selection)
* 	req 5.  If evidence is digitally available inside a member state it must be made available through OOTS
*   req 33/34.  End-to-end security (SDG art 14.3.e; EIF P8).  
* Note: EU only takes care of the point-point security between National Access Points. There is no technical solution for true end-to-end with encryption and signing.

HLA, Evidence requester
* Loop 0.	Api get list of dataservices including Emreg/EWP-URL 
* Loop 1. Request Emreg/EWP for preview-URL’s from available EMP’s.
* Loop 2. Request EMP at preview-URL for diploma’s
 
HLA, Evidence providers
* EU-level: Dataservice Directory (DSD)
* National/sectoral-level:  contains preview-URL’s of EMP’s
* EMP-level:  contains diploma’s  for one or more diploma-issuers 

HLA, Evidence exchange & e-Delivery
* Loop 0 is not cross-border --> REST-API
* Loop 1 in HLA is ‘cross-border’ (hence: e-Delivery), Emreg/EWP is at EU-level (hence API)
* Loop 2 in HLA is a exchange, in Emrex it’s a front-office exchange

HLA, Identification and authentication
•	Identity matching OOTS:  requester exchanges  user attributes for identity matching
