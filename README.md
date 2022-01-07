# UNICEF <> UNHCR Interagency Interoperability

Documentation for the Interagency Interoperability solution between the Primero and Progresv4 case management systems. This repository includes template OpenFn jobs (or "integration scripts") for automating referrals between the UNICEF and UNHCR systems, as well as general interagency guidance for re-using this solution for other Primero implementations and locations. 

## Gambella Pilot
This solution is actively being piloted in Gambella, Ethiopia. Visit [openfn.github.io/primero-progres/](https://openfn.github.io/primero-progres/) to learn more about this specific implementation, project background, and technical documentation. 

## How to Re-Use & Customize this solution
The key steps for a re-implementation of this solution include: 

### 1. Localizing the data element mapping requirements
Mapping specifications specify which Primero fields map to which Progres v4 fields. While fields from the standard Interagency forms will largely not change, every Primero implementation may have customized data elements that require unique data exchange specifications. This is a business analysis exercise to make sure that data exchanged is translated correctly and sent to the right location in target systems. 

See this **template mapping specification** that can be clones & customized for your specific implementation: https://docs.google.com/spreadsheets/d/1y3bFz7AL8H4D-H-G4WVx-vdrxwzroyGKTvFCMBvjwCI/edit?usp=sharing

Note: 
1. See column `R` for which Primero fields are referenced in standard Interagency forms _or_ need to be configured in your implementation. 
2. See column `T` for which Primero field mappings will likely be localized for your implementation. 
3. See the other tabs (e.g., [Protection Concerns Mapping](https://docs.google.com/spreadsheets/d/1y3bFz7AL8H4D-H-G4WVx-vdrxwzroyGKTvFCMBvjwCI/edit#gid=482307958)) for field value options that may need to be mapped to UNHCR's available data values for this specific location. 

For example, the list of Primero protection concerns may differ between Primero implementations in different locations, so the mapping specification should describe how the implementation’s Primero protection concerns should map to UNHCR’s list of available specific needs.

Once the mapping specifications are finalized, they will need to be implemented in the OpenFn jobs (or "integration scripts"). See next step for more. 

### 2. Forking the Github repository
To clone the OpenFn jobs for customization, this repository can be forked to create a new implementation-specific repository for hosting the OpenFn jobs and documentation, and managing version control as changes are made. 
[https://github.com/OpenFn/unicef-unhcr-io/](https://github.com/OpenFn/unicef-unhcr-io/)

Look for the `Fork` button option in the top right corner of the window. 

### 3. Cloning OpenFn project configuration
The OpenFn jobs are automatically triggered and monitored via the OpenFn platform.  

To clone the project configuration and setup a new OpenFn project space, contact support@openfn.org requesting a copy of the UNICEF <> UNHCR interagency solution configuration. 

### 4. Implementation & Testing
Once the new Github repository and OpenFn project are created for your specific implementation, you can proceed with implementing the data element mapping specification changes required (identified in step #1). 

Follow the project [Implementation Checklist](TO_UPDATE**) for additional tasks and milestones to consider as you get ready to test the job changes and prepare for go-live. 

## Questions? 
Contact support@openfn.org for questions regarding this solution and its documentation. 
