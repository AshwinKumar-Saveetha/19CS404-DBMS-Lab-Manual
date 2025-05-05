# Experiment 1: Entity-Relationship (ER) Diagram
```
Name: Ashwin Kumar A
Reg No: 212223040021
```
## Scenario Chosen:
University

## ER Diagram:

![image](https://github.com/user-attachments/assets/857b180d-fac1-4c37-aa70-56f603c23671)

## Entities and Attributes:
### Student:
Attributes: StudentID (PK), Name, Gender, DOB, Email, Phone, Address
### Instructor:
Attributes: InstructorID (PK), Name, Phone, Email
### Department:
Attributes: DepartmentID (PK), Department Name, Head of Department (FK → Instructor.InstructorID)
### Course:
Attributes: CourseID (PK), Course Name, Credits, DepartmentID (FK → Department.DepartmentID)
### Enrollment:
Attributes: EnrollmentID (PK), EnrollmentDate, Grade, StudentID (FK → Student.StudentID), CourseID (FK → Course.CourseID)
### Schedule:
Attributes: ScheduleID (PK), Day, Time, CourseID (FK → Course.CourseID), InstructorID (FK → Instructor.InstructorID), ClassroomID (FK → Classroom.ClassroomID)
### Classroom:
Attributes: ClassroomID (PK), Building, Room Number, Capacity

## Relationships and Constraints:
### Enrollment (EnrollmentID, StudentID, CourseID)
PK: EnrollmentID
FKs:
StudentID → Student(StudentID)
CourseID → Course(CourseID)
Type: Many-to-Many (via associative entity)
### Course (CourseID, DepartmentID)
PK: CourseID
FK: DepartmentID → Department(DepartmentID)
Type: Many-to-One
### Instructor (InstructorID, CourseID) (via Schedule or a separate junction table)
PK: InstructorID
Relationship Type: Many-to-Many
### Schedule (ScheduleID, CourseID, ClassroomID, InstructorID)
PK: ScheduleID
FKs:
CourseID → Course(CourseID)
InstructorID → Instructor(InstructorID)
ClassroomID → Classroom(ClassroomID)
Type: Composite Association

## RESULT:
Thus, we have created an E-R Diagram for the chosen scenario successfully, defining the necessary entities, attributes, relationships, and constraints.
