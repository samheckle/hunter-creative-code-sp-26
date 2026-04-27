# Week 12: 4/27/26

## Agenda

1. Tutorial: Continuing External Libraries
2. Demos and References

---

## Continuing External Libraries

As per our [class 11](./class_11.md#tutorial-external-libraries) discussion, we will look at how to import a library and use it in our own sketches. 

### Example Library: Using ml5

https://ml5js.org/ is a library built on top of p5 to use machine learning. They have a few different types of tools that you are welcome to use, but today's demo will focus on BodyPose https://docs.ml5js.org/#/reference/bodypose

The first thing we always do when using an external library is open up our `index.html` and import the library code.

```html
<script src="https://unpkg.com/ml5@1/dist/ml5.js"></script>
```

### Example Library: Using p5.glitch

https://ffd8.github.io/p5.glitch/ allows you to directly manipulate the binary data of a sketch to create a glitch effect. 

We can import it by using

```html
<script src="https://cdn.jsdelivr.net/npm/p5.glitch@latest/p5.glitch.js"></script>
```

### Example Library: Using p5.touchgui

https://github.com/L05/p5.touchgui/ is a library that *overrides* DOM manipulation for p5 specific elements. 

```html
<script src="https://unpkg.com/p5.touchgui@0.5.2/lib/p5.touchgui.js"></script>
```

---

## Demos and Videos

### In-class demos

### Review Videos

- Coding Train [ml5 playlist](https://youtu.be/26uABexmOX4?si=V5nfU5nYDGSpDuB5)
