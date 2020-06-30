
**<img>**

# The 5 Step Designer
The first 5 steps to designing almost any website

---

# Motivation
While learning how to program websites on my own, I’ve made the conclusion that it’s really hard to find a way to really lay any foundation on how to even get an idea out and into our ever expanding virtual world. 

Most tutorials and lessons I could find out there seemed to only show me how to get started on that particular project we happened to be working on during that time, but every project felt fragmented and difficult to retain when it came to trying to apply the same logic to my own projects. 

So, I decided to spend some time and find a process that helps me get going on just about any idea that requires an online presence. 

---

## The 5 Step Designer:
00 [Plan](#plan)
01 [Layout](#layout)
02 [Place](#place)
03 [Style](#style)
04 [Refine](#refine)
05 [Experience](#experience)

# Summary
So, I’ve been using The Odin Project to learn most of my front-end development skills, and in the Web Development 101 course, the first project they ask of you is to recreate the desktop version of the Google homepage with only HTML and CSS (basically, make it look like the page, don’t bother making it function like the page).

Since this project only requires the design-side of developing a webpage, I figured it would be perfect to use it as my example for The 5 Step Designer.

*Note:*
*This is by no means a complete process for developing and implementing a website, it just really helps me get my ideas going. I’ll later have another repo on my Github documenting my steps to programming any website, as well (The 5 Step Programmer). For that reason, The 5 Step Designer is primarily focused on UI /UX.* 

I hope this repo can provide some use to those who’ve come across it. 

---

### Room For Improvements:
- Although this project does not require the vertical menu and ad-space column within the **Main [content]**, it would be best for me to still ad empty containers for these sections (and have their display property argument set to none within the CSS)
    - This would really help with the versitility and essentially create a pretty decent HTML/CSS framework for future projects
---

# 0. Plan
This is the time to figure out why the webpage exists, and what the webpage should do. If you don’t do this first, the rest just seems… pointless(?). Hope that’s not too harsh, but yeah, it’s like trying to cook up a meal before knowing how many people you’re feeding, when supper-time begins...ends, how many courses to serve, or even where supper-time is.

*Note: I tend to stay away from the computer at this step, as working on the white-board helps with my thought-process. I like to do this throughout the 5 steps, so I will mark these areas with a **<WB>** tag*

- Since this project doesn’t require any major functionality (no programming here), Javascript (or any other programming language) will not be used within this example.

- Because of this, step (0) can be greatly minimized for this particular example. With that being said, I will fully fulfill step (0) as if functionality was required on this project, because it’s that important of a step to me.

The **main function of this webpage is** to allow a user to submit their input (what they want to search on google.com) by typing their response and submitting (by clicking on a button, or by simply pressing Enter onto the keyboard of the user’s, after typing their response)

The **main features of this webpage are** direct links to mutliple destinations. 
The number of main features on this webpage is **14:**

**Top [navBar]:**
**1.**	About (Google) link;
**2.**	Google Store link;
**3.**	Gmail link;
**4.**	Google Images link;
**5.**	Javascript onClick drop-down-menu for Google Shortcuts/Apps (displayed as icon: Grid)
**6.**	Javascript Google Account Sign-in button

**Main [content]:**
**7.**	Submit button for search entry form;
**8.**	A Submit button that randomly produces a submitted search query for the user;

**Bottom [footer]:**
**9.**	Google’s solicit to advertising link;
**10.**	Google For Small Business link;
**11.**	Link to a destination that explains how google search works;
**12.**	Link to Google’s Privacy Policy;
**13.**	Link to Google’s Terms & Conditions;
**14.**	Javascript onClick drop-down-menu for google search settings;

- Now that I've decided on my main features and the vertical positions of their respected sections, I can then move onto determining if I need any horizontal-sections (columns) as well. So far, our layout is beginning to look a lot like the [Holy Grail Layout](https://css-tricks.com/books/fundamental-css-tactics/holy-grail-layout-5-lines-css/), with just one exception: Our **Main [content]** (our middle-vertical section) will only consist of one horizontal-section and opt-out of the vertical-menu and ad-space sections (columns):

**<gif>**

## Personal Rules of Thumb:
- It is always best to design according to what media most of your viewers will be experiencing your webpage on. Now-a-days, the mobile phone is one of the most widely used medias, alongside personal tablets. Because of this, it's usually best practice to utilize a **[mobile-first](https://designshack.net/articles/mobile/mobilefirst/) approach** to design
- IDs and Classes should clearly identify content's relevance and/or location on viewport
```html
        <div id ="Navbar"></div>
        <div id ="mainContent"></div>
        <div id ="Footer"></div>
```
- For clarity, always start IDs and Classes with its parent conatainer name
```html
        <div id ="Navbar">
            <div class ="navbar_leftside"></div>
        </div>
```
- Keep CSS [selectors](https://doc.qt.io/Qt-5/stylesheet-syntax.html) in the same order as the HTML IDs and Classes are

<table>
<tr>
<th>
HTML
</th>
<th>
CSS
</th>
</tr>

<tr>
<td>
<pre>
<!--
    <div id ="Navbar">
        <div class ="navbar_leftside"></div>
    </div>
    <div id ="mainContent">
        <div class ="maincontent_logo"></div>
    </div>
-->
</pre>
</td>
<td>
<pre>

    #Navbar{}
    .navbar_leftside{}
    #mainContent {}
    .maincontent_logo {}

</pre>
</td>
</tr>
</table>

# 1. Layout
- **<WB>** Design the layout of your webpage
**<img>**
- Build the parent containers for each section of your webpage in HTML
**<img>**
    - *hint: place temporary text in the divs in order to see them*
    **<gif>**
- Color the HTML divs in CSS for a better visual of each section before placing each in the desired area of the viewport
**<img>**

## Features
What makes your project stand out?

## Code Example
Show what the library does as concisely as possible, developers should be able to figure out **how** your project solves their problem by looking at the code example. Make sure the API you are showing off is obvious, and that your code is short and concise.

## Installation
Provide step by step series of examples and explanations about how to get a development env running.

## API Reference

Depending on the size of the project, if it is small and simple enough the reference docs can be added to the README. For medium size to larger projects it is important to at least provide a link to where the API reference docs live.

## Tests
Describe and show how to run the tests with code examples.

## How to use?
If people like your project they’ll want to learn how they can use it. To do so include step by step guide to use your project.

## Contribute

Let people know how they can contribute into your project. A [contributing guideline](https://github.com/zulip/zulip-electron/blob/master/CONTRIBUTING.md) will be a big plus.

## Credits
Thanks CSS-Tricks! You're one of my favorite resources! 
[Complete Guide to Grid Layout](https://css-tricks.com/snippets/css/complete-guide-grid/)

#### Anything else that seems useful

## License
A short snippet describing the license (MIT, Apache etc)

MIT © [Yourname]()
