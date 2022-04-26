---
title: "W"
linkTitle: "W"
weight: 4
description: >
  ## WebAssembly (WASM)
---

> The Dawn of a New Era!

WebAssembly is a new type of code that can be run in modern web browsers — it is a low-level assembly-like language with a compact binary format that runs with near-native performance and provides languages such as C/C++, C# and Rust with a compilation target so that they can run on the web. It is also designed to run alongside JavaScript, allowing both to work together.

<p align="center">
    <img src="wasm.png" alt="WASM" />
</p>

WebAssembly has huge implications for the web platform — it provides a way to run code written in multiple languages on the web at near native speed, with client apps running on the web that previously couldn't have done so.

WebAssembly is designed to complement and run alongside JavaScript — using the WebAssembly JavaScript APIs, you can load WebAssembly modules into a JavaScript app and share functionality between the two. This allows you to take advantage of WebAssembly's performance and power and JavaScript's expressiveness and flexibility in the same apps, even if you don't know how to write WebAssembly code.

### How WASM Works?

<p align="center">
    <img src="wasm-working.png" alt="Working" />
</p>

Wasm programs are deployed in two stages. First, a Wasm module is generated from the source code:

- Write the application in your preferred language.

- Create a pre-compiled Wasm module.

- Distribute the module—ideally, using a CDN for low latency.

Once the Wasm module is built, it can be run anywhere with a few lines of JavaScript glue:

- Load the Wasm module.

- Create an instance of the module.

- Call the instance’s functions.

**Compilation**

You can write a Wasm module in any language that supports it or in the text assembly directly. For instance, take this C file called answer.c:

```
int answer() {
 return 42;
}
```

To generate a standalone .wasm module, you can use emscripten. Emscripten is a C and C++ compiler that generates JavaScript files and WebAssembly binaries:

`emcc answer.c -O2 -s SIDE_MODULE=1 -o answer.wasm`

The result of the compilation is a file called answer.wasm. This file can now be loaded in a browser, as a server component.

For the most part, emscripten’s emcc can be used as a drop-in replacement for GNU’s gcc. Therefore, it can compile any portable C or C++ library and bring it to the Web.

**Running in the browser**

To run a Wasm module in the browser, the .wasm file must be loaded, instantiated, and invoked. You can choose among the multiple loading methods described in the JavaScript API.

For example, this script loads answer.wasm in the browser and shows the output (the number “42”) in an alert box:

```
fetch('answer.wasm').then(response =>
 response.arrayBuffer())
 .then(bytes =>
 WebAssembly.instantiate(bytes))
 .then(result =>
 alert(result.instance.exports.answer()));
```

**Running outside the browser**

The primary motivation behind WebAssembly was to enable developers to run advanced applications in browsers. Nevertheless, nothing prevents you from running Wasm modules on servers.

For instance, you can run answer.wasm in Node.JS with just a few lines of code:

```
const fs = require('fs');
const run = async () => {
 const buffer = fs.readFileSync("./answer.wasm");
 const result = await WebAssembly.instantiate(buffer);
 console.log(result.instance.exports.answer());
};
run();
```

### Examples of WebAssembly

WebAssembly programs can go where no JavaScript has gone before, namely media edition, image recognition, transcoding, VR and high-end games, emulation, or desktop-tier applications.

More use cases include:

- Recording and encoding audio.
- Encoding video.
- Rendering 3d objects in real time.
- Re-encoding images on the fly.
- Editing and annotating PDFs.
- Createing a fully featured text editor.
- Visualizing data in real time.
- Doing real time physics simulation.

WebAssembly has been successfully deployed in the real world, too:

- eBay implemented a universal barcode scanner.
- Google Earth can run in any browser now, thanks to WebAssembly.
- The Unity and the Unreal game engines have been ported to WebAssembly. You can even run the Unreal Epic Zen Garden demo.
- The Doom 3 engine has also been ported to WebAssembly. You can play the demo online.
- Alternatively, you can create custom games in the browser with Construct3.

### Key Takeaways

- With around 40 languages that can compile to WebAssembly, developers can finally use their favorite language on the Web.
- WebAssembly does not replace JavaScript; in fact, some JavaScript code is required to load WebAssembly modules.
- WebAssembly runs in all major browsers and in all platforms. Developers can reasonably assume WebAssembly support is anywhere JavaScript is available.
- WebAssembly can also run in servers.
