# Group 8 MIST 4610 Group Project 1

## Team Name:
47114 Group 8

## Team Members:
1. Eryn Williams @erynwilliams
2. Jenny Gentry @jmg15190
3. Ariana Gonzalez @
4. Josh James @joshanttt
5. Jose Medrano @josemedjr
6. Rebekah Bradbury @rebekahbradbury 

## Problem Description 
Pretend you are the owner/operator of a emergency healthcare clinic needing to build a
relational database. You hired some students from the MIST 4610 class at the University of
Georgia to create the database for you. They need to know more about your organization to
identify which entities, attributes, and relationships are important for you. Start by describing
your business as a real client.

## Data Model:
Data Model Description: 

Our data model is based on the services of a health-care clinic. First off, our clinic services patients, within this entity, patients are identified by a unique patient id. In addition, other attributes about patients include, patient name, date of birth, gender, contact information and medical history. Meds are available at this clinic, identified by their medID.  As there are many patients seen at the clinic, many meds are available as well, the entities Patients and Meds share a many-to-many relationship with their associative entity being Prescriptions. Prescriptions capture the relationship of which patients are prescribed which medications. Each patient can have multiple prescriptions and each medication can be prescribed to multiple patients. Prescriptions are identified by PrescripID.
 
 The MedStaff table shares a one to many relationship with the Prescriptions table. This means that Medical Staff members can write many different prescriptions, but each prescription is only written by one staff member. The MedStaff table is composed of medStaffID, serving as the unique identifier, followed by attributes: name, position, and contact. Position being the title they hold (Doctor, NP, Nurse, CRNA). In addition, MedStaff shares a many-to-many relationship with Patients, their associative entity being Appointments. Appointments capture the relationship of which patients are seen by which medical staff at specific times. Each patient can have multiple appointments with different medical staff members and each medical staff member can have multiple appointments with different patients. The Appointments table is identified by a specific apptID, unique to each individual appointment. The entity MedRecord is used to record medical information from an appointment and shares a one-to-one relationship with appointments, meaning that there is one medical record associated with each appointment. The Billing table also shares a one-to-one relationship with Appointments meaning for each appointment, there is one bill. Billing also shares a many-to-many relationship with Insurance, with the associative entity being InsuranceBilled. InsuranceBilled captures the relationship of which billing entries are associated with which insurance policies. This relationship demonstrates that each billing entry can be associated with multiple insurance policies and each insurance policy can be associated with multiple billing entries. 
 
  The entity, Insurance,  is used to record insurances accepted by the clinic,  table is identified by a unique providerID which is the specific insurance provider code. Insurance shares a many-to-many relationship with Patient, the associative entity being InsurancetType. The associative entity Insurance Type captures the relationship of which patients are associated with what insurance policies and the specific type of insurance for each patient. The relationship shows that each patient can have different insurance policies, and each insurance provider can offer many different insurance plans/options. Lastly is the Service table, used to define the type of service performed at an appointment. Service shares a many-to-many relationship with appointments, connected through the associative entity, AssignedService. AssignedService defines the relationship between which service is being performed at a specific appointment. Assigned service is identified by a unique assignmentID. Overall, this relationship demonstrates that for each appointment many services are available to perform, and many services can be assigned to appointments. 


![image](https://github.com/rebekahbradbury/Group-8-MIST-4610-/assets/163002826/44f8c974-1818-4438-ac5d-a74eccfd5213)


## Data Dictionary: 


## Queries:
Data Matrix -

1. Query 1 lists the ID's and names of Medical Staff who have treated more than 2 patients.
<img width="1126" alt="Screenshot 2024-03-24 at 8 01 19 PM" src="https://github.com/rebekahbradbury/Group-8-MIST-4610-/assets/163002386/3952fce1-2983-40da-a41c-5e64f292679f">

Explain:

2. Query 2 lists the top 10 most frequently used medications names and the number of patients using them across all rooms in the clinic.
<img width="1126" alt="Screenshot 2024-03-24 at 8 01 55 PM" src="https://github.com/rebekahbradbury/Group-8-MIST-4610-/assets/163002386/14846020-85ef-49f8-ab87-5b683c5643ba">

Explain:

3. Query 3 lists all the names of patients with a balance due on their account and that amount due.
<img width="1126" alt="Screenshot 2024-03-24 at 8 02 16 PM" src="https://github.com/rebekahbradbury/Group-8-MIST-4610-/assets/163002386/410b15c7-31ef-461f-b9a1-f84c3153bdf5">

Explain:


4. Query 4 lists the information for all patients along with their total billing amount.
<img width="1126" alt="Screenshot 2024-03-24 at 8 02 34 PM" src="https://github.com/rebekahbradbury/Group-8-MIST-4610-/assets/163002386/1de209a8-7a68-4439-94a1-b6c8634411de">

Explain:


5. Query 5 lists the names of female patients and their average deductible only if their plan type begins with the letter T.
<img width="1126" alt="Screenshot 2024-03-24 at 8 05 48 PM" src="https://github.com/rebekahbradbury/Group-8-MIST-4610-/assets/163002386/86a0e60c-68dc-4468-ad9b-4dd5648b0fc6">

Explain:


6. Query 6 lists all medications currently prescribed to a patient.
<img width="1126" alt="Screenshot 2024-03-24 at 8 02 49 PM" src="https://github.com/rebekahbradbury/Group-8-MIST-4610-/assets/163002386/35f79b8c-4182-4b4f-b4cc-697be5ea36f1">

Explain:


7. Query 7 lists the patient name and their amount of insurance billed that is greater than the average amount of insurance billed to all patients.
<img width="1126" alt="Screenshot 2024-03-24 at 8 07 35 PM" src="https://github.com/rebekahbradbury/Group-8-MIST-4610-/assets/163002386/37f268f4-e09f-47df-b1c1-e5641ffb2a24">

Explain:


8. Query 8 lists the number of appointments attended by patients under each insurance provider.
<img width="1126" alt="Screenshot 2024-03-24 at 8 03 05 PM" src="https://github.com/rebekahbradbury/Group-8-MIST-4610-/assets/163002386/a3724c1b-7a05-48eb-8af5-d6071ca25b53">

Explain:


9. Query 9 lists the insurance plan type and average deductable amount for each insurance plan.
<img width="1126" alt="Screenshot 2024-03-24 at 8 08 19 PM" src="https://github.com/rebekahbradbury/Group-8-MIST-4610-/assets/163002386/9280ddd7-f994-4dac-a2d3-290d5d002d01">

Explain:


10. Query 10 lists the name of patients and the date of the appointment for those who are receiving a type of drainage service.
<img width="1126" alt="Screenshot 2024-03-24 at 8 11 37 PM" src="https://github.com/rebekahbradbury/Group-8-MIST-4610-/assets/163002386/d7644f18-4e5d-4864-86fb-6cb79375d639">

Explain:



## Database Information:

Name of the database: ns_Sp24_47114_Group8

Additional Information: 
