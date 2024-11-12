# Tool Learning Log

## Tool: **Easy Toggle State**

## Project: **Personality Quiz**

---

### 9/30/24: LEARNING LOG 1
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



### 10/21/24:LEARNING LOG 2 

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


3. **Tabs with ARIA*** 


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


Like I said before, the difference in code is crystal clear. In my opinion, I would say that ARIA Tabs are the most complex.One is the least complex on the list, while three is the most complex. Since I am a beginner to this tool, I will be choosing to stick with the Simple Tabs. 


**Next up:** I will start working on my tinkering webpage in my IDE. 

### 11/8/24: LEARNING LOG 3


* Text


<!--
* Links you used today (websites, videos, etc)
* Things you tried, progress you made, etc
* Challenges, a-ha moments, etc
* Questions you still have
* What you're going to try next
-->
†
