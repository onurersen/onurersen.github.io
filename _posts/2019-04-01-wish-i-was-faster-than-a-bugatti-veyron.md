---
layout: page
title: "Wish I was faster than a Bugatti Veyron"
author: "Berat Onur Ersen"
date: 2019-04-01
draft: false
permalink: /2019-04-01-wish-i-was-faster-than-a-bugatti-veyron/
tags: bug
---

My indoor cycling automation script drove me crazy last week. I was conveniently pushing my cycling sessions and it was processing.  
...then suddenly chart script produced a stupid visual for average km/h and maximum km/h.

![picture alt](/img/strange-tesseract-issue/avg_km_h.png)

![picture alt](/img/strange-tesseract-issue/max_km_h.png)

Sure, there was a faulty execution in the script for 28th of March.  
It was telling me that I hit max speed 500 km/h and average speed as 250 km/h on the bike - woohoo! faster than a Bugatti Veyron :)

I tried to address the problem and fix this ridiculous output last 2 weeks.  

KM/H values on session images are decimal values. It was obvious, my OCR script was processing each and every line seamlessly except 28th of March.  

For that day's session Average and Max KM/H values were **25.0 / 50.0** and the script was converting this value on the image as **250 / 500** :(

The conversion was wrong for only 25.0 / 50.0 - any other numerical pairs were converted correctly!

I found the solution by increasing contrast enhancement value from **4.0** to **7.0**.

```
def enhance_image_contrast(image):
    enhancer = ImageEnhance.Contrast(image)
    enhanced_image = enhancer.enhance(7.0)
    return enhanced_image
```

It was fixed.  
I don't understand inconsistency in processing and why conversion was wrong for only that 25.0 / 50.0 values... 
 
Anyway, it was fixed and I know I'm not that fast :)

![picture alt](/img/strange-tesseract-issue/bugatti_veyron.jpg)