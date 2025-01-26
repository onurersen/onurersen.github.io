---
layout: page
title: "Automation and Orchestration"
author: "Berat Onur Ersen"
date: 2019-03-04
draft: false
permalink: /2019-03-04-automation-and-orchestration/
---

Automation and orchestration are two domains those go hand in hand, however, shall not be mixed up.
Sometimes we assume that we already know some concepts but when we just try to answer the simplest questions, unfortunately, we get confused.  
In this short post, I will try to explain things starting with back to basics.

---

**Automation Concept**

I like **"Shepherd and the Dog"** analogy that I made up myself :) :

If a shepherd can do shepherding without a dog then why does he need a dog? Of course, he can shepherd all the sheep himself,
 but when there is a dog right there then he can sleep conveniently under a tree. By the way, his nimble dog would be taking care of the herd :) In this analogy, the dog is the automation. Humans need more important things to do (apart from sleeping), so we need dogs to take care of usual things while we work hard on other important tasks.
 
![picture alt](/img/automation-and-orchestration/funny_dog.gif)

After untangling why we need automation, let's discuss basic automation types.
 
The most primitive type of automated task/process can be extracting information from a system continuously for monitoring. 

**_Example:_**
I would be using a script to gather stats like my last commit, 
last successful build, biggest file in the project etc.

Another type of automation would occur as a result of a conditional change within a system. If something happens in a system, 
then it will trigger some job to be done automatically.

**_Example:_**
Automation project I had done with my [indoor cycling sessions.](https://onurersen.github.io/2019-02-28-indoor-cycling-automation/)

But what if I create a scheduled pipeline execution?

Yes, that is another kind of automation when I schedule a pipeline execution to build the project and synch sessions with graphs every day at 3 a.m. 

Last automation type is when we lock our internet banking password, trying to log in having Caps Lock on :) 
We can go to forums and our bank's FAQ or we can simply pick up the phone and call the call-center to chat with an agent-bot to unlock our password.
That bot helps us provide some information to re-create our password. Here we use the advantage of our bank automating password reset process using nothing but customer himself/herself.

To recap we have below automation types:

* **auto-execute** tasks requiring manual work (manual task automation)
* **scheduling** tasks to be executed in particular timing (scheduled automation)
* getting **triggered** as a result of manual **interaction** (triggered automation)
* processes helping humans to **solve their problems on their own** (self-service automation)

The most important advantage of automation is minimizing manual interactions (human touch) - making humans deal with _human-touch-requiring_ problems.

![picture alt](/img/automation-and-orchestration/tinder.gif)

---

**Orchestration Concept**

Let's say we automated everything. Lots of things happening without our control, but how will these processes will be managed?
Who will coordinate those unmanaged automated tasks? How will the outcome of those tasks be evaluated?

There we need something like a maestro to orchestrate all the things going on. Unmanageable automation requires orchestration.

Think that we have an expense reporting system. We report those expenses belonging latest business trip.
Everything's bundled and put on our manager's desk. 
She approves our docs and someone needs to carry expense information to a higher manager (bills, invoices etc.). Then later those docs are needed to be approved by one of 3 grandfather managers. 
Due to which grandfather manager approves, expense goes to different grand-grand father manager and then to HR and then to Finance and then your brain blows up :)

![picture alt](/img/automation-and-orchestration/blown_up.gif)

Here we need a **workflow** orchestration. Automated online expense reporting system working integrated with a workflow. All the manual work goes through some particular stage and routes meeting certain conditions. Here we need is not straight automation rather an orchestration.

To coordinate and monitor the execution of procedures automated system needs some written or programmed routines list which is called a **runbook**. Physical forms of these runbooks would be like 
 military emergency procedures are applied in case of an emergency situation:

1. alert team leader
1. evacuate staff
1. rescue high-value documents
1. call the main military base
 
![picture alt](/img/automation-and-orchestration/emergency_cat.gif)

Digital runbooks need a server (to host), a runner process (to execute tasks, i.e. Gitlab Runner) and a data-layer (to log or save data).

Final orchestration type I will mention in this post is **pipeline orchestration**.

Pipeline concept is very familiar for people working on DevOps domain. In terms of CI / CD, the chain of processes are designed and deployed using pipelines. 
During each stage on a pipeline, something for delivery is done. Pipelines are deemed as orchestrators towards delivery. 
Through a pipeline sourcecode is built, it is tested, versioned and deployed.

Last but not least; orchestrator systems can communicate with systems they orchestrate using different methods;

* orchestrator and system being orchestrated running on a **local machine** (orchestrating on local)
* via a **remote communication protocol** (orchestrator and system being orchestrated is communicated using a specific protocol)
* **an agent communicating with orchestrator is installed** on the system being orchestrated 
* **a service communicating with orchestrator is installed** on the system being orchestrated

---

End of the post. 

Hoping that I clarified something we already knew :)