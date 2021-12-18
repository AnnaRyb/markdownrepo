# Session Replay, an eagle-eyed error detection tool


Have you ever wondered if it is possible to detect 	[application](https://www.dynatrace.com/support/help/how-to-use-dynatrace/real-user-monitoring/basic-concepts/applications) flaws in a split second? 
>It is now possible with the [Session Replay](https://www.dynatrace.com/support/help/how-to-use-dynatrace/real-user-monitoring/basic-concepts/session-replay) feature that retrieves entire [user session](https://www.dynatrace.com/support/help/how-to-use-dynatrace/real-user-monitoring/basic-concepts/user-session) consisting of related [user actions](https://www.dynatrace.com/support/help/how-to-use-dynatrace/real-user-monitoring/basic-concepts/user-actions), in the form of video recording.
>>This is how it works.

  **Example scenario**
  >Imagine an online shop, www.performancewear.com that sells clothing and accessories through a single-page application running on Amazon AWS.
  
  **Problem**
  >Ashley is a client who was trying to place her order via website form but was unable to complete her transaction. After filling in a few fields, she found out that the system  froze and remained unresponsible despite corrections and webpage reloads. 
  
  **Approach**
  >The Dynatrace platform's user-friendly, AI-powered dashboard replays all steps taken by Ashley and detects suspicious behavior.
  
  **Outcome**
 >Inefficiences are determined and mitigated.
 
Whenever you face issues with your application, you just need to perform a few steps to precisely determine the cause of failure and repair it immediately.

 **__Step 1__**. Check the Dynatrace dashboard for open issues and deviations. You can see critical areas organized into themed cards, including, among others:
 * Problems
 * Smartscape
 * Applications
 * Synthetic Monitors
 * Databases
 * Application Performance with [Apdex rating](https://www.dynatrace.com/support/help/how-to-use-dynatrace/real-user-monitoring/basic-concepts/ratings/apdex-ratings), JavaScript errors,  and a graph illustrating user actions per minute, including
 [Load Actions](https://www.dynatrace.com/support/help/how-to-use-dynatrace/real-user-monitoring/basic-concepts/user-actions#load-action), 
  [XNR Actions](https://www.dynatrace.com/support/help/how-to-use-dynatrace/real-user-monitoring/basic-concepts/user-actions#xhr-action),
 [Custom Actions](https://www.dynatrace.com/support/help/how-to-use-dynatrace/real-user-monitoring/basic-concepts/user-actions#custom-action)
 * Goal Performance

 <In the example below, a single problem as well as a sudden drop in conversion rate were identified.
 
![screenshot](https://github.com/AnnaRyb/Screenshots/blob/main/Deviations_.jpg)
**__Step 2__**. By clicking on the issue icon, you are transferred to the error details screen. It can be figured out what exact item is affected (for example, the drill-down functionality, and the impact area, such as main page). Other information include:
       * the exact type of error (such as JavaScript error)
       * the error map with a split into application, services and infrastucter as per below pattern

| Tables       |      Affected | Recovered| Monitored|
|------------  |:-------------:|------:   |------:   |
|Application   |       1       | 16005    |3456789   |
|Service       |       0       |   128    |567892    |
|Infrastructure|       0       |6789023   |51114678  |



