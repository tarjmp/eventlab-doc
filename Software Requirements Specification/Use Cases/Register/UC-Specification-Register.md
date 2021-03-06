# Use-Case Specification: Register
#### EventLAB

*Version 1.0*

---
## Table of Contents

&emsp; [1. Register](#1-register)<br/>
&emsp;&emsp; [1.1 Brief Description](#11-brief-description)<br/>
&emsp; [2. Flow of Events](#2-flow-of-events)<br/>
&emsp;&emsp; [2.1 Basic Flow](#21-basic-flow)<br/>
&emsp;&emsp;&emsp; [2.1.1 Narrative](#211-narrative)<br/>
&emsp;&emsp;&emsp; [2.1.2 Activity Diagram](#212-activity-diagram)<br/>
&emsp;&emsp;&emsp; [2.1.3 Mockups](#213-mockups)<br/>
&emsp;&emsp; [2.2 Alternative Flows](#22-alternative-flows)<br/>
&emsp;&emsp;&emsp; [2.2.1 Request New Confirmation E-Mail](#221-request-new-confirmation-e-mail)<br/>
&emsp; [3. Special Requirements](#3-special-requirements)<br/>
&emsp; [4. Preconditions](#4-preconditions)<br/>
&emsp; [5. Postconditions](#5-postconditions)<br/>
&emsp; [6. Extension Points](#6-extension-points)<br/>

## 1. Register

### 1.1 Brief Description

The purpose of this use case is to create a new user account to allow any person to register to the application.

## 2. Flow of Events
### 2.1 Basic Flow
1. A guest enters the registration process by clicking the "Register" button on any page.
2. He fills in the required user data and transmits it via a click on the submit button.
3. The server checks the provided data and continues only on valid inputs. The user is asked to correct the data otherwise.
4. An automatic e-mail message is generated and sent by the system to verify the provided e-mail address.
5. The guest opens the e-mail and follows the activation link in the message.
6. A new user account is created and a new private calendar is set up for the user.
7. The user gets logged in and redirected to his user calendar.

#### 2.1.1 Narrative

![Feature File](../../Features/register.feature)

#### 2.1.2 Activity Diagram
![Activity Diagram Register](Activity-Diagram-Register.png)

#### 2.1.3 Mockups
##### Register Screen
![Mockup 1](Mockups/1%20-%20Register%20Screen.png)

##### Registration fails
![Mockup 2](Mockups/2%20-%20Fail%20Register.png)

![Mockup 3](Mockups/3%20-%20Fail%20Register.png)

##### Registration Screen filled in
![Mockup 4](Mockups/4%20-%20Register%20Screen%20filled%20in.png)

##### Confirmation Mail Screen
![Mockup 5](Mockups/5%20-%20Confirm%20Mail%20Screen.png)

##### User Calendar
![Mockup 6](Mockups/6%20-%20User%20Interface.png)



### 2.2 Alternative Flows

#### 2.2.1 Request New Confirmation E-Mail

The user might not receive a confirmation e-mail due to spam filters, technical issues, etc... In this case, he can request another one by simply clicking on the "send confirmation e-mail" link provided in the application.

 This will resend the same confirmation e-mail and will not affect the validity of the previous confirmation link.

## 3. Special Requirements
The guest must have a valid e-mail address and must be able to receive and open messages sent to this address.

## 4. Preconditions
The application is accessed via a guest account, so the user must not be logged in.

## 5. Postconditions
n/a

## 6. Extension Points

To calulate the function points for a specific use case we used the [TINY TOOLS FP Calculator](http://groups.umd.umich.edu/cis/course.des/cis525/js/f00/harvey/FP_Calc.html).

    Score:      36,58 Function Points
    Time spent: 3d 5h 9m
	
![Function Points Register](FP-Register.png)