Download Link: https://assignmentchef.com/product/solved-cs224-homework-2-legend-of-seeplusia-reloaded
<br>
The object oriented approach advocates encapsulation of related information in a class. A program proceeds by creating instances of the classes and having the instances interact with each other.

Object oriented <em>design </em>refers to deciding which information to group together and how. Alternately, it refers to deciding the classes for your program and their attributes (characteristics) and methods (behavior). This is not so much a science as it is an art—there are many possible designs for a given problem and all of them are <em>correct</em>.

In this assignment, we will redesign Legend of SeePlusia in an object oriented manner. We will encapsulate all information related to game logic in a Game class. Information related to a location will be represented in a Location class. We will model the information related to traveling from one location to another in a Road class. We will implement a Map class to model a map consisting of Location and Road objects. Finally, we will create a Player class to hold information and behavior relevant to the player.

<h1>Setting up the Map</h1>

Declarations of the classes Location, Road, and Map are attached. Write a corresponding implementation file for each class.

Use the above implementations to implement Map::set map() so as to create the map of SeePlusia given on Page 2. This is the same map as in the previous assignment.

One way roads, e.g. from <em>Swamps of Despair </em>to <em>Sands of Quick</em>, are modeled as follows. The corresponding Road object contains pointers to both Location objects. The Location with the missing direction has the corresponding pointer set to NULL. For example, the south pointer of the Location object corresponding to <em>Sands of Quick </em>stores NULL.

<h1>Game Logic</h1>

Game logic is encapsulated in the Game class. Declarations of the Player and Game classes are in the attached files. Implement them with the same logic as in the previous homework.

Once everything is set up, the main program is simply as follows.

<table width="609">

 <tbody>

  <tr>

   <td width="156"><strong>int </strong>main( <strong>int </strong>argc , Game game; game. run ();<strong>return </strong>0;}</td>

   <td width="104"><strong>char </strong>∗∗argv )</td>

   <td width="349">{</td>

  </tr>

 </tbody>

</table>

Put this main program in a file main.cpp.

<h1>Representing the Map</h1>

One benefit of encapsulation is that different components of the game are now independent of each other. For example, our game can now run on any valid map. A text representation of the map of SeePlusia is in the attached file seeplusia.txt. It has the following format.

<ul>

 <li>The first line contains, <em>n</em>, the number of locations in the map.</li>

 <li>Following the first line are 2 lines each for every location. The first of the 2 lines contains the id of the location and the second contains its name. The first location is the start location.</li>

 <li>Next are 10<em>n </em>lines—10 lines for each of the <em>n </em> These 10 lines list the location’s id, its neighboring locations and the number of days required to travel to each, and any special characteristic of the location. A blank value for a field indicates that the field does not apply to this location.</li>

</ul>

Implement the method, Map::read map(), that takes a parameter indicating the name of a map file, i.e. the file specifies a map in the above format. The method, Map::read map(), should read the map from the file and update the Map object accordingly. Test your method on the file, seeplusia.txt.

<h1>Level Maker</h1>

Write a map file in the format described above to represent the map on Page 3. Name the file mymap.txt and test your game by loading and playing this map.

<h1>Map of SeePlusia</h1>

Page 2 of 3