1. HTML (index.html)
The HTML file structures the calculator interface.

Key Elements:
DOCTYPE and HTML Structure: Defines the document type and sets up the basic structure of the HTML document.

Head Section:
Contains metadata like character set and viewport settings for responsive design.
Links to the external CSS file (style.css) for styling.
Sets the title of the page to "CALCULATOR".

Body Section:
>Contains a div with the class container that centers the calculator on the page.
>Inside this, there is another div with the class calculator that holds the input field and buttons.
>The input field (<input type="text">) displays the current calculation and has an ID of output-screen.
>Buttons are created for digits (0-9), operations (+, -, *, /, %), a decimal point, and functionalities like clear (Cl), delete (Del), and calculate (=). Each button calls a JavaScript function when clicked.

2. CSS (style.css)
The CSS file styles the calculator, making it visually appealing.

Key Styles:
Universal Selector: Resets margin and padding for all elements and sets a background color and font.

Container and Calculator Styles:
The .container class centers the calculator both vertically and horizontally using Flexbox.
The .calculator class uses a grid layout to organize buttons in a 4-column format.

Input Field:
Styled to span all columns, with a specific height, background color, and text alignment.

Button Styles:
Each button has uniform height and width, rounded corners, and a background color. The equal button has a different width and a distinct style.

3. JavaScript (script.js)
The JavaScript file adds functionality to the calculator.

Key Functions:
display(num): Appends the clicked number or operator to the input field.
javascript
function display(num) {
    outputScreen.value += num;
}

Calculate(): Evaluates the expression in the input field using eval(). It also handles errors by alerting the user if the input is invalid.
javascript
function Calculate() {
    try {
        outputScreen.value = eval(outputScreen.value);
    } catch (err) {
        alert("Invalid");
    }
}

Clear(): Clears the input field.
javascript
function Clear() {
    outputScreen.value = "";
}

del(): Deletes the last character from the input field.
javascript
function del() {
    outputScreen.value = outputScreen.value.slice(0, -1);
}
This function resets the input field to an empty string when called.

Summary:

This calculator application consists of an HTML structure for the interface, CSS for styling, and JavaScript for functionality. The user can input numbers and operations using buttons, see the current input in the text field, and perform calculations, with error handling for invalid inputs. The layout is responsive and visually appealing, making it a user-friendly tool.# Digitalbhem
