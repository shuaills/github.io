---
title: 'How to Read a Research Paper'
date: 2023-08-19  
permalink: /posts/2023/08/how-to-read-research-paper/
tags:
  - Research Skills
---
This post summarizes an efficient three-pass approach for reading research papers, based on the article "How to Read a Paper" by S. Keshav.

## Three-Pass Approach 

### First Pass (5-10 mins)

- Read title, abstract, intro, headings, conclusions  
- Get a bird's-eye view
- Assess category, context, correctness, contributions, clarity

<button id="toggleFirst" onclick="toggleVisibility('first')">Ask yourself after 1st Pass</button>

<div id="first" style="display:none">

At the end of the first pass, you should be able to answer:

1. Category: What type of paper is this? A measurement paper? An analysis of an existing system? A description of a research prototype?
2. Context: Which other papers is it related to? Which theoretical bases were used to analyze the problem?
3. Correctness: Do the assumptions appear to be valid?
4. Contributions: What are the paper’s main contributions?
5. Clarity: Is the paper well written?

</div>


### Second Pass (up to 1 hour)

- Read in detail, ignoring proofs etc.
- Make notes on key points, questions, comments
- Grasp purpose, methods, techniques, results
- Assess assumptions, approach, validity of conclusions

<button id="toggleSecond" onclick="toggleVisibility('second')">Ask yourself after 2st Pass</button>

<div id="second" style="display:none">

At the end of the second pass, you should have a thorough grasp of the paper's main thrust and evidence. This is adequate for a paper you're interested in but that is outside your research specialty.

</div>

### Third Pass (1-5 hours)

- Attempt to virtually recreate the work 
- Challenge assumptions, evaluate techniques, interpret results
- Compare recreation to actual paper
- Identify gaps, innovations, limitations

<button id="toggleThird" onclick="toggleVisibility('third')">Ask yourself after 3st Pass</button>

<div id="third" style="display:none">

At the end of the third pass, you should be able to thoroughly deconstruct and critique the paper by surfacing assumptions, innovations, strengths and weaknesses. This is helpful for reviewing papers. 

</div>

## Doing a Literature Survey

- Find 3-5 recent papers with academic search, skim their related work sections
- Identify shared citations and repeated author names - download their key papers  
- Identify where top researchers in that field publish
- Quickly scan recent proceedings of those top conferences 
- Iterate on key papers found through backward snowball sampling

## Benefits

- Estimates time needed to review papers, adjust depth as needed
- Provides systematic way to thoroughly understand papers
- Helps review papers, conduct surveys, keep up with research
- Develops skills in critical analysis and recreation of research

<script>
function toggleVisibility(id) {
  const div = document.getElementById(id);
  if (div.style.display == "none") {
    div.style.display = "block";
  } else {
    div.style.display = "none"; 
  }
}
</script>