+++
date = "2016-10-22T23:10:00+01:00"
draft = false
title = "Research I Wish I'd Done Before I Started"
+++

There is a wealth of information out there about synth DIY, most of which I was unaware of when I first started toying with the idea of building my own modular synthesizer. What I knew about modular synthesizers was that they are made up of separate modules that you can combine with cables. I knew about some of the common modules, having used software synthesizers for a long while, but that's about where my knowledge ended.

## Power

I had built power supplies before, so I figured, before I start building modules, I should build a power supply board. I built a dual 5V power supply (-5 and +5V). Later I would learn that virtually all existing schematics for analog synthesizer modules are designed around a +/-12V supply, sometimes +/-15V.

I had built my first module (a MIDI input module almost entirely of my original design) based on this, so only after that I realized my error. To this day I'm working with the +/-5V setup. It has involved a lot of component value modification of existing circuits.

On the upside, being forced to swap out component values (mostly by trial and error) forced me to understand the workings of the circuit more deeply, so I'm certainly not angry about it.

### Recommendation

If you are about to start building your own synth, I recommend you go with +/-12V; it will save you a lot of hassle. It will also let you use pre-existing modules.

---

## Mounting

I designed a case for my synth in Sketchup, and then shoddily put it together in 25mm-thick MDF wood. I decided to put a panel on the back with a lot of banana sockets, for power distribution. Modules would have a front panel and a rear panel; the front panel would be the user-facing side with knobs, signal connectors, and what have you, while the back would just offer power connection points.

Mounting in my synth is done by drilling holes in a planks, and screwing PCB standoffs in said holes. I'm using several stacked standoffs and washers to get the front panels to be level with each other. PCBs and front panels are connected to eachother with the same stack of standoffs. The result is, well, rather hard to maintain. Unscrewing a front panel is a chore, and I need entirely too many PCB standoffs for it.

### Recommendation

Look into the Eurorack standard, which is based on very common rack-mount used in professional audio equipment, but also server racks. Eurorack is an adaption of it where you can mount modules with a width less than the usual 19", through standardizing of width units. The front panels get mounted in nuts that sit in a rail. PCBs can be mounted to the front panels using angle brackets, and otherwise sort of float free. This lets you undo 2 to 4 screws and just pull the module out, instead of the mess I've got going.

I actually intend to build a new case based on this system, and redesign all my front panels to work with it. That'll be a job and a half, and will probably cost me a pretty penny too.

Some relevant links:

- [Eurorack on SDIY wiki](http://www.sdiy.info/w/Eurorack)
- [Eurorack DIY parts on SDIY wiki](http://www.sdiy.info/w/Eurorack_DIY_parts)

---

## Attenuation

In the context of synthesizers, attenuation is reducing the intensity of a signal. As a concrete example, you can have a low frequency oscillator that adds vibrato to an audible oscillator. By attenuating the <abbr title="Low Frequency Oscillator">LFO</abbr> signal before it reaches the main oscillator, you can control how far the pitch will swing.

I've made a couple of modules so far (oscillator &times; 3 and filter) where I provide inputs to control a parameter, and I have included a potentiometer knob on the module's panel to set the intensity of the incoming signal.

These attenuation knobs easily take up a lot of space on a front panel, resulting in annoyingly large modules.

### Recommendation

This recommendation comes pretty much directly from Ray Wilson himself, on Music From Outer Space. Instead of putting attenuators in every module, just provide the plain input connection. Add a separate module in the synthesizer which is just a bank of attenuators. That way, they are available in the synth for where-ever you need them, without making every other module much larger.

When I get around to redesigning my front panels when switching to eurorack (as mentioned earlier), I'll be cutting out the attenuators from my existing modules.
