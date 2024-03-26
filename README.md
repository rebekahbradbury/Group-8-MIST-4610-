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

Explain: This query allows the clinic to decipher which medical staff have serviced more than 2 patients, informing them on how many patients each member of the medical staff are attending to over a period of time. Being able to track medical staff and how many patients they are seeing is essential in an emergency health clinic for organizational and efficiency purposes. 

2. Query 2 lists the top 10 most frequently used medications by their names and the number of patients currently taking the medicine.
<img width="1126" alt="Screenshot 2024-03-24 at 8 01 55 PM" src="https://github.com/rebekahbradbury/Group-8-MIST-4610-/assets/163002386/14846020-85ef-49f8-ab87-5b683c5643ba">

Explain: This query generates the number of patients currently using one of the top 10 medications provided by the clinic. Identifying the most used medications can help the clinic track which medications they may need to order soon or on a more frequent basis. 

3. Query 3 lists the names of patients with a balance due on their account and the amount due.
<img width="1126" alt="Screenshot 2024-03-24 at 8 02 16 PM" src="https://github.com/rebekahbradbury/Group-8-MIST-4610-/assets/163002386/410b15c7-31ef-461f-b9a1-f84c3153bdf5">

Explain: This query generates the names of patients who have an "unpaid" status listed on their account and the amount they owe. This information is important because it notifies the clinic of which patients they need to contact about paying outstanding bills. It is also important for insurance purposes, as many patients may use co-pay or may change insurances and be unaware that certain charges may not be covered based on their plans. Lastly, if bills are not eventually paid, the clinic will need this information to report the outstanding bill to collections. 


4. Query 4 lists patientID, patientName, dob, gender, contact and medHistory and total billed amount 
<img width="1126" alt="Screenshot 2024-03-24 at 8 02 34 PM" src="https://github.com/rebekahbradbury/Group-8-MIST-4610-/assets/163002386/1de209a8-7a68-4439-94a1-b6c8634411de">

Explain: This query lists all available patient information, their medical history and how much they were billed. 


5. Query 5 lists the average deductible of female patients whose insurance plan type begins with T
<img width="1126" alt="Screenshot 2024-03-24 at 8 05 48 PM" src="https://github.com/rebekahbradbury/Group-8-MIST-4610-/assets/163002386/86a0e60c-68dc-4468-ad9b-4dd5648b0fc6">

Explain: The health clinic might need to use this query to assess the financial burden on female patients with specific insurance plans. Understanding the average deductible for a certain demographic can aid in financial planning, resource allocation, and more to ensure fair access to healthcare services for female patients with particular insurance plans. Such insights can inform decision-making processes aimed at enhancing the overall patient experience and ensuring that healthcare remains accessible and affordable for all.


6. Query 6 lists the medicine name and the percentage of patients who are taking a med with a dosage less than 100mg
![image](https://github.com/rebekahbradbury/Group-8-MIST-4610-/assets/163002826/920881a2-8531-4c1c-943e-4fb1b2ecdc9b)


Explain: Understanding which medications patients are using allows the clinic to monitor the effectiveness of treatments. If a significant percentage of patients are taking a particular medication but not showing improvement, it may indicate that the treatment protocol needs adjustment.


7. Query 7 lists the patient name and their amount of insurance billed that is greater than the average amount of insurance billed to all patients.
<img width="1126" alt="Screenshot 2024-03-24 at 8 07 35 PM" src="https://github.com/rebekahbradbury/Group-8-MIST-4610-/assets/163002386/37f268f4-e09f-47df-b1c1-e5641ffb2a24">

Explain: The health clinic may want to know the patients who have paid more than the average for all patients can help ensure quality care and identify bill errors or fraud. Being able to identify patients who pay more than the average amount allows the health clinic to conduct quality checks with surveys to ask the patients if they are satisfied with the service and bill they were provided. Also, this allows the health clinic to check for any potential fraud errors to discover the reason why these patients are being billed more than average


8. Query 8 lists the number of appointments attended by patients under each insurance provider.
![image](https://github.com/rebekahbradbury/Group-8-MIST-4610-/assets/163002826/3fbe0952-f46b-4dcd-a21c-41cac7202b10)


Explain:
Health clinics may want to know the number of appointments attended by patients based on insurance providers to determine which insurance providers are best and which ones may be the worst. Many appointments with the same provider may imply that that specific insurance provider may be best for patients because they offer a good plan for patients, are affordable, and show care for their customers. Meanwhile, providers with not many appointments may imply those providers don’t have good plans for patients, making it difficult for patients to make appointments.


9. Query 9 lists the insurance plan type and average deductable amount for each insurance plan.
<img width="1126" alt="Screenshot 2024-03-24 at 8 08 19 PM" src="https://github.com/rebekahbradbury/Group-8-MIST-4610-/assets/163002386/9280ddd7-f994-4dac-a2d3-290d5d002d01">

Explain: 
Being able to know the average deductible for each insurance plan type, the health clinic may help patients avoid potential barriers and conflicts due to their insurance plan. The clinic could look ahead to see the insurance the patients have and create the most affordable plan for the treatment they will receive. This information will also help the financial planning aspect of the clinic so they will be prepared for the amount that patients will be paying after insurance. It will also allow for the health clinic to provide insurance insight on which plan type the patient should choose that will be most beneficial for their treatments and medications.

10. Query 10 lists the name of patients and the date of the appointment for those who are receiving a type of drainage service.
<img width="1126" alt="Screenshot 2024-03-24 at 8 11 37 PM" src="https://github.com/rebekahbradbury/Group-8-MIST-4610-/assets/163002386/d7644f18-4e5d-4864-86fb-6cb79375d639">

Explain:
The health clinic may want to know the names and date of their patients appointments to ensure they are arriving on time and on the correct date. This would also ensure that there is enough staff on that day and that each patient is receiving the correct service, which in this case is a drainage service. Having access to this information also allows for staff specializing in a type of drainage service to know what days they have to go into the health clinic and who they are operating this service on. 





## Database Information:

Name of the database: ns_Sp24_47114_Group8

Additional Information: 
