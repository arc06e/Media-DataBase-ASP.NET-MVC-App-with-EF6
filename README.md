#  Media-DataBase-ASP.NET-MVC-App-with-EF6


  ## Adam's Media Database (AMDb)
  <!--
   -demo: https://adams-media-database-app.azurewebsites.net
-->
 
  ## Description
  Welcome to my personal media database! I built this ASP.NET MVC app with Entity Framework 6. I started this project to gain a deeper understanding of MVC design patterns 
  and learn how to interact with databases through Entity Framework. As a frequent patron and deep admirer of public libraries, I thought it would be great to design this project so that I could chart all of my current and past library acquisitions and many ways they relate to one another. 
  
  ## Current Features
  * Seed Method which populates new database with a sample set of data to demonstrate app's key features.
  * CRUD functionality:
     * allows users to add, read, edit, and remove authors, books, movies, and contributors(cast and crew) from database.
  * Type-Per-Concrete-Class(TPC) Entity Inheritance pattern:
     * book and movie models inherit from abstract medium base class model.
     * author and contributor models inherit from abstract person base class model.
  * Multiple Entity Relationships:
     * one-to-many relationship between author and books.
        - uses foreign key and navigation properties.
     * many-to-many relationship between contributors(cast and crew) and movies.
        - uses navigation properties and a join table with payload(roles).
  * Utilizes both Models and ViewModels to allow users to:
     * display data from multiple tables in one page.
     * update multiple db tables in one submission.

## Set-Up Guide
1. Clone project in local directory:<br/>
``` gh repo clone arc06e/Media-DataBase-ASP.NET-MVC-App-with-EF6 ```
2. If you encounter the following server error: 'Could not find a part of the path ... bin\roslyn\csc.exe', run this command in your Package Manager Console:<br/>
``` Update-Package Microsoft.CodeDom.Providers.DotNetCompilerPlatform -r ```

## Intended Improvements
Time permitting, I would love to add a new join table to store which movies are adapted from existing books and books which are in turn novelizations of existing movies. Beyond that, it would be great to incorporate TV shows and Radio programs with their own respective join tables which would indicate which were adapted from existing intellectual properties. Oh, we haven't even got to comic books yet! 
