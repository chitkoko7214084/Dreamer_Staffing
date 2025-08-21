
# Domain Model

classDiagram
    direction RL
      
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

# classes 
Applicant: The person applying.

Application: The submitted form.

WorkHistory: The applicant's job experience.

Assessment: The test scores.

Staff: The employees using the system.

Skill: The specific skills tracked.
