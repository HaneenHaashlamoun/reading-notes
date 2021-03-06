# Django CRUD and Forms

![CRUD](https://repository-images.githubusercontent.com/218840721/2b62d680-1b9b-11ea-8803-ea00232783e3)

- An HTML Form is a group of one or more fields/widgets on a web page, which can be used to collect information from users for submission to a server. Forms are a flexible mechanism for collecting user input because there are suitable widgets for entering many different types of data, including text boxes, checkboxes, radio buttons, date pickers and so on. Forms are also a relatively secure way of sharing data with the server, as they allow us to send data in POST requests with cross-site request forgery protection.

- While we haven't created any forms in this tutorial so far, we've already encountered them in the Django Admin site — for example, the screenshot below shows a form for editing one of our Book models, comprised of a number of selection lists and text editors.

## Django form handling process
![handling process](https://media.geeksforgeeks.org/wp-content/uploads/20200107124202/flowChart-1-1024x682.png)

-  Display the default form the first time it is requested by the user. The form may contain blank fields (e.g. if you're creating a new record), or it may be pre-populated with initial values (e.g. if you are changing a record, or have useful default initial values).
- The form is referred to as unbound at this point, because it isn't associated with any user-entered data (though it may have initial values). Receive data from a submit request and bind it to the form.
- Binding data to the form means that the user-entered data and any errors are available when we need to redisplay the form. Clean and validate the data.
- Cleaning the data performs sanitization of the input (e.g. removing invalid characters that might be used to send malicious content to the server) and converts them into consistent Python types.
- Validation checks that the values are appropriate for the field (e.g. are in the right date range, aren't too short or too long, etc.) If any data is invalid, re-display the form, this time with any user populated values and error messages for the problem fields. If all data is valid, perform required actions (e.g. save the data, send an email, return the result of a search, upload a file, etc.)
- Once all actions are complete, redirect the user to another page.x

### HTML Forms

- The submit input will be displayed as a button (by default) that can be pressed by the user to upload the data in all the other input elements in the form to the server (in this case, just the team_name). The form attributes define the HTTP method used to send the data and the destination of the data on the server (action):

- action: The resource/URL where data is to be sent for processing when the form is submitted. If this is not set (or set to an empty string), then the form will be submitted back to the current page URL. method: The HTTP method used to send the data: post or get. The POST method should always be used if the data is going to result in a change to the server's database because this can be made more resistant to cross-site forgery request attacks. The GET method should only be used for forms that don't change user data (e.g. a search form). It is recommended for when you want to be able to bookmark or share the URL.

- Django's form handling uses all of the same techniques that we learned about in previous tutorials (for displaying information about our models): the view gets a request, performs any actions required including reading data from the models, then generates and returns an HTML page (from a template, into which we pass a context containing the data to be displayed). What makes things more complicated is that the server also needs to be able to process data provided by the user, and redisplay the page if there are any errors.

- arguments that are common to most fields are listed below (these have sensible default values):

required: If True, the field may not be left blank or given a None value. Fields are required by default, so you would set required=False to allow blank values in the form.

label: The label to use when rendering the field in HTML. If a label is not specified, Django will create one from the field name by capitalizing the first letter and replacing underscores with spaces (e.g. Renewal date).

label_suffix: By default, a colon is displayed after the label (e.g. Renewal date:). This argument allows you to specify a different suffix containing other characters (s).

initial: The initial value for the field when the form is displayed.

widget: The display widget to use.

help_text (as seen in the example above): Additional text that can be displayed in forms to explain how to use the field.

error_messages: A list of error messages for the field. You can override these with your own messages if needed.

validators: A list of functions that will be called on the field when it is validated.

localize: Enables the localization of form data input (see link for more information).

disabled: The field is displayed but its value cannot be edited if this is True. The default is False.



## Templates
The "create" and "update" views use the same template by default, which will be named after your model: model_name_form.html (you can change the suffix to something other than _form using the template_name_suffix field in your view, for example template_name_suffix = '_other_suffix')

      
© Haneen Hashlamoun

