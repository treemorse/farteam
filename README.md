<div align="center">
  <h1>Individual Programming Project Final Report</h1>
  <i>Cross-platform mobile app for fitness exercises</i>
  </br></br></br>
</div>

<p align="left">
  <b>
    Prepared by: Daniil Zondberg </br>
    Supervisor: Hadi Saleh </br>
    Date: May 28 2022
  </b>
</p>

# Abstract
During the last few years the fitness industry has experienced a significant decrease in revenue due to the pandemic[^1].
While many fitness employees were being laid off[^2], virtual training, home gyms and outdoor exercise became extremely popular[^1]. 
</br></br>
Based on this data, an assumption can be made that currently, the demand for fitness lessons from experienced instructors exceeds the supply.
This project's main goal is to provide jobs for fitness coaches, as well as to create an environment for ex gym members
to communicate with professional fitness instructors.
</br></br>
In order to achieve this goal, I have created a cross-platform mobile application for fitness instructors and their potential clients.
The main function of the app is a lesson-builder feature, which provides the users with an opportunity to specify the type 
of fitness lessons they want to give/take. To establish frictionless communication between users, this information, 
combined with a link to its creator, is placed on a map based on the specified location in the form of a pinpoint.
</br></br>
>###### The application is soon to become a Farteam™ product[^3]. Code will not be provided due to the possibility of copyright infringement.

# Table of contents
1. [ Introduction. ](#intro) 
2. [ Review. ](#review)
3. [ Project Implementation. ](#primp)
4. [ Conclusion. ](#conc)
5. [ References. ](#ref)

<a name="intro"></a>
# Introduction
According to the relevant fitness industry statistics, the predicted industry revenue of more than $100bn was not achieved due to gym closures around the world. A Nielsen survey[^4] concluded that approximately 80% of the adult population exercise or have the desire to exercise regularly. Due to the lack of gyms caused by the pandemic and with the help of technological improvements in internet connectivity and streaming, virtual fitness services such as Peloton are increasingly becoming very popular. Before the restrictions, the online fitness market was valued at $6bn and in 2027 its worth 
is predicted to increase significantly, almost reaching $60bn dollars. 
</br></br>
Online fitness applications, however, lack *actually* useful feedback, experience and personal connection which professional fitness coaches can provide. A reasonable solution to this problem appears in the combination of the mobile app user experience and a personal fitness lesson given by an experienced instructor. 
The purpose of this project is to create a service which realizes the potential of this combination. Initially, the service is supposed to be realized as a MVP. After receiving the necessary funding, the product will serve as a protoype for future development. Thus, the main goal is to create a MVP and present it to investors.
</br></br>
>## Objectives:
>1. Assemble list of requirements
>2. Design app architecture
>3. Design UI
>4. Code the basis for future development
>5. Integrate DBs and APIs
>6. Implement functionality
>7. Test services
>8. Deploy app

<a name="review"></a>
# Review and comparative analysis
## Competition
The Farteam mobile app as a product faces competition on the following two markets:
</br>
1. Fitness app market
2. Freelance market

### Fitness apps
A thorough analysis of the fitness app market has shown that many mobile apps such as Strava™ or FitOn™ accomplish the job of motivating their users by providing them with daily goals and opportunities to communicate with their friends through an integrated and conveniently simplified social network. These two features allow users to experience the thrills of competition and achievement, which are necessary emotions for fitness lovers. Nevertheless, the Farteam app is intended for a different audience. The target audience mainly consists of people, for whom mentorship and professionalism are significant when it comes to self-improvement. The current popular fitness apps mostly provide simple guides, which are independently interpreted by the users. Thus, no analogues can be currently found on this market.

### Freelancers
All popular freelance platforms can be divided into two groups:
</br>
1. For freelancers with specific skills
2. For all types of freelancers

After conducting a research among the platforms of the first group, no eye-catching fitness-oriented freelance websites were found. Fitness instructors who are unable to work at a gym, mainly take orders on platforms from the second group. Since these platforms don’t belong to a certain category, there is no need in verifying the freelancers' professional skills before giving access to the platforms' services. The Farteam app, which is specifically designed as a platform for freelancing fitness coaches, guarantees high-quility services by verifying the instructors' identity and their experience in fitness.
</br></br>
Based on the analysis, the application will most likely do well, once deployed to the Play Store and App Store platforms.

## Requirements
### Funcitonal
1. Framework for cross-platform mobile app development
>I have chosen to use `Flutter`, because it has comprehensible state-management libraries and it renders widgets at a very high speed. React Native was also one of the reasonable candidates, but it was a bit to complex for a MVP.[^5]
2. Map API
>I have currently integrated `Yandex Maps` and `MapBox`, both seem to be good choices. MapBox allows unlimited requests for free, while Yandex Maps is very accurate in Russia, which is the starting which is the country, where the application will be released initially. Depending on the amount of money allocated for the MVP, one of the two will be chosen. For now it is Yandex Maps.[^6][^7]
3. Database for user data, lesson data, etc.
> `Firebase` appears to be the sound choice, because it is a free-for-testing cloud solution, which is perfectly compatible with Flutter. It provides authentication methods, various kinds of storage and internal functionality for app deployment. It is perfect for a MVP.[^8]

### Non-functional

1. Verification document
2. A Terms of Service document
3. A General Agreement
4. Contract for instructors

>##### These non-functional requirements are being developed by our legal team.

<a name="primp"></a>
# Project Implementation
## Architecture
The application's backend is completely controlled by Firebase. This includes:
1. Authentication methods
2. Databases
3. Hosting

<img src="https://github.com/treemorse/farteam/blob/main/assets/Auth.jpg" align="left" width="384" height="244">

### Authentication method
The authentication process requires an email address and a password.
</br>
Any user can create an account, log in and reset their password.
</br>
Authentication data, which includes the user ID and their email is stored automatically

<br clear="left"/>

### Databases
Only one type of database is used in the application: the Firestore Database. It contains two collections: 
1. Users
2. Lessons

Each row in the users collection contains a user ID, a verification checker and the user's profile information.
The rows in the lessons collection contain all the information given by some user, including the creators ID and an array of user IDs, which represents people who are interested in some particular lesson.

### Hosting
Hosting is automatically provided by Firestore. The application deployment process, which has been tested before is also very simple.

<a name="conc"></a>
# Conclusion

<a name="ref"></a>
# References 
[^1]: [Wellness Creative Co.](https://www.wellnesscreatives.com/fitness-industry-statistics-growth/)
[^2]: [Finances Online](https://financesonline.com/gym-membership-statistics/#:~:text=In%202019%2C%20American%20adults%20spent,memberships%20(Finder%2C%202020).)
[^3]: [Farteam](https://farteam.club/)
[^4]: [Nielsen survey](https://emduk.org/wp-content/uploads/2018/10/Consumer-fitness-trends-Nielsen-research-2013-exec-summary.pdf?x49114)
[^5]: [Flutter](https://flutter.dev/)
[^6]: [Yandex Maps](https://yandex.ru/dev/maps/?p=realty)
[^7]: [MapBox](https://docs.mapbox.com/api/overview/)
[^8]: [Firebase](https://firebase.google.com/)
