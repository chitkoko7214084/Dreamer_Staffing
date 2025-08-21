Class Diagram 📊
Classes
Applicant
Attributes:
applicantId: int (PK)
firstName: string
lastName: string
email: string
phone: string
dateOfBirth: date
readinessScore: int
readinessCategory: enum
Methods:
calculateReadinessScore()
categorizeApplicant()
Application
Attributes:
applicationId: int (PK)
submissionDate: date
status: enum
isStaffEntered: boolean
Methods:
submitApplication()
WorkHistory
Attributes:
workHistoryId: int (PK)
companyName: string
jobTitle: string
startDate: date
endDate: date
duties: string
reasonForLeaving: string
Methods:
(None specified)
Assessment
Attributes:
assessmentId: int (PK)
englishScore: int
safetyScore: int
Methods:
getEnglishScore()
getSafetyScore()
Staff
Attributes:
staffId: int (PK)
firstName: string
lastName: string
username: string
role: enum
Methods:
createApplicant()
manageApplicants()
Skill
Attributes:
skillId: int (PK)
skillName: string
Methods:
(None specified)
Relationships
Applicant to Application
Relationship: One-to-One (1..1)
Description: An Applicant has one Application.
Applicant to WorkHistory
Relationship: One-to-Many (1..*)
Description: An Applicant can have multiple WorkHistory records.
Applicant to Assessment
Relationship: One-to-One (1..1)
Description: An Applicant has one Assessment.
Application to Staff
Relationship: Many-to-One (*..1)
Description: An Application may be entered by a Staff member.
Applicant to Skill
Relationship: Many-to-Many (*..*)
Description: An Applicant can have many Skills, and a Skill can be held by many Applicants. (This relationship is typically resolved with a linking table, such as ApplicantSkill).
