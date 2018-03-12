# Forms with HTML and JavaScript
- Forms are the primary means to get data from the front end to various back end systems.
- Typically when a form is submitted, the data is sent to a script on the back end that does something with it and then redirects the user to another page or back to where they were before.
- Forms generally have three pieces of information that accompany any transmission:
	- Where to send the data
	- How to send it
	- What is being sent


## Accessing Form Field Data
- Although much of the processing will likely occur on the back end, there are many reasons to use JavaScript to read the form data and do something with it.
- One of these reasons is validation - checking the form for errors before it is submitted.
- Reading data is straightforward with jQuery's `.val()` function. It can be used as a getter and a setter:

#### Getter

```js
$("#form-field").val();
```
#### Setter

```js
$("#form-field").val("New value!");
```
- Often these fields are pulled out via JavaScript into an object:

#### HTML

```HTML
<input type="text" id="username" />
<input type="password" id="password" />
<button type="button" id="submit-button">Submit</button>
```
#### JS

```js
$(document).on("click", "#submit-button", function() {
	var formInfo = {
		username: $("#username").val(),
		password: $("#password").val()
	};
});
```

## `event.preventDefault()`
- Most times when dealing with forms in JavaScript you want to make sure that the form is not submitted until it has been processed appropriately.
- To prevent forms from submitting automatically, we can use the `event.preventDefault()` method:

```js
$(document).on("click", "#submit-button", function(event) {
	event.preventDefault();

	var formInfo = {
		username: $("#username").val(),
		password: $("#password").val()
	};
});
```

## Simple Form Validation
- This method of reading form data with JavaScript is most commonly used for form validation.
- One of the simplest checks we can make is that all fields have been filled out and not left blank.
- Here's an example using a for-in loop to check the form for blank submissions:

```js
for (field in formInfo) {
	if (formInfo[field] === "") {
		alert("Please fill in all fields.");
		return false;
	}
}
```
- This loop with go through the object and check for blank entries.
- If a blank is found, and alert will be triggered and the parent function will return false. This will prevent any further action from taking place.
- When applying validation on a form using JS its common practice to set the `type` attribute of the submit button to "button". This will make sure it doesn't submit the form without going through the validation first.

## Simple Validation Exercise
- In this exercise you will add simple validation to your form.
- First start off by binding a click event to your submit button that will pull out all of the form fields into an object.
- Create a loop that will check each field for a blank submission.
- Prevent any further action from taking place.
- If each field is filled out, alert your user "Thanks for submitting the form!".
