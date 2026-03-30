# Week 09: 3/30/26

## Agenda

1. Project #4 Feedback Session
2. Tutorial: Generating Sound with p5.js
3. In-Class Work Time with Group
4. [Demos, Videos, Useful Links](#demos)

## Project #4 Feedback Session

In [this cryptpad](https://cryptpad.fr/doc/#/2/doc/edit/CQzOCMmqMyBuZIQUQ68KIhm4/), follow this framework for feedback:

- Values:
  - audience responses: what is meaningful, evocative, interesting, exciting, and/or striking? what is working for you?
- Questions:
  - artist questions: from your homework, what questions did you have about the project? answer these as a group
  - audience questions: what are you curious about? can be concept, theme, technical implementation, etc.
- Suggestions:
  - audience suggestions: if you were to take this concept, what would you do? how would it change or improve?

## Tutorial: Generating Sound with p5.js

Each note that exists from instruments is related to a specific frequency. For example, a [piano](https://en.wikipedia.org/wiki/Piano_key_frequencies) can be broken down by [this chart](https://upload.wikimedia.org/wikipedia/commons/a/ad/Piano_key_frequencies.png)

What this means for us is that we can generate tones by using the basic frequency (in the hz units) and electronically mimic the sound waves coming from each place.

![sound waves](https://www.thedawstudio.com/wp-content/uploads/2016/08/Types_of_Soundwaves.jpg)

We can mathematically create a scale by seeing what is the ratio between the note, the hz, and the ratio.

| note | hz  | ratio |
| ---- | --- | ----- |
| C    | 262 | 1     |
| D    | 294 | 1.122 |
| E    | 311 | 1.189 |
| F    | 349 | 1.335 |
| G    | 392 | 1.498 |
| A    | 415 | 1.587 |
| B    | 466 | 1.782 |

#### Modifying Sound Files based on Freq (HZ)

The `.rate()` method that exists on sound files allows us to use this ratio to create a new tone!

#### Using Oscillators

We can customize sound files using the frequency, but we can also create new tones using the oscillator class in p5.sound.

```js
// p5.Oscillator takes 2 parameters:
// 1. frequency (note) to be played
// 2. type of waveform (sine, triangle, square, sawtooth)
let osc = new p5.Oscillator(261, 'triangle');
```

The frequency is determined by the note (see above table), and the waveform is the literal sound wave that moves through the air. We are mimicking this electronically.

## In-Class Work Time with Group

If your group is gone, consider other things to work on:

- think about improving your proposal via feedback received
- begin technical implementation of your project
- research related artistic works
- watch coding train videos
- plan out a visit to a gallery for the extra credit
- do the reading assignment

## Demos

### Videos

[Same as last week](./class_08.md#videos) if you did not watch already.
