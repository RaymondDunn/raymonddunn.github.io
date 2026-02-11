---
title: Rendering gameplay with patterned light
date: 2025-09-02T19:37:00.000Z
description: 'Using a DMD like a projector'
image: /images/20250902 sinistar projection.PNG
imageAltAttribute: ''
tags:
  - optics
  - phd
---
## DMDs for light patterning

During my PhD I was tested a [microscopy device](https://www.mightexbio.com/polygon/) made my Mightex. This is a digital micro-mirror device (DMD), which enables spatial light modulation (SLM) by an array of addressable micromirrors.

So cool! You treat the DMD like a pixel array. The core idea is shown here:

![ray](/images/20250902_1000_microscope_2.jpg)

Individual pixels can be "on" (pointing at the sample), or "off" (non-reflecting, what exactly this means depends on the chip). You also get graded values with dithering which means fast on/off alternation, with varying duty cycle, kind of like analog approximation on your typical Arduino microcontroller.

For reasons I should talk in detail about in another post, we selected this DMD product because it's been engineered for high precision and rapid updates, making it useful for a primitive form of closed-loop experimental optophysiology.

## Rendering Sinistar gameplay

Now is this DMD fast enough? On the spec sheet it quotes an update rate of 6600 fps, but how does that play with camera exposure, which is tricky to synchronize.

In other words, how could we intuitively evaluate this? The thing is, this is literally a projector. So I thought it would be fun to render gameplay of the retro video game Sinistar.

Images were taken with 10ms exposure at 70fps (I think the Polygon could go faster but I was limited by camera readout speed) with 40x 1.25 NA WI objective. No visual edits/filtering other than typical compression/rendering with h264 codec. Frames were extracted from Sinistar gameplay.

{{< youtube id="B5WnxQo6htY" >}}

Pretty fun :) Torsten tweeted out this video and I sent this to the Mightex folks.
