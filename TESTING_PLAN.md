\#\# 1\. Overview  
This plan describes how this project will be tested.    
It connects requirements, test cases, expected results, and automated testing opportunities into one organized system.

\---

\#\# 2\. Requirements / User Stories  
List the main user stories your tests must cover.

\- \*\*US-1 — Game Is Compatible with PC & Mobile\*\*  
  \- Acceptance Criteria:  
    \- Both PC and Mobile players can join a match at the same time (Crossplay)  
    \- Mobile Inputs/Outputs match PC

\- \*\*US-2 — Game accepts controller inputs \*\*  
  \- Acceptance Criteria:  
    \- Games Accepts and responds to Xinputs when connected  
    \- Gamepad binds for controller

\---

\#\# 3\. Test Procedures  
Each test procedure must include:    
• Related requirement    
• Setup    
• Steps    
• Expected result   
• Automation decision  

\#\#\# Test Case T-1: Connection Tests  
\- \*\*Related Requirement(s):\*\* US-1  
\- \*\*Purpose:\*\* Both PC and Mobile can connect  
\- \*\*Setup:\*\* Javascript for setting up servers and joining them   
\- \*\*Test Steps:\*\*  
  1\. Create a Match with PC as the server host  
  2\. Have a mobile device join that server  
  3\. Repeat steps 1-2 but with mobile as host  
\- \*\*Expected Result:\*\* Both can join each other without any abnormalities  
\- \*\*Automation Candidate:\*\* No, Whether it works at all is more important than specific results

\#\#\# Test Case T-2: Interaction Tests   
\- \*\*Related Requirement(s):\*\* US-1  
\- \*\*Purpose:\*\* Both PC and Mobile can interact with each other  
\- \*\*Setup:\*\* Javascript for servers, player actions, inputs, and outputs  
\- \*\*Test Steps:\*\*  
  1\. Create a Match for both to join  
  2\. Check That Actions on mobile match PC and vise versa  
  3\. Record results of interactions  
\- \*\*Expected Result:\*\* Both can join each other without any abnormalities  
\- \*\*Automation Candidate:\*\* Yes, It is important that interactions match between both

\#\#\# Test Case T-3: Controller Connection  
\- \*\*Related Requirement(s):\*\* US-1  
\- \*\*Purpose:\*\* Controllers are accepted as input devices on both PC and Mobile devices  
\- \*\*Setup:\*\* Javascript for controller Inputs  
\- \*\*Test Steps:\*\*  
  1\. Connect Controller to PC using USB  
  2\. See if inputs on controller both work in Menu and Matches  
  3\. Repeat 1-2 with Bluetooth  
  4\. Repeat 1-3 with Mobile  
\- \*\*Expected Result:\*\* Controller Connects and can use all game functions by itself  
\- \*\*Automation Candidate:\*\* No, only functionality Needs to be reported

\#\#\# Test Case T-4: Controller Connection  
\- \*\*Related Requirement(s):\*\* US-1  
\- \*\*Purpose:\*\* Controller Inputs changed to different inputs and still function  
\- \*\*Setup:\*\* Javascript for controller Inputs and changing them  
\- \*\*Test Steps:\*\*  
  1\. Connect Controller to PC  
  2\. See if default inputs on controller work  
  3\. Change Inputs / Bindings in settings in game  
  4\. See if new inputs on controller work  
  5\. Repeat 1-4 with Mobile  
\- \*\*Expected Result:\*\* Changed Inputs still do their expected outputs  
\- \*\*Automation Candidate:\*\* No, only functionality Needs to be reported

\---

\#\# 4\. Expected Results  
Summaries of expected outcomes:

\- \*\*Test T-1:\*\* Expected → "PC and Mobile connect without any abnormalities"  
\- \*\*Test T-2:\*\* Expected → "Game Interactions on PC and Mobile match"  
\- \*\*Test T-3:\*\* Expected → "Controller simply connects to PC and Mobile without difficulty"  
\- \*\*Test T-4:\*\* Expected → "Controller Bindings can be changed without issue"

\---

\#\# 5\. Automated Test List  
Automation is ideal for repetitive, rule-based, or high-volume tests.

\#\#\# Automated Test Candidate: T-2  
\- Why automate: Multiple interactions are to be tested and results should always repeat

\---

\#\# 6\. Boundary & Edge Case Reference  
Bring in your boundary/edge cases.

\- \*\*B-1 — Latency\*\*  
  \- Related Requirement: US-1  
  \- Expected Behavior: Mobile and PC behavior should match even on worse or better connections

\---

\#\# 7\. Traceability Summary  
Requirement → Test Case(s) → Expected Result → Automation

Example:  
\- \*\*US-1\*\* → T-1, T-2  → PC & Mobile work, PC & Mobile do the same things T-2 → No, Yes   
\- \*\*US-2\*\* → T-3, T-4  → Controller connects to PC & Mobile, Controllers can change Bindings → No, No

\---

\#\# 8\. Plan Status  
\- Last Updated: 12/8/2025  
\- Requirements Covered: US-1, US-2  
\- Requirements Not Covered Yet: unknown  
\- Automated Tests Identified: T-2  
