# Entry 5 ♡
##### 4/28/25

In this entry:
1. Go over my progress in learning my tool.
2. Reflect on progress in completing MVP of my Freedom Project Website

## Content
Over the past few weeks, I’ve made major progress in learning the tools needed to build my final Freedom Project website. Earlier on, I practiced my skills by creating a demo website using HTML, CSS, and JavaScript. Now, I've taken everything I learned and applied it to create the actual Freedom Project website. 

## Tinkering
I used arrays in JavaScript to store my quiz questions and answers, and I built functions that recorded user input and calculated results.

I also worked carefully on the user flow, making sure users could move smoothly from one question to the next. One tricky part was resetting the radio buttons after each question, which I solved by reviewing examples from <a href="https://www.w3schools.com/js/default.asp">W3Schools</a> and <a href="https://developer.mozilla.org/en-US/docs/Web/API/Document/querySelector"> MDN Web Docs</a>.

Here’s a code snippet that shows how I managed user selections:


``` js
function getSelectedAnswer() {
    const selected = document.querySelector('input[name="question"]:checked');
    if (selected) {
        return selected.value;
    } else {
        alert("Please select an answer before continuing.");
        return null;
    }
}
```

* ```document.querySelector('input[name="question"]:checked')``` grabs the user's selected radio button.

* If no answer is selected, the code alerts the user to choose one before proceeding.


## Skill
Throughout this process, I improved major skills like _troubleshooting_

One example: when moving to the next question, I noticed that previous answers weren't clearing properly. After using console logs to track what was happening, I realized I needed to reset the form between questions. Solving small problems like this made me much more confident in debugging and refining my code step-by-step.

## Next Steps & EDP (Engineering Design Process)
Right now, I’m at Step 5 of the EDP: Create a Prototype. I have finished building the minimum viable product (MVP) 

Next, I’ll move into Step 6: Test and Evaluate, making sure everything works smoothly and preparing final improvements (beyond MVP). 

[Previous](entry04.md) | [Next](entry06.md)

[Home](../README.md)
