---
layout: post
title:      "Sometimes an overambitious project needs to be dropped"
date:       2019-11-03 19:09:55 +0000
permalink:  sometimes_an_overambitious_project_needs_to_be_dropped
---


I was working on the sinrata project this week and had a great idea for key management but alas it was to grand a project.  between numerous issues and spending 10+ hours just fixing a single bug I had to scrap it because I wasn't going to finish it in time.   So on a friday I scrapped it deleting the repo so the only evidence is on my hard drive and made a new project for a game library.

This game library will list all the games someone owns so they can see all their games no matter what platform/distributor they have it on.  the following line of code retreives the games from the sql table and lists it on the page.

`<% @games.each do |game| %>
        <a href="buildings/<%=game.id%>"> <%=game.name%> <a>
<% end %>`

From tere the user can click on the game and then edit details or delete it.  With any luck I will be done with it all today and if not im going to keep working on it up to review.
