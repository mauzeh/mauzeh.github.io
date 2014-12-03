---
layout: post
title:  "Demystifying Matplotlib’s Contour Plots"
date:   2012-12-30 20:31:20
categories: python matplotlib
---

Somehow I had a hard time trying to understand how to draw contour plots properly. This is mostly due to the online examples having lots of numpy array magic that I never quite had the time to fully study.

<div class="bb-pull-right bb-border bb-gap-inside bb-gap-left">
	<img src="{{site.baseurl}}/assets/images/logo_matplotlib.png" alt="Matplotlib" title="Matplotlib" width="250" />
</div>

Instead, I was looking for a Minimum Working Example (MWE), much like a “hello, world!” in contour world. As I could not find such a simple example, I had to resort to debunking the array magic and create an MWE of my own. I hope that sharing it here will help someone to understand the way it works from the ground up:

{% highlight python %}
import matplotlib.pyplot as plt
import numpy as np
 
ellipses = np.array([
    [18, 13, 10,  9, 10, 13, 18],
    [13,  8,  5,  4,  5,  8, 13],
    [10,  5,  2,  1,  2,  5, 10],
    [ 9,  4,  1,  0,  1,  4,  9],
    [10,  5,  2,  1,  2,  5, 10],
    [13,  8,  5,  4,  5,  8, 13],
    [18, 13, 10,  9, 10, 13, 18],
])
 
x = np.array([1, 2, 4, 8, 16, 32, 64])
y = np.array([1, 2, 3, 4, 5, 6, 7])
 
cs = plt.contour(x, y, ellipses)
plt.clabel(cs)
 
plt.show()
{% endhighlight %}

