# BurstCompiler

## Overview

* Burst is an LLVM based math-aware backend Compiler Technology. It takes the C\# jobs and produces highly-optimized code taking advantage of the particular capabilities of the platform.
* Burst is primarily designed to work efficiently with the Job system.
* Burst is working on a subset of .NET that doesn't allow the usage of any managed objects/reference types in your code \(class in C\#\).
* Supports a [subset of C\#](https://docs.unity3d.com/Packages/com.unity.burst@1.2/manual/index.html#cnet-language-support).

## Language Support

Unsupported features:

* Types:
  * `char` \(this will be supported in a future release\)
  * `string` as this is a managed type
  * `decimal`
* Managed arrays: You should use instead a native container, `NativeArray<T>` for instance.
* `catch`
* `try/finally` \(which will come at some point\)
* `foreach` as it is requiring try/finally \(This should be supported in a future version\)
* Storing to static fields except via Shared Static
* Any methods related to managed objects \(e.g string methods...etc.\)

## Links

* [Burst User Guide](https://docs.unity3d.com/Packages/com.unity.burst@1.2/manual/index.html).
* [Unity.Mathematics](https://docs.unity3d.com/Packages/com.unity.mathematics@1.2/manual/index.html) "A C\# math library providing vector types and math functions with a shader like syntax. Used by the Burst compiler to compile C\#/IL to highly efficient native code."
* Burst videos:
  * [Unite Austin 2017 - Writing High Performance C\# Scripts](https://www.youtube.com/watch?v=tGmnZdY5Y-E&feature=youtu.be) - Joachim Ante introduction.

