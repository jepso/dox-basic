<!DOCTYPE html> 
<html lang="en"> 
<head> 
  <title>Dox Basic</title> 
  <link rel="stylesheet" href="http://twitter.github.com/bootstrap/assets/css/bootstrap.css"/> 
  <link rel="stylesheet" href="http://twitter.github.com/bootstrap/assets/css/bootstrap-responsive.css"/> 
  <style> 
    pre { 
      background: #272822; 
      overflow: auto; 
      word-wrap: normal; 
      white-space: pre; 
    } 
    pre code { 
      font: 12px monaco, monospace; 
      color: #F8F8F2; 
    } 
    pre code .string { 
      color: #E6DB74; 
    } 
    pre code .number { 
      color: #AE81FF; 
    } 
    pre code .keyword { 
      color: #F92672; 
    } 
    pre code .comment { 
      color: #b3b3b3; 
    } 
    h1.pagetitle { 
      font-size: 4em; 
      margin-bottom: 20px; 
      margin-top: 20px; 
    } 
  </style> 
</head> 
<body> 
  <div class="container-fluid"> 
    <div class="row-fluid"> 
      <h1 class="pagetitle">Dox Basic</h1> 
    </div> 
    <div class="row-fluid"> 
      <div> 
         
           
         
           
            <div class="comment "> 
               
              <div class="description"><h1>Example Usage</h1>

<pre><code>npm install dox-basic -g
dox-basic -t "Library Name"&lt;index.js&gt;readme.html
</code></pre></div> 
               
            </div> 
           
         
           
            <div class="comment property"> 
              <h1>exports.name</h1> 
              <div class="description"><p>Parser name</p></div> 
               
                <pre><code>exports.name = 'dox-basic';</code></pre> 
               
            </div> 
           
         
           
            <div class="comment property"> 
              <h1>exports.version</h1> 
              <div class="description"><p>Parser version</p></div> 
               
                <pre><code>exports.version = '0.0.1';</code></pre> 
               
            </div> 
           
         
           
            <div class="comment method"> 
              <h1>exports.parse()</h1> 
              <div class="description"><p>Parse source code to produce documentation</p></div> 
               
                <pre><code>exports.parse = <span class="keyword">function</span>(source, options){
    options = options || {};
    <span class="keyword">var</span> title = options.title || <span class="string">'Documentation'</span>;
    <span class="keyword">var</span> dox = <span class="keyword">require</span>(<span class="string">'dox'</span>);
    <span class="keyword">var</span> obj = dox.parseComments(source);

    <span class="keyword">return</span> highlight(ejs.render(template, {title: title, comments:obj}));
}</code></pre> 
               
            </div> 
           
         
           
            <div class="comment method"> 
              <h1>exports.parseInner()</h1> 
              <div class="description"><p>Parse source code to produce documentation without the surrounding html page</p></div> 
               
                <pre><code>exports.parseInner = <span class="keyword">function</span>(source, options){

}</code></pre> 
               
            </div> 
           
         
      </div> 
    </div> 
  </div> 
  <script src="http://cdnjs.cloudflare.com/ajax/libs/twitter-bootstrap/2.0.2/bootstrap.min.js"/> 
</html>