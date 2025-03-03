# Entry 3  ♡
##### 2/3/25

In this entry:
1. Update on previous goal
2. Go over my progress in learning my tool.


## Content 

During the past few weeks I have been learning about Easy Toggle State JS. In the previous blog, I mentioned a goal that I wanted to accomplish. Working on my demo will help me implement the learning that I have done before the final freedom project.

## Tinkering 

During my tinkering, I had the chance to see how states like `on` or `off` could be managed in just a few lines of code. The straightforward API allowed me to toggle states between elements with a simple command, and the best part was that it worked. I experimented with how it interacts with user inputs. For example, when a button was clicked, the state toggled between active and inactive. Which then changes the button's appearance. I started seeing the potential for using this in creating simple UI interactions llike theme switches. By using Easy Toggle State JS you can create elegant and interactice interfaces.

Here is an example of code 

``` js

const toggle = new EasyToggleState('#toggleBtn');

// Toggle state when button is clicked
document.getElementById('toggleBtn').addEventListener('click', () => {
  toggle.toggleState(); // Switch between 'active' and 'inactive'

  // Update the display
  const state = toggle.getState();
  document.getElementById('status').textContent = state.charAt(0).toUpperCase() + state.slice(1);
});


```

Down below is an explanation in my own words: 

* `const toggle = new EasyToggleState('#toggleBtn')`  creates a new instance of the Easy Toggle State for the button.
* When you click the button, the `toggle.toggleState()` method switches between 'active' and 'inactive'.
* The  text is updated to show the current state which is either _active_ or _inactive_.

### Useful sources 
- I found the <a href="https://twikito.github.io/easy-toggle-state/">official website</a> quite helpful for understanding how to implement the library in your own projects.
- Exploring the <a href="https://github.com/Twikito/easy-toggle-state">GitHub repository</a> to see the source code and add to it.

## Skill 

**Self-Reflection** 
One important skill I developed during my tinkering stage was self-reflection. After each session of learning Easy Toggle State JS, I made it a point to take a step back and mentally process what went well and what could be improved. _For example, after tinkering, I reflected on the blocks of code and wrote comments_. This skill helped me not only learn the code but also become more aware of what I was coding. Through this ongoing self-reflection, I feel like I developed a habit of constantly looking for ways to improve. And not just in coding but in how I learn new libraries and solving problems.


## Next Steps & EDP (Engineering Design Process)

I am on step #3 of my EDP, which is to _Brainstorm_ possible solutions. I will still be brainstorming by working on my demo website and learning new concepts which I can implement to my freedom project website 



[Previous](entry02.md) | [Next](entry04.md)

[Home](../README.md)
