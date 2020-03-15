# Week 10A - Constrained Writing and Simple Text Analysis

## Overview
- For week 10, we will be looking at some ways to process and do some interesting things with *unstructured*, plain text - meaning text that has NOT (for example) been marked up with HTML or XML or markdown or JSON, or otherwise pre-processed
- ***Get started on this week's assignment's *early* - there's quite a bit of content for this week - and it's going to be mostly "new to you".***
- For 10A (today), we will first walk through some text manipulation techniques that will help us build a *palindrome detector*.
- We will then walk through how to count the frequency of words in a document, which you will need to know how to do for your Word Cloud HW
- See the lecture video links at the bottom of this page - the videos (in Section IV.) walk through the lecture notes (Section II.)
- See the myCourses dropboxes for the precise instructions of each HW assignment


## I. Agenda

- Topics:
  - Loading text into the browser
  - *Constrained writing*:
    - Palindromes
  - Look at unique word counting & stripping out "stop words"
    - Building a "word cloud" app

## II. Lecture Notes
- [Text-1 - Loading Plain Text](https://github.com/tonethar/IGME-330-Master/blob/master/notes/text-1.md)
  - A video linked below walks though these notes
  - There IS an associated HW assignment, the *HW - Palindrome Detector*
- [Text-2 - Constrained Writing](https://github.com/tonethar/IGME-330-Master/blob/master/notes/text-2.md)
  - There is NOT a video for this particular demo page, and there is NOT an associated HW assignment for this page - you have enough assignments to do this week!
  - Please DO take a look at some of the links on this page that discuss *constrained writing* techniques such as "Cut up & Fold in", as well as N+7
  - Look over the *Diastic Machine* demo - we have provided both the start code and the finished code for this. As with the *Palindrome Detector*, this example uses *regular expressions* to strip out punctuation and spaces
- [Text-3 - Simple Text Analysis](https://github.com/tonethar/IGME-330-Master/blob/master/notes/text-3.md)
  - A video linked below walks though these notes
  - There IS an associated HW assignment, *HW - Word Cloud*

## III. HW Assignments
- [HW - Palindrome Detector](https://github.com/tonethar/IGME-330-Master/blob/master/notes/HW-palindrome-detector.md)
- [HW - Word Cloud](https://github.com/tonethar/IGME-330-Master/blob/master/notes/HW-word-cloud.md)

## IV. Videos
- These will help with the HW assignments! 

1) [Text-1: Six ways to load text (19:04)](https://video.rit.edu/Watch/text-1-six-ways-to-load-text):
    - we walk through how the code works for the 6 text loading techniques above
    - we also work with some JavaScript we have not used in this class before:
      - be sure to note the difference between the `oninput` and `onchange` events
      - and note what these methods do:
        - `element.dispatchEvent()`
        - `event.stopPropagation()` & `event.preventDefault()`
        - `element.classList.add()` and `element.classList.remove()`
        - events and attributes related to drag & drop - which can be load files from the user's hard drive:
          - `draggable`, `ondragenter`, `ondragover`, `ondrop`, `event.dataTransfer.setData()`, `event.dataTransfer.getData()`
    - lastly, we use the `XMLHttpRequest` object to load files that are *local* to the web server where the HTML page is hosted (as opposed to files or services on *other* servers) 

2) [Text-1: Palindrome HW (21:57)](https://video.rit.edu/Watch/text-1-palindrome-HW):
    - definitely watch this one for valuable tips on completing the Palidrome homework! I give you plenty of hints on how to use regular expressions to strip out spaces and punctuation, and how to reverse your strings for comparison
    - you should "code along" with what we are doing in this video
  
3) These videos cover how to build an app that strips out "stop words", and counts the frequency of unique words in a document
    - [Demo: Word Counter Part A (17:24)](https://video.rit.edu/Watch/text-3-word-counter-part-A)
    - [Demo: Word Counter Part B (06:57)](https://video.rit.edu/Watch/text-3-word-counter-part-B)

<hr><hr>

| <-- Previous Unit | Home | Next Unit -->
| --- | --- | --- 
| [**week-08-notes.md**](week-08-notes.md)     |  [**Semester Interstitial.md**](interstitial.md) | [**week-10B-NEW.md**](week-10B-NEW.md)
