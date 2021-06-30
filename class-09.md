##vote=Herbie If the form control allows you to choose from a fixed set of answers (e.g. radio buttons, checkboxes or a drop down list), the web page author will add code that gives each option an automatic value chapter-07/form-structure.html HTML Form Structure With the post method the values are sent in what are known as HTTP headers.
You will see forms when registering as a member of a website, when shopping online, and when signing up for newsletters or mailing lists Form Controls ADDING TEXT: Making Choices: Submitting Forms: Uploading Files: Password input Like a single line text box but it masks the characters entered.
As a rule of thumb you should use the post method if your form: ● allows users to upload a file ● is very long ● contains sensitive data (e.g. passwords) ● adds information to, or deletes information from, a database If the method attribute is not used, the form data will be sent using the get method.
id We look at the id attribute on page 183, but the value is used to identify the form distinctly from other elements on the page (and is often used by scripts — such as those that check you have entered information into fields that require values) The element is used to create several different form controls.
The value of this attribute identifies the form control and is sent along with the information they enter to the server.
name When users enter information into a form, the server needs to know which form control each piece of data was entered into.
The name/value pairs sent to the server are: You should never change the name of a form control in a page unless you know that the code on the server will understand this new value.
(For example, in a login form, the server needs to know what has been entered as the username and what has been given as the password.) Therefore, each form control requires a name attribute.
username=Ivy If the form control allows the user to enter text, then the value of the form control is whatever the user ##has typed in.

X Whenever you want to collect information from 
visitors you will need a form, which lives inside a 
<form> element.
X Information from a form is sent in name/value pairs.
X Each form control is given a name, and the text the 
user types in or the values of the options they select 
are sent to the server.
X HTML5 introduces new form elements which make it 
easier for visitors to fill in forms.

js event

###In this chapter, you will learn how: INTERACTIONS EVENTS TRIGGER CODE RESPONDS CREATE EVENTS CODE TO USERS Events occur when users When an event occurs, In the last chapter, you click or tap on a link, hover or fires, it can be used saw how the DOM can or swipe over an element, to trigger a particular be used to update a page.###

e 0 Event : blur on username FUNCTION: checkUsername() Check the username is long enough ' I Get username + I Is username less than five characters? ' I Clear message Show error message 3 CALL CODE When the blur event fires on the username input, it will trigger a function called chec kUsername ().This function checks if the username is less than 5 characters.
Here is the syntax to bind an event to an element using an event listener, and to indicate which function should execute when that event fires: Adds an event listener to the DOM element node(s) METHOD element .addEventlistener('event', functionName [, Boolean]) ; ELEMENT DOM element node to target EVENT CODE Event to bind node(s) Name of function to in quote marks to call EVENT FLOW Indicates something called capture, and is usually set to f al se (see p260) The code starts II code to check the length of username named function.
c06/ js/ event-l istener.js II Declare function II Get feedback element II If username too short or more'; II Set msg II Otherwise II Clear msg ~ var elUsername = document .get El ementByld(' username') ; II Get username i nput II When it loses focus call checkUsername() elUsername.addEventlistener('blur' , checkUsername , false) ; The addEventli stener () method takes three properties: i) The event you want it to listen for.

Event name Start of anonymous function The named function .-Li includes parentheses el .add Event Listener(' blur' , function() The anonymous function is used containing the -- chec kUsername ( 5) ; parameter after the } f l ) , a se ; function name.
I ~nd of statement End of addEventl i stener() method Event flow Boolean (see p260) End of anonymous function The named function that requires the arguments lives inside the anonymous function.
USING PARAMETERS WITH EVENT HANDLERS & LISTENERS Because you cannot have parentheses after the function names in event handlers or listeners, passing arguments requires a workaround.

• Which element the event happened on If you need to pass arguments • Which key was pressed for a to a named function, the event keypress event object will first be passed to the • What part of the viewport the anonymous wrapper function user clicked for a c 1 i ck event (this happens automatically); (the viewport is the part of then you must specify it as a the browser window that parameter of the named function shows the web page) (as shown on the next page).
###PROPERTY target type cancel able METHOD IES-8 EQUIVALENT PURPOSE srcElement The target of the event (most specific element interacted with) type Type of event that was fired not supported Whether you.can cancel the default behavior of an element IES-8 EQUIVALENT PURPOSE PROPERTY preventOefault() returnValue Cancel default behavior of the event (if it can be canceled) stopPropagation() cancelBubble Stops the event from bubbling or capturing any further @ EVENTS 1 .. EVENT LISTENER WITH NO PARAMETERS function checkUsername( e) { Q) var target = e.target ; //get target of event } var el = document.getElementByid('username'); el.addEventlistener('blur', checkUsername , false); 1.###

###balsamic vinegar JAVASCRIPT c06/js/event-del egation.js function getTarget(e) if (le) { e = window.event; } return e.target I I e.srcEl ement; ® function itemDone(e) { II Remove item from t he list ~ var target, elParent, elGrandparent; 0 target = getTarget(e); ~ elParent = target.parentNode; ~ elGrandparent = target.parentNode.parentNode; Q9) elGrandparent.removeChi ld(elParent); ® ® II Prevent the link from taking you elsewhere i f (e.preventDefaul t) { e.preventDefault(); else { e.returnValue = f alse; II Declare function II If there is no event object II Use old IE event object II Get the t arget of event II Declare function II Declare variabl es II Get the item cli cked link II Get its l ist item I I Get its list II Remove list item from list II If prevent Default() works -II Use preventDefault() II Otherwise II Use old IE version II Set up event listeners to call itemDone() on click G) var el = document.getElementByld('shoppinglist');ll Get shopping list ~ if (el .addEventlistener) { II If event listeners work ~ el .addEventlistener('click ' , functi on(e) { II Add listener on click itemDone(e); II It calls itemDone() }, false); II Use bubbling phase for flow else { 11 Otherwise @) el.attachEvent('onclick' , function(e){ II Use old IE model : onclick itemDone (e) ; II Call itemDone() } ) ; EVENTS @ WH ICH ELEMENT DID AN EVENT OCCUR ON? When calling a function, the event object's target property is the best way to determine which element the event occurred on.###

###c06/js/ keypress.js II Decl are variabl es var textEntered, charDisplay, counter, lastKey; textEntered = document.getElementByld('message').value; charDisplay = document.getElementByld('charactersleft'); counter = (180 - (textEntered.length)); charDisplay.textContent = counter; II Decl are function II Decl are variables II User's text II Counter element II Num of chars left II Show chars left lastkey = document .getElementByid ('lastkey'); lastkey.textContent = 'Last key in ASCII code : II Get last key used ' + e.keyCode; II Create msg el = document.getElementByld('message'); el.addEventlistener('keypress', charCount, false); l;li.Jllli II Get msg element II keypress event EVENTS @ FORM EVENTS There are two events that are commonly used with forms.###

###c06/ js/exampl e.js var username, noteName, textEntered, target; noteName = document.getElementByld('noteName'); function writelabel(e) if (le) { e = window .event; target =event.target I I event.srcElement; textEntered = e.target.value; noteName.textContent = textEntered ; JAVASCRIPT II Declare variables II Elemen t that holds note II Declare function II If event object not present II Use IES-8 fallback II Get target of event II Value of that el ement II Update note text II This is where the record I pause controls and functions go ... II See right hand page if (document .addEventlistener) II If event listener support ed document.addEventlistener('click', function(e){ ll For any click document recorderControls(e); }, false) ; II If input event fi res on username i nput call username .addEventlistener('input', writelabel, II Call recorderControls() II Capture during bubbl e phase writelabel () false); else { II Otherwise document .attachEvent('onclick' , recorderControls(e); } ) ; function(e){ II IE fall back: any cl ick II Calls recorderControl s() II If keyup event fires on username input call writelabel() username.attachEvent('onkeyup', writelabel, false); 8 EVENTS ... j I , 1 ~ t The recorderContro 1 s () function is automatically passed the event object.###