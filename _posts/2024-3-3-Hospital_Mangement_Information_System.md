---
layout: post
title: Hospital Mangement Information System
date: 2024-3-3 12:00 +0200
categories: [Outsystems]
tags: [database,sql]
---
## Building the Foundation for Efficiency: Unveiling the Database Model of My Hospital Management System:
- This model ensures the efficient storage and retrieval of critical data, like appointments, users, and their statuses. Let's delve deeper and explore how this model lays the groundwork for a more efficient hospital experience!

![Desktop View](/assets/img/posts/HMISDataModel.png)
 
### This database model lays the groundwork for a more efficient hospital experience in a few ways:

- Organized Data Storage: The model separates information into specific tables. This makes it easier to find and manage data compared to having everything stored in one big table. Imagine searching through a filing cabinet with everything piled together versus one with folders for different categories – that’s the difference this model offers.

- Reduced Redundancy: By separating information into tables, the model reduces the need to store the same data in multiple places. This helps to minimize errors and inconsistencies that can arise when information is duplicated.

- Standardized Data: The model uses lookup tables like “Appointment\AppointmentPriority” and “Appointment\AppointmentStatus”. These ensure that all appointments use consistent labels for things like priority and status. This standardization makes it easier to understand and filter data for reports and analysis.

- Relationships Between Data: The model allows you to link data across tables. For example, an appointment can be linked to a specific patient and can have one priority and one status. This makes it possible to retrieve all the relevant information about an appointment quickly and easily.

Overall, this database model provides a solid foundation for an efficient hospital management system. By  organizing data effectively, reducing redundancy,  standardizing data, and  facilitating relationships between data, the model helps streamline  administrative tasks and frees up  staff time to focus on what matters most – patient care.

- This Flowchart is describe the login client action that happen when the user click on login button 
![Desktop View](/assets/img/posts/Login.png)

#### In Switch apper Four of condition that check user role to get in has page, and i use 4 function to set this condition lets explain this functions :  
##### HR Check Role Function
![Desktop View](/assets/img/posts/Hr.png)
 - I write in Javascript object:
 ```javasript
 $parameters.IsHR = $public.Security.checkIfCurrentUserHasRole($roles.HR);
 ```
##### Code Explation: 
1. Assigning a Value to a Parameter:

- The code first assigns a value to a parameter named $parameters.IsHR.
- This suggests that $parameters is likely a collection of variables or settings used within the application.

2. Checking User Role:

- The value being assigned comes from a function call: $public.Security.checkIfCurrentUserHasRole($roles.HR).
This function appears to check the current user's role within a security framework.
- It likely returns a Boolean value (either true or false) indicating whether the user has a specific role.

3. Targeting the HR Role:

- The function is specifically checking for the "HR" role, as indicated by $roles.HR.
- It's reasonable to assume that $roles is a dictionary or object containing available roles within the system.

4. Action Based on Role:

- The outcome of the function call (whether the user has the HR role or not) will be stored in the $parameters.IsHR variable.
- This variable can then be used to control subsequent actions or visibility of features within the application. 

##### Doctor Check Role Function
![Desktop View](/assets/img/posts/Staff.png)
 - I write in Javascript object:
 ```javasript
$parameters.IsStaff =  $public.Security.checkIfCurrentUserHasRole($roles.Staff)
 ```
##### Code Explation: 
1. Assigning a Value to a Parameter:

- The code first assigns a value to a parameter named $parameters.IsStaff.
- This suggests that $parameters is likely a collection of variables or settings used within the application.

2. Checking User Role:

- The value being assigned comes from a function call: $public.Security.checkIfCurrentUserHasRole($roles.Staff).
This function appears to check the current user's role within a security framework.
- It likely returns a Boolean value (either true or false) indicating whether the user has a specific role.

3. Targeting the Staff Role:

- The function is specifically checking for the "Staff" role, as indicated by $roles.Staff.
- It's reasonable to assume that $roles is a dictionary or object containing available roles within the system.

4. Action Based on Role:

- The outcome of the function call (whether the user has the HR role or not) will be stored in the $parameters.IsStaff variable.
- This variable can then be used to control subsequent actions or visibility of features within the application.

##### Doctor Check Role Function
![Desktop View](/assets/img/posts/Doctor.png)
 - I write in Javascript object:
 ```javasript
$parameters.IsDr = $public.Security.checkIfCurrentUserHasRole($roles.Doctor)
 ```
##### Code Explation: 
1. Assigning a Value to a Parameter:

- The code first assigns a value to a parameter named $parameters.IsDr.
- This suggests that $parameters is likely a collection of variables or settings used within the application.

2. Checking User Role:

- The value being assigned comes from a function call: $public.Security.checkIfCurrentUserHasRole($roles.Doctor).
This function appears to check the current user's role within a security framework.
- It likely returns a Boolean value (either true or false) indicating whether the user has a specific role.

3. Targeting the Doctor Role:

- The function is specifically checking for the "Doctor" role, as indicated by $roles.Doctor.
- It's reasonable to assume that $roles is a dictionary or object containing available roles within the system.

4. Action Based on Role:

- The outcome of the function call (whether the user has the HR role or not) will be stored in the $parameters.IsDr variable.
- This variable can then be used to control subsequent actions or visibility of features within the application.

##### Patient Check Role Function
![Desktop View](/assets/img/posts/Patient.png)
 - I write in Javascript object:
 ```javasript
$parameters.IsPA = $public.Security.checkIfCurrentUserHasRole($roles.Patient)
 ```
##### Code Explation: 
1. Assigning a Value to a Parameter:

- The code first assigns a value to a parameter named $parameters.IsPA.
- This suggests that $parameters is likely a collection of variables or settings used within the application.

2. Checking User Role:

- The value being assigned comes from a function call: $public.Security.checkIfCurrentUserHasRole($roles.Patient).
This function appears to check the current user's role within a security framework.
- It likely returns a Boolean value (either true or false) indicating whether the user has a specific role.

3. Targeting the Patient Role:

- The function is specifically checking for the "Patient" role, as indicated by $roles.Patient.
- It's reasonable to assume that $roles is a dictionary or object containing available roles within the system.

4. Action Based on Role:

- The outcome of the function call (whether the user has the HR role or not) will be stored in the $parameters.IsPA variable.
- This variable can then be used to control subsequent actions or visibility of features within the application.
## Explation of UI
##### Human Resoures DashBoard
![Desktop View](/assets/img/posts/Hrboard.png)

- HR Portal: The process begins within the "HR Portal." This suggests that HR personnel have exclusive access to initiate account creation for doctors and staff.

- Selection Screen: Within the HR Portal, HR personnel are presented with a choice: "Show Doctor Information" or "Show Staff Information." This allows them to specify the type of account they want to create or manage.

- Doctor Management: Choosing "Show Doctor Information" likely leads to a screen displaying existing doctor information or a form for entering new doctor details. Here, HR personnel can add new doctors to the system, possibly including essential details like name, qualifications, and credentials.

- Staff Management (Optional): Similarly, choosing "Show Staff Information" could lead to a screen displaying existing staff information or a separate form for creating new staff accounts. This suggests that doctors and staff might be managed differently within the HMIS.

- Account Creation: In both scenarios (doctor or staff), there's likely an option to create a new account. This could involve filling out additional details or assigning access permissions relevant to the chosen role (doctor or staff).

##### Staff DashBoard
![Desktop View](/assets/img/posts/Staffboard.png)

- Staff Portal: The process starts within the "Staff Portal," indicating that staff members have access to view and manage patient information, appointments, and potentially create new patient accounts.

- Patient Information & Appointments: Upon logging into the staff portal, staff likely see an overview screen displaying existing patient information and their corresponding appointments. This consolidated view allows staff to efficiently access relevant patient data.

- Create Checkup (Optional): A button labeled "Create Checkup" suggests staff can initiate the creation of a new checkup appointment. This likely leads to a separate screen for scheduling.

- Checkup Creation Screen (Optional): Within the "Create Checkup" screen, staff can choose the following:
- - Patient Name: Select a patient from a list or search for a specific one.
- - Checkup Date & Time: Choose the date and time for the scheduled appointment.
- - Assign Doctor: Select a doctor from a list to assign them to the checkup. This functionality allows staff to manage doctor workload and patient-doctor matching.

##### Doctor DashBoard
![Desktop View](/assets/img/posts/DrBoard.png)
- Doctor Portal : This screen is home page for doctor and he can move into the DrAppoiment screen 

- DrAppoiment : In this Screen there is the table that appear the Appiment that staff assign it to the doctor

##### Patient DashBoard
![Desktop View](/assets/img/posts/PaitentBoard.png)
- Paitent Portal : This screen show the detail of appoiment that staff get it for paitent
