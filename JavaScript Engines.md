# JavaScript Engines

A JavaScript engine is a dedicated program that interpreters your JavaScript code and executes it. You write human-readable JavaScript, but the computer's processor understands machine code. The engine is the crucial translator and executor in between.

While implementations vary, most modern engines follow a sophisticated process far beyond simple line-by-line interpretation:

- The engine first reads and parses your code and checks for any errors so that it can create an internal representation of your code's structure which is like an _Abstract Syntax Tree._
- Then your code is complied into byte-code as this allows the code to start executing quickly. An engine might support Just-in-Time compilation that allows the engine's profiler to monitor code that runs frequently.
- This code is then sent to an optimizing compiler. It makes assumptions based on the observed runtime behavior and compiles that specific section directly into highly optimized **machine code** for the host system's architecture.
- The processor executes the generated machine code or the engine interprets the bytecode/AST.
- JavaScript is garbage-collected. The engine automatically manages memory allocation and de-allocation. It periodically needs to identify memory that is no longer reachable by the program (garbage) and reclaim it to prevent memory leaks.
- The engine doesn't exist in a vacuum. It's embedded within a host environment (like a browser or Node.js). It uses APIs provided by this environment to interact with the outside world.

> [!Note]
> If one of the assumptions made during optimization turns out to be wrong later (e.g., a variable suddenly holds a different type than expected), the engine needs to gracefully bail out of the optimized code and fall back to the interpreted or less optimized version.

## Different types of Engines

- The V8 engine is the most popular JavaScript engine developed by google and is used in all Chromium based browsers and Node.js.
- SpiderMonkey is a JavaScript engine developed by Mozilla for the Firefox browser, Written primarily in C++ and Rust it was developed by Brenden Eich himself.
- JavaScriptCore is developed by Apple for Safari browser and webkit framework. Focuses on fast startup and efficient memory usage, particularly important on mobile devices.
- Chakra was a JavaScript engine created by Microsoft for the Internet Explorer and the non-chromium version of Microsoft Edge. It had its own distinct architecture.