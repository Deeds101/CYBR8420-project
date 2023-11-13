# Part 1: Threat Modeling

### Data Flow Diagram

![image](https://github.com/Deeds101/CYBR8420-project/assets/107895832/0260b259-08b2-451b-854e-3346181445c4)

Diagram was compiled from individual team members' diagrams to mitigate redundancy and increase simplicity.

TMT Report - https://github.com/Deeds101/CYBR8420-project/blob/main/DFD-Final.htm

# Part 2: Observations

## Findings

1. ### **Spoofing the ITFlow Web Portal Process**

ITFlow Web Portal may be spoofed by an attacker and this may lead to information disclosure by Core Database. Consider using a standard authentication mechanism to identify the destination process.

**Justification:** Aside from authentication, there is no additional verification measure indicated for DB and web portal communication. May need additional control implemented.\
\
    **Finding** - Cross-Site Request Forgery: There was a concern with cross-site request forgery utilizing browser session cookies. A quick review showed that  protections may not have been in place for   this threat. However, after a review of the code, we found that ITFlow utilizes a specialized session token for sensitive functions to prevent cross-site request forgery attacks.
![image](https://github.com/Deeds101/CYBR8420-project/assets/107895832/3af35be5-9071-47b9-914d-5560132efe18)


2. ### Spoofing of Source Data Store Core Database

Core Database may be spoofed by an attacker and this may lead to incorrect data delivered to ITFlow Web Portal. Consider using a standard authentication mechanism to identify the source data store.

**Justification:** Core Database requires authorization, but additional verification requirements may need implemented.\
\
  **Finding** - We found input obfuscation is reasonably accounted for, and MFA exists within the software yet it is optional. It would be recommended to change this to an 'Opt-out' instead of an 'Opt-in' feature.

## Reflection
For this week's assignment, our team worked well together. We were able to have regularly scheduled meetings as well as add other meetings to accomodate the time necessary to plan out what was needed. One thing we did add this week to allow for more time for review of the diagrams of others was to ask that all diagrams be loaded into Git Hub by Friday. This gave all team members the time to review and add comments where necessary and gave time for those with comments on their diagrams to change those diagrams to better align with the evidence and comments given. We were also able to flex with the changing schedules of those in our group due to illness and work needs coming up throughout the week. Overall, the group continues to work well together and meet all necessary course requirements.
