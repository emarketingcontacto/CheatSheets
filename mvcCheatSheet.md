	# H1MVC Todo

## Create Project 
# New Changes 

	dotnet new mvc [options] [template options]
	dotnet new mvc --name [name] --language [C#] --auth none

### Nuggets

Microsoft.EntityFrameworkCore 
Microsoft.EntityFrameworkCore.Tools
Microsoft.VisualStudio.Web.CodeGeneration.Design

### EF

dotnet tool install --global dotnet-ef --version 8.0.0
dotnet add package Microsoft.EntityFrameworkCore --version 8.0.0
dotnet add package Microsoft.EntityFrameworkCore.Tools --version 8.0.0
dotnet add package Microsoft.AspNetCore.Identity.EntityFrameworkCore --version 8.0.0
dotnet add package Microsoft.AspNetCore.Diagnostics.EntityFrameworkCore --version 8.0.0

#### Database 

Install-Package Microsoft.EntityFrameworkCore.SqlServer  --version 8.0.0 
dotnet add package Microsoft.EntityFrameworkCore.SqlServer --version 8.0.0 

### Start with Models
	`C#
		// Add Annotations // 
		[Key] 
		[Column(TypeName = "varchar(12)")]

### Adding Relashionships

public Nullable<int> catId { get; set; }
public virtual Category Category { get; set; }

### Create classl for dbContext 

	`C# 
	public class TransationDbContext:DbContext{
	public TransationDbContext(DbContextOptions)<TransactionDbContext>options) : base (options){}

	public class NameContext : DbContext
   	{
       public NameContext (DbContextOptions<NameContext> options) : base(options){}
   	}

### Add Connection String on appsetings,json 

 <connectionStrings>
    <add name="localConnString" connectionString="Server= LAPTOP-UOEP98J6;Database=TestOne;User Id=sa;Password=admin"/>
  </connectionStrings>


	Add DB Context in Program.cs 
		builder.Services.AddDbContext <[TransactionDbContext]>
		(options=>options.UseSqlServer(bilder.Configuration.GetConnectionString("ConnextionName")));  /* Add Database Manager */


### Add DBContext Service on Program.cs  
	`C# 
		builder.Services.AddDbContext<AppDBContext>(options=>options.UseSqlServer(builder.Configuration.GetConnectionString("DevConnString")));
	`

### Build App


###	Open Pakage Manager Console 
		Add-Migration "Initial Create" 
		Update Database 

### Check Database  

### Add Controllers

### Create Views

### Add views to Menu 

### FontAwesome Library 
