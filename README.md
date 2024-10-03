# On-Going Project

Create your Workspace
Create an on premises Data Gateway (on-premises Link Service)
Steps:
- On top right, click on 'settings' tab
- From the dropdown, click on 'Manage connections and gateways' to check if you have an existing on premises gateway installed under 'on-premises data gateway'. In our case we have non.
- Then open your browser , and navigate to this address--> https://learn.microsoft.com/en-us/data-integration/gateway/service-gateway-install . To download the on-premises data gateway      installer.
- Scroll down and click on 'Download and install a standard gateway' 
- After downloading the file, open the file, click the 'check' to accept terms of use
- Then, click 'install'
- After successful installation, sign in with your Microsoft account email address
- Click 'Next'
- Give your gateway a name under 'New on-premise Gateway' field, say---(onpremisesgateway)
- Input gateway recovery key
- Confirm gateway recovery key
- Then, click on 'Configure'
- Then, click on 'Close' button
- Go back to your Fabric environment to refresh your page
- Click on 'settings' tab
- From the dropdown, click on 'Manage connections and gateways'
- Click on 'on-premises data gateway'
- Then, click on 'status' to confirm if your data gateway is online.

To move Data from on-premises to Lakehouse
- From the bottom left, click on the switch and choose 'Data Factory' switch among number of switches that pops up.
- Then, click on Dataflow Gen 2
- On the top left, click on 'Get data' 
- From the dropdown, click your data source, (SSMS)
- Under 'Connect to data source', fill the necessary credentials : Server Name --> Database--> Data Gateway --> Authentication (Choose 'Basic')--> User Name--> Password
- Then, you gain access to your on premise database.
- Pick tick table(s) you want to move to your lakehouse in Fabric
- To the bottom right, click 'create'
Perform some data cleaning, like removing unwanted columns, ensuring the right data type for each column and so on
- E.g. Remove unwanted columns from each of the tables loaded
Choose Data storage destination
- Click the table you want to move to your Lakehouse
- Then, at the bottom right, click on Data Destination '+' sign
- From the dropdown, pick 'Lakehouse' option
- Connection Credential --> connection--> input  name of your data gateway connection e.g. onpremisegateway
- Click 'Next'
- under 'Choose Destination Target', pick 'New Table' if your table is a new table and 'Existing Table' if you want to attend data to an already existing table
- To your left, click on the lakehouse you want to save the data
- Click 'Next'
- A column or schema mapping comes up
- Then click on 'save settings' to your right, if you are OK with the Schema mapping, otherwise click back to your left to make the necessary corrections
Repeat the same process for the other tables to migrate them into Lakehouse, when done with migrating all the tables to Lakehouse, then you publish your Dataflow Gen 2 by
- Click on the 'Publish' button at the bottom right

