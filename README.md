<h1 align="center">Real Estate Website</h1>

<p align="center">
  <a href="https://dotnet.microsoft.com/en-us/apps/aspnet">
    <img src="https://img.shields.io/badge/ASP.NET-MVC%205-blue?style=for-the-badge&logo=dotnet&logoColor=white" alt="ASP.NET MVC 5">
  </a>
  <a href="https://dotnet.microsoft.com/en-us/download/dotnet-framework/net472">
    <img src="https://img.shields.io/badge/.NET%20Framework-4.7.2-512BD4?style=for-the-badge&logo=.net&logoColor=white" alt=".NET Framework 4.7.2">
  </a>
  <a href="https://www.microsoft.com/en-us/sql-server">
    <img src="https://img.shields.io/badge/SQL%20Server-2017%2B-CC2927?style=for-the-badge&logo=microsoft-sql-server&logoColor=white" alt="SQL Server">
  </a>
  <a href="https://entityframework.net/">
    <img src="https://img.shields.io/badge/ORM-Entity%20Framework%206-brightgreen?style=for-the-badge" alt="Entity Framework 6">
  </a>
  <a href="LICENSE">
    <img src="https://img.shields.io/badge/license-MIT-darkred?style=for-the-badge" alt="License">
  </a>
</p>

<p align="center">
  <b>A comprehensive, professional real estate listing and management platform.</b><br><br>
  <i>Built with ASP.NET MVC 5 for robust backend logic, Entity Framework 6 for data persistence, and Microsoft SQL Server.</i>
</p>
<br>
<p align="center">
  <a href="#technical-architecture">
    <img src="https://img.shields.io/badge/Architecture-222222?style=flat" />
  </a>
  <span> · </span>
  <a href="#project-structure">
    <img src="https://img.shields.io/badge/Structure-222222?style=flat" />
  </a>
  <span> · </span>
  <a href="#key-features--modules">
    <img src="https://img.shields.io/badge/Features-222222?style=flat" />
  </a>
  <span> · </span>
  <a href="#technical-specifications">
    <img src="https://img.shields.io/badge/Specs-222222?style=flat" />
  </a>
  <span> · </span>
  <a href="#deployment--installation">
    <img src="https://img.shields.io/badge/Deploy-222222?style=flat" />
  </a>
</p>

---
<br>
<h2 align="center">Technical Architecture</h2>

The application follows the **Classical MVC (Model-View-Controller)** pattern, designed for scalability and maintainability. It leverages the .NET ecosystem to provide a secure and efficient environment for real estate operations:

1.  **Frontend (Views):** Utilizes Razor syntax with Bootstrap 3/4 for a responsive and user-friendly interface. jQuery handles client-side transitions and dynamic interactions.
2.  **Web Layer (Controllers):** ASP.NET MVC 5 controllers orchestrate the business logic, ranging from property listing management to advanced filtering.
3.  **Data Persistence (Models & EF6):** An Object-Relational Mapper (Entity Framework 6) manages communication between the application's domain models and the SQL Server backend.
4.  **Security (Identity):** Integrated ASP.NET Identity 2.x for secure user authentication, registration, and role-based access control.

---
<br>
<h2 align="center">Project Structure</h2>

```
RealEstateWebsite/
├── ASP.NET Project/                          # Core development workspace
│   ├── RealEstateWebsite.sln                 # Visual Studio Solution
│   ├── RealEstateWebsite/                    # Main MVC Project Directory
│   │   ├── App_Start/                        # Route, Bundle, and Auth configurations
│   │   ├── Controllers/                      # Request handling and logic
│   │   ├── Models/                           # Data entities and EF Context
│   │   ├── Views/                            # Razor UI templates
│   │   ├── Content/                          # CSS and static styling assets
│   │   ├── Scripts/                          # jQuery and client behavior
│   │   ├── Web.config                        # Application settings and connection strings
│   │   └── packages.config                   # NuGet dependency manifest
│   └── ilanImages/                           # Property listing image repository
│
├── SQL Database/                             # Database assets
│   ├── EmlakSite.bak                         # SQL Server Database Backup
│   └── Database_Notes.txt                    # DB configuration guide
│
├── Report/                                   # Project documentation and reports
├── .gitignore                                # Version control exclusions
├── LICENSE                                   # MIT License terms
├── Promotion Video.mp4                       # Project demonstration video
└── Versions.txt                              # Versioning history and changelog
```

---
<br>
<h2 align="center">Key Features & Modules</h2>

### 1. Listing Management (`IlanController`)
The core functionality of the platform allows users to browse, view detailed property information, and manage listings.
- **Dynamic Filtering:** Search by property type, status (Sale/Rent), and location.
- **Image Handling:** Integrates with the `ilanImages/` directory for visual property presentation.

### 2. Location Services (`Sehir`, `Semt`, `Mahalle`)
A hierarchical location system for precise property categorization:
- **City (Sehir):** Top-level region management.
- **District (Semt) & Neighborhood (Mahalle):** Granular location filtering for localized searches.

### 3. Integrated Authentication (`AccountController`)
Powered by ASP.NET Identity to ensure secure user interaction:
- **Registration & Login:** Secure password hashing and cookie-based sessions.
- **Role Management:** Admin-level controls for platform oversight.

### 4. Admin Dashboard (`AdminController`)
A central hub for site administrators to manage property types, statuses, and site-wide configurations.

---
<br>
<h2 align="center">Technical Specifications</h2>

<table align="center">
  <tr>
    <th align="center">Component</th>
    <th align="center">Technology Stack</th>
  </tr>
  <tr>
    <td align="center">Framework</td>
    <td align="center">ASP.NET MVC 5 (.NET Framework 4.7.2)</td>
  </tr>
  <tr>
    <td align="center">Data Persistence</td>
    <td align="center">Entity Framework 6.x (ORM)</td>
  </tr>
  <tr>
    <td align="center">Database Engine</td>
    <td align="center">Microsoft SQL Server 2017+</td>
  </tr>
  <tr>
    <td align="center">Security Layer</td>
    <td align="center">ASP.NET Identity 2.2</td>
  </tr>
  <tr>
    <td align="center">UI / Frontend</td>
    <td align="center">Razor, Bootstrap, jQuery</td>
  </tr>
</table>

---
<br>
<h2 align="center">Deployment & Installation</h2>

### 1. Repository Acquisition
Clone the repository to your local development environment:
```bash
git clone https://github.com/Zer0-Bug/RealEstateWebsite.git
```

### 2. Database Restoration
The project includes a pre-configured database backup:
1.  Launch **SQL Server Management Studio (SSMS)**.
2.  Right-click 'Databases' and select **'Restore Database...'**.
3.  Choose the `EmlakSite.bak` file from the `SQL Database/` directory.
4.  Ensure the restored database name aligns with your connection string.

### 3. Application Configuration
1.  Open `RealEstateWebsite.sln` in **Visual Studio 2019/2022**.
2.  Update the connection string in `Web.config`:
    ```xml
    <connectionStrings>
      <add name="EmlakContext" connectionString="Data Source=YOUR_SERVER;Initial Catalog=EmlakSite;Integrated Security=True" providerName="System.Data.SqlClient" />
    </connectionStrings>
    ```
3.  Restore NuGet packages via the **Package Manager Console**.

### 4. Execution
Press `F5` or click **'IIS Express'** in Visual Studio to launch the application.
Default access: `http://localhost:[RANDOM_PORT]`

---
<br>
<h2 align="center">Contribution</h2>

Contributions are welcome to enhance the RealEstateWebsite ecosystem. To contribute:

1. Fork the repository.
2. Create a new branch for your change:  
   `git checkout -b feature/your-feature-name`
3. Commit your changes with a clear and descriptive message:  
   `git commit -m "Add: brief description of the change"`
4. Push your branch to your fork:  
   `git push origin feature/your-feature-name`
5. Open a Pull Request describing the changes made.

All contributions are reviewed before being merged. Please ensure that your changes follow the existing code style and include relevant documentation or tests where applicable.

---
<br>
<h2 align="center"><b><i>Environment & Requirements</i></b></h2>

> [!IMPORTANT]
> - **OS:** Windows 10/11 (Required for .NET Framework development).
> - **IDE:** Visual Studio 2019/2022 with ASP.NET and web development workload.
> - **Database:** LocalDB or a full SQL Server instance (2017 or newer).

> [!NOTE]
> - This project is a demo/sample implementation intended for learning and evaluation. Do not use the demo data or bundled images in production without replacing them with appropriate assets and sanitized test data.
---

<br>
<p align="center">
  <a href="mailto:777eerol.exe@gmail.com">
    <img src="https://cdn.simpleicons.org/gmail/D14836" width="40" alt="Email">
  </a>
  <span> × </span>
  <a href="https://www.linkedin.com/in/eerolexe/">
    <img src="https://upload.wikimedia.org/wikipedia/commons/c/ca/LinkedIn_logo_initials.png"
         width="40"
         alt="LinkedIn">
  </a>
</p>

---

<br>
<p align="center" style="margin-top:10px; letter-spacing:4px;">
  ∞
</p>
