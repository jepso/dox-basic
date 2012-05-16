<%= title %>
<%= ('=======================================================================================================').substr(0, title.length) %>

<% comments.forEach(function(comment){ 
  if(!comment.ignore && !comment.isPrivate){ if(comment.ctx){ %>
# <%= comment.ctx.string %><% } %>

<%- comment.description.full %>
<% if(comment.tags){
  comment.tags.forEach(function(tag){
%>@<%=tag.type%><%if(tag.types){%> {<%=tag.types.join("|")%>}<%}%> <%=tag.name||''%> <%=tag.description||''%>   
<%})
}
} 
}) %>