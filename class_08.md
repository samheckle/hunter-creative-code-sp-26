# Week 08: 3/23/26

## Agenda

1. Reading Discussion #2
2. Tutorial: Data Structures Part 2: Objects
3. Tutorial: p5.js Sound
4. [Demos, Videos, Useful Links](#demos)

---

## Reading Discussion #2

Take notes in [this document](https://cryptpad.fr/doc/#/2/doc/view/AqZw5EHtyN42hNcfwsCuCGyZZHvHu-teW0NuyVzcCaw/)

- How are you currently using AI? Do you use AI in your artistic processes now?
- What are the different approaches you might take in using AI in the future (if you will)?
- Can technology be biased? Or is it designed that way?
- When you were younger, how did you imagine your adult life? What did you imagine yourself doing? Has AI changed that?

### An Analogy (thank you [@rory](https://x.com/rorys))

Sometimes using the most effecient and fastest tool has a time and a place...

<img src="https://p.kagi.com/proxy/delivery-person-on-a-electric-bike-on-broadway.jpg?c=N7Pi3QNEaSL6_svD8glSC__wDVyV2V3zvCInmdfWCWK-40QsqR_1nDkQnMTPr53cBKuEuHyK39pUZ9jVclrH7cWgzCHFXUcE4LPMsv0qgvTq8H7WTqxXSmFT8VSz_mJ40RtGujoRq_FPeE6MPuRxrI3pDcajCJXFOJhhwVubLEqErwGvEfF6lXCNouF3WLXhALHKy15pem_9IcY54yBz_Lxqa7nuE5STEOJsTZ2LTBiHpWHYxEnFmbfwCkeStRTo" style="width:300px">

We don't want to make something unnecessarily challenging for us because we have tools at our disposal! We don't need to prove ourselves like cyclists in Tour de France...

<img src="https://p.kagi.com/proxy/20220724TDF1023-A.S.O.-Charly-Lopez-1-2048x1366.jpg?c=iETRpTZQOV3K8Lzi6jhDE2mCdW9Y3kddNhEcGv3APuoOvkcz1e8C26-6jZf5Kl8wxsZB0eM3741CicIx1cDv1Gaa6VOuvopuX25CUzcL_mN-WoOPkD5p5Pj-L65pmMLLa92ULtkHVVX6yYpPyXwUgZxexaHSsvIptJWCR8G41XE%3D" style="width:300px">

But we need to be transparent about using these tools and making sure we are actually exercising, otherwise why are you here?

<img src="https://p.kagi.com/proxy/spin_main.jpg?c=bqzFZPkbUk3SKxZ345F1kQj1flyhL3AATty8oi60V7-ZcQZM3rg5e1Emyh_wHhBvxD_NIJX0c9HxBS3wrbD55-waA6Bzx628HjuQmmm4A_i1JU3UAFrPcem2VOf8E-kV" style="width:300px">

## Data Structures Part 2: Objects

An object is a data structure similar to an array.

<table>
<tbody>
<tr><td>object</td><td>

data structure that holds variables using key-value pairs. it is unordered.

</td></tr>
<tr><td>key</td><td>

the `property` we access when we want to retrieve a piece of data from the object.

</td></tr>
<tr><td>value</td><td>

similar to the `element` in an array, the data that is stored

</td></tr>
</tbody>
</table>

#### Objects are also like tables

<table>
<tbody>
<tr><td>property</td><td>word1</td><td>word2</td><td>word3</td><td>word4</td></tr>
<tr><td>value</td><td>"this"</td><td>"is"</td><td>"a"</td><td>"sentence"</td></tr>
</tbody>
</table>

```js
let data = {
    word1: "this",
    word2: "is", 
    word3: "a",
    word4: "sentence"
}
```

#### Unique Attributes of an Object

We can add new `properties` by simply using a new property name. 

```js
let myObj = {
    a: 10,
    b: 15
}
myObj.c = 20
// this automatically adds .c as an accessible property
// the new object is {a:10, b:15, c:20}
```

## Tutorial: p5.js Sound

To use sound in p5, we use the [p5 sound library](https://p5js.org/reference/p5.sound/), which allows us to add, manipulate, and create sound with p5.

### Sources for sound:

- [orchestral sample library](http://virtualplaying.com/virtual-playing-orchestra/)
- [free music archive](https://freemusicarchive.org/)
- [freesoundorg](https://freesound.org/)
- [bbc sound effects](http://bbcsfx.acropolis.org.uk/)
- [free sound picture](https://www.soundofpicture.com/)

### Sound Project references

- https://teropa.info/loop/#/title
- https://www.nytimes.com/interactive/2018/09/21/magazine/voyages-travel-sounds-from-the-world.html
- http://jazz.computer/
- https://patatap.com/
- https://youtu.be/HI1raqxrUdk?si=j01yIjgDCCW91PpI
  - cassie's [sketch](https://editor.p5js.org/cassie/sketches/YZHxZ9ffl) recreating it

## Tutorial: Sound Files and Microphone

### Microphone Input

We can create microphone input using the `new p5.AudioIn()`. This uses the class syntax of `new` to create an instance of the AudioIn class, and we can assign that to a variable. 

***Note: Some browsers hate this, so if you use Firefox or not Chrome, you might need to change the version of your p5 to 0.9.0 in `index.html`***


```js
let mic = new p5.AudioIn()
```

Once we have created it, we need to start the audio input.

```js
mic.start()
```

We can measure the volume of the microphone using
```js
mic.getLevel()
```

## Review Documentation and Videos

### Review Documentation

* [object](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object)

### Videos

* [7.3 Arrays of Objects](https://youtu.be/fBqaA7zRO58?si=ZSNTxbtpKlpeK4Jz)
* [17.1: Loading and Playing sound](https://youtu.be/Pn1g1wjxl_0?list=PLRqwX-V7Uu6aFcVjlDAkkGIixw70s7jpW)
* [17.3: Timing, Jumps and Cues](https://youtu.be/SfA5CghXw18?list=PLRqwX-V7Uu6aFcVjlDAkkGIixw70s7jpW)
* [17.4: Amplitude Analysis](https://youtu.be/NCCHQwNAN6Y?list=PLRqwX-V7Uu6aFcVjlDAkkGIixw70s7jpW)
* [17.5: Adding Sound Effects - video tutorial](https://youtu.be/40Me1-yAtTc?list=PLRqwX-V7Uu6aFcVjlDAkkGIixw70s7jpW)
* [17.6: Sound Synthesis - video tutorial](https://youtu.be/Bk8rLzzSink?list=PLRqwX-V7Uu6aFcVjlDAkkGIixw70s7jpW)
* [17.8: Microphone Input](https://youtu.be/wUSva_BnedA?list=PLRqwX-V7Uu6aFcVjlDAkkGIixw70s7jpW)
* [17.9: Sound Visualization: Graphing Amplitude](https://youtu.be/jEwAMgcCgOA?list=PLRqwX-V7Uu6aFcVjlDAkkGIixw70s7jpW)
* [17.10: Sound Visualization: Radial Graph](https://youtu.be/h_aTgOl9J5I?list=PLRqwX-V7Uu6aFcVjlDAkkGIixw70s7jpW)
* [17.11: Sound Visualization: Frequency Analysis with FFT](https://www.youtube.com/watch?v=2O3nm0Nvbi4&list=PLRqwX-V7Uu6aFcVjlDAkkGIixw70s7jp