Dox Basic 
========= 
 
 
 
# Example Usage

    npm install dox-basic -g
    dox-basic -t "Library Name"<index.js>readme.html
    dox-basic -m -t "Library Name"<index.js>readme.md 
 
# exports.name 
 
Parser name 
 
# exports.version 
 
Parser version 
 
# exports.parse() 
 
Parse source code to produce documentation

 
@param {string} source JavaScript source code with comments    
@param {object} [options]     
@param {string} [options.title] The title of the javascript library    
@param {bool} [options.md] If true, render a markdown output rather than html    
@return {string} undefined An html representation of the documentation    
 
# exports.parseInner() 
 
Parse source code to produce documentation without the surrounding html page

 
@param {string} source JavaScript source code with comments    
@param {object} [options]     
@return {object} undefined {html:&quot;HTML representation of docs&quot;, css:&quot;link to a css style sheet to include&quot;}    
