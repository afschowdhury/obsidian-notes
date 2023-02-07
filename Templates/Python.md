---
type: Coding
tags: python
category: work
for_inteview: 
creation_date: <% tp.file.creation_date()%>
modification_date: <% tp.file.last_modified_date() %>
---

 <% await tp.file.move("/Python/" + tp.file.title) %> 
Current Folder : <% tp.file.folder() %>




[[<% tp.date.now("DD-MM-YYYY") %>]]

