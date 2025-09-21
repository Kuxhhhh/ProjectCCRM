# Campus Course & Records Manager (CCRM)

This project is a working Java SE for the CCRM assignment. It implements core domain classes, services, a CLI menu, CSV import/export, and a backup utility (NIO.2). It demonstrates many syllabus requirements and includes additional utilities and notes.

## How to install java on windows
To start coding in Java, you first need to install the Java Development Kit (JDK) on your system.

Step 1: Visit the official Oracle website https://www.oracle.com/in/java/. Click on the "Download Java" icon as shown in the below image.

Step 2: Now you can see the latest version is JDK 25 and there are options for Linux, macOS, and Windows. Click on the Windows option and then click the x64 Installer option to download the .exe file for 64-bit Windows OS.

<img width="962" height="437" alt="image" src="https://github.com/user-attachments/assets/2c03afeb-870e-48a4-8988-0cf9c78fad95" />



 

Step 3: Go to Downloads and double-click on that downloaded jdk-23_windows-x64_bin.exe file. So now Java Installation Wizard get open and then click Next button.

Step 4: Now we will set the environment variables for Windows OS. Open the C drive, go to Program Files > Java > jdk-25 (or your installed version) > bin folder. Now, copy the path and we will use this path when configuring the environment variables.
<img width="795" height="120" alt="image" src="https://github.com/user-attachments/assets/fa95cb1a-1d9f-41ca-9812-ffc91dd90042" />


 

Search for environment variable on your system, then click on the Environment Variables button.
<img width="563" height="416" alt="image" src="https://github.com/user-attachments/assets/387c61d8-354b-44f7-9fff-8b9bff83da92" />


 

In the system variable section, select the path variable and then click the option Edit.
<img width="478" height="531" alt="image" src="https://github.com/user-attachments/assets/2ee0d1e7-a4e8-4cfe-aa9e-91640baf6704" />



 
Paste the path that copied earlier, and click OK to save the changes.

Step 5: Verify the Installation. Open command prompt and type the below command to verify the Java version that is installed in the system.
Cmd: java --version
<img width="739" height="316" alt="image" src="https://github.com/user-attachments/assets/2007cf84-22bf-43c0-8091-bc0e3a7b1854" />


 


## How to compile & run

step 1: open elcipseIDE or IntelliJ
Step 2: click on open project

<img width="499" height="410" alt="image" src="https://github.com/user-attachments/assets/966be996-2f0d-4029-99e3-ef13ee6b191c" />


 




Step 3: select the ccrm project folder and click on ok.


<img width="538" height="551" alt="image" src="https://github.com/user-attachments/assets/2378bfc5-5887-4e5a-aac7-e81aedf62357" />


 

Step 4: navigate to  ProjectCCRM/CCRM_Project_Java/out/production/CCRM_Project_complete/edu/ccrm/cli

/Main.class, then double click on it.

Step 5: right click anywhere on the code then choose run “mainmenu.main()”.


<img width="635" height="491" alt="image" src="https://github.com/user-attachments/assets/63494c9e-b9b0-4b56-8fae-eb61275bdbc1" />


 

result

<img width="962" height="209" alt="image" src="https://github.com/user-attachments/assets/499ffa58-6cf0-4b25-9984-7ef761cd1afc" />



 


(see USAGE.md for detailed instructions)

## Java evolution (short timeline)
- 1995: Java 1.0 — "Write once, run anywhere" motto, basic language and libraries.
- 1998: Java 2 (J2SE) — major API additions (collections).
- 2004: Java 5 — generics, annotations, enhanced for-loop, enums.
- 2014: Java 8 — lambdas and Streams (important for this project).
- 2017-2021+: Java 9-17 — modularity (JPMS), local-variable type inference (var), performance improvements.
- 2021-2024+: Ongoing: records, pattern matching, performance and API enhancements.

  


## Java ME vs Java SE vs Java EE (Jakarta EE)
- **Java ME**: Micro Edition for embedded and constrained devices (IoT, phones historically).
- **Java SE**: Standard Edition — desktop and client/server apps, core libraries, what this project uses.
- **Java EE / Jakarta EE**: Enterprise Edition — servlets, JPA, EJBs, for large server-side enterprise applications.

### Comparison Table

| Feature | **Java ME** | **Java SE** | **Java EE / Jakarta EE** |
| :--- | :--- | :--- | :--- |
| **Full Name** | Micro Edition | Standard Edition | Enterprise Edition |
| **Primary Use** | Embedded and constrained devices (IoT, phones historically) | Desktop and client/server applications | Large server-side enterprise applications |
| **Core Components** | A subset of SE libraries for resource-constrained environments | Core libraries and APIs | Servlets, JPA, EJBs, etc. for enterprise-level services |


### Comparison Table

| Feature | **JVM** | **JRE** | **JDK** |
| :--- | :--- | :--- | :--- |
| **Full Name** | Java Virtual Machine | Java Runtime Environment | Java Development Kit |
| **Purpose** | Runs compiled bytecode | Provides an environment to run Java applications | Provides tools to develop, compile, and run Java applications |
| **Contains** | N/A | JVM + standard class libraries | JRE + compiler (`javac`) + development tools |


## JDK vs JRE vs JVM
- **JVM**: Java Virtual Machine — runs compiled bytecode.
- **JRE**: Java Runtime Environment — JVM + standard class libraries to run Java apps.
- **JDK**: Java Development Kit — JRE + compiler (`javac`) and development tools.

## Mapping table (syllabus topic -> file/class demonstrating it)
- Encapsulation, getters/setters: `edu.ccrm.domain.Person`, `Student`, `Course`.
- Inheritance & Abstraction: `edu.ccrm.domain.Person` (abstract) -> `Student`, `Instructor`.
- Polymorphism & toString(): `Person#toString`, overrides in `Student`, `Instructor`.
- Enums (Semester, Grade): `edu.ccrm.domain.Semester`, `Grade`.
- Streams & filtering: `edu.ccrm.service.CourseService`, `StudentService`.
- NIO.2 File I/O: `edu.ccrm.io.ImportExportService`.
- Singleton pattern: `edu.ccrm.config.AppConfig`.
- Builder pattern: `edu.ccrm.domain.Course.Builder`.
- Custom Exceptions: `edu.ccrm.domain.DuplicateEnrollmentException`, `MaxCreditLimitExceededException`.
- Assertions: `edu.ccrm.service.EnrollmentService` (enable at runtime with `-ea`).
- Immutable class: `edu.ccrm.util.ImmutableName`.
- Nested classes: `edu.ccrm.domain.NestedDemo` (static nested + inner).
- Interfaces: `edu.ccrm.util.Persistable`, `edu.ccrm.util.Searchable`.
- Anonymous inner class: `edu.ccrm.cli.MainMenu` (Runnable callback).
- Lambdas: used in service filtering and streams across services.

## Enabling assertions
Run the JVM with `-ea` to enable assertions. Example:
```
java -ea -cp out edu.ccrm.cli.MainMenu
```

##Acknowledment
References used: geeksforgeeks, javatpoint.


