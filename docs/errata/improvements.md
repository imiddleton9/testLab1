**Improvements** (3 items)

If you have suggestions for improvements, then please [raise an issue in this repository](https://github.com/markjprice/apps-services-net7/issues) or email me at markjprice (at) gmail.com.

- [Page 72 - Executing stored procedures using ADO.NET](#page-72---executing-stored-procedures-using-adonet)
- [Page 81 - Defining the Northwind database model](#page-81---defining-the-northwind-database-model)
- [Page 362 - Building a web service that supports OData](#page-362---building-a-web-service-that-supports-odata)

# Page 72 - Executing stored procedures using ADO.NET

> Thanks to [Bob Molloy](https://github.com/BobMolloy) for raising this [issue on 31 December 2022](https://github.com/markjprice/apps-services-net7/issues/3).

In Step 2, I wrote, "In your preferred database tool, add a new stored procedure. For example, if you are using 
SQL Server Management Studio, then right-click Stored Procedures and select Add New Stored Procedure."

It would be better to add an extra step, "In your preferred database tool, add a new stored procedure. For example, if you are using SQL Server Management Studio, then **expand the Programmability node,** right-click Stored Procedures, and select Add New Stored Procedure."

# Page 81 - Defining the Northwind database model

> Thanks to [Bob Molloy](https://github.com/BobMolloy) for raising this [issue on 31 December 2022](https://github.com/markjprice/apps-services-net7/issues/4).

In Step 4, I show text that must be entered as a single line at the command-line, as shown in the following command formatted as in the print book:
```
dotnet ef dbcontext scaffold "Data Source=.;Initial 
Catalog=Northwind;Integrated Security=true;TrustServerCertificate=true;" 
Microsoft.EntityFrameworkCore.SqlServer --output-dir Models --namespace 
Northwind.Console.EFCore.Models --data-annotations --context NorthwindDb
```

Here is the same command as a single line to make it easier to copy and paste:
```
dotnet ef dbcontext scaffold "Data Source=.;Initial Catalog=Northwind;Integrated Security=true;TrustServerCertificate=true;" Microsoft.EntityFrameworkCore.SqlServer --output-dir Models --namespace Northwind.Console.EFCore.Models --data-annotations --context NorthwindDb
```

I recommend that you copy and paste long commands like this from the ebook into a plain text editor like Notepad, and then make sure that the whole command is properly formatted as a single line, before you then copy and paste it to the command-line. 

Copying and pasting directly from the ebook is likely to include newline characters and missing spaces and so on that break the command.

# Page 362 - Building a web service that supports OData

> Thanks to Bob Molloy for emailing me about this issue on 5 January 2023.

In Step 3, you add a reference to a project that is outside the solution. In Step 4, you build the project at the command-line or terminal by using the following command: `dotnet build`. 

There is a note to explain that if you try to use the **Build** menu in Visual Studio then you will see an error. This is because Visual Studio cannot find projects that are outside a solution. In early drafts of the book, this was the first time this situation occurred which is why I put the note here. In later drafts, the SQL Server and Cosmos DB chapters were moved earlier. So then the first time the situation occurs is in Chapter 3 on page 130. In the next edition I will move the note to the first time the situation occurs.