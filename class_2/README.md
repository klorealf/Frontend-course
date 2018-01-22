# HTML Review and Introduction to CSS

## HTML Review

## Working with Directories
- In order to link files correctly it's important to understand how directories work.
- Let's take an example of an image called puppies.jpg that is located inside of a folder called img. Let's see how the `img` tag changes as the files get moved around.
- It's also important to note that if you move a file after you make changes to it in the editor you should exit the editor and re-open the file.

## Using CSS with HTML
- There are three main ways to use CSS - inline styles, the `style` tag in the `head`, and a separate .css file that is linked to the HTML.
- Linking a stylesheet to the HTML document is the best-practice way to use CSS styles.
- Here is the syntax for the `link` tag:

```html
<link rel="stylesheet" href="style.css" />
```

## CSS Breakdown
- Each CSS style set starts with a selector.
- Selectors allow you to identify which elements you want to apply styles to.
- Here is an example of a selector with a couple rules:

```css
p {
	color: red;
	font-weight: bold;
	background-color: blue;
}
```

- This example selects all paragraph tags on the page and applies the below styles to them.

## CSS Selectors
- There are three common basic selectors in CSS.
- The first is the element selector. This is not a very specific selector:

```css
div {
	color: red;
}

table {
	color: red;
}

p {
	color: red;
}
```

- The second is the id selector. By convention id's should not be used more than once per page:

```css
#my-div {
	background-color: #990000;
}
```

- The third is the class selector. Classes by convention can be used multiple times throughout the page:

```css
.my-divs {
	background-color: #EBEBEB;
}
```

## CSS Colors
- Colors in CSS can be defined in a few different ways.
- The first we have already seen - calling them out by their name symantically (red, green, blue, etc.)
- The second way is by using HEX colors. HEX codes represent shades of red, green, and blue.

![HEX Colors](img/hex_colors.png)

- You can find color codes on a number of websites and other programs like Photoshop. [Colorpicker.com](http://www.colorpicker.com/) is a good example.
- Another way of defining CSS colors is via `rgba()`. Rgba accepts values for red, green, and blue as well as an alpha value for transparency.
- Each RGB value is from 0 to 255. Alpha values are from 0 to 1.

## CSS Review
- Where should CSS styles go?
- How does the CSS syntax work?
- Give examples of 3 different CSS selectors.

## Introduction to Git
- Git is a source control management tool.
- Git allows you to store and update your code in a structured way.
- Git includes history of changes you make, so you can create "checkpoints" and track your work better over time.
- Git is an intelligent tool, and does many things for you automatically, but can be tricky to use in some cases. It takes a bit of learning to get fully comfortable with Git.

## What is GitHub?
- GitHub is a service that lets you host Git repositories in the cloud.
	- In other words, they are hosted remotely by GitHub, and can be downloaded from / uploaded to over the internet.
- GitHub allows you to easily distribute code to others by sharing your repository.
- GitHub lets you view your code online easily with a web interface.
- GitHub is free to use as long as you make your code public.
Private repositories cost a monthly fee.

## Git Class Demonstration
- We will practice setting up a new Git repository and pushing it to GitHub.
- Note that empty repositories cannot be added to GitHub.
- Here is a cheatsheet of commands we will be using:

Add files to Git tracking:

```
git add -A
```

Commit files to local Git repository:

```
git commit -m "Initial commit"
```

Add remote to push to:

```
git remote add origin http://yourgithuburl.com
```

Push to remote repository:

```
git push -u origin master
```

## About Me Homework
- We will now work on coding an about me page (use the Wendy G. Bite one as a guide).
- We will be incorporating our HTML knowledge with CSS styles to accomplish this.

![Betty White Resume](img/WendyBite_AboutMe.png)


## Wendy G. Bite Resume Stretch Challenge
- For this exercise we will be using the mockup below to code our own page.
- Link the about me page we created earlier to your resume page.

![Wendy G. Bite Resume](img/WendyBite_Resume.png)
