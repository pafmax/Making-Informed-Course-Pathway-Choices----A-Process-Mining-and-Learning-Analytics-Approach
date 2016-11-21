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

# Start text

Learning is a pathway, made of actors (students), events (subjects) and outcomes (marks) that occur in a course thoughout a  timeline. In this sense, it is no more than common sense to think that, in education, appliying process mining is a good idea. Some previous work has been performed in the area and dealt with the challenge  with different levels of sucess, by understanding different key-points in the process, either be drop outs or clustering student behaviours.
In this study we take this concept a step further by increasing our scope to a whole university. In such a high-level approach, we define new challenges and problems and how to adress educational process mining at scale.


Educational process mining has been tried before in small samples, and previous work have uncovered many of the issues with this sort of processes. In a way, learning pathways do not behave like more traditional operational processes. They are much more  convoluted. In the past, clustering and minimizing the complexity of the patways was used to tackle this problem in order to extract value from the information. We think this solution simplifies the outcomes and overlooks the importance of outlier pathways in the learning pathway.


The reason why process mining in education is so difficult has to do with the variability of events and mostly, in our case, with the concept drift issue. Cairns et al define such challenges very well and, like many other propose clustering to overcome them. In doing process mining for students following a degree pathway by enroling into subjects, one is bound to the ever changing nature of course structures and the apparent randomness of subject choices by students, especially when dealing with transdiciplinary courses, that become nearly custom-built. Also, the structure of the pathway never has defined return points or start points, as students can, in theory, enrol in courses at every point of the course.

In this article we propose a different approach. Instead of minimizing the variability, we embrace that uncertanty and developed an exploratory application built for end-users, either course coordinators, lecturers or even students, that provides insight on the pathway outcomes without having to deal with the complexity of the process. Although it is a more simplistic simplistic approach to process mining, it scales well and provides good overall information.

## Scope

We set ourselves to understand the learning pathways of students at the UTS in any given course, and how the results in a subject would historically affect the results in another different subject.