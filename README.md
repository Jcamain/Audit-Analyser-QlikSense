# Audit-Analyser-QlikSense
Repository for the Qlik Sense Audit Analyser.

This is an app that has been around for a number of years, but I decided not to keep it hidden and to share it with others.  Happy for people to take it and develop it further.

It is pretty simplistic but allows user to read the advanced audit logs when this has been turned on:

////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////

//First Turn on advanced logging in QlikSense


//Go to Engines->Logging in QMC. In the Tracing section set Audit log level to Info
https://support.qlik.com/articles/000014849

If you are using the Ops Monitor Rest Interface, then you will need to give the relevant user access to run this connector as well in the QMC.  This will be needed for the App Tree Structure as well.

This part of the code has come from the original 'Governance Dashboard' for Qlik Sense which is no longer supported and developed by someone else.  However this code is reading from my 'App's table - the data from the apps data comes from the 'Monitor_apps_REST_app' connection - this is created as standard and is used by the operations monitor as well, but users will need access to that connector.

To exclude sessions relating to reloads by the Sense Distribution service - WHERE ActiveUserId <> 'sa_scheduler' and ActiveUserId <> 'sa_repository';

////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////
