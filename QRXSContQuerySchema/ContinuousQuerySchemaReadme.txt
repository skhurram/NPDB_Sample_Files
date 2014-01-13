
The Data Bank Continuous Query Schema Readme for Use with QRXS
===============================================
The Data Bank Home Page: http://www.npdb.hrsa.gov
QRXS Web Page: http://www.npdb.hrsa.gov/software/downloadsAndDocumentation.jsp

Change History
--------------
(Early 2014) Revision 1.05
             Removed the deprecated npdb and hipdb elements from the response files.
             Added additionalEntityName field in the response files.   

08/27/2012   Revision 1.04
             Added the maintainedUnder element to the reportData element.
             Deprecated the npdb and hipdb elements.

08/22/2011   Revision 1.03
             Increased length of elements organizationName, entityName, affiliation/name, hospitalAffiliation/name,
             agencyProgramName, investigatingAgency/agencyName, forAuthorizedUseBy, and sender to 60 characters.

08/30/2010   Revision 1.02
             (Changes for PDS Schema version 1.01)
             Affiliation record is no longer required.
             Added correctedFields element for correction reports in response files.
             Added previousDisclosureDate element to indicate when and if a report was previously disclosed.
             Masked creditCard/number, agentDBID and ssn fields in response files.

08/31/2009   Revision 1.01
             Removed the numberOfSubjectsChargedSeparately element from the Charge Receipt record.
             Added the subjectNotificationFailure item to the report (PDS Response, Report Disclosure) element.
             Changed the length of the professional school name to 200 characters.
             Added the voidReason item to the void element.

04/20/2009   Revision 1.0
             Initial Release
