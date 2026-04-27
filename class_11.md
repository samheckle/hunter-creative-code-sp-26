# Week 11: 4/20/26

## Agenda

1. Project #4 Share
2. Final Project
3. Tutorial: Webcam
4. Demos and References

---

## Project #4 Share

Critique structure:

- Be respectful to your peers!
- Avoid "I like this" and be as specific as possible.
- You are welcome to follow the praise/question/polish framework
  1. Praise: what is meaningful, evocative, interesting, exciting, and/or striking? what is working for you?
  2. Question: what are you curious about? can be concept, theme, technical implementation, etc.
  3. Polish: if you were to take this concept, what would you do? how would it change or improve?

## Tutorial: External Libraries

p5.js and p5.sound.js are two core frameworks that we have used in this class that focus on graphic and sound explorations in the web. But, we can also use _external_, meaning not maintained by the Processing Foundation, libraries that leverage p5 to do interesting things.

We can see a full list of the libraries of p5 by visiting https://p5js.org/libraries/directory/

For your final project, you will pick a library to research and teach the class through a short demo that you will build. Each presentation will cover:

1. what the library does and how it might be used in real world
2. how the library works
3. short demo on the library

Each presentation should be ~10 minutes long, including the demo. _Your demo must differ from any examples given by the library themselves_.

There are lots of interesting things to explore here:

- 3D (I would also look at the WebGL tutorials: https://p5js.org/tutorials/)
- [p5 riso](https://antiboredom.github.io/p5.riso/) if you wanted to make it physical
- [p5 glitch](https://ffd8.github.io/p5.glitch/)
- continue with advanced p5.sound library
- look into other functionality of p5.js that may not have been covered in class

Good benchmarks for choosing a library to work with:

- What does the documentation look like?
- Is it well-supported by the p5 community? When was the last time the library was updated?
- Are there a lot of tutorials using the library?
- Is it an interesting topic to you?

### Video Explorations

We can leverage the webcam to do a lot of things inside p5.js, and we can even manipulate individual pixels.

Let's start with regular pixel manipulation and then add a library on top of it.

The most important line of code for video allows us to enable webcam usage.

```js
// prompts the browser to use the webcam
webcam = createCapture(VIDEO);
```

We could _also_ use a phone camera instead if we wanted

```js
// if i am using a phone camera
let constraints = {
	audio: false,
	// back camera code
	video: {
		facingMode: {
			exact: 'environment', // back camera
		},
	},
	// front camera code
	//video: {
	//facingMode: "user"
	//}
};
webcam = createCapture(constraints);
```

What this does is allow us to add the webcam as an HTML element. If we wanted to hide that element and just display the camera on the screen, we could write

```js
//... in the setup
webcam.hide();
//... in the draw
// display webcam data to the draw
image(webcam, 0, 0);
```

## Demos and Resources

### Demos

### External Resources

- Allison Parrish, [Working with Video](https://creative-coding.decontextualize.com/video/)
- Coding Train `ml5` Playlist [Introducing ml5 using FaceMesh](https://thecodingtrain.com/tracks/ml5js-beginners-guide/ml5/0-introduction/patt-vira)
- Coding Train [Live Video and `createCapture()`](https://thecodingtrain.com/tracks/pixels/pixels/createCapture) Playlist
