---
layout: page
title: "Indoor Cycling Automation"
author: "Berat Onur Ersen"
date: 2019-02-28
draft: false
permalink: /2019-02-28-indoor-cycling-automation/
tags: sports
---

I personally like doing activities indoor and outdoor.
My favorite outdoor activities are running, biking, hiking, windsurfing, kite-surfing.
I switch between those due to the season. In summer times I tend towards water sports.  
I'm a long-term member of a local sports center. 

During the winter season, my major indoor activities are running on a treadmill, playing basketball and swimming. 
In the past, I wanted to be a fitness guy, trying to build muscles but I could not keep up much with dumbells and heavy exercises :(
There I made up my mind to be athletic rather than pumping iron.

Then I started joining training classes open for all members. Once I found myself in extreme training class which made me paralyzed 
for at least 3 days :) It's a high intense interval training class during which you jump, squat, push-up 
do tons of aerobic exercises in a short time.
There were also other classes athletic training, functional movements etc. 
Those are HIIT classes too, but not as brutal as extreme, I don't why I chose to join that :)

About 3 months ago, sports center renewed their spinning bikes and brought brand new digitally equipped ones. 
That spinning concept changed and it became "indoor cycling". 
In the cycling room, they put a projector showing real videos on a big curtain, 
videos making you feel like riding in the jungle or on a highway or in a city.
For more information about the system visit [Team ICG.](https://www.teamicg.com/en/digital/training-app)

![picture alt](/img/indoor-cycling-automation/indoor_cycling_class.png)

I joined one of those indoor cycling classes and found it very motivational. 
In a world, even every breath we take (by Sting) is data, recording 
my cycling session was a superb opportunity for a lately-automation guy like me!

Indoor cycling bike is a quite easy machine with pedals, handlebar, resistance level pin, and a tiny digital screen.
It has the same resistance functionality with spinning bikes. 

![picture alt](/img/indoor-cycling-automation/icg_bike.jpg)

If you want to increase your heart rate, you increase resistance level and then it becomes harder to pedal.
There are 5 resistance zones. Resistance zone #1 makes pedals lightest and feels like you're riding straight on the road or downhill.
Resistance zone #5 is the hardest one to pedal, for that it's generally used to burn fat.

![picture alt](/img/indoor-cycling-automation/icg_screen.jpg)

Apart from those functionalities, best thing IMHO is; indoor cycling 
bike has a digital module that can pair with the mobile app and transfer data.
Finishing every session, I started recording my entire performance.
Data like total kilometers, calories burn, rpm information, zone durations are kept on the app.
The application is fair enough, alright... but lacking analytics. I can see 
my performance for each session but can **NOT** view if I was becoming better or not.

---

...and we come to the point where I created my personal automation project to analyze how far I'm going with my performance.

I call myself a Java guy. I've been part of Java-based project for years.
I understand and create solutions in Java fast, but this time I wanted to go something different, 
I wanted to create something using a scripting language. 

I had previous tasks where I used Perl.
Those were about text-processing and although it is quite an old language, I liked Perl very much.
I thought if I go with Perl, I won't be learning something new, that's why I chose Python for this tiny task.

Let me tell what I've done...

I created a project where everything is done automatically inside python scripts.
Only human interaction is pushing a session image. 

Session image? 

Arggh! I did not tell about the session image.
Yes, it's simple as hell, I just create a screenshot of results screen on mobile app :)

![picture alt](/img/indoor-cycling-automation/sample_session.png)

My simple automation :

* first crops related area - with numeric info from each image
* increases cropped image contrast (to increase text reading accuracy)
* reads values of each session from the images and dumps in a file - here an image2text conversion which is also called OCR (optical character recognition) happens
* finally draws time-series line charts - showing progress through time.

I created two docker images/docker containers for stages during processing.

* a container for data processing via python-tesseract-opencv 
* a container for visualization via matplotlib

Last but not least, I configured to publish those generated charts into this blog post automatically.
Which means with every new session below charts will be refreshed.

Now, this helps me to see if I'm doing good or not :)  

![picture alt](/img/indoor-cycling-automation/quote.png)

If you see a change in charts, then you know I'm still joining those classes :)

Wanna see the project? Click [here.](https://github.com/onurersen/indoor-cycling-sessions)

![picture alt](/img/indoor-cycling-automation/charts/avg_calories_burnt.png)

![picture alt](/img/indoor-cycling-automation/charts/avg_kilometers.png)

-             |  -
:-------------------------:|:-------------------------:
![picture alt](/img/indoor-cycling-automation/charts/calories_burnt_in_session.png)  |  ![picture alt](/img/indoor-cycling-automation/charts/kilometers_in_session.png)
![picture alt](/img/indoor-cycling-automation/charts/max_km_h.png)  |  ![picture alt](/img/indoor-cycling-automation/charts/avg_km_h.png)
![picture alt](/img/indoor-cycling-automation/charts/max_rpm.png)  |  ![picture alt](/img/indoor-cycling-automation/charts/avg_rpm.png)
![picture alt](/img/indoor-cycling-automation/charts/total_duration.png)  |  ![picture alt](/img/indoor-cycling-automation/charts/zone5_duration.png)
![picture alt](/img/indoor-cycling-automation/charts/zone4_duration.png)  |  ![picture alt](/img/indoor-cycling-automation/charts/zone3_duration.png)
![picture alt](/img/indoor-cycling-automation/charts/zone2_duration.png)  |  ![picture alt](/img/indoor-cycling-automation/charts/zone1_duration.png)