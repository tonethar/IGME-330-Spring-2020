# Week 10A - Constrained Writing and Simple Text Analysis

## Overview
- For week 10, we will be looking at some ways to process and do some interesting things with *unstructured*, plain text - meaning text that has NOT (for example) been marked up with HTML or XML or markdown or JSON, or otherwise pre-processed
- Today, we will walk through some text manipulation techniques that will help us build a *palindrome detector*:
  - using *regular expressions* to strip out puncutation and spaces
  - turns

## I. Agenda

- Topics:
  - Loading text into the browser
  - *Constrained writing*:
    - Palindromes
  - Look at word counting, stop words, and building a word cloud app
- Homework
  - [HW - Palindrome Detector (Due: 3/26)](https://github.com/tonethar/IGME-330-Master/blob/master/notes/HW-palindrome-detector.md)
  - [HW - Word Cloud (Due: 3/29)](https://github.com/tonethar/IGME-330-Master/blob/master/notes/HW-word-cloud.md)

## II. Lecture Notes
- [Text-1 - Loading Plain Text](https://github.com/tonethar/IGME-330-Master/blob/master/notes/text-1.md)
- [Text-2 - Constrained Writing](https://github.com/tonethar/IGME-330-Master/blob/master/notes/text-2.md)
- [Text-3 - Simple Text Analysis](https://github.com/tonethar/IGME-330-Master/blob/master/notes/text-3.md)

## III. HW Assignments
- [HW - Palindrome Detector](https://github.com/tonethar/IGME-330-Master/blob/master/notes/HW-palindrome-detector.md)
- [HW - Word Cloud](https://github.com/tonethar/IGME-330-Master/blob/master/notes/HW-word-cloud.md)

# IV. Videos
- These will help with the HW assignments:
  - [Text-1: Six ways to load text (19:04)](https://video.rit.edu/Watch/text-1-six-ways-to-load-text):
    - we walk through how the code works for the 6 text loading techniques above
    - we also work with some JavaScript we have not used in this class before:
      - be sure to note the difference between `oninput` and `onchange`
      - and note what these methods do:
        - `element.dispatchEvent()`
        - `e.stopPropagation()` & `e.preventDefault()`
        - `element.classList.add()` and `element.classList.remove()`
        - events and attributes related to drag & drop - which can be load files from the user's hard drive: `draggable`, `ondragenter`, `ondragover`, `ondrop`, `dataTransfer.setData()`, `dataTransfer.getData()`
    - lastly, we use the `XMLHttpRequest` object to load files that are *local* to the web server where the HTML page is hosted (as opposed to files or services on *other* servers) 
  - [Text-1: Palindrome HW (21:57)](https://video.rit.edu/Watch/text-1-palindrome-HW):
    - definitely watch this one for valuable tips on completing the homework! I give you plenty of hints on how to use regular expressions to strip out spaces and punctuation, and how to reverse your strings for comparison
    - [Demo: Word Counter Part A (17:24)](https://video.rit.edu/Watch/text-3-word-counter-part-A)
    - [Demo: Word Counter Part B (06:57)](https://video.rit.edu/Watch/text-3-word-counter-part-B)

<hr><hr>

| <-- Previous Unit | Home | Next Unit -->
| --- | --- | --- 
| [**week-08-notes.md**](week-08-notes.md)     |  [**Semester Interstitial.md**](interstitial.md) | [**week-10B-NEW.md**](week-10B-NEW.md)
