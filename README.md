![](/images/ahlsbanner.png)

*** 
# A-HLS Employee Experience Onboarding Workflow Documentation

## **Overview**

The Employee Experience Onboarding accelerator delivers 20+ pre-configured Salesforce Flows to display tasks assigned to new hires and their managers in single system. These pre-built Flows are available for download into your Salesforce org free of charge.

## **Business Objective**

The objective of the Accelerator is to help engage new employees from Day 1, help employees to learn the company culture more quickly, and provide a better employee experience.

## **Business Value and Benefits**

A great onboarding process sets the tone for the entire employee experience. Focusing on things like company culture, employee development, and frequent check-ins show new hires that you care about their experience at your company. Extending these focus areas beyond your onboarding period then continues that strong employee experience, from hire to retire. Employee Onboarding can improve the readiness, fit and performance of every employee who takes on a new role in the organization. An effective onboarding solution can offer the following benefits:

* Increases Employee Engagement
* Reinforces Company Culture
* Improves Employee Performance
* Increases the Ability to Attract new Talent
* Increases Employee Retention
* Reduces Cost of Turnover

## Industry Focus and Workflow

### Primary Industry:

* Healthcare and Life Sciences

### Intended End User:

* Multiple

## Package Includes:

*Flows (23)*

* Onboarding_Journey_Manager
* Onboarding_Journey_Manager_Manager_Tasks
* Onboarding_Task_90_Day_Feedback
* Onboarding_Task_Complete_Employee_Welcome_Check_In
* Onboarding_Task_Complete_Self_Evaluation_on_Goals_and_Performance
* Onboarding_Task_Create_Your_Individual_Development_Plan
* Onboarding_Task_Enroll_in_Benefits
* Onboarding_Task_Enroll_in_Development_Training
* Onboarding_Task_Enroll_in_New_Hire_Orientation
* Onboarding_Task_Establish_Employe_Training_Development_Plan
* Onboarding_Task_Manager_Check_in_Week1
* Onboarding_Task_Meet_with_your_Coach_Mentor
* Onboarding_Task_Refine_Your_Development_Plan
* Onboarding_Task_Review_Development_Objectives_with_Manager
* Onboarding_Task_Review_Documents
* Onboarding_Task_Review_Employee_Performance_Objectives
* Onboarding_Task_Review_Goals_and_Performance_With_Manager
* Onboarding_Task_Revisit_Career_Goals
* Onboarding_Task_Schedule_Employee_Manager_Next_Check_In
* Onboarding_Task_Set_Career_Goals
* Onboarding_Task_Set_New_Goals_Objectives_Add_to_Development_Plan
* Onboarding_Task_Verify_Employee_Profile
* Onboarding_Task_Week_1_Feedback
* Onboarding_Task_Welcome_Video

*LWCs (2)*

* directNavigationHeader
* directNavigationFooter

*Aura Component*

* flowButton

*Static Resources*

* EEOnboarding
* EEOnboardingCareer
* EEOnboardingSMART
* EEOnboardingWelcome

## Configuration Requirements

### Pre-Installation Steps:
Work with your Salesforce accont team to ensure you have a work.com org that meets these requirements:
1. A customer has the necessary Work.com licenses for the Employee Workplace, Employee Concierge, and HRSC managed packages installed and functional in the org prior to package install.
2. This includes the necesssary permission sets, permission set licenses, and permission set groups for the above work.com managed pacakges.
3. A customer has their employee hierarchy setup in the Work.com org prior to package install.

### Installation Steps:

1. Install the [Employee Expereince Onboarding](https://login.salesforce.com/packaging/installPackage.apexp?p0=04tDp0000006OoV) unmangaged package.

### Post-Install Configuration Steps:

1. Create **Transition Plan Template** record and import the **Transition Plan Tasks** and **Transition Plan Template Tasks** records per the below instructions. 
2. Make sure the newly installed Flows are active in the org. 
3. Place the Onboarding_Journey_Manager and Onboarding_Journey_Manager_Manager_Tasks Flows on your Salesforce Console and/or Experience Cloud page(s). 

### Data Creation & Import Steps:

The steps require an org with the below Assumptions

1. Create **Transition Plan Template** record- In the HR Service Center app create a Transition Plan Template record and complete the following fields:
    1. Template Name - New Employee Onboarding
    2. Transition Type - Onboarding
    3. Description - New employee onboarding template (or your preferred description) 
    4. Is Active - checked 
    5. Welcome Text - complete this field if you would like
      ![](/images/transitionplantemplateimage.png)
2. Import **Transition Plan Tasks** - import [2 - EE Onboarding Transition Plan Tasks.csv](https://github.com/healthcare-and-life-sciences/employee-experience-onboarding/blob/main/Data%20Files/2%20-%20EE%20Onboarding%20Transition%20Plan%20Tasks.csv) using the Data Import Wizard
3. Import **Transition Plan Template Tasks** - import [3 - EE Onboarding Transition Plan Template Tasks.csv](https://github.com/healthcare-and-life-sciences/employee-experience-onboarding/blob/main/Data%20Files/3%20-%20EE%20Onboarding%20Transition%20Plan%20Template%20Tasks.csv) using the Data Import Wizard. Make the following lookup field matching selections (see below screenshot)
    1. Select **Transition Plan Task Name **field to match against to set the Transition Plan Task lookup field.
    2. Select **Transition Plan Template Name **field to match against to set the Transition Plan Template lookup field.
    ![](/images/transitionplantemplatetasks.png)

## Assumptions

* A customer has the necessary [Work.com](http://work.com/) licenses for the Employee Workplace, Employee Concierge, and HRSC managed packages installed and functional in the org prior to package install. This includes the necesssary permission sets, permission set licenses, and permission set groups for the above work.com managed pacakges.
* A customer has their employee hierarchy setup in the [Work.com](http://work.com/) org prior to package install.
* Any users that are accessing the page(s) where these Flows are used need to have an employee record in that org. If the user doesn't have an employee record in the org it will cause an Apex CPU time limit exceeded error. 
* If these Flows will be accessed from an Experience Cloud site, that site is activated and functional. 
* A customer uses the above data import steps. This package is dependent on that data.   
* A customer is assuming Salesforce Lightning Experience — not Classic.
* The Accelerator uses the Lightning Design System standards and look. Customers may want to apply their own branding which can be achieved.

## Revision History
