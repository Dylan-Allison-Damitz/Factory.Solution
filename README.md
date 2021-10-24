# Dr. Sillystringz Factory Manager 

#### By Dylan Allison-Damitz

## Technologies Used :floppy_disk:
* _NuGet Package Manager_
* _C#_
* _.Net 5_
* _REPL_
* _MySQL_
* _MySQL Workbench_
* _Microsoft Enity Framework_

## Description :page_with_curl:
_A web-based C# application that allows Dr. Sillystringz to manage and keep track of the engineers at his factory, as well as the machines each engineer is qualified to repair and operate. This project uses the Microsoft Entity Framework and migrations to create and store database inputs automatically_

## Setup/Installation Requirements :triangular_ruler:

* Clone github repo: https://github.com/Dylan-Allison-Damitz/Factory.Solution.git
* Navigate into the directory from your desktop: `cd Factory.Solution`
* Open in Vs code: `code .`
* Navigate to the Factory directory using the terminal: `cd Factory`
* To install dependencies, run: `dotnet restore`


## Updating appsettings.json

* In order for the Entity Framework to automatically create the database, you'll need to have your `appsettings.json` set up properly 
* Create an `appsettings.json` file within the `Factory` folder
* Copy and paste the following code into the file:

```
{
  "ConnectionStrings": {
      "DefaultConnection": "Server=localhost;Port=3306;database=dylan_allison_damitz;uid={YOUR-USERNAME};pwd={YOUR-PASSWORD};"
  }
}
```
* Make sure you remove the curly brackets after entering in your username and password
* Once your database connection is complete, return to the terminal and run `dotnet build` to compile the project

## Implementing Migrations

* Once `appsettings.json` has been created and filled out, assure you are still within the `Factory` foler and enter the command `dotnet tool install --global dotnet-ef --version 3.0.0` to ensure Enitity Framework is installed on your system
* Enter `dotnet ef migrations add Initial` to automatically create the database
* Type `dotnet ef database update` to assure any changes have been accounted for
* `dotnet run` will compile the project and launch in your local browser

## License :clipboard:
MIT &copy; 2021 _Dylan Allison-Damitz_
## Contact Information :mailbox:

_Dylan Allison-Damitz:
dylandamitz@gmail.com_
