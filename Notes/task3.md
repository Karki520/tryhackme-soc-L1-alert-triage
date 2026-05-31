# Task 3 - Alert Properties Notes

**Room:** SOC L1 Alert Triage  

### What I learned
In SOC, every alert has some common properties. SIEM can be different but these fields are almost same everywhere.

### Alert Properties

**1. Alert Time**
- When alert was created
- Alert triggers few minutes after actual event
- Ex: Event at 15:32, Alert at 15:35
- Use: For making timeline of attack

**2. Alert Name** 
- Short title of what happened
- Based on detection rule name
- Ex: Unusual Login Location, Email Marked as Phishing, RDP Bruteforce, Data Exfiltration
- Use: Quick idea of attack type

**3. Alert Severity**
- Shows urgency of alert
- Set by detection engineers, we can change if needed
- Levels: 
    - Low/Informational = not urgent
    - Medium/Moderate = need to check
    - High/Severe = check fast
    - Critical/Urgent = check immediately

**4. Alert Status**
- Tells if someone is working on it or not
- New/Unassigned = no one picked, I can take
- In Progress/Pending = someone is working
- Closed/Resolved = triage done, skip it

**5. Alert Verdict**
- Also called alert classification
- Tells if alert is real threat or noise
- True Positive = Real attack happened
- False Positive = No threat, just noise
- None = not decided yet, need investigation

**6. Alert Assignee**
- Analyst assigned to this alert
- Also called alert owner
- Assignee takes responsibility
- If L2 assigned, I don't need to work

**7. Alert Description**
- Explains what alert is about
- Usually has 3 parts:
  1. Logic of detection rule
  2. Why this activity = attack
  3. How to triage - optional

**8. Alert Fields**
- Actual values that triggered alert
- Comments from SOC analysts
- Ex: Hostname, Commandline, File name, MD5, IP
- Use: For investigation and checking on VirusTotal

### My workflow as L1
First check 3 things: Severity + Status + Verdict  
If Severity = High/Critical AND Status = New AND Verdict = None  
Then this alert is for me to triage.

### Note to self
Confused at first why so many fields. Now clear - Time for timeline, Severity for priority, Verdict for decision. Rest all are evidence.
