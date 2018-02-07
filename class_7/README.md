# Forms 
- Forms are the primary means to get data from the front end to various back end systems.
- Typically when a form is submitted, the data is sent to a script on the back end that does something with it and then redirects the user to another page or back to where they were before.
- Forms generally have three pieces of information that accompany any transmission:
	- Where to send the data
	- How to send it
	- What is being sent

## The `form` Tag
- The form tag is used to enclose the form fields you want to send to the backend, as well as to contain information about where the data is going.
- Here is what a simple login `form` tag could look like:

```
<form action="/login" method="POST"></form>
```

## The `input` Tag
- The `input` tag provides a box for the user to enter information.
- With HTML5 we have many different input types available to us. Here are a few common ones:
	- `<input type="text" />`
	- `<input type="password" />`
	- `<input type="email" />`
	- `<input type="tel" />`
- While some of them may not look any different on the computer, they will open up different keyboard on a mobile device.
- Let's take a look at a demonstration using an iPhone.

## The `select` and `option` Tags
- The `select` and `option` tags go together to create dropdown lists.
- They can be hard-coded, but they are often generated dynamically via the back end service.
- Let's take a look at the syntax:

```
<select>
	<option value="CA">California</option>
	<option value="NY">New York</option>
</select>
```

## Checkboxes and Radios
- Checkboxes and radios are used to select pre-defined values from a list.
- Here are a couple examples:

```
<input type="checkbox" name="tos-agree" value="accept" />
```
and

```
<input type="radio" name="accept" value="accept" />
<input type="radio" name="accept" value="decline" />
```
- Both of these input types have hard-coded values because they are pre-defined.

## Field `name` Attributes
- Each field that you want to use to accept and transmit data will have to have a `name` attribute.
- The name attribute is essentially the parameter that identifies that piece of information to the server on the back end.
- Adding names is simple:

```
<input type="text" name="username" />
```
or

```
<select name="state">
	<option value="">Choose State</option>
	<option value="CA">California</option>
	<option value="NY">New York</option>
</select>
```

## Styling Form Fields
- Form fields have some default rendering associated with them, but it is always a good idea to overwrite that with some custom styling.
- Let's take a look at how we can apply some basic styling to create a nice uniform feel.
- Bootstrap also provides us a class called `form-control` that takes care of standardizing all of our form fields for us.

## Form Exercise
- For this exercise we will practice using form tags to create a simple form.
- Below is a mockup of what we want to accomplish. Try to replicate the same basic design using Bootstrap.
- For the states dropdown you may want to look online for a copy and paste-able script instead of having to type them all in.
- Pay attention to which input field types to use.

![HTML Form](img/html_form.png)
