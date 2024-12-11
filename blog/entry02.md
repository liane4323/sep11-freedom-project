# Entry 2 ♡
##### 12/11/24

In this entry:

1. Finalize the content that I will be putting on my DEMO website.
2. Go over my progress in learning my tool.


## Content 

During the past few weeks I have been learning more about Easy Toggle State JS. In the previous blog, I mentioned the creation of a DEMO page. Creating a demo website will help me implement the learning that I have done before the final.

## Tinkering 

In the process of learning my tool, I chose to pick two features to start learning. This decision helped me be on track with my learning progress and deeply understand concepts. Down below, I will go over the process of me picking a feature.

The first thing that I did was visit my tools website <a href = "https://twikito.github.io/easy-toggle-state/" > (Easy Toggle State) </a> . I viewed the source over and over again to see what would be of use to me then I saw a feature called `tabs`. This feature reminded me of tabs open on a browsing app. When looking at this feature, I noticed that there were 3 versions that we can pick from. At first I didn't get the difference between these versions because the outcome of this feature was the same. In order to understand the difference, I decided to take a glimpse of the code, they were very different.

Below is the 3 different tabs and an explanation of them in my own words:
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


Like I said before, the difference in code is crystal clear. In my opinion, I would say that ARIA Tabs are the most complex because they allow enhancement in accessibility and so much more. "Simple Tabs" is the least complex on the list, while three is the most complex. Since I am a beginner to this tool, I will stick with the Simple Tabs.

### DEMO WEBSITE 

The first thing that I did was open my IDE and cd into my tool tinkering folder. After that I googled the HTML and CSS layout in order to get started. I placed the layout where it needed to be and started coding what I want my base to look like. I refreshed my memory on CSS code, one thing that I found very helpful was my SEP10 notes. I am so grateful that I took specific notes on concepts that I didn't really get and paraphrase in order to properly understand. _For this freedom project I want to be able to project my thinking so future me could easily progress_.


After finishing all the basics this is what my DEMO page looks like:


<img width="1279" alt="Screenshot 2024-12-09 at 10 26 51 AM" src="https://github.com/user-attachments/assets/7cc22fed-fba1-4cf9-bba5-725cafd3d590">



## EDP (Engineering Design Process)

I am on step 2 of this process, which is **research** the problem. 

## Skill

**Self-Discipline** is an important skill that I believe I touch up on the most. I believe that I worked on this skill because I made it my responsibility to complete my priority tasks first and give in my full effort. If I failed to do so, I took away the things that distracted me. For instance, I remember when I was in the process of completing my FP (freedom project) content, I got distracted by my phone for a period of 2 hours. I let myself waste 120 minutes instead of doing something productive. I felt unpleasant with my actions. I decided to step up and take action so I can ensure that I won't get distracted. I gave my phone to my sister to hold it for me until I was done with what I needed to complete. As a result, this occurrence made me wake up to my senses and see how important it is to have boundaries and limits within ourselves.


## Next Steps 

Now I am ready to _**Brainstorm**_ possible solutions.

[Previous](entry01.md) | [Next](entry03.md)

[Home](../README.md)
