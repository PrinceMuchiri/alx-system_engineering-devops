0x19. Postmortem

Issue Summary:
On May 10th, 2023 at 3:00 PM EST, the login service for our web application experienced a 30-minute outage. During this time, users were unable to log in to their accounts and were met with error messages. Approximately 70% of users were affected, resulting in a significant loss of potential revenue for the company.
Timeline:
3:00 PM: The outage was detected when users began reporting issues logging in.
3:02 PM: The monitoring system triggered an alert for high error rates in the login service.
3:05 PM: The team began investigating the issue, assuming it was a problem with the authentication server.
3:10 PM: The team discovered that the authentication server was not the root cause and began investigating other parts of the login service.
3:20 PM: The team identified a recent code deployment as the cause of the issue and began reverting the deployment.
3:30 PM: The login service was restored to full functionality, and users were able to log in without issue.
Root Cause and Resolution:
The root cause of the outage was a bug introduced in the recent code deployment that caused the login service to crash. The bug was due to a missing error check in the code, which caused an unhandled exception that led to the service failure. The issue was fixed by reverting the problematic code deployment and updating the code to include proper error handling.
Corrective and Preventative Measures:
To prevent similar outages in the future, we will implement the following measures:
Improve our testing process to catch potential issues before code deployment.
Implement more comprehensive error handling in our code.
Increase the monitoring and alerting for the login service to detect issues more quickly.
Review our code deployment process to ensure that proper checks and balances are in place to prevent problematic code from being deployed.
In conclusion, the login service outage on May 10th was caused by a bug introduced in a recent code deployment. The issue was promptly resolved by reverting the deployment and updating the code to include proper error handling. We have identified corrective and preventative measures to prevent similar outages in the future and will implement them as soon as possible. We apologize for any inconvenience this may have caused our users and are committed to providing a reliable and seamless experience for all.


