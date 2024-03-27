# Group 8 MIST 4610 Group Project 1

## Team Name:
47114 Group 8

## Team Members:
1. Eryn Williams [@erynwilliams](https://github.com/erynwilliams)
3. Jenny Gentry [@jmg15190](https://github.com/jmg15190)
4. Ariana Gonzalez [@ag45846](https://github.com/ag45846)
5. Josh James [@joshanttt](https://github.com/joshanttt)
6. Jose Medrano [[@josemedjr](https://github.com/josemedjr)](https://github.com/josemedjr/MIST4610GroupProject1)
7. Rebekah Bradbury [@rebekahbradbury](https://github.com/rebekahbradbury)

## Problem Description 
As a group, we were tasked with building a relational database for the various entities within an emergency health-care clinic. At the clinic, patients can receive various types of medical services and are treated by professionals. Our model aims to visual portray the relationships present between the various entities of a health-care clinic. Our goal is to populate sample data and possible queries that may serve as an asset to the clinic, helping to store and analyze needed data. Our hope is that the model will improve day-to-day functions and overall efficiency for the clinic. 




## Data Model:
Data Model Description: 

Our data model is based on the services of a health-care clinic. First off, our clinic services patients, within this entity, patients are identified by a unique patient id. In addition, other attributes about patients include, patient name, date of birth, gender, contact information and medical history. Meds are available at this clinic, identified by their medID.  As there are many patients seen at the clinic, many meds are available as well, the entities Patients and Meds share a many-to-many relationship with their associative entity being Prescriptions. Prescriptions capture the relationship of which patients are prescribed which medications. Each patient can have multiple prescriptions and each medication can be prescribed to multiple patients. Prescriptions are identified by PrescripID.
 
 The MedStaff table shares a one to many relationship with the Prescriptions table. This means that Medical Staff members can write many different prescriptions, but each prescription is only written by one staff member. The MedStaff table is composed of medStaffID, serving as the unique identifier, followed by attributes: name, position, and contact. Position being the title they hold (Doctor, NP, Nurse, CRNA). In addition, MedStaff shares a many-to-many relationship with Patients, their associative entity being Appointments. Appointments capture the relationship of which patients are seen by which medical staff at specific times. Each patient can have multiple appointments with different medical staff members and each medical staff member can have multiple appointments with different patients. The Appointments table is identified by a specific apptID, unique to each individual appointment. The entity MedRecord is used to record medical information from an appointment and shares a one-to-one relationship with appointments, meaning that there is one medical record associated with each appointment. The Billing table also shares a one-to-one relationship with Appointments meaning for each appointment, there is one bill. Billing also shares a many-to-many relationship with Insurance, with the associative entity being InsuranceBilled. InsuranceBilled captures the relationship of which billing entries are associated with which insurance policies. This relationship demonstrates that each billing entry can be associated with multiple insurance policies and each insurance policy can be associated with multiple billing entries. 
 
  The entity, Insurance,  is used to record insurances accepted by the clinic,  table is identified by a unique providerID which is the specific insurance provider code. Insurance shares a many-to-many relationship with Patient, the associative entity being InsurancetType. The associative entity Insurance Type captures the relationship of which patients are associated with what insurance policies and the specific type of insurance for each patient. The relationship shows that each patient can have different insurance policies, and each insurance provider can offer many different insurance plans/options. Lastly is the Service table, used to define the type of service performed at an appointment. Service shares a many-to-many relationship with appointments, connected through the associative entity, AssignedService. AssignedService defines the relationship between which service is being performed at a specific appointment. Assigned service is identified by a unique assignmentID. Overall, this relationship demonstrates that for each appointment many services are available to perform, and many services can be assigned to appointments. 


![image](https://github.com/rebekahbradbury/Group-8-MIST-4610-/assets/163002826/44f8c974-1818-4438-ac5d-a74eccfd5213)
#

## Data Dictionary: 
<img width="695" alt="Screenshot 2024-03-27 at 10 13 38 AM" src="https://github.com/rebekahbradbury/Group-8-MIST-4610-/assets/163002386/3f1561ac-14f2-4133-8e38-3ec8f7f3178a">

<img width="671" alt="Screenshot 2024-03-27 at 10 13 58 AM" src="https://github.com/rebekahbradbury/Group-8-MIST-4610-/assets/163002386/5579f892-6350-4f2d-b126-c0ce8b04a5e7">

<img width="668" alt="Screenshot 2024-03-27 at 10 14 18 AM" src="https://github.com/rebekahbradbury/Group-8-MIST-4610-/assets/163002386/ddd43dee-45f0-4c25-b5b5-ed7923e3df5c">

<img width="671" alt="Screenshot 2024-03-27 at 10 14 40 AM" src="https://github.com/rebekahbradbury/Group-8-MIST-4610-/assets/163002386/6bfd847f-caa7-470e-a067-1ac7065e8dfb">

<img width="667" alt="Screenshot 2024-03-27 at 10 14 56 AM" src="https://github.com/rebekahbradbury/Group-8-MIST-4610-/assets/163002386/3fa6b8f0-6602-43a1-b7d7-4c2ae5648f14">

<img width="678" alt="Screenshot 2024-03-27 at 10 15 21 AM" src="https://github.com/rebekahbradbury/Group-8-MIST-4610-/assets/163002386/9423da04-00ef-4c6f-9f2f-44552e9aae07">

<img width="669" alt="Screenshot 2024-03-27 at 10 15 36 AM" src="https://github.com/rebekahbradbury/Group-8-MIST-4610-/assets/163002386/664f64d7-d123-48c0-be85-eddf83a574ee">

<img width="644" alt="Screenshot 2024-03-27 at 10 16 02 AM" src="https://github.com/rebekahbradbury/Group-8-MIST-4610-/assets/163002386/f9929e77-cff4-4f2d-a304-fec4b90564b1">

<img width="644" alt="Screenshot 2024-03-27 at 10 17 59 AM" src="https://github.com/rebekahbradbury/Group-8-MIST-4610-/assets/163002386/73ead041-fb33-484c-98c9-ffb72c229cd6">

<img width="639" alt="Screenshot 2024-03-27 at 10 18 15 AM" src="https://github.com/rebekahbradbury/Group-8-MIST-4610-/assets/163002386/564df81b-0230-48ff-96fc-526a53712d86">

<img width="655" alt="Screenshot 2024-03-27 at 10 18 28 AM" src="https://github.com/rebekahbradbury/Group-8-MIST-4610-/assets/163002386/1a332faf-b175-4b78-95b8-eb97ea280da1">

<img width="641" alt="Screenshot 2024-03-27 at 10 18 40 AM" src="https://github.com/rebekahbradbury/Group-8-MIST-4610-/assets/163002386/afb63edf-95b6-421a-bb97-173cfd0ea3b8">




## Queries:
<img width="620" alt="Screenshot 2024-03-27 at 10 12 05 AM" src="https://github.com/rebekahbradbury/Group-8-MIST-4610-/assets/163002386/0372da59-7fee-4506-8d7b-7686a94f5ab5">


#
 

1. Query 1 lists the ID's and names of Medical Staff who have treated more than 2 patients.
![image](https://github.com/rebekahbradbury/Group-8-MIST-4610-/assets/163002826/77d536df-5ef5-4bec-870d-3e55a090341b)


Explain: This query allows the clinic to decipher which medical staff have serviced more than 2 patients, informing them on how many patients each member of the medical staff are attending to over a period of time. Being able to track medical staff and how many patients they are seeing is essential in an emergency health clinic for organizational and efficiency purposes. 
#
 
2. Query 2 lists the top 10 most frequently used medications by their names and the number of patients currently taking the medicine in descending order

![image](https://github.com/rebekahbradbury/Group-8-MIST-4610-/assets/163002826/ad4380c3-17f4-4ee3-b40a-7a18711fbc5b)


Explain: This query generates the number of patients currently using one of the top 10 medications provided by the clinic. Identifying the most used medications can help the clinic track which medications they may need to order soon or on a more frequent basis. 
# 

3. Query 3 lists the names of patients with a balance due on their account and the amount due.
![image](https://github.com/rebekahbradbury/Group-8-MIST-4610-/assets/163002826/cd49663f-71ed-49e8-8854-746ee94c3816)


Explain: This query generates the names of patients who have an "unpaid" status listed on their account and the amount they owe. This information is important because it notifies the clinic of which patients they need to contact about paying outstanding bills. It is also important for insurance purposes, as many patients may use co-pay or may change insurances and be unaware that certain charges may not be covered based on their plans. Lastly, if bills are not eventually paid, the clinic will need this information to report the outstanding bill to collections. 
#

4. Query 4 lists the names of medical staff who are doctors 
![image](https://github.com/rebekahbradbury/Group-8-MIST-4610-/assets/163002826/cdba9b5a-0f7d-4cdf-b0eb-b0ba6de279e1)


Explain: For an emergency health clinic, it's crucial to quickly identify which doctors are available to provide immediate care. Knowing the names and availability of all doctors enables clinic staff to respond promptly to emergency situations.
#

5. Query 5 lists the average deductible of female patients whose insurance plan type begins with T
![image](https://github.com/rebekahbradbury/Group-8-MIST-4610-/assets/163002826/2573458f-6aaa-45b5-bec7-176a6e59de99)


Explain: The health clinic might need to use this query to assess the financial burden on female patients with specific insurance plans. Understanding the average deductible for a certain demographic can aid in financial planning, resource allocation, and more to ensure fair access to healthcare services for female patients with particular insurance plans. Such insights can inform decision-making processes aimed at enhancing the overall patient experience and ensuring that healthcare remains accessible and affordable for all.
#

6. Query 6 lists the medicine name and the percentage of patients who are taking a med with a dosage less than 100mg
![image](https://github.com/rebekahbradbury/Group-8-MIST-4610-/assets/163002826/920881a2-8531-4c1c-943e-4fb1b2ecdc9b)


Explain: Understanding which medications patients are using allows the clinic to monitor the effectiveness of treatments. If a significant percentage of patients are taking a particular medication but not showing improvement, it may indicate that the treatment protocol needs adjustment.
#

7. Query 7 lists the patient name and their amount of insurance billed that is greater than the average amount of insurance billed to all patients.
   
![image](https://github.com/rebekahbradbury/Group-8-MIST-4610-/assets/163002826/3d9edd6a-116a-4bd4-9a6d-7b16d5ea19f4)


Explain: The health clinic may want to know the patients who have paid more than the average for all patients can help ensure quality care and identify bill errors or fraud. Being able to identify patients who pay more than the average amount allows the health clinic to conduct quality checks with surveys to ask the patients if they are satisfied with the service and bill they were provided. Also, this allows the health clinic to check for any potential fraud errors to discover the reason why these patients are being billed more than average
#

8. Query 8 lists the number of appointments attended by patients under each insurance provider.
![image](https://github.com/rebekahbradbury/Group-8-MIST-4610-/assets/163002826/af4b269f-4852-4b94-8606-ab96dac5ef5a)



Explain:
Health clinics may want to know the number of appointments attended by patients based on insurance providers to determine which insurance providers are best and which ones may be the worst. Many appointments with the same provider may imply that that specific insurance provider may be best for patients because they offer a good plan for patients, are affordable, and show care for their customers. Meanwhile, providers with not many appointments may imply those providers don’t have good plans for patients, making it difficult for patients to make appointments.
#

9. Query 9 lists the insurance plan type and average deductable amount for each insurance plan.
![image](https://github.com/rebekahbradbury/Group-8-MIST-4610-/assets/163002826/480b6c7f-748c-454f-9130-30e7bcf8caf4)


Explain: 
Being able to know the average deductible for each insurance plan type, the health clinic may help patients avoid potential barriers and conflicts due to their insurance plan. The clinic could look ahead to see the insurance the patients have and create the most affordable plan for the treatment they will receive. This information will also help the financial planning aspect of the clinic so they will be prepared for the amount that patients will be paying after insurance. It will also allow for the health clinic to provide insurance insight on which plan type the patient should choose that will be most beneficial for their treatments and medications.
#

10. Query 10 lists the name of patients and the date of the appointment for those who are receiving a type of drainage service.

![image](https://github.com/rebekahbradbury/Group-8-MIST-4610-/assets/163002826/025a4220-0d8a-414f-8dc7-5e24f8e49c7c)


Explain:
The health clinic may want to know the names and date of their patients appointments to ensure they are arriving on time and on the correct date. This would also ensure that there is enough staff on that day and that each patient is receiving the correct service, which in this case is a drainage service. Having access to this information also allows for staff specializing in a type of drainage service to know what days they have to go into the health clinic and who they are operating this service on. 
#




## Database Information:

Name of the database: ns_Sp24_47114_Group8

Additional Information: 
