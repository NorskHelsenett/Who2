Using Who2

Who2 is a test tool. In this first public version 1.3.3.0 the following systems can be partially tested
RF, Reseptformidleren.
SFM, Sentral forskrivningsmodul.

The main form is used to send prescription messages and is for use with the RF services

On the main forms top menu a single menu item is enabled, this is the main menu for SFM services an has one subitem, Basis enabled.
This will open the SFM Basis form.


From version 1.4.0.0, released October 22nd, the SyntPoP integration was moved to HelseId authentication.
Users will need to contact HelseId and generate a HelseId token that will have to be included in the app.config file of the application.
Users will also need to register in SyntPoP and get a ClientId to be used in the application. Users will need to generate a minimum of one list of Synthetic individuals. The list(s) will be visible in the application, based on the OwnerId supplied from SyntPop.
The keys that will be neded in app.config:
<add key ="SyntpopAPIUrl" value="https://sdapi.syntpop.utvikling.nhn.no/"/>
 <add key ="SyntpopListID" value="Guid from SyntPoP"/>
 <add key ="SyntpopScope" value ="nhntsd:syntpop-api/full-access"/>
 <add key ="SyntpopAudience" value ="https://helseid-sts.test.nhn.no/"/>
 <add key ="SyntpopClientId" value="Guid from SyntPoP"/>
 <add key ="SyntPopOwnerId" value="Guid from SyntPoP"/>
 <add key ="SyntPopWebKey" value='HelseID token'/>
