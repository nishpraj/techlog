Geom-99 Virtual Machine Setup Log

Date – 6th March 2024
Start Time – 7.10 Pm
Activity Description – 
Setting up VM Instances 
Step 1 – Logged in to the Google Cloud Console using the Gmail account which has the Google Credits and given to the instructor.
Step 2 – On the Google Cloud Console, Changed the Project by Creating a new Project 
 ![image](https://github.com/nishpraj/techlog/assets/145711084/26a41194-e2ac-4dbc-be82-728acea7c1b8)


Step 3 – From the Navigation Menu, scrolled through the “Compute Engine” Option and Went to the “VM Instances” 
Click on Three Lines on the Left of Google Cloud Icon.
Then Go to Compute Engine and in that click the 
VM INSTANCES
![image](https://github.com/nishpraj/techlog/assets/145711084/e2d44154-219e-4b8d-afd3-d5ad2079b11f)









Step 4 - On the VM Instances tab – 
Click on the “Enable” in the Compute engine API option 
It will Enable the VM Services in the Account associated with the Credits 
Problem 01 – After clicking on the Enable option it asked for the Account Details and Credit Card Details 
Reason of the Problem – On the Billing tab, The Account associated with the Credits was not Selected.
Solution – Click on the Three lines option on the Left of the Google cloud Logo,
Go to the Billing and on the very first option “Billing Account” drop down menu, Select the “Billing Account for Education” Option.

![image](https://github.com/nishpraj/techlog/assets/145711084/398d11f4-142b-4010-8999-422a6668e57d)






After this Step – 
Go to the Compute Engine option and in that - VM Instances tab – 
Click on the “Enable” in the Compute engine API option 
It will Enable the VM Services in the Account associated with the Credits.

Step – 5: Creating VM Instance – 
On the VM Instance Tab, click in the “Create Instance” option and Enter the Name of your Choice to your VM.
 ![image](https://github.com/nishpraj/techlog/assets/145711084/cc392b94-e555-4d93-a139-fdff3985bf26)

1.Now, in this Particular Activity, we must change the Boot Disk, so Scroll down until you find the Boot Disk Information and then Click on “Change” option.
 ![image](https://github.com/nishpraj/techlog/assets/145711084/001f8658-5ca6-47c7-86c4-91b35e01326b)

2. Click on Custom Images in the Boot Disk Change Option and select the “Shawn’s ArcGIS Server”
Select the Latest Version of the Image if more than one option is available or select the One if only one option is available.
3. After Changing the Boot Disk, go back and scroll down to “Firewall” Option and Check the HTTP and HTTPS Traffic Checkbox.
4. Click on “Create”

Step 6 – Password Setup 
After the VM Instance is Created, you will see it in the VM Instance Home page.
Now, go to the Three dots option besides the Connect Column and Click on “Set Windows Password” Option to set the Password.
![image](https://github.com/nishpraj/techlog/assets/145711084/b767da73-5cb8-4b79-a67b-b001bc2e2868)







Now, enter the Username, for this activity the Username is provided in the Checklist, enter that and click on “SET” to generate the Password.
Save the Password safely and securely because this password will be used to Login into the VM.


Step 7 - Setting Up Firewall Rules
Firewall rules are established to get the VM run.
1.	Go to the “VM Instances” page and scroll down to find the “Set up Firewall rules” option. 
2.	Click “Set up Firewall rules” and set the Name, Target and IP ranges.
In this Activity, the name of the rule is “flemingrdp444”, target is set to “Allow all instances in this Network” and IP is set to “0.0.0.0/0”
IP is set to 0.0.0.0/0 to allow any computer on the internet so that we log in to our VM via any computer. (It is less secured and not recommended)
3.	Define the Port number and Click “Create”.
 ![image](https://github.com/nishpraj/techlog/assets/145711084/119e5b9a-a10f-4cc9-bde0-6888aa40c19b)
![image](https://github.com/nishpraj/techlog/assets/145711084/e51e0bd6-1c9a-44cb-a7ac-0d1da265d420)
![image](https://github.com/nishpraj/techlog/assets/145711084/4d744ed7-0d90-4ad5-94c7-5de4df78f405)

 
 

Step 8 – GCP Firewall Rules for ArcGIS Server Manager 
1.	Go to the Search bar on the Top and Search “VPC Network” and Click “Create Firewall Rule”.
2.	Just like the Previous one, setup the Name, Target, IP ranges and Specified TCP Ports of the ArcGIS Server manager. (6443 and 6080).

End Time – 8.00 Pm
Date – 6th March 2024
Time Spent – 50 Minutes
Step 9 – Login into the VM –
Date – 6th March 2023
Time – 8.00 PM 
To launch the Virtual machine, I went to the Start menu of my local Computer and Searched “Remote Desktop Connection”.
In that, we have to enter the IP Address which was generated in the VM Instance which was created earlier. 
Note – The IP address changes everytime we restart the VM. 
 ![image](https://github.com/nishpraj/techlog/assets/145711084/cffb38d9-def6-4c68-b1d6-5ea8d851ff28)

In the Computer field, enter the IP address and Port Number.
Problem – Got an Error while connecting to VM – Unable to establish the Connection.
 ![image](https://github.com/nishpraj/techlog/assets/145711084/3d85e232-d402-46ce-b1e6-80b8cb74ab7d)

Reason – Forgot to enter the Port number after the IP Address while connecting.
 ![image](https://github.com/nishpraj/techlog/assets/145711084/9ca4df7d-14d7-4328-a6f8-776cec79b385)

Solution and Reason – We must enter the Port Number with the IP address as there is a Firewall rule setted up which only allows to connect to the VM if the Port Number is specified. 



Enter the Login Credentials which was entered during the Step 6 – Password Setup.
Note – Do not use your Fleming Account here, it will give error or won’t Connect you to the VM, Instead, go to the “Use a Different Account” option and Enter the Credentials to successfully login into VM.

![image](https://github.com/nishpraj/techlog/assets/145711084/bcca1d64-eda8-4097-a148-bb308ecbd611) ![image](https://github.com/nishpraj/techlog/assets/145711084/5c38b9ae-e60c-42ac-aa3c-7f009ebb3106)







After Successful login, you will be prompted to the VM, in the VM we settled some Firewall rules too so that we can access the ArcGIS Server Management.
Step 10 – Firewall Rules Setup in Virtual Machine
To setup the Firewall Rules, login to the VM and In the VM navigate to Start Menu.
Search for the “Windows Defender Firewall with Advanced Security”

![image](https://github.com/nishpraj/techlog/assets/145711084/47f26ed1-fb3d-4589-a75d-353de4ecc7db)









Open it and select the “Inbound Rules” option on the Left of the Screen and Select “New Rule” option on the Right of the Screen.
![image](https://github.com/nishpraj/techlog/assets/145711084/5d933d1a-3af7-49ec-9d4a-8cd4218b3bb2) ![image](https://github.com/nishpraj/techlog/assets/145711084/2bbfffed-344c-4ca7-b8db-00104167fb0d) ![image](https://github.com/nishpraj/techlog/assets/145711084/1cab8377-77fc-4876-9c0c-74a55e1d2e99) ![image](https://github.com/nishpraj/techlog/assets/145711084/1ada0cf5-055e-409e-81a5-67903f9f9edd)












After Selecting the “New Rule” option, Select the “Port” option and Click Next.
Now, Select the “TCP” option and then Select and enter the “Specified Local Ports”
Here, the Port numbers used are 6443 and 6080.
And after clicking Next rest of the Values will be remain as Defaults. 
Click Finish and the Rule is Setup now.

Now the VM is completely setup and Ready to go. 



End Time – 8.30 Pm
Date – 6th March 2024
Time Spent – 30 Minutes
Log of Publishing the Canada Map in ArcGIS Server using the VM

Date – 6th March 2024
Start time – 8.30 Pm
End Time – 8.50 Pm
Time Spent – 20 Minutes
Activity Description – Publishing the Canada Map from ArcGIS Pro to ArcGIS Server in the VM.

Step 1 - Starting the VM and Logging into it.
Open Google Console, Go to Compute engine and then VM Instances.
Select the VM which was created earlier.
Start the VM to generate the IP address to Login to the VM.
 ![image](https://github.com/nishpraj/techlog/assets/145711084/3e5f2400-3f96-4207-aec0-eab5018bf678)

Use the IP address to Log in to the VM.
Step 2 – Data Preparation 
On the Desktop of the VM, Extract the Canada.zip file to the “Gisworkspace” folder in the C drive of the VM.
After extracting the Data, Minimize the VM and Get back to the local computer and Launch ArcGIS PRO.
Step 3 – Data Publishing
Open ArcGIS Pro and Create a new project in a Folder of your choice.
Copy the Shapefile of Canada and paste it to the Project.
Now – Connect the Server of the VM to the ArcGIS PRO.
Navigate to “Insert” option on the top of the Application and Click the “Connections” option.
Click on the “Server” option and navigate to “New Server Connection” option.
![image](https://github.com/nishpraj/techlog/assets/145711084/9e9589a6-c2b9-4221-8efa-927670a05988)









Now, Enter the link – https://IPAddress:6443/arcgis



In the Link, to get connected with the Server’s management services we have to enter the port number just after the IP address, so that we can get rights to Publish and Edit the Map in the Server.
Enter the Username and Password.
In this activity, the Username is siteadmin 
Password is mentioned in the Checklist.
After successfully connecting the server, you will see the Server option appears on the Catalog pane showing the Files in the Server.
 ![image](https://github.com/nishpraj/techlog/assets/145711084/cfe7f1d0-7f10-49ca-baf4-4d1030a92124)

Now, Right click on the server and Click “Publish” option and then “Map Service” to Publish the Map in the Server.
Select the Map and Click OK
Give the Name of the Map, add description and Select or Create the folder you want the map to be published in. 

In the Data option, select the 
“Reference Registered Data” 
To the folder. 
![image](https://github.com/nishpraj/techlog/assets/145711084/37557189-12fd-4080-870c-cd9f97676ec7)









Finally, click “Analyze” to analyse the errors.
Here, we will get 2 errors which have to be solved.
1.	Unique numeric ID’s
![image](https://github.com/nishpraj/techlog/assets/145711084/87e4ca3a-99b4-4763-9220-1420d9add7dc)






Right click on the Error and Select “Auto-assign IDs Sequentially.” To get out of the error.
2.	Data Source Registration

![image](https://github.com/nishpraj/techlog/assets/145711084/1cf86d28-1cd8-4261-a4b9-5995cadbc991)



Right click on the Warning “Layer’s Data source is not Registered” and select the “Register Data source with Server.” Now, Reanalyze the errors and finally click Publish.
Log of Displaying Data published in Server as Webmap in ArcGIS Online

Date – 7th March 2024
Start Time – 2.15 Pm 
End Time – 2.45 Pm 
Activity Description - Uploading the Map's Feature Layer from ArcGIS REST services of the VM to ArcGIS Online via URL.
Step 1 – Getting the Rest Services URL 
1.	Started the VM and Obtained the IP address
2.	In the web browser of Local Computer, entered the Link https://23.236.49.195:6443/arcgis/rest/services to access the Rest Services of ArcGIS Pro


3.	The Port number “6443” is important and needed to access the ArcGIS Rest Services 
4.	After entering the Link, the browser will say that the Network is not Secure, and It will give Error.
5.	On the Screen, clicked on the “See Advanced Option” and Clicked on the Proceed to “IP address” which let me get in the Services Directory.
 ![image](https://github.com/nishpraj/techlog/assets/145711084/b2527731-29e5-4fab-ad02-656fb3f4ddc7)

6.	On the Directory, Select the Folder in which the Map Services is published.
 ![image](https://github.com/nishpraj/techlog/assets/145711084/0fc6d343-5999-47b8-844d-0cf2b5973118)



7.	Select the Map and then it will let you see the MetaData of the Map.
![image](https://github.com/nishpraj/techlog/assets/145711084/0cb9ef88-7a8d-43d6-8f04-1ab629308365)

![image](https://github.com/nishpraj/techlog/assets/145711084/8bd48037-df3f-43bf-9482-2716607aad05)



















8.	After that, On the Browser’s URL window, Copy the URL and Remove the Port number.

![image](https://github.com/nishpraj/techlog/assets/145711084/f3aaccf6-4094-444b-a278-58501d8f90a9)





9.	Open and logged in to ArcGIS Online
10.	In the Contents Menu, on the left of the screen clicked on New Item.
11.	Clicked on URL and Pasted the URL.
12.	Given the Name, Summary, description and Tags to the map.
13.	At last, clicked on Save and Done.
The map has now been published to ArcGIS Online and is Referenced from the Server of the VM.

End Time – 2.45 Pm 
Time Spent – 30 Minutes
Total Time Spent During the Activity – Apprx. 2 hours 10 Minutes

