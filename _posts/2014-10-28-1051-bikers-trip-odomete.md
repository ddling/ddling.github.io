---
layout: post
title: "1051. Biker's Trip Odomete"
description: "A sicily problem solution"
category: sicily
tags: [sicily, easy]
---
{% include JB/setup %}

{% highlight c++ %}
#include <iostream>
#include <iomanip>
#include <cstdio>

using namespace std;

int main()
{
    const float P = 3.1415927;
    float diameter;
    int revolutions;
    float time;
    int count = 1;
    while (true) {
        cin >> diameter >> revolutions >> time;
        if (revolutions == 0) break;
        float perimeter = P * diameter;
        float distance_in_mile = perimeter * revolutions / 12 / 5280;
        float miles_per_hour = perimeter * revolutions / 12 / 5280 / (time / 60 / 60);
        printf("Trip #%d: %.2f %.2f\n", count, distance_in_mile, miles_per_hour);
        count ++;
    }
    return 0;
}                                 
{% endhighlight %}
