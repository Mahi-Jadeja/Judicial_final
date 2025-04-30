# ⚖️ Judicial Case Manager System

## 📌 Project Overview
The **Judicial Case Manager System** is a Java-based desktop application that streamlines court case management, supporting roles like judges, lawyers, petitioners, and court staff. It integrates GUI-based interaction using Java Swing with a robust backend structure utilizing JDBC, DAO patterns, and Object-Oriented Programming (OOP) principles.

---

## 🚀 Features

### ✅ User Authentication
- Login system for Admin, Judges, Lawyers, etc.
- Session management using `SessionManager.java`

### 🗃️ Case & Entity Management
- Manage court cases, hearings, evidence, appeals, settlements, bail requests, and more.
- Class structure includes `CaseDetails`, `Hearing`, `CourtRoom`, `Person`, etc.

### 👨‍⚖️ Admin Functionalities
- Allocate cases and hearings
- Manage court staff and courtrooms
- Track case history and status

### 👤 User Functionalities
- Role-based data access for Lawyers, Judges, Petitioners, etc.
- View assigned cases, hearings, and status updates

---

## 💾 Data Storage & Handling
- Uses MySQL database with JDBC connectivity
- DAO classes perform secure operations using `PreparedStatement`
- Exception-safe methods with custom exception handling

---

## ⚠️ Exception Handling
- `DatabaseException`: Issues in DB connection or queries  
- `ValidationException`: Invalid form entries  
- `CaseNotFoundException`, `UserNotFoundException`: Entity not found cases

---

## 🛠️ Utility Classes
- `Validator.java`: Input validation  
- `DateUtil.java`: Date formatting (SQL ↔ Java)  
- `IDGenerator.java`: Auto-generates unique IDs  
- `SessionManager.java`: Tracks logged-in user info

---

## 🖥️ GUI Layer (Java Swing)
- `LoginFrame`, `WelcomeScreen`, and `AdminDashboard`
- Modular panels for each entity: `CaseManagementPanel`, `HearingPanel`, etc.
- Reusable components: `FormBuilder`, `TableBuilder`, `ButtonFactory`

---

## 📁 Project Structure
```
📦 JudicialCaseManagerSystem
├── 📂 src
│   └── 📂 main
│       ├── 📜 App.java                          # Main launcher class
│
│       ├── 📂 db
│       │   └── 📜 DatabaseConnection.java       # JDBC connection setup
│
│       ├── 📂 model                             # POJO (entity) classes
│       │   ├── 📜 CaseDetails.java
│       │   ├── 📜 Person.java                   # Abstract class
│       │   ├── 📜 Evidence.java
│       │   ├── 📜 Hearing.java
│       │   ├── 📜 Settlement.java
│       │   ├── 📜 Appeal.java
│       │   ├── 📜 Court.java
│       │   ├── 📜 CourtRoom.java
│       │   ├── 📜 CourtStaff.java
│       │   ├── 📜 CaseHistory.java
│       │   ├── 📜 BailRequest.java
│       │
│       │   ├── 📂 person                        # Subclasses of Person
│       │   │   ├── 📜 Petitioner.java
│       │   │   ├── 📜 Respondent.java
│       │   │   ├── 📜 PoliceOfficer.java
│       │   │   ├── 📜 Lawyer.java
│       │   │   └── 📜 Judge.java
│       │
│       │   └── 📂 interface
│       │       └── 📜 ICaseManager.java         # Interface for abstraction
│
│       ├── 📂 dao                               # DAO classes for DB operations
│       │   ├── 📜 CaseDAO.java
│       │   ├── 📜 PersonDAO.java
│       │   ├── 📜 EvidenceDAO.java
│       │   ├── 📜 HearingDAO.java
│       │   ├── 📜 SettlementDAO.java
│       │   ├── 📜 AppealDAO.java
│       │   ├── 📜 CourtDAO.java
│       │   ├── 📜 CourtRoomDAO.java
│       │   ├── 📜 CourtStaffDAO.java
│       │   ├── 📜 CaseHistoryDAO.java
│       │   └── 📜 BailRequestDAO.java
│
│       ├── 📂 exception                         # Custom exception handling
│       │   ├── 📜 DatabaseException.java
│       │   ├── 📜 CaseNotFoundException.java
│       │   ├── 📜 ValidationException.java
│       │   └── 📜 UserNotFoundException.java
│
│       ├── 📂 util                              # Utility classes
│       │   ├── 📜 Validator.java
│       │   ├── 📜 DateUtil.java
│       │   ├── 📜 IDGenerator.java              # Static ID generator
│       │   └── 📜 SessionManager.java           # Tracks current user
│
│       └── 📂 gui                               # GUI Layer using Swing
│           ├── 📜 LoginFrame.java
│           ├── 📜 WelcomeScreen.java
│           ├── 📜 AdminDashboard.java
│
│           ├── 📂 panels                        # Individual panels
│           │   ├── 📜 CaseManagementPanel.java
│           │   ├── 📜 PersonManagementPanel.java
│           │   ├── 📜 EvidencePanel.java
│           │   ├── 📜 HearingPanel.java
│           │   ├── 📜 SettlementPanel.java
│           │   ├── 📜 AppealPanel.java
│           │   ├── 📜 CourtRoomPanel.java
│           │   ├── 📜 CourtStaffPanel.java
│           │   ├── 📜 BailPanel.java
│           │   └── 📜 CaseHistoryPanel.java
│
│           └── 📂 components                    # Reusable GUI components
│               ├── 📜 TableBuilder.java
│               ├── 📜 FormBuilder.java
│               └── 📜 ButtonFactory.java
│
├── 📂 resources
│   └── 📜 application.properties                # DB config & constants
│
├── 📂 lib                                       # (Optional) for external jars
├── 📜 JudicialCaseManagerSystem.sql            # MySQL DB schema
└── 📜 README.md                                 # Project overview
```


---

## 🧑‍💻 Technologies Used
- **Language**: Java  
- **Database**: MySQL + JDBC  
- **Framework**: Swing (GUI)  
- **Design**: OOP principles, DAO Pattern  
- **Tools**: IntelliJ IDEA, Git, GitHub

---

## 👥 Team Members and Responsibilities

| Name              | Role                   | Responsibilities                                                              |
|-------------------|------------------------|-------------------------------------------------------------------------------|
| Mahi Jadeja       | Backend Developer      | Designed all POJO classes & DAO layers with OOP and interface-based abstraction |
| Priyanshi Faldu   | Exception Handler      | Developed custom exception framework for robust error handling               |
| Manan             | Frontend Developer     | Built complete Swing GUI with panels, navigation, and backend integration    |
| Nakshatra Pal     | Database Integrator    | Created DB schema and integrated JDBC for data persistence                   |


---

