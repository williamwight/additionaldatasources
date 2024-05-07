# additionaldatasources

 

Rest Documentation
Root URI is /datasources
Parameters are required except where noted
Verb	URI	Action	Sample Request	Sample Response
GET	/account	
Get all Data Sources accounts assigned to the specified Report Suite.

Query parameters:

report_suite_id
GET /datasources/account?report_suite_id=myrsid
[
	{
		"id":1,
		"name":"Account1",
		"email":"example@adobe.com",
		"ftpHostname":"ftp.example.omniture.com",
		"ftpUsername":"myrsid_123",
		"ftpPassword":"secret1",
		"type":"Generic Summary Data"
	},
	...
]
POST	/account	
Create a new Data Sources account

Query parameters:

report_suite_id
type
name
email
POST /datasources/account?report_suite_id=myrsid&type=generic&name=Account2?email=example@adobe.com
{
	"id":2,
	"name":"Account2",
	"email":"example@adobe.com",
	"ftpHostname":"ftp.example.omniture.com",
	"ftpUsername":"myrsid_456",
	"ftpPassword":"secret2",
	"type":"Generic Summary Data"
}
GET	/account/<data_source_id>	
Gets the specified Data Sources account

Query parameters:

report_suite_id
GET /datasources/account/1?report_suite_id=myrsid
{
	"id":1,
	"name":"Account1",
	"email":"example@adobe.com",
	"ftpHostname":"ftp.example.omniture.com",
	"ftpUsername":"myrsid_123",
	"ftpPassword":"secret1",
	"type":"Generic Summary Data"
}
DELETE	/account/<data_source_id>	
Deletes the specified Data Sources account

Query parameters:

report_suite_id
DELETE /datasources/account/1?report_suite_id=myrsid
{
	"result":"success",
	"message":"Data Sources account has been deleted"
}
POST	/job	
Upload a Data Sources data file

Query parameters:

report_suite_id
data_source_id
Form data:

file
POST /datasources/job?report_suite_id=myrsid&










 
