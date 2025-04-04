# Tool Learning Log

## Tool: **Easy Toggle State**

## Project: **Personality Quiz**

---

### 9/30/24: Learning Log 1
* First thing that I did was search up "Easy Toggle State for beginners" on Youtube, I only found tutorials on how to make toggles from scratch.
 * Instead of watching tutorials, I wanted to explore the <a href = "https://twikito.github.io/easy-toggle-state/" > Easy Toggle State </a> website.
* When exploring the website of my tool, I took a look at the demo page. _The demo page is a website that developers made in order to show us how the concepts of this tool work._
* Link to the demo page website: https://twikito.github.io/easy-toggle-state/demo
  * On the demo page I tried to visualize how I want to layout my quiz. The developers that created the demo page used features like **Tabs and Checkboxes**
  * Later on, I officially came up with 1 feature that I will be using in my website. The feature is called **"Radio buttons"**.
<img width="577" alt="Screenshot 2024-10-07 at 6 49 09 AM" src="https://github.com/user-attachments/assets/e721d6d5-acbe-4d72-bfa8-2551d9342264">

* I chose this feature because it looks like an answer choice section from a quiz. It reminded me of google forms that I would fill out in school. You can see the resemblance in the picture above.


Here 3 phrases that I have learnt + their meanings in my own words:

* **recurrent behavior** - atterns or actions that repeat over time (mostly through functions).
* **native component** - a UI element for the use of better performance on many devices.
* **ARIA** - make web applications more accessible like screen readers (_Accessible Rich Internet Applications_).


**Next up:** I will pick another feature that is suitible for my freedom project.



### 10/21/24: Learning Log 2

 Starting off from where I left on the last log, the previous feature that I picked was Radio buttons. My main task for this learning log is to discover another feature that I will use for my Freedom Project Website. In order to find the most suitable, I will be _tinkering_.

* The first thing that I did was visit my tools website <a href = "https://twikito.github.io/easy-toggle-state/" > (Easy Toggle State) </a>
 * I viewed the source over and over again to see what would be of use to me
 * I saw a feature called **Tabs**
    * This reminded me of tabs open on a browsing app
    * I will be using Tabs as another feature that will be included in my Webpage
* When looking at tabs, I saw that there was 3 versions of them. At first I didn't get the difference because the outcome of this feature was the same. However the code was very different


Below will be the three different tabs and the difference of each:
* **simple tabs** -  Basic tab functionality, with mouse support only
* **tabs and arrow keys** - Adds keyboard accessibility, allowing users to navigate between tabs using arrow keys
* **tabs with ARIA** - Enhances accessibility, enabling support for screen readers, etc

I will provide example codes of each tab:


1. **Simple Tabs**

```js
<div class="tabs">
  <ul>
    <li><a href="#tab1">Tab 1</a></li>
    <li><a href="#tab2">Tab 2</a></li>
  </ul>
  <div id="tab1" class="tab-content">Content for Tab 1</div>
  <div id="tab2" class="tab-content">Content for Tab 2</div>
</div>

```

2. **Tabs and Arrow Keys**

```js
let tabs = document.querySelectorAll('.tab');
tabs.forEach((tab, index) => {
  tab.addEventListener('keydown', (e) => {
    if (e.key === 'ArrowRight') {
      tabs[(index + 1) % tabs.length].focus();
    } else if (e.key === 'ArrowLeft') {
      tabs[(index - 1 + tabs.length) % tabs.length].focus();
    }
  });
});
```


3. **Tabs with ARIA**


html part of code:
```html
<div role="tablist">
  <div role="tab" id="tab1" aria-controls="panel1" aria-selected="true" tabindex="0">Tab 1</div>
  <div role="tab" id="tab2" aria-controls="panel2" tabindex="0">Tab 2</div>
</div>
<div role="tabpanel" id="panel1" aria-labelledby="tab1">Content for Tab 1</div>
<div role="tabpanel" id="panel2" aria-labelledby="tab2">Content for Tab 2</div>

```
Javascript part of code:

```js
const tabs = document.querySelectorAll('[role="tab"]');
const panels = document.querySelectorAll('[role="tabpanel"]');

tabs.forEach(tab => {
  tab.addEventListener('click', function() {
    tabs.forEach(t => t.setAttribute('aria-selected', 'false'));
    panels.forEach(p => p.setAttribute('hidden', 'true'));

    this.setAttribute('aria-selected', 'true');
    document.getElementById(this.getAttribute('aria-controls')).removeAttribute('hidden');
  });
});

```


Like I said before, the difference in code is crystal clear. In my opinion, I would say that ARIA Tabs are the most complex. One is the least complex on the list, while three is the most complex. Since I am a beginner to this tool, I will stick with the Simple Tabs.


**Next up:** I will start working on my tinkering webpage in my IDE.

### 11/8/24: Learning Log 3

Previously, I picked another feature that I will be including in my website. I chose Tabs, however I didn't explain the significance/role that it would have in my website.

* I wanted to get an idea of how my wepage laayout would be
  * Immediatley I startedlooking for inspo so I went to Google Forms to be reminded of their format.
 * I dont want my Quiz webpage to be exactly the same as Google Forms so, I thought that I would include tabs to be a part of the end of the quiz.
  * As the user finishes the quiz, they keep the total of the points they earned from answering the choices. I will then use tabs to seperate the personalities into their given group based on the points earned.

* Going back to my start up progress from LL1 in my IDE, I created tinkering files that would be used for my "Tinkering Website"
* I am planning to make this webesite to test out features that I learn/am willing to use.

Here is an img of my IDE pov so far:
<img width="375" alt="Screenshot 2024-11-11 at 7 32 25 PM" src="https://github.com/user-attachments/assets/a5cac76a-d574-4a54-8659-2fe1470dda4f">

* I am willing to practice my CSS skills from past years in order to enhance my tinkering website.
 * I will be labelling this task as **_Beyond MYP_**

I inserted a HTML, CSS, and JS layout in order to be prepared for my upcoming Demo Webpage.

```html
    <head>

        <!-- Required meta tags -->
        <meta charset="utf-8">
        <meta name="viewport" content="width=device-width, initial-scale=1">
        <title>Demo Site</title>
        <link rel="stylesheet" href="./style.css">
        <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0-alpha1/dist/css/bootstrap.min.css" rel="stylesheet" />
        <link href="style.css" rel="stylesheet" type="text/css" />
         <!-- Link to the Easy Toggle State JS from CDN -->
    <script src="https://cdnjs.cloudflare.com/ajax/libs/easy-toggle-state/1.16.0/easy-toggle-state.min.js" defer></script>

        <style>
            /* CSS */
        </style>

    </head>

```
As you can see above, I made sure everything in the `<head>` was sorted out and linked. I then continued to write basic HTML code in order to start up my DEMO Page. I linked the Easy Toggle State JS from <a href = "https://cdnjs.com/libraries/easy-toggle-state">CDN</a>. _I made sure to link the most recent and updated version so my code would be able to run smoothly_

- One thing that I would like to keep up is include `<!-- comments -->` In order to be organized and keep notes to prep for the final Webpage


``` html
<main>

 <h1>Welcome to My Website</h1>
 <p> This website was created so I could test my coding skills, BEHOLD!!! THE!!! TOGGLE!! SITE!!   </p>

</main>
```
My goal is to keep everything simple, but practice my JS skills using the tool that I am currently learning. I have to link my tool in order to use it but I am having trouble in doing so. I am finished with my prep and ready to go!


**Next up:** Practice radio buttons



### 11/18/24: Learning Log 4

In the previous learning log, the main things that I focused on was picking another tool to use for my freedom project. In this learning log I will be using my previous knowledge of CSS and HTML to startt working on my demo website.


* The first thing that I did was open my IDE and cd into my tool tinkering folder
   * After that I googled the HTML and CSS layout
   * I placed the layout where it needed to be and started coding what I want my base to look like
<<<<<<< HEAD

* I refreshed my memory on CSS code, one thing that I found very helpful was mt SEP10 notes
* I am so grateful that I took specific notes on concepts that I didn't really get and paraphrase in order to properly understand
* For this freedom project I want to be able to project my thinking so future me could easily progress

* Let me show you a piece of information that came useful when I was working on my base for the demo website.

Different type of inputs:

* text - `<input type="text" />`
* checkbox - `<input type="checkbox" />`
* radio - `<input type="radio" />`
* button - `<input type="button" />`

This was a note jotted down in my notes. In Unit 1: Basic Web Design, I thoroughly explained concepts in HTML and CSS with examples of the code. I can use my SEP10 notes as a resource for making my freeodm project this year.

Another thing that I accomplished during the duration of this learning log is finding the perfect CSS gradient for my demo website. The code that I used is:

```css
    background: linear-gradient(240deg, #eeaeca, #94bbe9, #f1d7e7);
```

 The color of a website is very important because:

* Colors on a website change the look of a website
* Connect the user to your website
* Affects how people feel
* What they see
* How they act


_tertiary colors_ = The combination of primary and secondary colors


**Next up:** Improve the base + implement your tool!!!

### 12/2/24: Learning Log 5
N/A

### 12/9/24: Learning Log 6

After all the CSS and Basic HTML code my DEMO cite is finalized and ready to go

Down below is a screenshot of the final CSS + Basic HTML look for my DEMO site:
<img width="1279" alt="Screenshot 2024-12-09 at 10 26 51 AM" src="https://github.com/user-attachments/assets/7cc22fed-fba1-4cf9-bba5-725cafd3d590">


Now that everything is set up, I need to learn more about my tool.

- I open up the <a href = "https://twikito.github.io/easy-toggle-state/" > Easy Toggle State </a> website.


**_Basic State State_**

```js
const toggleState = new ToggleState(false);

// Toggle from false to true
toggleState.toggle();  // true

// Toggle back from true to false
toggleState.toggle();  // false
```
**What I learnt:** When using new `ToggleState()`  I can initialize a state with a default value (in this case, false). The `toggle()` method automatically flips the state between true and false without needing to manually write it. This saves time and reduces the chances of mistakes in the code when managing boolean values.


- The Easy Toggle State is a great tool when it comes to using booleans (true/false).
- I learned that this tool helps the readability of code. It waters down everything and makes it easier for us to use

On the demo website I tried creating a `toggleCheckbox`. Now that I'm trying to code it is kind of difficult but I will get through it. This is the code that I used

``` js
        <label for="toggleCheckbox">Toggle Checkbox</label>
        <input type="checkbox" id="toggleCheckbox">
```

Without any CSS, this is what the original Checkbox looks like so far:

<img width="191" alt="Screenshot 2025-01-01 at 9 12 19 PM" src="https://github.com/user-attachments/assets/2f464e3c-70a3-4417-ac28-5ca6ec6f4e93" />

In my next log, I will use the `toggleCheckbox` to create a series of questions on my DEMO website!


### 1/3/25: Learning Log 7

As stated in the previous log. I will create a series of questions using the `toggleCheckbox`.

The series of questions (Check for yes; leave blank for no):

1. Do you like cake?
2. Have you worked out today?
3. Do you have pets?
4. Are you a teenager?
5. Is your favorite color red?

This is the list of questions that will be included in my DEMO site.

Code:

``` js
<ul>
    <li>
        <label for="toggleCheckbox">Do you like cake?</label>
        <input type="checkbox" id="toggleCheckbox"></li>
    <li>
        <label for="toggleCheckbox">Have you worked out today?</label>
        <input type="checkbox" id="toggleCheckbox"></li>
    <li><label for="toggleCheckbox">Do you have pets?</label>
        <input type="checkbox" id="toggleCheckbox">
</li>
<li><label for="toggleCheckbox">Are you a teenager?</label>
    <input type="checkbox" id="toggleCheckbox"></li>
    <li><label for="toggleCheckbox">Is your favorite color red?</label>
        <input type="checkbox" id="toggleCheckbox"></li>
  </ul>

```

This is what my code looks like at the very moment. I want to improve how it shows up on the webpage. Like the spacing and where/how it is adjusted


### 2/24/25: Learning Log 8

Previously, I was using my Demo Site to test out the new coding that I learned. I will now be working on my Freedom Project webpage. The first thing that I did was create a <a href = "https://github.com/liane4323/sep11-freedom-project/blob/main/prep/plan.md "> plan </a> with deadlines.

By making this plan, I am ensuring that I will fully make use of my time and stay organized with my project. I also read <a href = "https://kidshealth.org/en/teens/focused.html " > this website </a>  in order to get motivation for tackling school work ahead 

For the project, the first thing that I need to do is create the HTML structure for the quiz start page. This includes the questions that need to be asked. I *brainstormed* questions and did my *research* on different personality types in this reading log.

Main 3 Types of Personality Traits:

* **Psychoticism**: A personality trait associated with risk-taking, impulsivity, and some antisocial behaviors.
* **Neuroticism**: A trait linked to negative emotions such as anxiety, worry, and fear.
* **Extraversion**: A personality type characterized by high energy, sociability, and friendliness.


Here are the Quiz Questions I came up with:

Do you enjoy being the center of attention?
Yes → Extraversion
No → Neuroticism or Psychoticism


Do you often act without thinking about the consequences?
Yes → Psychoticism
No → Neuroticism or Extraversion


Do you get stressed or anxious easily?
Yes → Neuroticism
No → Psychoticism or Extraversion


Do you prefer spending time alone rather than in a group?
Yes → Neuroticism or Psychoticism
No → Extraversion


### 3/10/25: Learning Log 9
For this learning log, I worked on building the initial structure for my personality quiz website. I used _HTML, CSS, and JavaScript_ to set up the quiz’s front-end and ensure smooth transitions between the quiz sections. Here's a breakdown of what I did:


**HTML Structure**

I started by creating a basic HTML layout for the quiz, making sure that each quiz section was defined. I used the following:

* Buttons to navigate through the quiz sections.
* Radio buttons for users to select their answers ("Yes" or "No").
* A results section that will display the final personality type based on the answers provided.

**JavaScript**

To make the quiz interactive, I implemented two key JavaScript functions:

* ``toggleSection(currentSection, nextSection)``
 * This function hides the current section and shows the next section when a user clicks "Next." It allows the quiz to move from one question to the next without refreshing the page. 

* ``showResults():``
 * This function collects the user’s answers and determines the personality type.

**CSS Styling**

I used simple CSS to:

* Initially hide all quiz sections except for the first one
* Set the layout so each quiz question appears sequentially as the user answers and clicks "Next."
* Styled the buttons and other elements using _Bootstrap_

Honorable mentions:<a href = "https://www.w3schools.com/"> W3schools </a> & <a href = "https://www.freecodecamp.org/learn"> freeCodeCamp </a>


### 3/17/25: Learning Log 10 


In this log, I focused on building the core structure of my personality quiz. I defined an array of objects to store quiz questions, answer choices, and scores based on personality types. 


**Key Accomplishments:**
1. Defining the Quiz Data Structure (Array of Objects)
I created an array where each object represents a question.


_Example of an array object structure:_

```
const questions = [
  {
    question: "What’s your favorite activity?",
    answers: [
      { text: "Reading", score: 2 }, 
      { text: "Sports", score: 1 },
      { text: "Music", score: 3 }
    ]
  },
];
```

This structure helps keep everything organized as the quiz evolves.



**Challenges & Solutions:**
Structuring the Scoring System: I had to figure out how to assign scores to answers so that personality traits could be calculated correctly. I used key-value pairs inside each object to map answers to specific personality scores.

Example:


```{ text: "Reading", score: 2 } // Mapping "Reading" to a score```

I tested different ways to retrieve and display questions, aiming to make the transitions feel smooth for the user.

Next Steps:
Finalize the array and test the functionality to ensure it correctly stores and retrieves data.
Write functions to calculate quiz results based on user input.
Improve the user experience by refining how questions are displayed and making transitions between sections smoother.

This week, I’ve made great progress by building a solid foundation for my quiz. The structure I’ve set up makes it easy to add more questions and expand the quiz later. Excited to move forward with the result calculations next!

### 4/1/25: Learning Log 11

In this log, I restructured the quiz questions into a more efficient format, making it easier to retrieve and score user responses. Additionally, I refined the JavaScript functions responsible for handling user input, calculating quiz results, and displaying questions.


* Improved Quiz Flow: Instead of hardcoding each question into the HTML, I implemented a function to dynamically load and display each question.
* Smoother Transitions: Sections now fade in and out smoothly to create a more polished user experience.
* Error Handling: Users must select an answer before proceeding, preventing skipped questions and ensuring accurate results.
* Refined Scoring System: The quiz now correctly sums user scores and determines their personality type

  
``` js 
function loadQuestion() {
    let questionObj = questions[currentQuestion]; // Get the current question object from the array
    document.getElementById("question-text").textContent = questionObj.question; // Display the question text

    let optionsContainer = document.getElementById("options"); // Select the div where options will go
    optionsContainer.innerHTML = ""; // Clear previous question's options

    questionObj.answers.forEach((answer, index) => { // Loop through answer choices
        let input = `<input type='radio' name='answer' value='${questionObj.scores[index]}'> ${answer}<br>`; // Create a radio button input
        optionsContainer.innerHTML += input; // Add the input to the options container
    });
}
```
This function pulls the current question from the questions array, updates the question in the HTML, and generates answer option as radio buttons. 


<!--
* Links you used today (websites, videos, etc)
* Things you tried, progress you made, etc
* Challenges, a-ha moments, etc
* Questions you still have
* What you're going to try next
-->
