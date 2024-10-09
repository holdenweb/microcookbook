# Brainstorming

This page is to capture ideas - they can be 0.35-baked or fully formed.
Feel free to add to any conversations - please leave your initials after
each contribution [_sh_]

Here we have:

* [Recipe ideas](#recipe-ideas): concepts for hardware+software projects
    * [Model train speed display](#model-train-speed-display)
    * [Hot Wheels speed trap](#hot-wheels-speed-trap)
    * [Timer banner for lightning talks](#timer-banner-for-lightning-talks)

* [Editorial ideas](#editorial-ideas): suggestions about how to organize
and produce the book, as well as possible variations
    * [Semantic line breaks](#semantic-line-breaks)
    * [Device-specific books](#device-specific-books)
    * [Polyglot variations](#polyglot-variations)

## Recipe ideas

### Model train speed display

One micro:bit, a pair of lasers, and light sensors to
measure the speed of a model train or miniature car.
The lasers and sensors are on opposite sides of the track.
When a vehicle blocks the parallel beams in succession,
the micro:bit computes and displays the speed,
using configurable units. [LR]

```tags
Tags: micro:bit, laser, phototransistor, laser, hotwheels, model railroad
```


### Hot Wheels speed trap

One RaspberryPi Pico, a camera, a pair of lasers, and light sensors to
photograph a miniature car as it passes.
The speed is written to the image before it is saved.

This is similar to [Model train speed display](#model-train-speed-display),
with the addition of the photo capture and using a different microcontroller.

Bonus feature: an embedded HTTP server hosts a static leaderboard page
with the top 5 photos ranked by speed.
The page is updated with each new photo reading.
 [LR]

```tags
Tags: RPi Pico, camera, laser, phototransistor, hot wheels, model railroad, camera, HTTP
```

### Timer banner for lightning talks

Lightning talk sessions work best when there is a large timer visible to
the speaker and the audience—so they know when to clap ;-)

This project is a 1 meter wide banner made of fabric with a
3-digit display to show a countdown from
five minutes shown as 5:00.
The segments of the digits and the colon are made of LED strips sewn on the fabric,
together with the microcontroller
and a pair of buttons to set and restart the timer.

A key technique in this project is how to use the output pins of
an ESP32 to drive LED strips that require higher voltage and
draw more current than the microcontroller can provide.

Bonus feature: provide HTTP end points to set and restart the timer.

```tags
Tags: ESP32, LED strip, HTTP
```

## Editorial ideas

### Semantic line breaks

After writing two books in **AsciiDoc** I've adopted
[semantic line breaks](https://sembr.org/).
Essentially, that's the practice of adding a physical line break in the source text
at the end of each period or even clauses within a period,
to avoid long lines in the source.

Most editors default to dynamic line wrap when we write plain text.
This means that a seven line paragraph in the output is naturally coded as
a single *very long physical line*,
making it difficult to use diffs during edits and reviews.

I wrote this section using semantic line breaks.

Please browse the [semantic line breaks](https://sembr.org/) site for
more details and rationale. [LR]

### Device-specific books

Once we design and implement a project on one microcontroller,
it's often very easy to port it to a different device.
This means we could publish microcontroller-specific variations
of essentially the same book without too much extra effort.

A book with a specific microcontroller in the title
may be more attractive to readers looking for projects
tailored to the microcontroller they have.

Those books would be a follow-ups to the initial volume,
which is a collection of projects using whatever
microcontrollers each of us wants to play with. [LR]

### Polyglot variations

Our focus is **MicroPython**, of course.

But once we have a bunch of projects and explanations written
with **MicroPython**, it should not be too hard to rewrite them in
*TinyGo*, *Rust*, or *JavaScript* and make more derived books.

As a bonus, a few polyglot projects would provide a very interesting
comparison between languages, toolchains, and hardware APIs. [LR] 
