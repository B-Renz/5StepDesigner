
**{img}**

# The 5 Step Designer
The first 5 steps to designing almost any website

---

# Motivation
While learning how to program websites on my own, I’ve made the conclusion that it’s really hard to find a way to really lay any foundation on how to even get an idea out and into our ever expanding virtual world. 

Most tutorials and lessons I could find out there seemed to only show me how to get started on that particular project we happened to be working on during that time, but every project felt fragmented and difficult to retain when it came to trying to apply the same logic to my own projects. 

So, I decided to spend some time and find a process that helps me get going on just about any idea that requires an online presence. 

---

## The 5 Step Designer:
- 00 [Plan](#plan)
- 01 [Layout](#layout)
- 02 [Place](#place)
- 03 [Style](#style)
- 04 [Refine](#refine)
- 05 [Experience](#experience)

# Summary
So, I’ve been using The Odin Project to learn most of my front-end development skills, and in the Web Development 101 course, the first project they ask of you is to recreate the desktop version of the Google homepage with only HTML and CSS (basically, make it look like the page, don’t bother making it function like the page).

Since this project only requires the design-side of developing a webpage, I figured it would be perfect to use it as my example for The 5 Step Designer.

*Note:*
*This is by no means a complete process for developing and implementing a website, it just really helps me get my ideas going. I’ll later have another repo on my Github documenting my steps to programming any website, as well (The 5 Step Programmer). For that reason, The 5 Step Designer is primarily focused on UI /UX.* 

I hope this repo can provide some use to those who’ve come across it. 

***Please Note:***
This guide is intended for those who have a good foundation in HTML and CSS basics and some experience writing HTML and CSS within their personal editor (while hopefully using a live-feed server to see a preview of your markup file). If you understand the diference between [flexbox and grid](https://medium.com/youstart-labs/beginners-guide-to-choose-between-css-grid-and-flexbox-783005dd2412) and when either would be of more use, following along should be cake (simple).

---

### Room For Improvements:
- [ ] Although this project does not require the vertical menu and ad-space column within the **Main [content]**, it would be best for me to still ad empty containers for these sections (and have their display property argument set to none within the CSS)
    - This would really help with the versitility and essentially create a pretty decent HTML/CSS framework for future projects
    
- [ ] Add a link to my future blog post on helping those that are having trouble wrappng their head around the concepts of ***parent vs. child elements*** by using a brief HTML/CSS sample to explain. Link will be anchored to last bullet-point in the **Place** section

- [ ] Add a link to my future blog post on ***closing that mysterious gap*** by using a very short HTML file that displays a search bar and a search icon as a submit button. Link will be anchored to first bullet point in the **Style** section

---

# 0. Plan <a name ="plan"></a>
This is the time to figure out why the webpage exists, and what the webpage should do. If you don’t do this first, the rest just seems… pointless(?). Hope that’s not too harsh, but yeah, it’s like trying to cook up a meal before knowing how many people you’re feeding, when supper-time begins...ends, how many courses to serve, or even where supper-time is.

*Note: I tend to stay away from the computer at this step, as working on the white-board helps with my thought-process. I like to do this throughout the 5 steps, so I will mark these areas with a **{WB}** tag*

- Since this project doesn’t require any major functionality (no programming here), Javascript (or any other programming language) will not be used within this example.

- Because of this, step (0) can be greatly minimized for this particular example. With that being said, I will fully fulfill step (0) as if functionality was required on this project, because it’s that important of a step to me.

The **main function of this webpage is** to allow a user to submit their input (what they want to search on google.com) by typing their response and submitting (by clicking on a button, or by simply pressing Enter onto the keyboard of the user’s, after typing their response)



The **main features of this webpage are** direct links to mutliple destinations. 
The number of main features on this webpage is **14:**

**Top [navBar]:**
1.	About (Google) link;
2.	Google Store link;
3.	Gmail link;
4.	Google Images link;
5.	Javascript onClick drop-down-menu for Google Shortcuts/Apps (displayed as icon: Grid)
6.	Javascript Google Account Sign-in button

**Main [content]:**
1.	Submit button for search entry form;
2.	A Submit button that randomly produces a submitted search query for the user;

**Bottom [footer]:**
1.	Google’s solicit to advertising link;
2.	Google For Small Business link;
3.	Link to a destination that explains how google search works;
4.	Link to Google’s Privacy Policy;
5.	Link to Google’s Terms & Conditions;
6.	Javascript onClick drop-down-menu for google search settings;



Now that I've decided on my main features and the vertical positions of their respected sections, I can then move onto determining if I need any horizontal-sections (columns) as well. So far, our layout is beginning to look a lot like the **[Holy Grail Layout](https://css-tricks.com/books/fundamental-css-tactics/holy-grail-layout-5-lines-css/)**, with just one exception: Our **Main [content]** (our middle-vertical section) will only consist of one horizontal-section and opt-out of the vertical-menu and ad-space sections (columns): <br />

**{gif}**

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
- Keep CSS [selectors](https://doc.qt.io/Qt-5/stylesheet-syntax.html) in the same order as the HTML IDs and Classes 

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

    div id ="Navbar">
        div class ="navbar_leftside"></div>
    </div>
    div id ="mainContent">
        div class ="maincontent_logo"></div>
    </div>
    
</pre>
</td>
<td>
<pre>

    #Navbar{
        background-color: #FF8700;}
    .navbar_leftside{
        background-color: #FF0000;}
    
    #mainContent {
        background-color: #00FFFF;}
    .maincontent_logo {
        background-color: #FF8700;}
    
</pre>
</td>
</tr>
</table>

*Special reference: [How to Display Two Markdown Code-Blocks Side-by-Side](https://stackoverflow.com/questions/35381425/how-to-disply-two-markdown-code-blocks-side-by-side)*
- Always start your CSS with universal selectors first before moving onto the first ID or Class in your HTML
```css
html, body {
    background-color: #fffaf4; 
    font-family: Arial, Helvetica, sans-serif;
    font-size: small;
    height: 100vh;}
*{
    text-decoration: none;
    padding: 0;
    margin: 0;}
    
    
#Navbar{
    background-color: #FF8700;}
.navbar_leftside{
    background-color: #FF0000;}
```
---

# 1. Layout <a name ="layout"></a>
- **{WB}** Design the layout of your webpage <br />
**{img}**
- Build the parent containers for each section of your webpage in HTML <br />
```html
    <body>
        <div id="container">
            <div id="viewport">
                <div id="navbar"></div>
                <div id="logo"></div>
                <form>
                    <div id="searchform"></div>
                    <div id="shortcuts"></div>
                </form>
                <div id="footerlinks"></div>
            </div>
        </div>
    </body>
```
   *hint: place temporary text in the divs in order to see them* <br />
```html
<div id="navbar">
    NAVBAR <!--Placeholder-->
</div>
<div id="logo">
    LOGO <!--Placeholder-->
</div>
<div id="searchform">
    SEARCHFORM <!--Placeholder-->
</div>
<div id="shortcuts">
    SHORTCUTS <!--Placeholder-->
</div>
<div id="footerlinks">
    FOOTERLINKS <!--Placeholder-->
</div>
```
<img src="https://5stepdesigner.s3-us-west-2.amazonaws.com/layoutpic1.png" width="33%" height="auto"> <br />
    
- Color the HTML divs in CSS for a better visual of each section... <br />


<img src="https://5stepdesigner.s3-us-west-2.amazonaws.com/layoutpic2.png" width="33%" height="auto"> <br />


before placing each in the desired area of the viewport
 
<img src="https://5stepdesigner.s3-us-west-2.amazonaws.com/layoutpic3.png" width="33%" height="auto">


- Now, check to confirm each section flex's and grids according to the size of the viewport <br />
**{gif}**

# 2. Place <a name ="place"></a>
- Start adding your content within the parent divs you just made in your HTML file
    - remember to keep your parent divs independent from the content
    
   | :heavy_check_mark: *(clean)* | :x: *(dirty)* |
   | --- | --- |
   | **div** id ="Navbar"> <br /> &nbsp;&nbsp; **div** class ="navbar_content"> <br /> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; ***content*** <br /> &nbsp;&nbsp; /**div**> <br /> /**div**> <br /> | **div** id ="Navbar"> <br /> &nbsp;&nbsp;&nbsp;&nbsp; ***content*** <br /> /**div**> <br /> |

- Ensure that added content is within its parent container and without any overflow
    - If adjustments are needed, adjust them in your CSS file <br /> 

<img src="https://5stepdesigner.s3-us-west-2.amazonaws.com/placepic1.png">

- While in your CSS file, move your content (your [child elements](https://github.com/B-Renz)) in the desired area of the viewport <br />

<img src="https://5stepdesigner.s3-us-west-2.amazonaws.com/placepic2.png">

# 3. Style <a name ="style"></a>
- By this point, you should exclusively be working in CSS. Exceptions could be having to place two elements on the same line in order to [close a gap](https://github.com/B-Renz)
- Ensure that fonts and images are properly sized, text borders and buttons are properly styled

<img src="https://5stepdesigner.s3-us-west-2.amazonaws.com/stylepic1.png">

Let's take the background colors off of the containers now:

<img src="https://5stepdesigner.s3-us-west-2.amazonaws.com/stylepic2.png">

- Ensure every content that the user is expected to 'click' on has a pointer over the element when hovering over it
- Ensure that the layout and content are properly sized and moved according to each responsive layout
    - When you squeeze and stretch the width of the viewport window, does everything fall into place? How about when you squeeze and stretch the height? <br />
    **{gif}**
- Color anything you'd like <br />

<img src="https://5stepdesigner.s3-us-west-2.amazonaws.com/stylepic3.png">

*Note: It's usually best practice to always have some tone of color for the negative space on your page instead of pure white* <br />

<img src="https://5stepdesigner.s3-us-west-2.amazonaws.com/stylepicdouble.png">

# 4. Refine <a name ="refine"></a>
- This step is meant to just make the page ['pop'](https://creativemarket.com/blog/design-clients-make-it-pop) a little
    - technically, this step can be considered optional, but I really wouldn't recommend it (it just helps shows a certain attention to detail)
    
| *Before:* | *After:* |
| --- | --- |
| <img src="https://5stepdesigner.s3-us-west-2.amazonaws.com/refinepic0.png" width="100%"> | <img src="https://5stepdesigner.s3-us-west-2.amazonaws.com/refinepic01.png" width="100%"> |

- Check dev-tools and click this icon to see how your webpage looks on each device: <br />
**{gif}**
- If you are not satisfied with what you see, add the necessary [@media queries](https://css-tricks.com/css-media-queries/) that will satisfy your needs (Although, if done correctly, you should only be tapping into your inner perfectionist at this point -- modifications should be minimal)

<img src="https://5stepdesigner.s3-us-west-2.amazonaws.com/refinepic2.png">

# 5. Experience <a name ="experience"></a>
- Now, include details that highlight your call to action
    - This would include your :active , :hover , :focus , :visited , and :required tags within your CSS selectors
- Although a good HTML and CSS file should already be started with [accessibility](https://css-tricks.com/improving-accessibility-24-ways/) in mind, it is best to check and ensure that the accessibility of everything on your webpage is up to [today's standards](https://www.w3.org/TR/WCAG21/)
- At this point we'd start throwing in our Javascript, but for this project, Javascript will not needed

## How to use?
index1.html = [Layout](https://codepen.io/b-renz/pen/oNbEyop) <br />
index2.html = [Place](https://codepen.io/b-renz/pen/KKVQeZw) <br />
index3.html = [Style](https://codepen.io/b-renz/pen/oNbEypE) <br />
index4.html = [Refine](https://codepen.io/b-renz/pen/mdVXKpz) <br />
index.html  = [Experience](https://codepen.io/b-renz/pen/ZEQrRrO) <br />

Go ahead and check out each finished step in [codepen](https://codepen.io/) by clicking on the links above. I'd recommend getting your HTML file started in your favorite editor, such as your ` <head></<head>` section (including a link to your CSS file and your font-awesome bucket link)

- If you haven't already set yourself up with a text-icon service account (to use icons) and a cloud file-storage service (to show images), go ahead and do so. Not sure where to start? Just create a free account on these trusted platforms:<br />
        - [font-awesome](https://fontawesome.com/): **Why?**  Let's you use a massive amount of icons, such as the 3 we use in this project<br />
        - [amazon web services](https://aws.amazon.com/) (aws): **Why?**   Store your images here in a public bin and use this new location for your `href=""`. Now, everyone can see the images on your webpage (like the Google logo we used in this project)<br />

## Contribute

Let people know how they can contribute into your project. A [contributing guideline](https://github.com/zulip/zulip-electron/blob/master/CONTRIBUTING.md) will be a big plus.

## Credits
Thanks CSS-Tricks! You're one of my favorite resources! 
[Complete Guide to Grid Layout](https://css-tricks.com/snippets/css/complete-guide-grid/)

#### Anything else that seems useful

## License
A short snippet describing the license (MIT, Apache etc)

MIT © [Yourname]()
