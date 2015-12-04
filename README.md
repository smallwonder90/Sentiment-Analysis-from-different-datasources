# Sentiment-Analysis-from-different-datasources
Form the bridge to different data sources through Datameer+Hortonworks playground and analyze the data tables to get the sentiment results

Step 1 : 

Install Datameer+Hortonworks Playground from http://download.datameer.com/hortonworks/
Start the Virtual Machine from Oracle VM Box ( http://127.0.0.1:8081 )
Once the VM is initiated , you will see the screen with above mentioned IP and SSH access root

Step 2:

Access http://127.0.0.1:8081 to access datameer on a webpage ,once you sign in to Datameer
Create a folder "analytics1" in Customer chrun Data mining to save our workbook.

Step 3:

Once the folder is created , Click on add on left uper corner ----> Data --> Import jop -->New Connection
This gives you the List of all servers from which you can create a databridge 

Step 4:

Select the Datasource and click Authorize so that it initializes the Data connection and generates the token 

step 5:

(In our project we have used Google Fusion Tables , Twitter API , Facebook to access the datasets)
Authorize Datameer with Facebook with a personal account
Once the Connection is generated ,Write the querry to pull the datatables 
Sample : 

          SELECT uid, name, sex, birthday FROM user 
          WHERE uid = me() 
          OR uid IN (SELECT uid2 FROM friend WHERE uid1 = me())
          
          for twitter:
          
          /search/tweets.json?q=@Datameer
          /statuses/home_timeline.json
          /statuses/user_timeline.json

          
  Step 6:
  
  If the querry is generated successfully , you will see the excel tabular format of the dataset
  Select the rules below "How to handle invalid Data" tab and click Next
  
  Step 7:
  
  Once the data is fetched to the workbook , Uncheck all the unnecessary columns and click Next
  Click on add new sheet to get the output column
  
  Step 8:
  
  Click on Fx ( to apply the formula ) below File option .
  Select text mining -Sentiment Analysis
  Select ANALYZE_POLARITY
  



