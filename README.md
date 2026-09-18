# java24bac10069
# Campus Course & Records Manager (CCRM)

## 📖 Project Overview
Campus Course & Records Manager (CCRM) is a **Java SE console-based application** that helps institutes manage:
- 👩‍🎓 Students (create/update, enroll/unenroll, transcripts)
- 📘 Courses (create/update, search, assign instructors)
- 📝 Enrollments & Grades (record marks, compute GPA, generate transcripts)
- 📂 File Utilities (import/export CSV, recursive backups, reports)

It demonstrates **Java OOP, NIO.2 file I/O, Streams, Date/Time API, exceptions, enums, design patterns (Singleton, Builder)**, and more.

---

📜 Evolution of Java (Brief Timeline)

1995: Java 1.0 released by Sun Microsystems
2004: Java 5.0 introduced Generics, Enums
2011: Oracle takes over Java
2014: Java 8 with Lambdas & Streams
2017: Java 9 modular system (Project Jigsaw)
2023+: Java 21 (LTS)


Java ME vs SE vs EE

Edition	:  Usage
Java ME :  Mobile & embedded devices
Java SE	:  Core platform for desktop & CLI apps
Java EE	: Enterprise apps (web servers distributed systems)



🔷JDK, JRE, JVM

JDK – Developer kit (compiler, debugger, libraries)
JRE – Runtime environment (to run Java apps)
JVM – Virtual machine that executes bytecode

Interaction:
Source Code (.java) → compiled by javac → Bytecode (.class) → runs on JVM inside JRE.


🖥️ Install Java on Windows

Download JDK from Oracle/OpenJDK
Install & set JAVA_HOME in Environment Variables

Verify:
java -version
javac -version


Eclipse IDE Setup

Install Eclipse IDE
File → New → Java Project → CCRM
Import src/ folder
Right-click CLIApp.java → Run As → Java Application


📑Mapping (Syllabus → Code)
Syllabus Topic	       File/Class
Encapsulation	       Student.java (private fields + getters/setters)
Inheritance	           Person.java → Student, Instructor
Abstraction	           Person.java (abstract methods)
Polymorphism	       TranscriptService.java using toString()
Singleton	           AppConfig.java
Builder	               Course.Builder
Exceptions	           DuplicateEnrollmentException.java
File I/O (NIO.2)	   ImportExportService.java
Recursion	           RecursionUtils.java
Enums	               Grade.java, Semester.java

✅ Assertions
Enable assertions when running:

java -ea -cp bin edu.ccrm.cli.CLIApp


##  How to Run
```bash
# Compile
javac -d bin src/edu/ccrm/cli/MainMenu.java src/edu/ccrm/cli/CLIApp.java src/edu/ccrm/domain/*.java src/edu/ccrm/service/*.java src/edu/ccrm/io/*.java src/edu/ccrm/util/*.java src/edu/ccrm/config/*.java

# Run
java -cp bin edu.ccrm.cli.CLIApp
