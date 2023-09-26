---
title: Audio Reactive Visuals
slug: /day2/audio-reactive-visuals
description: "Techniques for creating audio reactivity"
---

There are lots of ways to add interactive elements to your projects, and it's not uncommon to want to make your project react to audio. 



## Palette Tools | `audioAnalysis`

While we certainly could create our own audio analysis tool in TouchDesigner, we can also take advantage of an existing component in the palette called [audioAnalysis]. The audioAnalysis COMP takes an audio feed as an input and outputs several channels we can use to control our networks.

![image](/img/day2/audio-reactivity-01.png)

## Alternatives to TouchDesigner Audio Analysis

While it's often tempting to do everything you can in a single application, it can also be beneficial to break up the work across multiple applications. 

### TDAbleton

Depending on the type of audio integration you're looking for you may consider [TDAbleton] for achieving some of the audio interactivity you're after. The TDAbleton package can make integration with your Ableton set much easier, especially if you're focused on audio first. 

### PD or MaxMSP

Other node based programming environments that allow for signal processing include [MaxMSP] and [Pure Data]. Some artist / engineers preferer to do do their audio analysis in one of these applications and then send the results to TouchDesigner via OSC or UDP Messaging. This alternative can ensure that audio analysis is a separate concern and runs in another thread - which may help improve your application optimization. 

:::info Networking messaging

If you're collaborating with another artist, it can often be beneficial to use network messages to synchronize your applications. For example, if one creator is focused on audio you can still receive messages over the network to control the visual elements you've created in TouchDesigner. The same techniques we've explored using OSC messages from a control surface can also be used when sending control messages from another computer or application. 

:::

<!-- links -->

[audioAnalysis]:https://docs.derivative.ca/Palette:audioAnalysis
[TDAbleton]:https://docs.derivative.ca/TDAbleton
[Pure Data]: https://puredata.info/
[MaxMSP]:https://cycling74.com/products/max