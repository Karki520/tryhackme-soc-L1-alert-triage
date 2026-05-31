# Task 5 - Alert Triage Workflow Notes

**Room:** SOC L1 Alert Triage - TryHackMe   
**Topics:** How to triage an alert step by step

### Part 1: Triage Workflow - 3 Steps

After selecting the right alert, we cannot jump directly to a decision. We must follow a proper process.

#### 1. Initial Actions
**Purpose:** Take ownership of the alert + prevent other analysts from working on it

**Steps I need to do:**
1. **Assign to myself** - Become the owner of the alert. Now the responsibility is mine.
2. **Move to In Progress** - Change status. So no one in the team does duplicate work.
3. **Read details first** - Read alert name, description, key indicators. Don't investigate blindly.

**Why:** If not assigned, 2 people will work on the same alert. Waste of time in SOC.

#### 2. Investigation
This is the toughest step. Technical knowledge is needed here.

**If company has Workbooks/Playbooks:**
Follow SOP step by step. Each alert type has a different playbook. Easy.

**If no playbooks - 4 things to check:**
1. **Who is under threat?** - Which user is affected? Hostname, IP, network, website?
2. **What is the action?** - What is the alert saying? Suspicious login, malware, phishing attack?
3. **Check surrounding events** - What happened 5 min before/after the alert? Make a timeline. Attack chain will be clear.
4. **Verify with threat intel** - Check IP, MD5, domain on VirusTotal, AbuseIPDB. Is it a real threat or not?

**Note to self:** Don't make decisions in a hurry. If context is missed, I will give False Negative. Big risk.

#### 3. Final Actions
After investigation, 2 things need to be done. This is the final work of L1.

1. **Decide Verdict** - Is the alert malicious or not?
   - True Positive = Real attack happened 
   - False Positive = It was noise, nothing happened 
2. **Write detailed comment** - Write your steps. What you checked, why you gave that verdict. L2 should understand after reading.
3. **Move to Closed** - Change status to Closed on dashboard. Work done.

### Part 2: SOC Dashboard Notes

**Important TryHackMe tip:**
If triage is correct but flag is not received, it means some value is set wrong - Verdict, Severity, Status etc.

**Fix:** There is a `Restart` button at top right corner. Click and reset SOC dashboard. Then triage again.

### My Summary
Formula: Pick → Assign → In Progress → Read → Investigate 4 things → Verdict + Comment → Close

Earlier I thought L1 just closes alerts. Now I understand every step has a reason. If process is not followed, something will be missed.
