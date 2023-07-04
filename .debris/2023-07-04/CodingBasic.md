---
type: Coding  
tags: coding-basic
category: work
for_inteview: True
creation_date: <% tp.file.creation_date()%>
modification_date: <% tp.file.last_modified_date() %>
---

 <% await tp.file.move("/coding basic/" + tp.file.title) %> 
Current Folder : <% tp.file.folder() %>




[[<% tp.date.now("DD-MM-YYYY") %>]]
