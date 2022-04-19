![](Assests/Aspose.Words.cc97697c-63fc-481d-9044-2d20a7c2bcbe.001.png)

It’s Urgent - Flutter App

**About Me:** 

**Name:**	 	Akash Jaiswal

**University:**	National Institute of Technology, Tiruchirappalli, India

**Github:	 	[jaiakash (Akash Jaiswal) · GitHub](https://github.com/jaiakash)**

**LinkedIn:	<https://linkedin.com/in/akashjaiswal03>**

**Resume:	<https://github.com/jaiakash/resume-akashjaiswal/>**

**Location:**	Tiruchirappalli, Tamil Nadu, India

**Email:	 	<akashjaiswal3846@gmail.com>**

**Phone no:**	+91 96706 64115

**Timezone:**     	IST(GMT +5:30)

**Project:**      	[It's Urgent. | CCExtractor](https://ccextractor.org/public/gsoc/2022/itsurgent/)

**Discord:**      	Akash Jaiswal#3828

**Telegram:**      	<https://t.me/johnAKJ>

**Proposal:**      	<https://github.com/jaiakash/ccextractor_itsurgent_gsoc_proposal>

**Assets:**      	<https://drive.google.com/drive/folders/1qejQlF6bKNsXnbgLnuAFGoqZ1FrPcJye>

**Abstract:** 

This project aims to build an app that lets the caller decide if the call is urgent or not. It enables the user to determine that the specific call is critical and that the person should be disrupted from whatever they might be doing. Also mentioned here is that **this is not a dialer or phone app**. It's a **notification app that lets call decides for call urgency**, and it's up to the called person to pick up the call or not.

**Goals:**

Here are some goals for the project:

- UI for the app to select a contact to call and **choose the urgency rating and message of the call**.
- **Notification at the receiver end** shows the reason for the call and the urgency rating. It's up to the receiver to pick up the call or not.
- The receiver can “**urgent only notification**” if a certain rating is crossed. For example, if the user is in a meeting, they can set the limit rating to > 8/10 for notification. Otherwise, it can be 5/10 for any average use case.
- Show **floating UI** when the user makes a call from the stock dialer app to add the **“urgent rating**”.
- Add app to **quick tiles** of the phone for easy access..
- Once a feature is completed, I would be adding the  **unit tests** for the implemented feature.
- Setup **automatic CI/CD** on Github
- Setup **issue and PR template** on Github

**Implementation:**

App implementation is divided into the following **Milestones**

**(all dated mentioned below are of 2022)**

- **Community bonding period (April 19 to May 20)**
  - Interact and engage in the community, get to know my mentors and fellow students. Also, I would try to learn about other ongoing projects in the organisation, especially those related to flutter.
  - I will be discussing the **app flow** in detail with mentors. I would go with UI that is intuitive and easy to use and app flow that is efficient as much as possible.
  - I have already researched about some tools that would be used while building this app, for example, [Telephony library](https://pub.dev/documentation/telephony/latest/telephony/telephony-library.html), [call launcher](https://pub.dev/packages/url_launcher/score), [system alert,](https://pub.flutter-io.cn/packages/system_alert_window) broadcast receivers and background services, etc. During the community bonding period, I would explore more abou the tools that can be used to do the project and discuss the final choice of tools/ libraries with the mentor. Also, this app shouldn't be using many  third-party libraries packages, I will try to make it as simple as possible.
  - Since this app would be published on the **Google Playstore**, I would start preparing assets like icons.
  - **Finalise deadline and milestones** with the mentor and modify if any need arises.

![](Assests/Aspose.Words.cc97697c-63fc-481d-9044-2d20a7c2bcbe.002.png)

- **MILESTONE 1 (June 13 to June 22) - Discussion on the design and workflow of the app and setup of the basic dialer UI**
  - ![](Assests/Aspose.Words.cc97697c-63fc-481d-9044-2d20a7c2bcbe.003.png)![](Assests/Aspose.Words.cc97697c-63fc-481d-9044-2d20a7c2bcbe.004.png)
  - Coding officially begins
  - Setup the flutter project and repo on Github.
  - Create the app's design and get feedback on the plans from the mentor and any modifications by the mentor if given.
  - After getting confirmation for the design, I will go on coding part of the dialer UI of the app in the second week. The app will get all the contacts from users' contact lists and show them in the app. Users can choose any saved contact or dial a number for calling.

- **MILESTONE 2 (June 22 to July 1)- Firebase server setup**
  - ![](Assests/Aspose.Words.cc97697c-63fc-481d-9044-2d20a7c2bcbe.005.png)

- Setup the **firebase project** and set up **Firebase Cloud Messaging** and **Firebase Firestore**.
- Also, learn about the firestore database and research its querying and scaling abilities.
- Set up a [mock server](https://firebase.google.com/docs/rules/unit-tests) to test the features of the server. 
- **Firebase Firestore** would be used for storing the data since its better **integration with android** and **improved querying** compared to the firebase's real-time DB.
- Each user would have their unique id linked with the phone number. We can send notifications and query users using that id. We can implement as explained in this blog - [link](https://medium.com/firebase-developers/build-a-transactional-push-notifications-system-using-only-firebase-2b792bb25a60)

![](Assests/Aspose.Words.cc97697c-63fc-481d-9044-2d20a7c2bcbe.006.png)

![](Assests/Aspose.Words.cc97697c-63fc-481d-9044-2d20a7c2bcbe.007.png)

- **MILESTONE 3 (July 1 to July 12)- Auth and sign in (email and OAuth)**
  - This week will go on coding the auth and sign in for the user. Authentication would be done by phone verification. <https://firebase.flutter.dev/docs/auth/phone/>
  - ![](Assests/Aspose.Words.cc97697c-63fc-481d-9044-2d20a7c2bcbe.008.png)
  - **Google** and **Facebook OAuth** would also be implemented for easy sign-in.
  - The profile data and phone number would be saved on the server.

- **MILESTONE 4 (July 12 to July 29)- Decide urgency message and rating**
  - Setup **broadcast receiver** whenever a call is received, and a call is made, and display an appropriate notification regarding that.

![](Assests/Aspose.Words.cc97697c-63fc-481d-9044-2d20a7c2bcbe.009.png)![](Assests/Aspose.Words.cc97697c-63fc-481d-9044-2d20a7c2bcbe.010.png)

- Set the **urgency message and rating for any call**. The receiver will get a notification of the message and rating if the user has installed the app or will get a text message to install the app.

![](Assests/Aspose.Words.cc97697c-63fc-481d-9044-2d20a7c2bcbe.011.png)

- The notification would be delivered by [Firebase cloud messaging.](https://firebase.flutter.dev/docs/messaging/overview)
- Discuss the required changes for the completed milestones with the mentors.
- All the features would have been tested before, but now the app would be tested as whole in the **production environment**. Ensuring that none of code is breaking and will be solving any issue raised by mentor.
- By the end of the first week (24th July), the **basic version of app** would be ready in according to phase 1 evaluation.
- The features till that would be documented and i will post a **blog** for progress made till phase 1 **(Evaluation time July 25 to July 29).**

- **MILESTONE 5 (July 30 to August 11) - Feature “urgent only notification”**
  - Users can set “**notify for urgent calls only**” basically setting up the minimum rating for a call, so that he/she gets a notification. For example, the user has to go to a meeting. Then they can set min rating to 8/10, so for only very urgent call they get the notification. By **default,** it would be set to 5/10.
  - It would be implemented by filtering out the rating of incoming call. If urgency rating is more than the incoming call rating, then display the notification other wise not and call the call.
  - Add app to quick tiles of phone for easy access. User can enable and disable app from quick settings only. [Blog](https://medium.com/android-news/develop-a-custom-tile-with-quick-settings-tile-api-74073e849457)

![](Assests/Aspose.Words.cc97697c-63fc-481d-9044-2d20a7c2bcbe.012.png)

- **MILESTONE 6 (August 12 to August 22) - Final testing on devices and publishing on Play store**
  - By this time mentor would approved the design of app. Before uploading on play store, i will finish the final icon, banner, screenshot, and description needed while uploading on play store.
  - The app review takes time, so by that time i will start writing the **blog post**.
  - App is almost ready, the **app would be listed on play store** for “**early access**”. 
  - **Firebase Analytics** would also be setup for app. It provides many analytics tool built-in like **crashlytics**, **logging**, etc. I would see where user are struggling and try to improve in following weeks.

- **MILESTONE 7 (August 22 to September 6) - Show floating UI when the user makes a call from any dialer app.**
  - App would show **floating UI (android)** when user calls from any dialer app. User can write the reason for call and rating of urgency. Package - <https://pub.flutter-io.cn/packages/system_alert_window>

![](Assests/Aspose.Words.cc97697c-63fc-481d-9044-2d20a7c2bcbe.013.png)

- Final testing of app on various devices.
- **Blog post for the app and my gsoc experience till date.**
- **Release app on play store.**
- Hand over all the app, repo and firebase server config to the mentor for final evaluation

![](Assests/Aspose.Words.cc97697c-63fc-481d-9044-2d20a7c2bcbe.014.png) 

- **Optional MILESTONE** 
  - **Automatic CI/CD for repo for releasing builds**

If i get free time between i will also work on setting up ci/cd for the repo by **Github Actions** for automating many chore tasks like releasing builds, siging up apks, etc.

There are various tools listed on [flutter deployment doc](https://docs.flutter.dev/deployment/cd) like [codemagic](https://blog.codemagic.io/getting-started-with-codemagic/) and fastlane that could be used for setting up the workflow. Appropriate tools and actions would be implemented after discussion with mentor

  - **PR and issue template for bugs, features or feedback.**

User can **report bugs, request and give feedback** by ready-made templates on Github. These templates auto-populate the issue/pull-request description field and provide a skeleton framework that contributors can fill out. They help provide a baseline standard of informational quality and organisational rigour. 

- **Add a block list and sync across devices.**

User can **block ceratin people** if they feel their notification is annoying. Such contacts would be blocked to call too. 

Also **sync feature** would be implemented, so when a user login from another device then all logs will also be synced up. Such feature would be useful so user dont have to setup the settings, ratings, and block list when installing from new device.

This feature would be related to privacy, so i will be discussing with my mentor first whether to save sensitive data like contact and proceed accordingly.


**My background / Technical skills**

I am **Akash Jaiswal**, **2nd year engineering student at [National Institute of Technology, Tiruchirappali**](https://nitt.edu)**, India. My first encounter with programming was QBASIC in 6th grade. Then in class 7th, the language was changed to **Java**. My love for programming began at that stage. In my **high school,** i still remember making basic **android apps in the android studio** like tic tac toe game and age calculator, etc.

In my class 10th, i published my first app on Play Store, Sarkari Result All and one more app Learn Python. Both of these apps have **1k+ downloads,** that was a huge deal for class 10th kid. 

In my first sem, i started learning **c++** and **python**. I started doing **competitive programming** also. In Codechef my highest **rating is 1817 with 4 star** (userid [akashjaiswal03](https://www.codechef.com/users/akashjaiswal03)). Then i learned **android dev, web dev, flutter, react, node, django, graphql, fastapi, shell scripting, docker,, unity3d.** I started playing **CTF contests** during one of my college events.

Right now I am proficient in **app dev (both native and framework like react and flutter), and full-stack web dev (js, HTML, node, express, Django, react, flutter).** I use ubuntu 20.10 as my development machine and vscode and **sublime** as my text editors. Recently i tried learning server hosting, cloud and firebase.

I am also very active in **open source, college technical events and hackathons**. I participated in SIH 2022, DWOC, and TRI-NIT Hackathon. I won 3rd position in ICY Cup, 3rd position in code connoisseurs and 1st position in the Pragyan scavenger hunt. 1st position in IIT Roorkee Cryptotrader, 2nd position NIT Conclave Covalent event on Web3.

I was a member of [DeltaForce](https://delta.nitt.edu) , the official web team of NIT Trichy, where I worked as an **Android Developer** and **Full-Stack Web Developer**. With Delta, I got to work on various projects. Some of the projects like DWOC, [Delta Winter of Code](https://www.linkedin.com/company/delta-winter-of-code/?originalSubdomain=in) (open source competition like **GSOC** by students of NIT Trichy) or **Code Character** that was used by 5k+ people during  [Pragyan](https://www.pragyan.org/22/home/) the annual technical fest of NIT Trichy.

I am **Microsoft Learn Student Ambassador**, helping students of my college.  The MSP program enhances students’ employability by offering training in skills

not usually taught in academia, including knowledge of Microsoft technologies.

I am also a coordinator at [Technical Council (NIT Trichy)](https://www.linkedin.com/company/technical-council-nit-trichy/mycompany/), responsible for managing, ideating and supervising most things tech in the college. I worked on various campus development initiatives. Namely development of 3d website, wordle for NIT Conclave X.

My recent focus is on the **TecOS** initiative, **encouraging the open-source culture in our college**.

I am very active in open source. I try to participate in many of the open-source events happening. I participated in **KWOC, DWOC, and Hacktoberfest and this is my attempt in GSOC.** I am also actively involved in encouraging open-source culture in my college, I listed a few initiatives like org review, human of open source, etc under TeCOS.

Here are some of my projects.

**Contribution project** - 

[Delta Winter Of Code ](https://in.linkedin.com/company/delta-winter-of-code)website (a program similar to GSoC but by my college)

**Code Character 2022** 

An AI-based strategy game where user code their bot to attack other enemies while protecting their bases with robust defences 

<https://github.com/jaiakash/codecharacter-web-2022>

**Personal** **Projects** - 

<https://github.com/jaiakash/alphaq-file-server>

<https://github.com/jaiakash/Pawsome>

<https://github.com/jaiakash/snake-pygame>

<https://github.com/jaiakash/SpaceWar>

**Contributions to open source:**

**CCExtractor Beacon** - <https://github.com/CCExtractor/beacon/issues/160>

**CCExtractor Beacon** Backend - <https://github.com/CCExtractor/beacon-backend/issues/138>

**KWOC 2021** - <https://kossiitkgp.org/public-files/KWoC/2021-Certificates/Student/jaiakash.pdf>

**DWOC** - Participated as **Mentor** for Entrix  Organization in DWOC 2021

**Hacktoberfest -** Successfully completed Hacktoberfest 2021

**Hackerrank GHS** -<https://github.com/interviewstreet/ghs/pull/5>

**Ookla-Speedtest** - <https://github.com/sinha-debojyoti/Ookla-Speedtest.net-Crawler/pull/104>

**Codechef cards** -  <https://github.com/jaiakash/Codechef_Cards>

**Commitments:**

Most of the GSOC coding period lies during my college semester break so that I would work full time on the project. Only last month (August), I would be having my college classes, i would compensate it working on free time in weekends. I’m comfortable working anytime during this period. There won't be any gap or absences as such but in case of any emergency, I would inform my mentor beforehand.

**Weekly Commitment:** **40-50 hours**

I am more than ready to work well past my committed time if needed.
