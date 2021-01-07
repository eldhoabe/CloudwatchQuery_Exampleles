# CloudwatchQuery_Exampleles
Cloudwatch query samples



fields @timestamp,Response 

| parse RequestMessage "FromEmailAddress\":\"*\"" as fromemail

| filter StatusCode = "Failed"
| filter Response like /(401)/

| sort @timestamp desc
| limit 4000
