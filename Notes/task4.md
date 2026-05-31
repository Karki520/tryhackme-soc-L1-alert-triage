# Task 4 - Picking the Right Alert Notes

**Room:** SOC L1 Alert Triage  
**Topic:** How to prioritize alerts in SOC

### What I learned today
Every SOC team has their own rules for which alert to check first. But most SOCs use same basic logic in SIEM/EDR. 

### 3 Steps to pick right alert

**1. Filter the alerts first**
- Don't take alerts that are already reviewed or in progress
- Only pick "New" and "Unassigned" alerts 
- Reason: Duplicate work waste karta hai time. Team me coordination jaruri hai

**2. Sort by severity**
- Order: Critical -> High -> Medium -> Low
- Why: Detection engineers design rules like this. Critical alerts = more chance of real attack + more damage
- For me: Always start from top. Critical miss ho gaya toh problem

**3. Sort by time**
- After severity, check oldest alerts first
- Why: Older breach me hacker already data chori kar raha hoga. New alert wala abhi scan hi kar raha hai
- Example: 2 breaches hai. Purana wala hacker already exfiltrate kar raha, naya wala abhi discovery phase me

### My takeaway
Priority formula = Status + Severity + Time
1. Status = New/Unassigned only
2. Severity = Critical/High first  
3. Time = Oldest first


### Note to self
Pehele laga tha sabse naya alert important hota hai. Galat tha. Purana alert = hacker ko zyada time mila = zyada damage possible.
