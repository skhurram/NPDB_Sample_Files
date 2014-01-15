NPDB
====

How to test
-----------
*This guide shows how to test a request against the npdb web service.*

***
	
Remove white spaces and encode into base64:

[submission_file.test.xml](https://raw2.github.com/samsongz/NPDB_Sample_Files/master/QRXS_PDS_Enrollment_Sample_Files/submission_file.test.xml)

    $ cat submission_file.xml | tr -d '\t\r\n' | base64
    
Add encoded string to the request file:    

[request_file.xml](https://raw2.github.com/samsongz/NPDB_Sample_Files/master/request_file.xml)

    <?xml version="1.0" encoding="UTF-8"?>
    <soap:Envelope xmlns:soap="http://www.w3.org/2003/05/soap-envelope" 
    xmlns:qrx="http://www.npdb-hipdb.hrsa.gov/QrxsWebService">
      <soap:Header/> 
      <soap:Body>
        <qrx:Send> 
          <qrx:DataBankID>800000000000000</qrx:DataBankID>
          <qrx:UserID>1116521</qrx:UserID>
          <qrx:SubmissionFiles>
            <FileName>query.xml</FileName>
            <XmlFileData>
              <!-- Replace here with the base64 encoded submission file -->
            </XmlFileData>
          </qrx:SubmissionFiles>
        </qrx:Send>
      </soap:Body> 
    </soap:Envelope>
    
Make the request to the Web Service - `test endpoint`:

    curl \
    --header "Content-Type: application/soap+xml;charset=UTF-8" \
    --header "SOAPAction: Send" \
    --data @request_file.xml \
    https://qa.npdb-hipdb.hrsa.gov/qrxs/QrxsWebService
