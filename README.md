#  Session replay feature. See what your users do.


Have you ever wondered if it's possible to detect [application](https://www.dynatrace.com/support/help/how-to-use-dynatrace/real-user-monitoring/basic-concepts/applications) flaws in a split second? 
>It can be achieved thanks to the [Session Replay](https://www.dynatrace.com/support/help/how-to-use-dynatrace/real-user-monitoring/basic-concepts/session-replay) function that shows a video recording from the entire [user session](https://www.dynatrace.com/support/help/how-to-use-dynatrace/real-user-monitoring/basic-concepts/user-session), formed as a sequence of [user actions](https://www.dynatrace.com/support/help/how-to-use-dynatrace/real-user-monitoring/basic-concepts/user-actions) performed in your application, including those leading to errors. All actions are captured from the user's perspective in a movie-like format.

>Find out how Session replay works. Discover the functionality in only 6 steps and capture any type of issues in less than 5 minutes.

## **Example scenario**
  >Imagine an online shop, www.performancewear.com, offering clothing and accessories through a single-page application running on Amazon AWS.
  
## **Problem**
  >Ashley is a client who was trying to place her order via website form but was unable to complete her transaction. After filling in a few fields, she found out that the system  froze and remained unresponsive despite corrections and webpage reloads. 
  
 ## **Approach**
  >The Dynatrace platform's user-friendly, [AI-powered dashboard](https://www.dynatrace.com/support/help/how-to-use-dynatrace/dashboards-and-charts) identifies issues within application. However, the user action that led to an error does not explain what exactly happened. Session replay, in turn, retrieves all steps taken by Ashley and finds out why the application froze.
  
 ## **Outcome**
 >Inefficiencies are determined and can be mitigated.


 
 
## **__Recommended steps__** h1



### **__Step 1. Check the dashboard__**. 
 >Check the Dynatrace dashboard for open issues and deviations. You can see critical areas organized into themed cards, including:
 * [Problems](https://www.dynatrace.com/support/help/how-to-use-dynatrace/problem-detection-and-analysis).
 * [Smartscape](https://www.dynatrace.com/support/help/how-to-use-dynatrace/smartscape), with the number of Processes.
 * Applications affected.
 * [Synthetic monitors](https://www.dynatrace.com/support/help/how-to-use-dynatrace/synthetic-monitoring).
 * [Databases'](https://www.dynatrace.com/support/help/how-to-use-dynatrace/databases) condition.
 * Application performance with [Apdex rating](https://www.dynatrace.com/support/help/how-to-use-dynatrace/real-user-monitoring/basic-concepts/ratings/apdex-ratings), the number of JavaScript errors per minute,  and a graph illustrating user actions per minute, including
 [Load actions](https://www.dynatrace.com/support/help/how-to-use-dynatrace/real-user-monitoring/basic-concepts/user-actions#load-action), 
 [XNR actions](https://www.dynatrace.com/support/help/how-to-use-dynatrace/real-user-monitoring/basic-concepts/user-actions#xhr-action)
 and [Custom actions](https://www.dynatrace.com/support/help/how-to-use-dynatrace/real-user-monitoring/basic-concepts/user-actions#custom-action).
 * Goal performance, featuring Conversion rate for your [Conversion goals](https://www.dynatrace.com/support/help/how-to-use-dynatrace/real-user-monitoring/how-to-use-real-user-monitoring/web-applications/define-conversion-goals) and the number of Completions.
 * [Apdex performance ](https://en.wikipedia.org/wiki/Apdex).
 * Services (Web, Messaging, RMI/Custom).

 **In the example below, one problem, JavaScript errors and a sudden drop in conversion rate were identified (marked in red)**
 
![screenshot](https://github.com/AnnaRyb/Screenshots/blob/main/Deviations_.jpg)

### **__Step 2. Investigate open issues__**. 
>By clicking on the **Problems** icon, you are transferred to the error details screen. It can be figured out what items are affected (for example, the drill-down functionality, and the impact area, such as main page). It also offers:
* error status table within three main categories. Here, it states clearly the issue is within Application.

| Items        |      Affected | Recovered| Monitored|
|------------  |:-------------:|:--------:|:--------:|
|Application   |       1       |   -      |    24    |
|Service       |       0       |   -      |    92    |
|Infrastructure|       0       |   12     |    46    |

* business impact analysis, showing how many users are affected:

 ![screenshot](https://github.com/AnnaRyb/Screenshots/blob/main/Business%202impact%20analysis.png)
 
 
 ### **__Step 3. Find new errors__**.
 >By  drilling this issue further down, you can learn what types of problems were encountered. The situation is illustrated by the JavaScript error increase. 
 
 
 ![screenshot](https://github.com/AnnaRyb/Screenshots/blob/main/JavaScript%20Error.png)
 
 
 >You can also compare JavaScript errors with user actions on a timeline:
 
 
 
 
 ![screenshot](https://github.com/AnnaRyb/Screenshots/blob/main/Comparison.jpg)
 
 
 
 
 
 
 >Scroll down to the **Top 10 JavaScript errors** table to find out **new, unknown and high-frequency errors**, such as the one marked in red: 
 
 
 
 ![screenshot](https://github.com/AnnaRyb/Screenshots/blob/main/Top%2010%20JavaScript%20errors1.jpg)
 

 
 ### **__Step 4. Find error details__**.
 >By clicking on the **View Full Details** button on the right bottom of the **Top 10 JavaScript table**, you can view such error details as: 
 * page occurence. 
 * error message. 
 * stacktrace.
 * **exact user action that caused the issue** in the form of the command that was executed.
  
 [Source map for JavaScript error analysis](https://www.dynatrace.com/support/help/how-to-use-dynatrace/real-user-monitoring/how-to-use-real-user-monitoring/web-applications/source-map-support-for-javascript-error-analysis)
 
 
 
 ![screenshot](https://github.com/AnnaRyb/Screenshots/blob/main/User%20action.png)
 
 However, identifying the **exact user action that caused the issue** might not be sufficient in some cases.
 
 **__NOTE:__** Since www.performancewear.com a single-page application, you don't know where the command "**click on 'btn_sell-421198'** " was executed and what actions it was meant to perform. Therefore, further research is required.
  
  
  ### **__Step 5. Find specific user/users impacted and replay the session__**.
  
  
  * In order to find more details about the user and actions performed, get back to the **Business impact analysis** icon and click on the **Number of impacted users**:
  
  ![screenshot](https://github.com/AnnaRyb/Screenshots/blob/main/business%20impact%20analysis3.png)
  
  * Find and select the user who raised the issue from the list ![screenshot](https://github.com/AnnaRyb/Screenshots/blob/main/user%20search.png)
  
  * Find the affected session and click the **Replay** button![screenshot](https://github.com/AnnaRyb/Screenshots/blob/main/Replay%20button.png) 


   ### **__Step 6. Find where and why an error occured__**.
 >In the user's session's recording, you can detect the exact moment when issue was faced by the user and a specific field impacted:
 ![screenshot](https://github.com/AnnaRyb/Screenshots/blob/main/Postal%20code.png) 
 
 >In this case, Ashley inserted the postal code in an invalid format for the selected country field, prompting a loading indicator that did not dissappear and blocked moving to the next step. The recording shows Ashley's numerous attempts to continue after correcting the postal code, then filling in the form again, and finally quitting the application.


 > Session Replay's short movie is the best illustration of a customer journey, with every step she/he takes before and after an incident happens.
 
 **[Watch the video tutorial](https://video.dynatrace.com/watch/TNuevLCmF91DD1zW1X9bqD)** 
 
 
 ## In this section

1. [Section 1](#h1)
2. [Section 2](#section-2)
    - [Subsection a](#subsection-a)
    - [Subsection b](#subsection-b)
 
 
 
 
 
 

