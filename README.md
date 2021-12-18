# Session Replay, an eagle-eyed error detection tool


Have you ever wondered if it is possible to detect application flaws in a split second? >It is now possible with the Session Replay feature.
This is how it works.

  **Example scenario**
  >Imagine an online shop, www.performancewear.com that sells clothing and accessories through a single-page application running on Amazon AWS.
  
  **Problem**
  >Ashley is a client who was trying to place her order via website form but was unable to complete her transaction. After filling in a few fields, she found out that the system  froze and remained unresponsible despite several trials. 
  
  **Approach**
  >The Dynatrace platform's user-friendly, AI-powered dashboard replays all steps taken by Ashley and detects suspicious behavior.
  
  **Outcome**
 >Inefficiences are determined and mitigated.
 
Whenever you suspect that an error occurred, you just need to perform a few steps to precisely determine the cause of failure and repair it immediately.

 **__Step 1__**. Check the Dynatrace dashboard for open issues and deviations. You can see critical areas organized into themed cards, including
 * Problems
 * Smartscape
 * Applications
 * Synthetic Monitors
 * Databases
 * Application Performance
 *  Goal Performance
 In the example below, one problem and a sudden drop in conversion rate were identified.
![screenshot](https://github.com/AnnaRyb/Screenshots/blob/main/Deviations_.jpg)
Step 2. By clicking the issue icon, you are moved to the error details screen. It can be figured out easily what exact item is affected (for example, the drill-down functionality, and the impact area, such as main page). Other information include:
       the exact type of error (such as JavaScript error)
       the error map with a split into application, services and infrastucter as per below pattern

| Tables       |      Affected | Recovered| Monitored|
|------------  |:-------------:|------:   |------:   |
|Application   |       1       | 16005    |3456789   |
|Service       |       0       |   128    |567892    |
|Infrastructure|       0       |6789023   |51114678  |


| Tables        | Are           | Cool  |
| ------------- |:-------------:| -----:|
| col 3 is      | right-aligned | $1600 |
| col 2 is      | centered      |   $12 |
| zebra stripes | are neat      |    $1 |
