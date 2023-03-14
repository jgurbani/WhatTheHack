# Challenge 01 - OneAgent Observability on VM

[< Previous Challenge](./Challenge-00.md) - **[Home](../README.md)** - [Next Challenge >](./Challenge-02.md)

<!--
***This is a template for a single challenge. The italicized text provides hints & examples of what should or should NOT go in each section.  You should remove all italicized & sample text and replace with your content.***
-->
## Pre-requisites
Make sure you meet all the success criteria for Challenge0

<!--
*Your hack's "Challenge 0" should cover pre-requisites for the entire hack, and thus this section is optional and may be omitted.  If you wish to spell out specific previous challenges that must be completed before starting this challenge, you may do so here.*
-->

## Introduction

<!--
*This section should provide an overview of the technologies or tasks that will be needed to complete the this challenge.  This includes the technical context for the challenge, as well as any new "lessons" the attendees should learn before completing the challenge.*

*Optionally, the coach or event host is encouraged to present a mini-lesson (with a PPT or video) to set up the context & introduction to each challenge. A summary of the content of that mini-lesson is a good candidate for this Introduction section*

*For example:*

When setting up an IoT device, it is important to understand how 'thingamajigs' work. Thingamajigs are a key part of every IoT device and ensure they are able to communicate properly with edge servers. Thingamajigs require IP addresses to be assigned to them by a server and thus must have unique MAC addresses. In this challenge, you will get hands on with a thingamajig and learn how one is configured.

-->
While choosing the right migration strategies, such as re-hosting or re-architecting, one must assess the different risks, costs, and benefits. However, often the details of what is where and what is dependent on what within the technical stack is missing or poorly documented. All that may exist is out of date diagrams and a mix of monitoring tool metrics that must be "stitched" together.

Not having enough details about the current environment is hindering organizations ability to make the right decisions when planning what to migrate and when.

To address this problem, Dynatrace’s OneAgent can automatically discover the application, services, processes and to build a complete dependency mapping for the entire application environment. So, let’s begin!

### Lab Setup Diagram
Referring to the picture below, here are the components for lab 1.

#1 . Sample Application

Sample app representing a simple architecture of a frontend and backend implemented as Docker containers that we will review in this lab.

#2 . Dynatrace monitoring

The Dynatrace OneAgent has been installed by the workshop provisioning scripts and is communicating to your Dynatrace tenant.

#3 . Load generator process

A docker processes that sends simulated user traffic to the sample app using Jmeter run within a Docker container. You will not need to interact with this container; it just runs in the background.
![](images/challenge1-sampleapp-setup.png )




## Description

<!--
*This section should clearly state the goals of the challenge and any high-level instructions you want the students to follow. You may provide a list of specifications required to meet the goals. If this is more than 2-3 paragraphs, it is likely you are not doing it right.*

***NOTE:** Do NOT use ordered lists as that is an indicator of 'step-by-step' instructions. Instead, use bullet lists to list out goals and/or specifications.*

***NOTE:** You may use Markdown sub-headers to organize key sections of your challenge description.*

*Optionally, you may provide resource files such as a sample application, code snippets, or templates as learning aids for the students. These files are stored in the hack's `Student/Resources` folder. It is the coach's responsibility to package these resources into a Resources.zip file and provide it to the students at the start of the hack.*

***NOTE:** Do NOT provide direct links to files or folders in the What The Hack repository from the student guide. Instead, you should refer to the Resource.zip file provided by the coach.*

***NOTE:** As an exception, you may provide a GitHub 'raw' link to an individual file such as a PDF or Office document, so long as it does not open the contents of the file in the What The Hack repo on the GitHub website.*

***NOTE:** Any direct links to the What The Hack repo will be flagged for review during the review process by the WTH V-Team, including exception cases.*

*Sample challenge text for the IoT Hack Of The Century:*

In this challenge, you will properly configure the thingamajig for your IoT device so that it can communicate with the mother ship.

You can find a sample `thingamajig.config` file in the `/ChallengeXX` folder of the Resources.zip file provided by your coach. This is a good starting reference, but you will need to discover how to set exact settings.

Please configure the thingamajig with the following specifications:
- Use dynamic IP addresses
- Only trust the following whitelisted servers: "mothership", "IoTQueenBee" 
- Deny access to "IoTProxyShip"

You can view an architectural diagram of an IoT thingamajig here: [Thingamajig.PDF](/Student/Resources/Architecture.PDF?raw=true).

-->

## Objectives of this Challenge

🔷 Review Dynatrace OneAgent

🔷 Review real-time data now available for your application that you have to migrate

🔷 Review how Dynatrace helps with modernization planning

### Tasks

- Review OneAgent Status for Monolith VM to ensure its reporting in to Dynatrace UI
    - https://www.dynatrace.com/support/help/setup-and-configuration/dynatrace-oneagent/installation-and-operation/linux/installation/install-oneagent-on-linux#youve-arrived

- Review the Data on the Hosts monitoring screen
    - https://www.dynatrace.com/support/help/how-to-use-dynatrace/hosts/monitoring/host-monitoring

-   Review Smartscape screens
    - https://www.dynatrace.com/support/help/how-to-use-dynatrace/smartscape/visualize-your-environment-topology-through-smartscape

-  Review Services Screens
  - https://www.dynatrace.com/support/help/how-to-use-dynatrace/services

-   Analyze Service flow
    - https://www.dynatrace.com/support/help/how-to-use-dynatrace/services/service-flow

-  Analyze Service Backtrace
    - https://www.dynatrace.com/support/help/how-to-use-dynatrace/services/analysis/service-backtrace

-  Analyze Database screen
    - https://www.dynatrace.com/support/help/how-to-use-dynatrace/databases/analyze-database-services

-  Analyze Technologies Screen
    - https://www.dynatrace.com/support/help/how-to-use-dynatrace/process-groups/monitoring/overview-of-all-technologies-running-in-my-environment 

## Success Criteria

<!--
*Success criteria goes here. The success criteria should be a list of checks so a student knows they have completed the challenge successfully. These should be things that can be demonstrated to a coach.* 

*The success criteria should not be a list of instructions.*

*Success criteria should always start with language like: "Validate XXX..." or "Verify YYY..." or "Show ZZZ..." or "Demonstrate you understand VVV..."*

*Sample success criteria for the IoT sample challenge:*

To complete this challenge successfully, you should be able to:
- Verify that the IoT device boots properly after its thingamajig is configured.
- Verify that the thingamajig can connect to the mothership.
- Demonstrate that the thingamajic will not connect to the IoTProxyShip
-->
🔷 Review all Dynatrace screens on analyzing dependencies for your application

🔷 Review how Dynatrace helps with modernization planning

## Learning Resources

<!--

_List of relevant links and online articles that should give the attendees the knowledge needed to complete the challenge._

*Think of this list as giving the students a head start on some easy Internet searches. However, try not to include documentation links that are the literal step-by-step answer of the challenge's scenario.*

***Note:** Use descriptive text for each link instead of just URLs.*

*Sample IoT resource links:*

- [What is a Thingamajig?](https://www.bing.com/search?q=what+is+a+thingamajig)
- [10 Tips for Never Forgetting Your Thingamajic](https://www.youtube.com/watch?v=dQw4w9WgXcQ)
- [IoT & Thingamajigs: Together Forever](https://www.youtube.com/watch?v=yPYZpwSpKmA)

-->
- [Dynatrace OneAgent documentation](https://www.dynatrace.com/support/help/setup-and-configuration/dynatrace-oneagent)
- [Dynatrace OneAgent VM Exntesion](https://www.dynatrace.com/support/help/technology-support/cloud-platforms/microsoft-azure-services/oneagent-integration/integrate-oneagent-on-azure-virtual-machines/)

## Tips

<!--
*This section is optional and may be omitted.*

*Add tips and hints here to give students food for thought. Sample IoT tips:*

- IoTDevices can fail from a broken heart if they are not together with their thingamajig. Your device will display a broken heart emoji on its screen if this happens.
- An IoTDevice can have one or more thingamajigs attached which allow them to connect to multiple networks.

-->

## Advanced Challenges (Optional)

<!--
*If you want, you may provide additional goals to this challenge for folks who are eager.*

*This section is optional and may be omitted.*

*Sample IoT advanced challenges:*

Too comfortable?  Eager to do more?  Try these additional challenges!

- Observe what happens if your IoTDevice is separated from its thingamajig.
- Configure your IoTDevice to connect to BOTH the mothership and IoTQueenBee at the same time.
-->