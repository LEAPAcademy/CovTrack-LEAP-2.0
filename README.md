# CovidApp-Repo

COVTRACK

# Introduction:

The epidemic COVID-19, known as the coronavirus, continues to spread unabated. The Indian health care sector as well as the Indian State is facing difficulties concerning privacy considerations as it has to balance privacy concerns against the need to protect patients, employees, and customers from the potential infection. Though there is no legislation in India, which requires the protection of healthcare data and data protection in general, the right to privacy has been declared by the Supreme Court as a fundamental right.
To build an application that tracks the list of people the user has come in contact with and notifies them if any of the said people are tested to be COVID positive. By using this app, We can save the life of the people



# Business Requirements:

	Android/iOS/React-Native
 	Cloud Database ()
Data should be store in cloud database not in android application
COVID dashboard information details are dynamic
Need to collect information from Govt Websites, Upload to the cloud database to get a live update
Any user register with our COVID app. Those details should be saved in the cloud
Authentication should be provided for to check the validation
COVID info has to be visualized with some graphs
In case the user is near the red zone, Need to get a push notification
Track COVID tested positive person to avoid contact with people
With the help of gathered information, Promote those locations to as red zone (shutdown)


# Challenges
------------------


Need to load huge amount of data to the cloud database.

Dynamic data has to be visualized to the user end-user.

Sending a notification, When the user Near to the red zone.

GPS tracking to monitor COVID patients to avoid contacting the outside people.

To use a server for processing and also the integration of the server.

Getting user location input and relative data of their neighbourhood.






# Features
--------------

Functional Features:

Precautions of COVID-19
Need to get an alert notification, When anyone is near to the red zone.
Collects data from the user for more precise visualization.
Government helpline number.
Self-assessment 
Using the collected data for visualization and other operations.


Non Functional Features:

Login with username and phone number (The Person will be differentiated based on unique phone numbers)
COVID dashboard function.
Sensors and google map
Information database and area clusters info with google drive(Linked to Azure)./ Firebase
Collect data from the firebase as .csv or .xlsx for visualization using iventura.



# High Level Design:

![alt tag](https://github.com/LEAPAcademy/CovTrack-LEAP-2.0/blob/master/Final%20HLD%20CovTrack.png
)


APP Introduction
----------------

The stated purpose of this app is to spread awareness of COVID-19 and to connect essential COVID-19 - related health services to the people of India. This app augments the initiatives of the Department of Health to contain COVID-19 and shares best practices and advisories.COVID-19 is the infectious disease caused by the most recently discovered coronavirus. This new virus and disease were unknown before the outbreak began in Wuhan, China, in December 2019. COVID-19 is now a pandemic affecting many countries globally.
So we came up with app to help the people.


Login Page
-----------

![alt tag](https://github.com/LEAPAcademy/CovTrack-LEAP-2.0/blob/master/Login%20Page.jpeg)


Code in XML:

	<?xml version="1.0" encoding="utf-8"?>
    <RelativeLayout xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:app="http://schemas.android.com/apk/res-auto"
    xmlns:tools="http://schemas.android.com/tools"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    android:background="#000000"
    tools:context=".LoginActivity">

    <ImageView
        android:id="@+id/imageView2"
        android:layout_width="wrap_content"
        android:layout_height="200dp"
        app:srcCompat="@drawable/logo_cut" />

    <EditText
        android:id="@+id/iphno"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:layout_below="@+id/imageView2"
        android:layout_marginLeft="15dp"
        android:layout_marginTop="100dp"
        android:layout_marginRight="15dp"
        android:ems="10"
        android:hint="Enter Phone Number"
        android:inputType="phone"
        android:padding="20dp"
        android:textColor="#49E10F"
        android:textColorHint="#4ED21A"
        android:textSize="25dp" />

    <EditText
        android:id="@+id/ipswd"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:layout_below="@+id/iphno"
        android:layout_marginLeft="15dp"
        android:layout_marginTop="10dp"
        android:layout_marginRight="15dp"
        android:ems="10"
        android:hint="Enter Password"
        android:inputType="textPassword"
        android:padding="20dp"
        android:textColorHint="#4ED21A"
        android:textColor="#49E10F"
        android:textSize="25dp" />

    <CheckBox
        android:id="@+id/rmbrme"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:layout_below="@+id/ipswd"
        android:layout_centerVertical="true"
        android:layout_marginTop="20dp"
        android:layout_marginLeft="10dp"
        android:checked="false"
        android:text="Remember me"
        android:textColor="#48E115"
        android:paddingHorizontal="10dp"
        android:buttonTint="#48E115"
        android:textColorHighlight="#48E115"
        android:textColorHint="#48E115"
        android:textSize="17sp" />


    <Button
        android:id="@+id/frgt"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:layout_marginTop="10dp"
        android:layout_marginLeft="230dp"
        android:layout_below="@+id/ipswd"
        android:background="#000000"
        android:paddingHorizontal="10dp"
        android:text="Forgot Password?"
        android:textColor="#4BDF15" />

    <Button
        android:id="@+id/loginbtn"
        android:layout_width="match_parent"
        android:layout_height="50dp"
        android:layout_centerHorizontal="true"
        android:layout_marginTop="600dp"
        android:background="#000000"
        android:text="Login"
        android:textStyle="bold"
        android:textSize="25dp"
        android:paddingHorizontal="10dp"
        android:textColor="#4BDF15" />

     </RelativeLayout>
    
   
    
 Registration Page:
 
 ![alt tag](https://github.com/LEAPAcademy/CovTrack-LEAP-2.0/blob/master/Registration%20Page.jpeg)
 
 
 Code in XML
 
 	<?xml version="1.0" encoding="utf-8"?>
    <RelativeLayout xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:app="http://schemas.android.com/apk/res-auto"
    xmlns:tools="http://schemas.android.com/tools"
    android:layout_width="match_parent"
    android:background="#000000"
    android:layout_height="match_parent"
    tools:context=".RegisterActivity">

    <ImageView
        android:id="@+id/imageView3"
        android:layout_width="wrap_content"
        android:layout_height="200dp"
        app:srcCompat="@drawable/logo_cut" />

    <EditText
        android:id="@+id/rname"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:layout_below="@+id/imageView3"
        android:layout_marginLeft="15dp"
        android:layout_marginTop="50dp"
        android:layout_marginRight="15dp"
        android:ems="10"
        android:hint="Enter Name"
        android:inputType="text|textPersonName"
        android:padding="20dp"
        android:textColorHint="#4ED21A"
        android:textSize="25dp" />

    <EditText
        android:id="@+id/rphno"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:layout_below="@+id/rname"
        android:layout_marginLeft="15dp"
        android:layout_marginTop="10dp"
        android:layout_marginRight="15dp"
        android:ems="10"
        android:hint="Enter Phone Number"
        android:inputType="phone|number"
        android:padding="20dp"
        android:textColorHint="#4ED21A"
        android:textColor="#49E10F"
        android:textSize="25dp" />

    <EditText
        android:id="@+id/rpswd"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:layout_below="@+id/rphno"
        android:layout_marginLeft="15dp"
        android:layout_marginTop="10dp"
        android:layout_marginRight="15dp"
        android:ems="10"
        android:hint="Enter New Password"
        android:inputType="textPassword"
        android:padding="20dp"
        android:textColorHint="#4ED21A"
        android:textColor="#49E10F"
        android:textSize="25dp" />

    <EditText
        android:id="@+id/rcpswd"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:layout_below="@+id/rpswd"
        android:layout_marginLeft="15dp"
        android:layout_marginTop="10dp"
        android:layout_marginRight="15dp"
        android:ems="10"
        android:hint="Confirm New Password"
        android:inputType="textPassword"
        android:padding="20dp"
        android:textColorHint="#4ED21A"
        android:textColor="#49E10F"
        android:textSize="25dp" />

    <Button
        android:id="@+id/regdbtn"
        android:layout_width="match_parent"
        android:layout_height="50dp"
        android:layout_centerHorizontal="true"
        android:layout_marginTop="600dp"
        android:background="#000000"
        android:text="Create Account"
        android:textSize="25dp"
        android:textStyle="bold"
        android:paddingHorizontal="10dp"
        android:textColor="#4BDF15" />


    </RelativeLayout>

Firebase Database:
------------------

Firebase is one of cloud database provided by google. We used to store user information. Once they have registered, Can login into app. Authenticated by phone number and passoword. They enter those details correctly, validation happen corresponding their info stored in firebase data.


Firebase is a mobile platform that helps you quickly develop high-quality apps, grow your user base, and earn more money. Firebase is made up of complementary features that you can mix-and-match to fit your needs, with Google Analytics for Firebase at the core. You can explore and integrate Firebase services in your app directly from Android Studio using the Assistant window shown in figure 1.

First make sure you have installed Google Repository version 26 or higher, using the following steps:

Click Tools > SDK Manager.
Click the SDK Tools tab.
Check the Google Repository checkbox, and click OK.
Click OK to install.
Click Background to complete the installation in the background, or wait for the installation to complete and click Finish.
You can now open and use the Assistant window in Android Studio by following these steps:
Click Tools > Firebase to open the Assistant window.
Click to expand one of the listed features (for example, Analytics), then click the Get Started tutorial to connect to Firebase and add the necessary code to your app.


Add Firebase to your Android project

Prerequisites
Install or update Android Studio to its latest version.

Make sure that your project meets these requirements:

Targets API level 16 (Jelly Bean) or later
Uses Gradle 4.1 or later
Uses Jetpack (AndroidX), which includes meeting these version requirements:
com.android.tools.build:gradle v3.2.1 or later
compileSdkVersion 28 or later
Set up a physical device or use an emulator to run your app.
Emulators must use an emulator image with Google Play.

Sign into Firebase using your Google account.

If you don't already have an Android project and just want to try out a Firebase product, you can download one of our quickstart samples.


You can connect your Android app to Firebase using one of the following options:

Option 1: (recommended) Use the Firebase console setup workflow.
Option 2: Use the Android Studio Firebase Assistant (requires additional configuration).
Option 1: Add Firebase using the Firebase console
Adding Firebase to your app involves tasks both in the Firebase console and in your open Android project (for example, you download Firebase config files from the console, then move them into your Android project).

Step 1: Create a Firebase project
Before you can add Firebase to your Android app, you need to create a Firebase project to connect to your Android app. Visit Understand Firebase Projects to learn more about Firebase projects.

Create a Firebase project

Step 2: Register your app with Firebase
After you have a Firebase project, you can add your Android app to it.

Step 3: Add a Firebase configuration file
Add the Firebase Android configuration file to your app:

Click Download google-services.json to obtain your Firebase Android config file (google-services.json).

Move your config file into the module (app-level) directory of your app.

What do you need to know about this config file?

To enable Firebase products in your app, add the google-services plugin to your Gradle files.

In your root-level (project-level) Gradle file (build.gradle), add rules to include the Google Services Gradle plugin. Check that you have Google's Maven repository, as well.

	buildscript {
	
  	repositories {
   	 // Check that you have the following line (if not, add it):
    	google()  // Google's Maven repository
 	 }

  	dependencies {
   	 // ...

    // Add the following line:
    classpath 'com.google.gms:google-services:4.3.3'  // Google Services plugin
  		}
	}

	allprojects {
  	// ...

  	repositories {
    // Check that you have the following line (if not, add it):
    google()  // Google's Maven repository
    // ...
  		}
	}

In your module (app-level) Gradle file (usually app/build.gradle), apply the Google Services Gradle plugin:

	apply plugin: 'com.android.application'
	// Add the following line:
	apply plugin: 'com.google.gms.google-services'  // Google Services plugin

	android {
 		 // ...
	}



Data Visualization
------------------
i) Data visualization is the presentation of data in a pictorial or graphical format.
ii) It enables decision makers to see analytics presented visually, so they can grasp difficult concepts or identify new patterns.
iii) With interactive visualization, you can take the concept a step further by using technology to drill down into charts and graphs for more detail, interactively changing what data you see and how it’s processed.

History of data visualisation :- 
The concept of using pictures to understand data has been around for centuries, from maps and graphs in the 17th century to the invention of the pie chart in the early 1800s. Several decades later, one of the most cited examples of statistical graphics occurred when Charles Minard mapped Napoleon’s invasion of Russia. The map depicted the size of the army as well as the path of Napoleon’s retreat from Moscow – and tied that information to temperature and time scales for a more in-depth understanding of the event.

Why  data visualisation is important :-
Because of the way, we or  the human brain processes information, using charts or graphs to visualize large amounts of complex data is easier than poring over spreadsheets or reports. Data visualization is a quick, easy way to convey concepts in a universal manner – and we can experiment with different scenarios by making slight adjustments.
Data visualization can also:
-> Identify areas that need attention or improvement.
-> Clarify which factors influence the behavior.
-> Help to understand which location having more cases.
-> Predict future sales.



Collecting the Data from Govt website 

	import pandas as pd

	state_wise=pd.read_csv('https://api.covid19india.org/csv/latest/state_wise.csv')
	state_wise_selected=state_wise.drop(['Last_Updated_Time', 'Migrated_Other', 'State_code', 'Delta_Confirmed',
       'Delta_Recovered', 'Delta_Deaths', 'State_Notes'], axis=1)

	print(state_wise_selected)

	Total_recovered1=state_wise_selected['Recovered'][0]
	Total_deaths1=state_wise_selected['Deaths'][0]
	Total_active1=state_wise_selected['Active'][0]

	import matplotlib.pyplot as plt

	Count=[Total_recovered1,Total_deaths1,Total_active1]



	#C=float(Count)
	#group_labels=['Recoverd','Death','Active']
	group_labels=['Recovered\n'+str(Total_recovered1),
            'Deaths\n'+str(Total_deaths1) ,
            'Active\n'+str(Total_active1) ]
	colors=['yellowgreen','red','tomato']


	plt.figure(figsize=(5,5))
	plt.pie(Count,labels=group_labels,colors=colors)
	plt.title('Nationwide total Confirmed, Recovered and Deceased Cases', fontsize = 20)
	plt.show()
	

	--------------------------------------------------------------------------------------------------------------------------------------------------------

	import pandas as pd

	state_wise_daily_df=pd.read_csv("https://api.covid19india.org/csv/latest/state_wise_daily.csv")
	state_wise_daily_df


	state_confirmed=state_wise_daily_df[state_wise_daily_df['Status']=='Confirmed']


	#Confirmed cases in All States



	state_recovered=state_wise_daily_df[state_wise_daily_df['Status']=='Recovered']

	#Reconfirmed cases in All States


	state_deceased=state_wise_daily_df[state_wise_daily_df['Status']=='Deceased']

	#Deceased cases in ALL States

	state_deceased

	from matplotlib import pyplot as plt

	plt.plot(state_deceased['AP'] , state_deceased['Date'] )
	plt.xlabel('Death Count')
	plt.ylabel('Date')
	plt.title('This is the AP state Death count with days count')


	plt.plot(state_deceased['TN'] , state_deceased['Date'] )
	plt.xlabel('Death Count')
	plt.ylabel('Date')
	plt.title('This is the TamilNadu state Death count with days count')


	plt.plot(state_deceased['MH'] , state_deceased['Date'] )
	plt.xlabel('Death Count')
	plt.ylabel('Date')
	plt.title('This is the Maharashtra state Death count with days count')


	plt.plot(state_deceased['MP'] , state_deceased['Date'] )
	plt.xlabel('Death Count')
	plt.ylabel('Date')
	plt.title('This is the Madhya Pradesh state Death count with days count')


	plt.plot(state_deceased['TG'] , state_deceased['Date'] )
	plt.xlabel('Death Count')
	plt.ylabel('Date')
	plt.title('This is the Telangana state Death count with days count')




	plt.plot(state_confirmed['AP'] , state_deceased['Date'] )
	plt.xlabel('Confirmed Count')
	plt.ylabel('Date')
	plt.title('This is the AP state Death count with days count')


	plt.plot(state_confirmed['TN'] , state_deceased['Date'] )
	plt.xlabel('Confirmed Count')
	plt.ylabel('Date')
	plt.title('This is the TamilNadu state confirmed count with days count')


	plt.plot(state_confirmed['MH'] , state_deceased['Date'] )
	plt.xlabel('Confirmed Count')
	plt.ylabel('Date')
	plt.title('This is the Maharashtra state confirmed count with days count')


	plt.plot(state_confirmed['MP'] , state_deceased['Date'] )
	plt.xlabel('Confirmed Count')
	plt.ylabel('Date')
	plt.title('This is the Madhya Pradesh state confirmed count with days count')


	plt.plot(state_confirmed['TG'] , state_deceased['Date'] )
	plt.xlabel('Confirmed Count')
	plt.ylabel('Date')
	plt.title('This is the Telangana state Confirmed count with days count')


	plt.plot(state_confirmed['OR'] , state_deceased['Date'] )
	plt.xlabel('Confirmed Count')
	plt.ylabel('Date')
	plt.title('This is the Odisha state Confirmed count with days count')











about live update of corona cases every 5 min intervel

Streamlit
---------

We built Data Visualization web appliacation by using streamlit. It is one of the python module. 














 
	

