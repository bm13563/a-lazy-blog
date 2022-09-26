# The closest approach between two Polygons - an exploration of various spatial indexes

A previous job of mine involved heavy use of PostGIS, a semi-magical PostgreSQL extension that enables the user to perform complex computational geometry without straying too far from the cozy declarative comforts of SQL. That's a pretty elaborate way of saying that PostGIS is a piece of software that's used to analyze where things are, particularly in relation to one another. For example -- ever wanted to know know the exact distance between Stroud and Basingstoke? Nope? Well if you _did_, you could absolutely use some form of GIS, be it QGIS, ArcGIS or PostGIS to find out. This example hardly does justice to the breadth of real-world use cases for GIS, particularly PostGIS, which compared to it's aforementioned counterparts trades performance and scalability for a steep learning curve and a pre-requisite knoweledge of SQL.

Although it sounds kinda lame, I was always been curious about how PostGIS (or any other GIS) actually works. Now that I'm older, wiser (???) and a fully fledged software engineer, I've decided to revisit my old interest in GIS from first principles, and in the world of GIS, there seems no better place to start than finding the distance between two polygons.

## The problem

Finding the differene between two polygons should be kinda easy right? A polygon is just a load of points that have been joined up to create a shape. So, presumably all we need to do is find the difference between each point?

<iframe src="https://editor.p5js.org/bm13563/full/7nUsC6Scv"></iframe>