# Literature review

* process mining
* educational process mining
* Concept drift
* complexity
* other attempts

# Scope

* Major university
* Complete database
* holistic view
* focus on the end user

# Our data

* Six million events
* 300k students
* 50 years
* 1200 courses
* 16k subjects

# Our problem with our data

* Veracity
* Variance in course structure
* Size
* end-user

## Introduction
Students thrive not only for knowledge but also good outcomes. How can learners build systems that help students identify their best learning pathway? In this work, we present with the difficulties presented when trying to answer this question and we provide an initial tool to visualise outcomes.

Learning is a pathway, made of actors (students), events (subjects) and outcomes (marks) that occur in an organized course structure thoughout a limited timeline. In this sense, it is no more than common sense to think that, in education, appliying data mining techniques such as process mining is a good idea. Some previous work has been performed in the area [ref]  with different levels of sucess, [find the ref] very clearly defines the different key-points in the process, either be drop outs or clustering student behaviours.


Educational process mining has been tried before in small samples[refs], and previous work have uncovered many of the issues with this sort of processes. The work by [ref] does this understanding beautifully. In this study we take this concept a step further by increasing our population to a whole university and the timescale to decades. In such a high-level approach, we define new challenges and problems and how to adress educational process mining at scale.


In a nutshell, learning pathways do not behave like more traditional operational processes. They are much more  convoluted. In the past, clustering and minimizing the complexity of the patways was used effectiveley [ref] to tackle this problem and to extract value from the information. We think this solution, though usefull, simplifies the outcomes and severeley overlooks the importance of outlier pathways in the learning pathway.


The reason why process mining in education is so difficult has to do with the variability of events and mostly, in our case, with the concept drift issue. As said before, Cairns et al define such challenges very well and, like many other propose clustering to overcome them. In doing process mining for students following a degree pathway by enroling into subjects, one is bound to the ever changing nature of course structures and the apparent randomness of elective choices by students, especially when dealing with transdiciplinary courses, the pathways become nearly unique. Also, the structure of the pathway has no defined return points. This makes the underliying structure flexible and difficult to predict when moving outside a course and especially a faculty.

In this article we propose a different approach. Instead of minimizing the variability, we embrace that uncertanty and developed an exploratory application built for end-users: course coordinators, lecturers, or students. This tool provides insight on the pathway outcomes without having to deal with the complexity of the process. Although it is a more  simplistic approach to process mining, it scales well and provides good overall information.

## Scope

We set ourselves to understand the learning pathways of students at the University of Technology Sydney in any given course, and how the student results in a subject would historically affect the results in another different subject. This is important as it enables prospective students to understand what happened to previous cohorts that have the same characteristics as themselves in subjects they want to undertake. This will, hopefully, motivate students into choosing pathways they are more happy about, and fare better at subjects. On the other side of the coin one could argue that it favours underporformance as students can also choose more attainable subjects for their course. Either way, getting information on what happended historically to similar students helps these students perfom more informed decisions. We also wanted to make a system available to all levels of users in the university lecturing staff, from course coordinators to lecturers, it is important for their perfomance to better understand the performance of subjects and courses to whom they are connected.

## The data

Our data comes from the [university datawarehouse guys names] historical records of 6126013 enrollements in subjects in a period spanning for 50 years, though most of these enrollements happened in the last 20 years. This accounts for 317681 anonymous unique Id's or students.
In the dataset, there are 1297 unique courses and 16210 subjects in total, quite a lot more than the 495 courses and 2062 subjects available in 2015. This is because courses and subject nomenculature and structure change, sometimes even more than once a year. Therefore, subjects and courses have been added and removed during the timeline. As it is expectable, one should not find the same courses and subjects being lectured today that were available 50 years ago. The data contains information about the student background, their course and grades attained, as well as when then took the subject and when it was completed. Unfortunateley we only have information on the day a grade was given, not when the student started the subject, though there is information of the year the subject was available, hence we cannot calculate the duration of the enrollements.


This is a lage dataset that presents issues with both veracity and variability. Some of the elements have been altered to default values and there are many null and non available fields, though none empty. Because of the structure of the data, variability is also a large issue, as there is concept drifting issues in all courses. Moreover, we could not identify specific times when changes on subjects occur, as they are not periodical. For example, if we knew a subject would change every 5 years, then that could be factored. Moreover the data was obtained from different faculties that have different policies of collection and treatment of data.