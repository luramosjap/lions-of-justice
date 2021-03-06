
# IARS

Incident Accuracy Reporting System

<img src="https://github.com/embrace-call-for-code/lions-of-justice/blob/master/design-assets/IARS_user_interface_design.png" alt="User Interface design"  class="inline"/>


This solution starter was created by technologists from IBM.

# Table of Content
   1. Overview
   2. The idea
   3. How it works
   4. Diagrams
   5. Documents
   6. Technology
   7. Getting started
   8. Recommendations for Enhancements of Capabilities
   9. Resources
   10. License
   11. The Team

# 1. Overview
## Embrace Theme 
### Police & Judicial Reform and Accountability: 
From traffic stops and arrests to sentencing and parole decisions, use technology to better analyze real-world data, provide insights, and make recommendations that will drive racial equality and reform across criminal justice and public safety.

### Problem Statement: 
The lack of transparent and accurate data available to assess police behavioral infractions means, police reports can be falsified and contain other inaccuracies.

This solution addresses the hill outlined below related to the problem statement above:

### Hill: 
Internal affairs and civilians (such as witnesses) can both contribute to incident reports, creating a tamper-proof record with all accounts of the incident.

# 2. The Idea

A Content Management application for capturing statements from first-hand individuals relating to police incident reports. 
* Interface for first-hand individuals to input information or data related to incident report
* Automated/Manual flagging of errors and inaccuracies contained in initial incident reports based on collected data
* Cross reference report data with officer history on misconduct
* Mechanism for disputing claims in incident reports
 
# 3. How It Works

## Solution:


### Consideration

* If a 911 call is made, the event’s address, date, and time is logged as an incident. 

* An incident may or may not be given a case number 
* Incidents reported via app can be linked by provided case number (if known), or by correlating the submitted metadata(location, date, and time)  with a logged incident from the police department
* If an event has not yet been logged as an incident by the police department (ex: occurring live at a protest), reported incidents submitted through app can be tagged as pending until a matching police incident can be linked once filed.  


### Skills & Technologies Required

* Web Application built using Vue.js. This can be run locally or on IBM Cloud. The web application provides the dashboard and is at the core of the solution.
* Watson Speech To Text. The Watson STT API is used to NLP on audio loaded by witnesses and victims.
* Machine Learning - K-Means Clustering
* The database is Cloudant (lite Tier) running on the IBM Cloud.
* The storage for documents(incident reports, videos, audios) is IBM Cloud Object Storage. A free tier is available. 
* Blockchain: This was used to ensure that the submitted reports and information from victims and witnesses are tamper-proof. You can run the application without it.

The diagram describes the application flow

<img src="https://github.com/embrace-call-for-code/lions-of-justice/blob/master/design-assets/IARS.png" width="100%" height="100%" alt="User Interface design"  class="inline"/>

The diagram below walks you through the dashboard flow

<img src="https://github.com/embrace-call-for-code/lions-of-justice/blob/master/design-assets/IARS_Dashboard_flow.png" width="100%" height="100%" alt="User Interface design"  class="inline"/>

# 4. Design 

## Persona/ User

## user journey: AS-IS Experience

## user journey: TO-BE Experience

# 5. Architecture

The Component Model

<img src="https://github.com/embrace-call-for-code/lions-of-justice/blob/master/design-assets/IARS_component_model.png" width="100%" height="100%" alt="User Interface design"  class="inline"/>

The Operational Model 

<img src="https://github.com/embrace-call-for-code/lions-of-justice/blob/master/design-assets/IARS_operational_model.png" width="100%" height="100%" alt="User Interface design"  class="inline"/>

# The Team

* Product Managers: Osai Osaigbovo

* Architects: Laura Bennett, Abiola Asojo , Osai Osaigbovo , Shalisha Witherspoon

* Design: Lucia Ramos, Monica Martinez, Shonda Witherspoon

* User Research: Shonda Witherspoon, Debra Scott, Shalisha Witherspoon, Monica Martinez

* Development: Kalonji Bankole, Laura Bennett, Brandon Kravitz,  Tunde Olokodana, Danny Belitz

* IP Development Joseph Kozhaya

* Special Thanks Cedric Cook, Calvin Lawrence

# Getting started

## Prereqs
Install node and NPM (suggest using NVM https://github.com/nvm-sh/nvm#install--update-script )

## Run application
```
git clone https://github.ibm.com/kkbankol/embrace-lions-for-justice
cd embrace-lions-for-justice
cd frontend
npm install
npm run serve
```

## Start Blockchain
```
cd backend/blockchain/local
./startFabric.sh

git clone https://github.com/IBM/Blockchain-for-maintaining-Digital-Assets
```
