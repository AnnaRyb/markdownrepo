# Session Replay Tutorial for an accurate and early error detection.


Have you ever wondered if it is possible to detect 	[application](https://www.dynatrace.com/support/help/how-to-use-dynatrace/real-user-monitoring/basic-concepts/applications) flaws in a split second? 
>It is now possible with the [Session Replay](https://www.dynatrace.com/support/help/how-to-use-dynatrace/real-user-monitoring/basic-concepts/session-replay) feature that is a  video recording from the entire [user session](https://www.dynatrace.com/support/help/how-to-use-dynatrace/real-user-monitoring/basic-concepts/user-session), formed as a sequence of [user actions](https://www.dynatrace.com/support/help/how-to-use-dynatrace/real-user-monitoring/basic-concepts/user-actions) and their further analysis.
>>This is how it works. Discover the functionality in only 7 steps.

  ## **Example scenario**
  >Imagine an online shop, www.performancewear.com that sells clothing and accessories through a single-page application running on Amazon AWS.
  
  ## **Problem**
  >Ashley is a client who was trying to place her order via website form but was unable to complete her transaction. After filling in a few fields, she found out that the system  froze and remained unresponsible despite corrections and webpage reloads. 
  
 ## **Approach**
  >The Dynatrace platform's user-friendly, [AI-powered dashboard](https://www.dynatrace.com/support/help/how-to-use-dynatrace/dashboards-and-charts) identifies issues. However, the user action that led to an error does not explain what exactly happened. Session replay, in turn, retrieves all steps taken by Ashley and finds out why application froze.
  
  ## **Outcome**
 >Inefficiencies are determined and mitigated.


 
## **Recommended steps**

 **__Step 1. CHECK THE DASHBOARD__**. Check the Dynatrace dashboard for open issues and deviations. You can see critical areas organized into themed cards, including:
 * [Problems](https://www.dynatrace.com/support/help/how-to-use-dynatrace/problem-detection-and-analysis)
 * [Smartscape](https://www.dynatrace.com/support/help/how-to-use-dynatrace/smartscape), with the number of Processes
 * Applications affected
 * [Synthetic Monitors](https://www.dynatrace.com/support/help/how-to-use-dynatrace/synthetic-monitoring)
 * [Databases'](https://www.dynatrace.com/support/help/how-to-use-dynatrace/databases) condition
 * Application Performance with [Apdex rating](https://www.dynatrace.com/support/help/how-to-use-dynatrace/real-user-monitoring/basic-concepts/ratings/apdex-ratings), the number of JavaScript errors per minute,  and a graph illustrating user actions per minute, including
 [Load Actions](https://www.dynatrace.com/support/help/how-to-use-dynatrace/real-user-monitoring/basic-concepts/user-actions#load-action), 
  [XNR Actions](https://www.dynatrace.com/support/help/how-to-use-dynatrace/real-user-monitoring/basic-concepts/user-actions#xhr-action)
  and [Custom Actions](https://www.dynatrace.com/support/help/how-to-use-dynatrace/real-user-monitoring/basic-concepts/user-actions#custom-action)
 * Goal Performance, featuring Conversion Rate for your [Conversion Goals](https://www.dynatrace.com/support/help/how-to-use-dynatrace/real-user-monitoring/how-to-use-real-user-monitoring/web-applications/define-conversion-goals) and the number of Completions
 * Apdex Performance 
 * Services (Web, Messaging, RMI/Custom)

 **In the example below, a particular problem and a sudden drop in conversion rate were identified (marked in red)**
 
![screenshot](https://github.com/AnnaRyb/Screenshots/blob/main/Deviations_.jpg)

**__Step 2. INVESTIGATE OPEN ISSUES__**. 
By clicking on the **Problems** icon, you are transferred to the error details screen. It can be figured out what exact item is affected (for example, the drill-down functionality, and the impact area, such as main page). Other information include:
* the error table with a split into application, services and infrastucture as per the pattern below:

| Items        |      Affected | Recovered| Monitored|
|------------  |:-------------:|------:   |------:   |
|Application   |       1       |   -      |    24    |
|Service       |       0       |   -      |    92    |
|Infrastructure|       0       |   12     |    46    |

* business impact analysis, showing how many users are impacted:




 ![screenshot](https://github.com/AnnaRyb/Screenshots/blob/main/Business%202impact%20analysis.png)
 
 
 **__Step 3. FIND THE ERROR__** 
 By drilling this issue further down with clicking on Application Performance card in the Dashboard, you can learn what the exact type of issue was encountered, such as JavaScript error increase.
 
 
 
 
 ![screenshot](https://github.com/AnnaRyb/Screenshots/blob/main/JavaScript%20Error.png)
 
 
 
 
 
 You can also compare JavaScript errors with user actions on a timeline:
 
 
 
 
 ![screenshot](https://github.com/AnnaRyb/Screenshots/blob/main/Comparison.jpg)
 
 
 
 
 
 Scroll down to **Top 10 JavaScript errors** table to find out new, unknown and high-frequency errors, such as the one marked in red: 
 
 
 
 
 ![screenshot](https://github.com/AnnaRyb/Screenshots/blob/main/Top%2010%20JavaScript%20errors1.jpg)
 
 
 
 
 
 **__Step 4.FIND THE USER__** 
 By clicking on the **View Full Details** button on the right bottom of the Top 10 JavaScript table, you can view such error details as page occurence, error message, stacktrace and an **exact user action that caused the issue**.
 
 
 
 ![screenshot](https://github.com/AnnaRyb/Screenshots/blob/main/User%20action.png)
 
 
 ** __NOTE__** Since www.performancewear.com a single-page application, we do not know where the command "click on 'btn_sell-421198' " was executed and what it was meant to do in the context of application. In such scenario, search by a particular user can be performed by returning to the **business impact analysis** icon  and clicking on the **number of impacted users**:
 
  ![screenshot](https://github.com/AnnaRyb/Screenshots/blob/main/business%20impact%20analysis3.png)
  
  
  **__Step 5. REPLAY THE SESSION__**
  
  *  find and select the user who raised the issue on the list ![screenshot](https://github.com/AnnaRyb/Screenshots/blob/main/user%20search.png)
  
  *  and  find the session affected and replay the session![screenshot](https://github.com/AnnaRyb/Screenshots/blob/main/business%20impact%20analysis3.png) 
 
 
 
 
 
 

