---
layout: post
title: Array Data Structure
color: rgb(0,0,255) 
feature-img: "/assets/thumbnails/pexels/circuit.jpeg"
tags: [Array, Data Structure]
excerpt: This is a post regarding the array data structure in c plus plus. enjhoy your time reading it
author: bbb
---

# I am a BIG title

$$This + is =  a very tiny tiny post with less than 250 letters. $$

```cpp
#include <iostream>
using namespace std;
int arr[60];
void get_array()
{
    int n = 60;
    arr[0] = 1;
    arr[1] = 1;
    for(int i=2;i<n;i++)
    {
        arr[i] = (arr[i-1]+arr[i-2])%10;
    }
}


int get_fibonacci_last_digit(int n)
{
    return arr[n-1];
}

int main() {
    get_array();
    long long int n;
    cin >> n;
    while(n/60)
        n = n%60;
    cout<<arr[n-1];
   
}

```

** Varius sit amet mattis vulputate. Turpis egestas integer eget aliquet nibh praesent. Molestie nunc non blandit massa enim nec dui nunc.**

![](/assets/thumbnails/pexels/circuit.jpeg)

 Volutpat diam ut venenatis tellus in metus vulputate eu. Pellentesque nec nam aliquam sem et tortor consequat. Nam aliquam sem et tortor consequat. Consectetur lorem donec massa sapien. Scelerisque eleifend donec pretium vulputate sapien nec. Nulla porttitor massa id neque aliquam vestibulum morbi. Leo integer malesuada nunc vel risus commodo. Cursus risus at ultrices mi tempus imperdiet nulla malesuada. Orci phasellus egestas tellus rutrum tellus pellentesque eu. Gravida in fermentum et sollicitudin ac orci phasellus egestas. Praesent elementum facilisis leo vel fringilla est. Tempor orci dapibus ultrices in iaculis nunc sed augue lacus. Sed felis eget velit aliquet sagittis.

Leo vel orci porta non pulvinar neque laoreet suspendisse interdum. Diam phasellus vestibulum lorem sed risus. Justo donec enim diam vulputate ut. Arcu non sodales neque sodales. Enim ut sem viverra aliquet eget sit amet tellus. Lacus sed turpis tincidunt id aliquet risus feugiat in. Egestas sed sed risus pretium quam vulputate. Facilisis volutpat est velit egestas dui id ornare arcu odio. Egestas dui id ornare arcu odio ut sem. Elit sed vulputate mi sit amet mauris commodo quis. Bibendum est ultricies integer quis auctor elit sed. Sagittis orci a scelerisque purus semper eget duis at tellus. Elementum tempus egestas sed sed risus pretium.

Pretium lectus quam id leo in vitae. Malesuada fames ac turpis egestas. Id aliquet risus feugiat in ante metus dictum at tempor. Arcu cursus euismod quis viverra nibh cras pulvinar mattis nunc. Dolor sit amet consectetur adipiscing elit duis tristique. Et netus et malesuada fames ac turpis egestas. Leo in vitae turpis massa sed elementum. Sit amet facilisis magna etiam tempor orci. Tristique senectus et netus et malesuada fames ac. Mattis nunc sed blandit libero. Aenean et tortor at risus.

Lectus sit amet est placerat in egestas. Commodo ullamcorper a lacus vestibulum sed. Maecenas ultricies mi eget mauris pharetra et. Euismod elementum nisi quis eleifend quam adipiscing vitae proin. Feugiat vivamus at augue eget. Ultricies mi eget mauris pharetra. Aliquam vestibulum morbi blandit cursus risus. Praesent tristique magna sit amet purus gravida quis. Proin sed libero enim sed faucibus turpis in. Sit amet est placerat in egestas. Dui id ornare arcu odio ut sem nulla pharetra. Ut ornare lectus sit amet est placerat in. Tristique senectus et netus et malesuada fames ac turpis.