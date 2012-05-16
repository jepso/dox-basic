<%= title %>
<%= ('=======================================================================================================').substr(0, title.length) %>

<% comments.forEach(function(comment){ 
  if(!comment.ignore && !comment.isPrivate) {%>

<% if(comment.ctx){ %># <%= comment.ctx.string %><% } %>

<%- comment.description.full %>

  <% } 
}) %>