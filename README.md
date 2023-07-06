# MacOS `say` Command Examples

The `say` command is a macOS utility that uses the Speech Synthesis manager to convert text to audible speech. This README provides examples of how to use the `say` command effectively.

## Table of Contents

1. [Basic Usage](#basic-usage)
2. [Using Different Voices](#using-different-voices)
3. [Adjusting Speech Rate](#adjusting-speech-rate)
4. [Saving Speech to a File](#saving-speech-to-a-file)
5. [Reading From a File](#reading-from-a-file)
6. [Sending Output to Network](#sending-output-to-network)
7. [Interactive Mode](#interactive-mode)
8. [Choosing Audio Formats](#choosing-audio-formats)

## Basic Usage

To simply read text, type `say` followed by the text you want read:

```shell
say "Hello, World!"
```

## Using Different Voices

To change the voice, use the `-v` flag followed by the name of the voice:

```shell
say -v Samantha "Hello, World!"
```

To see all the voices installed on your system:

```shell
say -v '?'
```

## Adjusting Speech Rate

The speech rate can be modified with the `-r` option. This is measured in words per minute. For example, to slow the rate:

```shell
say -r 100 "Hello, World!"
```

## Saving Speech to a File

To save the speech to a file, use the `-o` flag followed by the filename:

```shell
say -o hello.aiff "Hello, World!"
```

## Reading From a File

To read from a file, use the `-f` option followed by the file name:

```shell
say -f myTextFile.txt
```

## Sending Output to Network

To redirect the speech output through AUNetSend, you can use `-n` option followed by the service name and IP port:

```shell
say -n "AUNetSend:8080" "Hello, World!"
```

## Interactive Mode

The `-i` flag makes the `say` command print text line by line during synthesis:

```shell
say -i "Hello, World!"
```

You can also specify the markup color:

```shell
say --interactive=green "Hello, World!"
```

## Choosing Audio Formats

To specify the file format for the output, you can use `--file-format` option:

```shell
say -o hello.caf --file-format=caff "Hello, World!"
```

To specify the audio data format:

```shell
say -o hi.m4a --data-format=alac "Hello, World"
```

To specify the sample rate and format:

```shell
say -o hi.caf --data-format=LEF32@8000 "Hello, World"
```

For a full list of possible commands and their usage, refer to the `say` man page by typing `man say` into your terminal.

This document provides a basic introduction to the `say` command in macOS. The possibilities are extensive and can be combined in various ways to achieve the desired output. Happy coding!