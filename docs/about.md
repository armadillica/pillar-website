# About

Some historical notes about how Pillar and the Blender Cloud came to be.

## Gooseberry Project - Cloud campaign
Blender Cloud was originally developed the next generation platform to share
and develop Open Content at the [Blender Institute](https://blender.institute).
The first iteration involved a simple Flask-based application, serving data
from a MySql database. The data was mainly Open Movies and Open Movie Workshops
content from past Blender Institute production.

Another notable feature of Blender Cloud, was complete crowdfunding/pledge
platform, which was used to raise funds for the production of the Gooseberry
project. Such plaftorm was meant to set up Blender Cloud subscriptions and
provide access to the content.

## Gooseberry Project - Attract
During the production of the [Cosmos Laundromat](https://cosmoslaundromat.org)
pilot, the Blender Cloud software was extended to improve its publishing
capabilites, so that potentially any member of the Blender Institute team could
publish content. An important aspect of this was asset processing (such as
image thumbnailing and video encoding), which was temporarily implemented as
background tasks on the Blender Cloud server.

Next to the existing Blender Cloud, the team started developing an improved
version of Attract, the production management tool originally developed during
the [Tears of Steel](https://tearsofseel.org) Open Movie project. The new
iteration of Attract was designed with the Blender Cloud in mind, looking for
a way to combine the existing publishing functionality with the project/shot
management fundcionality required.

This was the beginning of the Pillar framework, an
[Eve](http://python-eve.org/)-based application.

## Blender Cloud 3
After the the production of Cosmos Laundromat was completed, the team started
rewriting the Blender Cloud software using Pillar. The main architectural change
consited of the introduction of a new server component, accessible via a
RESTful API, which was reachable both by a web frontend and by Blender itself
with an addon.
