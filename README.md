# GIPEDI_Week-8-Report

##### NAME : PREETI POLAI

##### ID: FENGS113

##### MAIL ID: b18ec003@nitm.ac.in

##### Website: [Preeti Polai](https://sites.google.com/nitm.ac.in/preetipolai/about)

##### Date of Submission: July 9, 2021



### PROGRESS IN KOTLIN

<p align = "justify">The new concepts that I have learned in Kotlin include functions types. The function types are the variables that are assigned with a function. These variables can even be sent in the arguments as a standard variable—lambdas in one of the initializations of these variables. Lambda is a high-level function that drastically reduces the boilerplate code while declaring a function and defining the same.</p>

### GENERATION OF THE .CSV FILE FROM ROOM DATABASE

<p align = "justify">CSV file is simply a Comma Separated Values text file that represents structured data of some kind. To export to CSV file logic, we have to use a library for this, called [kotlin-csv](https://github.com/doyaaaaaken/kotlin-csv). This library has a simple interface and easy setup for importing and exporting. CSV files to the Room database and vice versa.</p> 

<p align = "justify">In code, initially, I created the instance of the File, the naming of the File is done so that it takes random values as the file name. This File initially is empty. Hence, we must put the database data into it. The database here contains five parameters - Date, Net Accelerometer data, Net Magnetometer data and Net Gyroscope data, timestamp(long) and the current time.</p>

![image](https://user-images.githubusercontent.com/71027537/124975727-edb28200-e04b-11eb-996b-26a0a4faf771.png)

<center>Fig 1: Generation of .CSV File</center>

- #### COROUTINES IN KOTLIN

<p align = "justify">The created. CSV file is now sent to the Coroutine Scope, such that all the activities occur in the back thread instead of the main thread. The use of coroutines ensures uninterrupted interaction of the user with the application. Coroutines allow both sequential and asynchronous network/database access and can be used in the Kotlin Application using a lifecycle Scope Library and the“suspend” keyword.</p>

- #### "SUSPEND" KEYWORD

<p align = "justify">When used within a function, the suspend keyword suspends the code segment followed by an async request until the request returns a response. It allows the code to run sequentially even when a few tasks are run on the background thread.</p>



<p align = "justify">In the Coroutine Scope, data is fetched from the Room database using the live data and then transported to the created CSV File. Here, we initially create the CSV file header, followed by for every new row a new entry of data is transferred to. CSV File.</p>

![image](https://user-images.githubusercontent.com/71027537/124975765-00c55200-e04c-11eb-98bb-6b679b226e8c.png)
<center>Fig 2:  Addition of Data to .CSV file</center>


<p align = "justify">Finally, when the .CSV file has the entire data, the Intent is sent such that the generated .CSV can be seen in some other CSV Viewer app - Sheets, Excel and others.</p>



- #### DELETION OF DATA DROM EXISTING ROOM DATABASE

  After the successful generation of the .CSV file. The data of the particular activity is removed from the Room database.

![image](https://user-images.githubusercontent.com/71027537/124975621-d378a400-e04b-11eb-8ad1-38f92f02db7f.png)
<center>Fig 3: Removal of data from Room Database after Activity Completion</center>



### ADDITION OF THE BUTTON IN UI

<p align = "justify">Following the advice of the Student Mentor, I have modified the UI so that the user can generate a separate datasheet for every new activity. I have put a "START "button on display. This lets the users start the record of the data of the sensors. As soon as they press start, the text of the button will change to "STOP." On pressing it again, it will enable the application to stop recording the sensor data and immediately create a new one. CSV file. This generated CSV File will be immediately displayed in some other app.</p>

Video Link : https://drive.google.com/file/d/1BcANmk7qDM2xHnCWob1mbFW2COtlA8N5/view


<img src="https://user-images.githubusercontent.com/71027537/124975853-1fc3e400-e04c-11eb-9cba-03b66e270094.jpeg" alt="Screenshot1" width="320"/>

Fig 4: Before Pressing START Button


<img src="https://user-images.githubusercontent.com/71027537/124975849-1e92b700-e04c-11eb-9282-3c55ab496edd.jpeg" alt="Screenshot1" width="320"/>
<img src="https://user-images.githubusercontent.com/71027537/124975859-218da780-e04c-11eb-8e68-3d853a1ac24b.jpeg" alt="Screenshot1" width="320"/>

Fig 5: After Pressing START Button



### INTERACTION WITH THE STUDENT MENTOR

<p align = "justify">After showing the results to the student mentor, Mr. Bodhibrata Mukhopadhyay, he directed to store the 3 sensor data in a row in each time stamp. At present, at a particular time only one among the 3 sensors is giving the data. At different timestamps, but there's very minor gap, so in that gap other two sensors are giving zero values. This needs to be rectified. Hence, this is the next task to accomplish.</p>

<img src="https://user-images.githubusercontent.com/71027537/124975856-20f51100-e04c-11eb-8fc6-b650c434927d.jpeg" alt="Screenshot1" width="320"/>

Fig 6: Preview of the .CSV file generated 
 
