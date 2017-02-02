## Android Static Analysis

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

### ART OAT Format
#### oat2dex-python
Extract DEX files from an ART ELF binary

https://github.com/jakev/oat2dex-python

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

#### enjarify
Enjarify is a tool for translating Dalvik bytecode to equivalent Java bytecode.

https://github.com/google/enjarify

#### ded
http://siis.cse.psu.edu/ded/

ded is a project which aims at decompiling Android applications. The ded tool retargets Android applications in .dex format to traditional .class files. These .class files can then be processed by existing Java tools, including decompilers.

#### bytecode-viewer
A Java 8 Jar & Android APK Reverse Engineering Suite (Decompiler, Editor, Debugger & More)

https://github.com/Konloch/bytecode-viewer

#### dexinspector
http://zairon.wordpress.com/dexinspector/

#### JEB
http://www.android-decompiler.com

#### jebPlugins
Various Jeb plugins, including obfuscation restore

https://github.com/flankerhqd/jebPlugins

#### JEB_Scripts
https://github.com/bkerler/JEB_Scripts

#### myJEBPlugins
https://github.com/CunningLogic/myJEBPlugins

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

#### JAADAS
https://github.com/flankerhqd/JAADAS

JAADAS is a tool written in Java and Scala with the power of Soot to provide both interprocedure and intraprocedure static analysis for android applications. Its features include API misuse analysis, local-denial-of-service (intent crash) analysis, inter-procedure style taint flow analysis (from intent to sensitive API, i.e. getting a parcelable from intent, and use it to start activity).

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

#### miasm
Reverse engineering framework in Python

https://github.com/cea-sec/miasm

#### smiasm
http://code.google.com/p/smiasm/

Miasm is a a free and open source (GPLv2) reverse engineering framework. Miasm aims at analyzing/modifying/generating binary programs.

#### armstorm
http://code.google.com/p/armstorm/

#### Darm
https://github.com/jbremer/darm

http://darm.re

#### Capstone
Capstone disassembly/disassembler framework: Core (Arm, Arm64, Mips, PPC, Sparc, SystemZ, X86, X86_64, XCore) + bindings (Python, Java, Ocaml)

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

#### Android-FixResources
Python script to resolve resource identifiers in disassembled (smali) Android Applications

https://github.com/jakev/Android-FixResources

#### AndroidManifestFix
AndroidManifest.xml文件修复工具。用于修复这个文件中属性名称缺失的问题。

https://github.com/zylc369/AndroidManifestFix

#### AmBinaryEditor
AndroidManifest Binary Editor

https://github.com/enimey/AmBinaryEditor

#### axmlprinter
Library for parsing and printing compiled Android manifest files

https://github.com/rednaga/axmlprinter

### Others
#### ApkAnalyser
https://github.com/sonyxperiadev/ApkAnalyser

ApkAnalyser is a static, virtual analysis tool for examining and validating the development work of your Android app. It's a complete tool chain which supports modification of the binary application with more printouts. You are then able to repack, install, run and verify the result from logcat. ApkAnalyser also supports resource analysis, and you can decode XML, look up resource references and detect potential issues in your app.

#### DexDumpSql
Convert DEX content to SQLite database

https://github.com/jakev/DexDumpSql

#### Reverse AIDL tool
https://github.com/opersys/raidl

#### keystore-decryptor
https://github.com/nelenkov/keystore-decryptor

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

https://github.com/dweinstein/pscout

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

#### IntentAnalysis
Static dataflow analysis of Android apps to extract intent values and count intent constructor calls

https://github.com/smee/IntentAnalysis

#### PATDroid
A Program Analysis Toolkit for Android

https://github.com/mingyuan-xia/PATDroid

#### smalisca
Static Code Analysis for Smali files

https://github.com/dorneanu/smalisca

#### IccTA
IccTA is an Inter-Component Communication based Taint Analysis tool. It based on FlowDroid and Epicc to perform inter-component (and also inter-app, thanks to ApkCombiner) privacy leaks in Android apps.

https://github.com/lilicoding/soot-infoflow-android-iccta

#### Amandroid
Amandroid is a static analysis framework for Android apps.

https://github.com/sireum/amandroid
