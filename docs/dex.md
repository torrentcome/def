# Dex
## Dex = Dalvik Executable Format

One of the most remarkable features of the Dalvik Virtual Machine (the workhorse under the Android system) is that it does not use Java bytecode. 

Instead, a homegrown format called DEX was introduced and not even the bytecode instructions are the same as Java bytecode instructions.

Compiled Android application code file.
Android programs are compiled into .dex (Dalvik Executable) files, which are in turn zipped into a single .apk file on the device. .dex files can be created by automatically translating compiled applications written in the Java programming language.

Dex file format:
```
 1. File Header
 2. String Table
 3. Class List
 4. Field Table
 5. Method Table
 6. Class Definition Table
 7. Field List
 8. Method List
 9. Code Header
10. Local Variable List
```
Android has documentation on the `Dalvik Executable Format` (.dex files). You can find out more over at the official docs: Dex File Format

.dex files are similar to java class files, but they were run under the Dalkvik Virtual Machine (DVM) on older Android versions, and compiled at install time on the device to native code with ART on newer Android versions.

You can decompile .dex using the dexdump tool which is provided in android-sdk.
