# Entry 4 ♡
##### 3/10/25

In this entry:
1. Go over my progress in learning my tool.
2. Reflect on progress in making my Freedom Project Website

## Content 
Over the past few weeks, I've made significant progress on my final Freedom Project. Earlier in the project, I focused on creating a DEMO website to practice the skills I had just learned, like HTML, CSS, and JavaScript. Now, I'm applying those skills to build the actual Freedom Project website.


## Tinkering 
I spent a lot of time tinkering with my personality quiz website. I started by working with arrays in JavaScript to store quiz questions and answers, which is crucial for making the quiz dynamic. The big focus was setting up the structure for how the questions would display and how user responses would be recorded. I also worked on linking the questions to a scoring system, which will help calculate personality types based on user input.

One thing that really helped during this process was using resources like <a href="https://www.w3schools.com/js/default.asp">W3Schools</a> and <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide">MDN Web Docs</a>. They were perfect for troubleshooting and learning new concepts, like how to work with arrays and manage user input dynamically.

Here is a code snippet example:

```js 

    const answer = document.querySelector('input[name="q1"]:checked')?.value; // Get the selected answer
    if (answer) {
        console.log("User selected:", answer);
    } else {
        alert("Please select an answer.");
    }
}
</script>
```
* `document.querySelector('input[name="q1"]:checked')` This retrieves the selected answer for question 1.
* `value` Gets the value of the selected radio button (either "Yes" or "No").
* `console.log()` Prints the selected answer to the console. If no answer is selected, it shows an alert.


## Skill 
Throughout the making of this entry, I’ve developed some important skills that go beyond just writing code. 

First, I’ve learned how to **manage data using arrays** and **how to structure that data** in a way that makes it easier to access and manipulate. This skill will definitely help in future projects where I need to organize large amounts of information.

Another skill I've developed is how to **troubleshoot issues** in real-time, especially when something doesn’t work as expected. For example, when I was working on displaying quiz questions dynamically, the answers wouldn't show up properly when the next question was displayed. I initially thought the issue was with the event listener, but after checking the logic, I realized the problem was that the HTML elements weren't being correctly updated when transitioning between questions.

This process required patience and **step-by-step problem-solving**. I learned the importance of testing small chunks of code to find the root of the issue rather than assuming the problem is in one specific area.


## Next Steps & EDP (Engineering Design Process)

I’m currently on step #5 of the Engineering Design Process (EDP): Create a prototype. At this stage, I’m continuing to code as I work on my website and learn along the way. Next steps will be to test and evaluate the prototype. 




[Previous](entry03.md) | [Next](entry05.md)

[Home](../README.md)
