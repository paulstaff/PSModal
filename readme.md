PSModal - v0.9.1
================

PSModal provides an easy-to-use modal window that displays beautifully cross-browser (well, it might not have been tested in IE, but does anyone really use IE?).  Generating a modal with PSModal involves calling one function--it's that simple!


Installation
------------


### Prerequisites

- [jQuery 2.0+](http://jquery.com) is required to run all PSToolkit plugins, including PSModal

### Instructions

1. Download [PSModal.zip](http://paulstaff.com/random/PSToolkit/PSModal/PSModal.zip).
2. Unzip the contents and include the `PSModal.js` and `PSModal.css` files in the plugins folder for your project.
3. Include the following two lines in the `<head>` section of your HTML file (be sure to change file path):

	```HTML
	<script src="path/to/plugins/folder/PSModa.js"></script>
	<link rel="stylesheet" href="path/to/plugins/folder/PSModal.css">
	```

4. Create `title`, `content`, and `options` (optional) variables to populate the modal window.  HTML can be passed in as the `content` variable to creacte a custom modal window:

	```Javascript
	var title = "Test Modal Title";

   	var content =  	'<div class="psModalItem">' +
                 	'   <div>This is an item in the modal window.  As you can see, the modal window retains CSS styles present in your project, such as font and HTML elements like the button below.</div>' +
                  	'</div> ' +
                 	'<div id="psModalFooter">' +
               		'   <div class="btn" onclick="PSModal.close()">Close Modal</div>' +
            		'</div> ';

 	var options = {
   		width: 800
 	};
	```

5. Call `PSModal.open()` with the three variables created above to generate the modal window:

	```Javascript
	PSModal.open(title, content, options);
	```


Using PSModal
-------------


### Variables to Create Modal

#### `title` Variable

The `title` variable is used to pass in the title displayed in the header section of the modal window.

#### `content` Variable

The `content` variable is used to pass in the main body of the modal window.  This variable is a string that can be comnposed of HTML elements to display custom information in the modal window.

There are number of preset elements designed and style specifically to be used in the `content` passed into the open modal function.  `content` can include any of these elements as well as any custom elements you wish to include.  Preset elements are as follows:

- `modalItem` - a standard `div` with appropriately styled margins and padding for PSModal.
- `modalFooter` - a `div` to be used at the bottom of the modal window; includes a dividing line at the top along with approriate margins and padding.

#### `options` Variable

The `options` variable is an optional variable that allows you to pass extra parameters to the modal window.  Current options are as follows:

- `width` - sets the width of the modal window (standard is 600px)


### Modal Functions

- `PSModal.open(title, content, options)` - function to open the modal window
- `PSModal.close()` - function to close the modal window


### Editing Your Modal Window

As explained above, the modal body will render custom HTML elements from the `content` variable, which allows you to control what the modal displays.  If you would like more control, you are able to edit the `PSModal.css` file to change the style of the modal itself.

In `PSModal.css`, sections that are required are clearly marked with a **Required Styles** comment while sections that are editable are marked with an **Add Custom Styles Here** comment.  (Technically, all style sections are editable, just make sure you know what you're doing first).  An example of the `psModalWindow` element CSS is below:

	```CSS
	#psModalWindow {

    	/* Required Styles */
    	position: relative;
    	z-index: 2000;

    	/* Add Custom Styles Here */
    	background: none repeat scroll 0 0 #FFFFFF;
    	border: 1px solid #CCCCCC;
    	border-radius: 5px;
    	min-width: 400px;

	}
	```


Developed By
------------

[Paul Staff](http://paulstaff.com)