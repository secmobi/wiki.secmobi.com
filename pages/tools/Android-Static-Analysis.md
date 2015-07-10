## Android Static Analysis Tool

### Dalvik Disassembling and Bytecode Manipulation
#### smali/baksmali
http://code.google.com/p/smali/

smali/baksmali is an assembler/disassembler for the dex format used by dalvik, Android's Java VM implementation. The syntax is loosely based on Jasmin's/dedexer's syntax, and supports the full functionality of the dex format (annotations, debug info, line info, etc.)

#### Dedexer
http://dedexer.sourceforge.net

Dedexer is a disassembler tool for DEX files. Dedexer is able to read the DEX format and turn into an "assembly-like format". This format was largely influenced by the Jasmin syntax but contains Dalvik opcodes. For this reason, Jasmin is not able to compile the generated files. Dedexer disassembles Optimized DEX (ODEX) files by default.

#### dexinfo
https://github.com/poliva/dexinfo

#### dexter
http://newandroidbook.com/tools/dexter.html

#### reverse-android
https://github.com/nelhage/reverse-android

Some miscellaneous Android reverse-engineering tools:

- ddx.el: An emacs mode for working with Android assembly.
- ddx2dot: A Python script for rendering methods in dedexer-produced assembly files to control-flow graphs using dot

#### IDA Pro
http://www.hex-rays.com/products/ida/index.shtml

#### dexdump
http://developer.android.com/sdk/index.html

dexdump if a tool included in Android SDK. It can simply parse DEX file format and Dalvik bytecodes in DEX files.

#### ASMDEX
http://asm.ow2.org/asmdex-index.html

ASMDEX is a bytecode manipulation library as ASM but it handles the DEX bytecode used by Android executables. Only the core library, the tree library and a tool to convert bytecode to code generating it (asmdexifier) are available. The underlying principle while developing ASMDEX was to keep it very similar to ASM to ease the cost of porting tools done for Oracle Java bytecode to Android bytecode.

#### dexterity
https://github.com/rchiossi/dexterity

#### dexrehash
https://github.com/cryptax/dextools

#### dexmaker
http://code.google.com/p/dexmaker/

A Java-language API for doing compile time or runtime code generation targeting the Dalvik VM.

#### APK Studio
http://www.vaibhavpandey.com/apkstudio

APK Studio is now made cross-platform and is available for download as a public-beta.

APK Studio is an IDE for decompiling/editing & then recompiling of android application binaries. Unlike initial release being Windows exclusive & also didn't support frameworks, this one is completely re-written using QT for cross-platform support. You can now have multiple frameworks installed & pick a particular one on a per project basis.

#### Virtuous Ten Studio
http://www.virtuous-ten-studio.com

#### APKfuscator
https://github.com/strazzere/APKfuscator

A generic DEX file obfuscator and munger. [[www.strazzere.com/papers/DexEducation-PracticingSafeDex.pdf|Download related slide.]]

#### ReDexer
http://www.cs.umd.edu/projects/PL/redexer/

Redexer is a bytecode instrumentation framework for Dalvik bytecode (used in Android applications). Redexer is a set of OCaml based utilities which helps programmers parse, manipulate, and generate bytecode for the Dalvik VM.

#### radare
http://radare.org

Opensource tools to disasm, debug, analyze, manipulate binary files. Support multi-architecture and multi-platform.

#### AppInspect
http://www.privateerlabs.net/products/appinspect

### Dalvik Decompilation

#### jadx
https://github.com/skylot/jadx
#### dex2jar
http://code.google.com/p/dex2jar/

dex2jar contains 4 components:

- dex-reader is designed to read the Dalvik Executable (.dex/.odex) format. It has a light weight API similar with ASM.
- dex-translator is designed to do the convert job. It reads the dex instruction to dex-ir format, after some optimize, convert to ASM format.
- dex-ir used by dex-translator, is designed to represent the dex instruction.
- dex-tools tools to work with .class files. It can be used to modify an apk or deobfuscate a jar.

#### dara
http://siis.cse.psu.edu/dare/index.html

#### ded
http://siis.cse.psu.edu/ded/

ded is a project which aims at decompiling Android applications. The ded tool retargets Android applications in .dex format to traditional .class files. These .class files can then be processed by existing Java tools, including decompilers.

#### dexinspector
http://zairon.wordpress.com/dexinspector/

#### JEB
http://www.android-decompiler.com

#### undx
http://undx.sourceforge.net

Undx is a bytecode translator, it converts the bytecode for the dalvik vm (a virtual machine for android applications) to standard java bytecode.

#### dex-decompiler
http://code.google.com/p/dex-decomplier/

As its name, dex-decompiler is a decompiler of DEX file.

#### Xenotix-APK-Decompiler
https://github.com/ajinabraham/Xenotix-APK-Decompiler
#### AndroChef
http://dj.navexpress.com/androchef.htm

### Java Decompilation
#### jd-gui
http://java.decompiler.free.fr/?q=jdgui

JD-GUI is a standalone graphical utility that displays Java source codes of “.class” files. You can browse the reconstructed source code with the JD-GUI for instant access to methods and fields. It supports Windows, Linux and Mac OS X.

#### Luyten
https://github.com/deathmarine/Luyten
#### JAD
http://www.varaneckas.com/jad/

JAD is a commandline Java decompiler.

#### procyon
https://bitbucket.org/mstrobel/procyon

#### soot
http://www.sable.mcgill.ca/soot/

Soot is a Java optimization framework. It provides four intermediate representations for analyzing and transforming Java bytecode:

- Baf: a streamlined representation of bytecode which is simple to manipulate.
- Jimple: a typed 3-address intermediate representation suitable for optimization.
- Shimple: an SSA variation of Jimple.
- Grimp: an aggregated version of Jimple suitable for decompilation and code inspection.

Soot can be used as a stand alone tool to optimize or inspect class files, as well as a framework to develop optimizations or transformations on Java bytecode.

#### dava
http://www.sable.mcgill.ca/dava/

Dava is a decompiler for arbitrary Java bytecode.

#### DecoJer
Home: http://www.decojer.org

Blog: http://blog.decojer.org

Code: http://code.google.com/p/decojer/

A (not yet ready) Java Decompiler Open Source Project.

#### JBE - Java Bytecode Editor
http://www.cs.ioc.ee/~ando/jbe/

JBE is a bytecode editor suitable for viewing and modifying java class files.

### ARM Disassembling
#### IDA Pro
http://www.hex-rays.com/products/ida/index.shtml

#### radare
http://radare.org

Opensource tools to disasm, debug, analyze, manipulate binary files. Support multi-architecture and multi-platform.

#### smiasm
http://code.google.com/p/smiasm/

Miasm is a a free and open source (GPLv2) reverse engineering framework. Miasm aims at analyzing/modifying/generating binary programs.

#### armstorm
http://code.google.com/p/armstorm/

#### Darm
https://github.com/jbremer/darm

http://darm.re

#### Capstone
http://www.capstone-engine.org/

### ARM Decompilation
#### Hex-ray Decompiler for ARM
http://www.hex-rays.com/products/decompiler/

#### arm-thumb-decompiler-plugin
https://code.google.com/p/arm-thumb-decompiler-plugin/

#### Retargetable Decompiler
http://decompiler.fit.vutbr.cz/index.php

### APK Repackaging
#### apktool
http://code.google.com/p/android-apktool/

It is a tool for reverse engineering 3rd party, closed, binary Android apps. It can decode resources to nearly original form and rebuild them after making some modifications; it makes possible to debug smali code step by step. Also it makes working with app easier because of project-like files structure and automation of some repetitive tasks like building apk, etc.

Google group: http://groups.google.com/group/apktool

#### signapk
http://source.android.com

signapk is a part of AOSP. It's used for signing a APK file.

### Android Binary XML Decoding
#### AXMLPrinter
http://code.google.com/p/android4me/

AXMLPrinter is a command line tool writing by Java which converts Android binary XML file (aka AXML file) into plaintext XML file.

#### axml2xml
http://code.google.com/p/android-random/downloads/detail?name=axml2xml.pl

axml2xml is another AXML converter but written by Perl.

#### apk-extractor
http://code.google.com/p/apk-extractor/

Android Application (.apk) file extractor and Parser for Android Binary XML. Written by Java.

#### xml-apk-parser
https://code.google.com/p/xml-apk-parser/

#### apktools
not the apktool
https://github.com/devunwired/apktools

#### axml
https://code.google.com/p/axml/
### Others
#### ApkAnalyser
https://github.com/sonyxperiadev/ApkAnalyser

ApkAnalyser is a static, virtual analysis tool for examining and validating the development work of your Android app. It's a complete tool chain which supports modification of the binary application with more printouts. You are then able to repack, install, run and verify the result from logcat. ApkAnalyser also supports resource analysis, and you can decode XML, look up resource references and detect potential issues in your app.

#### ART
http://androidcracking.blogspot.jp/2012/04/android-reverse-tools-art.html

An easy-mode gui for all your decompiling and recompiling needs. Supports Windows.

#### apk-recovery
http://code.google.com/p/apk-recovery/

Apk-recovery software is just a convenient tool which might help Android developers to recover main resources from their apk file.

#### MIUI patchrom tools
https://github.com/MiCode/patchrom_tools

#### RetroSkeleton
http://retroskeleton.com
easy online Android app rewriting

### Program Analysis

#### FlowDroid – Taint Analysis
http://sse-blog.ec-spride.de/android/flowdroid/

#### PScout
http://pscout.csl.toronto.edu

#### decaf-platform
http://code.google.com/p/decaf-platform/

#### SCanDroid
https://github.com/SCanDroid/SCanDroid

#### android-dataflow-analysis
https://code.google.com/p/android-dataflow-analysis/

#### smali-cfgs
http://code.google.com/p/smali-cfgs/

#### SAAF - Static Android Analysis Framework
http://code.google.com/p/saaf/

#### Chord
http://pag.gatech.edu/chord

#### STAMP
https://sites.google.com/site/stampwebsite/
