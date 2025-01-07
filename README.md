# FinSage

# 1 Data base
### Structure
- Domain - model
- Application - interface with DbSets
- Infrastructure - configurations of model, ApplicationDbContext, Extensions
(include starting account "admin")

- !Unsecure!: 
    1. "DefaultConnection": "Data Source=.;Initial Catalog=FinSage;User Id=kamil1;Password=1"
    2. options.UseSqlServer(connectionString).
            EnableSensitiveDataLogging()

### Create from scratch
- PM: 
update-database
- CMD from main project location  
cd */FinSage  
dotnet ef database update --project FinSage.Infrastructure --startup-project FinSage.WebAPI

### Create Migration
- PM:  
Add-Migration [name] -outputdir [Path]
- CMD:  
dotnet ef migrations add [name] --output-dir Persistence/Migrations --project FinSage.Infrastructure --startup-project FinSage.WebAPI
