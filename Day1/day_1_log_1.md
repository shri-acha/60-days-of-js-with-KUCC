# Logs

## How the internet works:
- What web is:
    So,internet is a global network between a computer and a server,but also can communicate with other computers.
- How the internet works:
    Internet in higher-sense,works by almost all the computers being somehow interconnected through physical mediums like TV cables,Wifi,etc.

- How a website is reached through a client:
    A website is reached through a simple process of the client requesting the server with a tailored request, 
    in response the server responses back with a response,containing the desired output.

    So basically:
        `Request(With headers) -> Response(By server)`
    <br>
`Note:The response contains various metadata to explain the data sent by the server.So the parser is able to parse the data and render it.`<br> 
But for the client to use the website,the website is to hosted in a domain,while a domain is a just a name,
the actual work is done by the DNS that converts the given domain into the corresponding IP-address that the server is hosted in.


## How the browser works:

- ### Components of a browser:

* #### User-Interface:
`User interface is the component of the browser that one is able to interact with but can't change.Essentially,it is like the components of the browser like: Settings,Address Bar,History`
* #### Browser Engine:
`Browser Engine is the part of the browser that is the interface of the user and the application,it executes any operations assigned.
For example: If the user wants to access the Settings menu by pressing settings options in the hamburger menu,
the the browser engine acts as the interface for the user to execute the operation`
* #### Rendering Engine:
`Rendering engine is a parser which parses the HTML,CSS,JS.
Parsing of each component involves converting HTML,CSS,JS into a render tree.`
<br>There also are components withing the rendering engine.like:
        + Networking layer
        + Javascript Interpreter 
        + UI Backend layer


- ### Basic rendering engine flow:

The basic rendering engine flow is in the following order:
* #### Parsing:

`Parsing is essentially translating a document into a structure that code can use.`
<br>


`Parsers are of two types:
`<br>

   + Conventional: Parses CSS and JS

   + Unconventional: Parses HTML

<br>
    
   * #### Parsing Process:
    `HTML is doesn't use a conventional parser as HTML is not contex free grammar(ie.even with errors,the html is rendered.)`<br>`A DOM Tree is parsed by slowly building a tree by using an opening tag and finding its corresponding closing tag.`

`Parsing involves:`<br>

   + Lexical Analysis
   
   `Lexer(Tokenizer) - Creates tokens and also sends it to the Parser`
   + Syntax Analysis
   `Parser - Applies syntax rules to the tokens and stores the token.`


* Render tree:
    `Render tree contains the visual elements in the order which they are going to be displayed.`  
    <br>
    `Note:A render tree is generated while DOM tree is constructed`
<br>
    `There maybe conditions of how the render objects shall be displayed like:
`
     + none 
     + inline
     + block,etc.
<br> (Yes,the css part comes here)


<br>
    `Note:The render objects are rectangles`
    
* Layout/Reflow:

`Layout calculates the position and size of the render object.
It is used for computing geometry.
it begins in the root object,that is in the <html>`
oOooh cool stuff.... coming up.
`Dirty bit system: A system that only changes the only the part of the layout than the entire layout when a render object is changed.`

`Note:When the font size is changed or the size of the screen is changed,the entire global layout changes`


* Paint:

`Paint traverses the render tree(which has render objects) and uses the paint method which is used to display content on the page.`
