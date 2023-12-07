#  Programming Assignment: Building a functional program.

 The assignment of the "Programming with JavaScript" course in the "Meta Front-End Developer Professional Certificate" course series. 
 
## Task 1: Build a function-based console log message generator

In this exercise, your task is to code a function named consoleStyler, which accepts four parameters:

color
background
fontSize
txt

Inside the body of the consoleStyler() function declaration, you need to do the following:

01. Create a new variable named message, and assign the following to it on the very first line inside the consoleStyler() function body.:

   "%c" + txt

02. Create a style variable and assign the following to it on the next line:

   color: ${color};

03. Next, update the style variable (using the += operator) with the following code:

   background: ${background}; 

04. Then, update the style variable (again, using the += operator) with the following code:

   font-size: ${fontSize};

05. Finally, console log the message and style variables inside the consoleStyler function declaration.

#### My Answer
function consoleStyler(color, background, fontSize, txt) {

    var message = "%c" + txt;
    var style = `color: ${color};`;
    style += `background: ${background};`;
    style += `font-size: ${fontSize};`;
    console.log(message, style); 
    
}

## Task 2: Build another console log message generator

Your task is to code another function, and name it celebrateStyler(). The function accepts a single parameter, 
reason, which should be of string data type.

Inside the function declaration's body, code the following:

01. A new variable, named fontStyle, assigning it this code:

"color: tomato; font-size: 50px";

02. On the next line, an if statement, verifying that reason == "birthday".

03. Inside the body of the if block, code the following:

console.log(%cHappy birthday, fontStyle);

04. On the next line, add an else if, and inside the parentheses, check that

reason == "champions"

05. Inside the else if block, add this code:

console.log(%cCongrats on the title!, fontStyle);

06. Add an else block, with the following code inside of it:
   
#### My Answer
function celebrateStyler(reason) {

    var fontStyle = "color: tomato; font-size: 50px";
    if (reason == "birthday") {
        console.log(`%cHappy birthday`, fontStyle);
    } else if(reason == "champions"){
        console.log(`%cCongrats on the title!`, fontStyle);
    } else {
       console.log(message, style); 
    }
}

## Task 3: Run both the consoleStyler and the celebrateStyler functions

Invoke the consoleStyler() function, with the following arguments:
<ul>
<li>'#1d5c63'</li>

<li>'#ede6db'</li>

<li>'40px'</li>

<li>'Congrats!'</li>
</ul>
Next, invoke the celebrateStyler() function, with the following argument:
<ul>
<li>'birthday'</li>
</ul>

#### My Answer
consoleStyler('#1d5c63', '#ede6db', '40px', 'Congrats!');
 
celebrateStyler('birthday');

## Task 4: Insert a congratulatory and custom message

01. Code another function, named styleAndCelebrate().

    The function declaration's body should consist of two function
    invocations: consoleStyler(color, background, fontSize, txt); celebrateStyler(reason);

02. Next, invoke the new function, using the following arguments:
<ul>
 <li>'ef7c8e'</li>
<li>'fae8e0'</li>
<li>'30px'</li>
<li>'You made it!'</li>
<li>'champions'</li>
</ul>

#### My Answer
function styleAndCelebrate(color, background, fontSize, txt, reason) {

consoleStyler(color, background, fontSize, txt);

celebrateStyler(reason);

}

## Call styleAndCelebrate

#### My Answer
styleAndCelebrate('ef7c8e', 'fae8e0', '30px', 'You made it!', 'champions');
