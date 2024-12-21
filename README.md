EventSubscriber  
EventConsumer  
EventPublisher  

Notifi Api -> majorly used by UIs  
Quiettime  
SchedulerService  
Reporting Sync  
Reporting  
Voltage  
Triggering  
Composition  
AlertEnrichment  

Delivery  
Azure  
Pushdevicemanagement  

Platform Manager-> Like Azure credentials for Push  
Tenant Manager->All the Alert types, their configuration like is recurring, important, mandatory, subscriptionless, AlertCategory  
Customer Manager->Customer configuration->Reporting dashboard, broadcast dashboard, report history, add user page(external and internal)   
NotifiUI-> for end user->All the alerts, their subscription, all the endpoints, their quitetime.  


Github Repository Flow -->WorkBranch like "work-24.3.2", then developer do its testing and merge the code to "Dev" branch through Pull request. Then after merge build is given to QA from Dev branch. After QA testing is succesful then it is merged to "RC-24.3.2"(Release canditate branch). Then QA do the complete integration testing here, and give good to go approval. Then from RC branch code is merged to "Master" branch.

From Work branch, developer test the code in "Next" Environment, QA do its testing on "test" environment on "Dev" branch code. Then QA take the "Master" branch code and do the testing  on "UAT" environment. Then this code is put on release cycle through service now request. Then code is deployed on "Cert" Environment for validation. Cert Environment is close replica of production environment. In  cert environment code is left for 15-30 days for the testing by different teams for their integration. If no issues are reported then it is release to Production

Scans like Fortify, Sonatype and Webinspect are run on "Dev" branch, then they are run on "Master" branch. 
