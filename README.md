# Team-Ricola - *PharmacAI* 
## Team Members 👩🏽‍⚕️👩🏻‍⚕️👩🏻‍⚕️👨🏽‍⚕️

| Names  | Emails |
| ------------- | ------------- |
| Adrian Altermatt  | adrian.altermatt@students.fhnw.ch  |
| Jana Brzak  | jana.brzak@students.fhnw.ch  |
| Sarah Meyer  | sarah.meyer@students.fhnw.ch  |
| Shathvika Karunakaran  | shathvikashima.karunakaran@students.fhnw.ch  |

## Links 🔗
- Medication Stock API: https://deepnote.com/workspace/sarah-0641-c9908259-8add-4a78-8c29-a62d49bf7322/project/PharmacAI-46d040bc-851a-49ab-a8fb-23c965475dff/notebook/Notebook%202-73dce108c691468dbef96242504c074b?
- Chatbot: Voiceflow -> Version live on https://digibp.github.io/Team-Ricola/
- PharmacAI Accounting: Google Sheets https://docs.google.com/spreadsheets/d/1m85WdAdZekZGYzg_zqUK3-oxw_vHrMGVca3PIfGTiGI/edit#gid=0
- PharmacAI Invoice: Google Docs https://docs.google.com/document/d/1RQujRKo-LbhSIdR-f65h1rv7RCbUMfGgSWIspmm3TJ0/edit
- PharmacAI Google Calendar: https://calendar.google.com/calendar/u/0?cid=cGhhcm1hY2Fpcmljb2xhQGdtYWlsLmNvbQ
- PharmacAI Apps Script: https://script.google.com/u/0/home/projects/1oZgKnxqsioHXGj6jILQQhcJkjZK_xmdxESsNL-3TSOj9LsOHmKzSZcob/edit

## Coach
- Andreas Martin
- Charuta Panda

## Introduction
The drug and pharmacy system in Switzerland is similar to those in other countries, but with some differences. Medicinal products that promise to cure specific ailments can only be purchased in pharmacies or rarely in "Drogerien". The drugs are categorized based on whether they require a prescription or are available over-the-counter (OTC). Commonly used drugs for minor ailments such as headaches and coughs can be purchased without a prescription. However, prescription from a medical doctor is required for drugs like antibiotics, pain relievers with high dosage, and drugs used in treating cancer.

## Goal 🎯
Our aim in this project is to optimize and digitalize the process of obtaining medication. The tool should be user-friendly for patients and employees.

## Implementation
- Camunda
- Voiceflow
- Voiceglow
- Make
- Google Calender
- Google Forms
- Flask

## Current As-Is Process
<img width="1544" alt="image" src="https://github.com/DigiBP/Team-Ricola/assets/95039367/185a93d7-7b26-4224-b5c5-886421aaabe1">

1. **Customer Arrival:** The customer arrives at the pharmacy.

2. **Needs Assessment:**
- The assistent assesses the customer's needs.
- Decision as to whether the customer is coming for a medication or an appointment.

3. **Medication Decision Making:**
- If the customer is there for medication, it's decided whether they know which medication they need and whether they have a prescription.
- If the customer has a prescription, they are asked to present it.

4. **Prescription Verification:**
- If a prescription is required, this will be checked.

5. **Medication Preparation:**

- It is determined whether the medication is pre-packaged.
- If so, the medication is prepared.
- If the medication is not pre-packaged, it is prepared accordingly.

6. **Inventory Check:**

- It is checked whether the medication is in stock.
- If the medication is in stock, it is handed over to the customer after verification by a second person.
- If the medication is not in stock, it is ordered.

7. **Customer Notification:**

- The customer is informed about the necessity of a prescription if required.
- The customer is notified when the medication is ready for pickup or has arrived.


8. **Medication Dispensing:**

- If the medication is available and verified, it is dispensed to the customer.

9. **Appointment Scheduling:**
    
- If the customer desires an appointment, different services such as measurements, vaccinations, coronavirus tests, medication checks, contraception counseling, and ear piercing are reviewed.
- The customer selects the desired service, and an appointment is arranged based on their needs.

10. **Service Execution:**
    
- The selected service is then executed according to the arrangement.

___________

### Issues with the current As-Is Proces 🚩

**Waiting times:** Pharmacies can have long waiting times, especially at peak times. This can be inconvenient, especially if you need urgent medication.

**Limited opening hours:** Pharmacies often have limited opening hours, which means patients may have difficulty getting their medication outside of regular business hours or on weekends.

**Personal presence required:** To pick up medication, patients usually have to physically go to the pharmacy. This can be a challenge for people with limited mobility or chronic illnesses.

**Confidentiality and stigma:** Some patients may feel uncomfortable asking for or picking up prescription or sensitive medications at the pharmacy due to privacy concerns or stigma.

**Language barrier:** Several languages are spoken in Switzerland and this can lead to communication problems, especially if the pharmacist or staff do not speak the patient's native language.
___________

## To-Be Process
![image](https://github.com/DigiBP/Team-Ricola/assets/95039367/fddf1507-f256-41c8-b833-5b499452067a)

1. **Service Start:**
- The process begins when the customer interacts with the chatbot.

3. **Determining Service Type:**
- The chatbot determines whether the customer needs medication or an appointment.

4. **Consulting a Prescription:**
- If medication is required, the chatbot assesses whether a prescription is necessary.
- If a prescription is needed, the chatbot proceeds to check the prescription.

5. **Prescription Checking and Drug Preparation:**
- Upon confirmation of the prescription, the system prepares the drugs.
- If the prescription is not required, the system directly prepares the drugs.

6. **Inventory Management:**
- The system checks if the medication is in stock.
- If the stock is sufficient, the order continues.
- If the stock is insufficient, the system triggers a reorder flow, which includes reordering low stock, restocking, and updating the inventory.

7. **Appointment Handling:**
- If an appointment is needed, the chatbot helps to book the appointment.

8. **Order Verification and Packaging:**
- The system verifies the order.
- If the order is correct, the package is prepared for shipping.

9. **Invoice Preparation:**
- The system prepares an invoice for the customer.

10. **Order Completion:**
- The order is finalized, and the process concludes with the customer being notified that their order has been processed.

### Benefits ✔️

**Time-saving:** Ordering medication through the chatbot is quick and convenient, eliminating the need to visit a pharmacy in person and saving time. 

**24/7 availability:** The chatbot is accessible round the clock, making it particularly helpful for those who require medication outside regular business hours. Ease of use: With an intuitive user interface and clear instructions, the chatbot enhances the user experience and simplifies the ordering process. 

**Quick responses:** The chatbot can promptly answer queries, provide medication information, and offer recommendations, improving the overall customer experience. 

**Automated order processing:** By automating the ordering process, the chatbot minimizes human error and streamlines the purchasing process, making it more efficient. 

**Discretion:** The chatbot provides a private and discreet setting for people who prefer to discuss their health issues confidentially. 

**Scalability:** The chatbot can handle multiple user interactions simultaneously, making it more scalable than relying solely on human staff.

## Chatbot

<img width="1550" alt="image" src="https://github.com/DigiBP/Team-Ricola/assets/95039367/5099805b-4972-4559-a6ec-00e350b73b9d">

The flowchart outlines a structured process for a pharmacy or medical service to handle customer needs. It starts by assessing whether the customer knows the drug they need. If they do, the service can directly order the medication, or set up an appointment or teleconsult. In cases where over-the-counter medication is sufficient, patient data is collected, verified, and an invoice is sent, concluding the interaction. For prescription medications, symptoms are discussed, a drug is recommended, and upon confirmation, either an over-the-counter drug is provided or a prescription is requested, followed by data collection and invoicing.

For unknown drugs, the process involves checking the medication request, verifying patient identity, and then either confirming the drug recommendation or proceeding to prescription if necessary.

Separately, for appointments or teleconsults, a date is requested, and upon finding a suitable slot, it is confirmed. Types of appointments vary from general measurements to vaccinations, COVID testing, general health checks, prescription of birth control pills, ear piercing, or a prescription consultation. Each service pathway concludes with patient data collection, invoicing, and ends the conversation, ensuring a clear and efficient resolution to the customer's needs.

### Booking an Appointment through the Chatbot
<img width="965" alt="Bildschirmfoto 2023-11-23 um 18 35 30" src="https://github.com/DigiBP/Team-Ricola/assets/60508037/da76a44c-5e20-4f8d-966a-1cfea2e33845">

#### Objective:
To document the automated appointment scheduling system for pharmacAI, detailing the digitalized interaction between the patient and the chatbot, and the subsequent backend processes using Google's Free Busy API, Make, and Camunda.

#### Process Flow:

1. Patient-Chatbot Interaction: The patient starts the conversation with the chatbot by requesting to book an appointment.
2. Date Request and Retrieval: The patient is asked for his preferred appointment date. It then sends a POST request to Google's **Free Busy API** to check for available slots.
3. Time Slot Display and Selection: Voiceflow displays the list of available time slots to the customer, who then selects a suitable time slot for the appointment.
4. Appointment Objective Inquiry: The customer has a choice between the most common pharmacy inquiries (e.g. vaccination recommendations).
5. Customer Information Collection: The personal information for the booking of the appointment is gathered, which is necessary for the invoice generation.
6. Data Submission and Event Creation: This gathered data is sent to Make via a POST request, from where on the setting of an appointment is triggered (see also: Make Scenario 1).
7. Workflow Management with Camunda: Simultaneously, a POST request is sent to Camunda to initiate the appointment management workflow.
Camunda handles the necessary steps to ensure the appointment is held successfully (User Task: Hold Appointment) and triggers the invoice generation (Service Task: Prepare Invoice) after the appointment.

<img width="392" alt="Bildschirmfoto 2023-11-23 um 19 52 37" src="https://github.com/DigiBP/Team-Ricola/assets/60508037/76df3d0a-34d8-4ba8-af2e-9482cb7622d7">
<img width="396" alt="Bildschirmfoto 2023-11-23 um 19 52 21" src="https://github.com/DigiBP/Team-Ricola/assets/60508037/acb2b35c-eb8b-4e79-9383-870c0959f61b">

POST Request to the Google Free Busy API

## Make Scenarios
### Scenario 1: Invoice Generation
This workflow automates the process of capturing data from the chatbot via a webhook and directly inputting that data into a Google Sheets document, from which an invoice can be generated. 
- Webhook Trigger: This is the starting point of the workflow. We have set up a custom webhook that waits for a POST request that is sent from the chatbot. When the webhook receives the JSON data, it triggers the automation.
- Google Sheets Action: The processed data is then sent to the Google Sheets document "PharmacAI Accounting" (https://docs.google.com/spreadsheets/d/1m85WdAdZekZGYzg_zqUK3-oxw_vHrMGVca3PIfGTiGI/edit#gid=0). The workflow takes the data from the webhook and adds a new row to the Google Sheets document with the data mapped to the appropriate columns.
- Google Apps Script Execution: After the data is entered into Google Sheets, a Google Apps Script (https://script.google.com/u/0/home/projects/1oZgKnxqsioHXGj6jILQQhcJkjZK_xmdxESsNL-3TSOj9LsOHmKzSZcob/edit) is triggered via "On Changed" trigger action. . The script processes the data in the new Google Sheets row and fills out our Google Docs invoice template "PharmacAI Invoice" (https://docs.google.com/document/d/1RQujRKo-LbhSIdR-f65h1rv7RCbUMfGgSWIspmm3TJ0/edit). 
- Invoice Generation: The Google Docs invoice templates placeholers are populated with the data to produce a finished invoice.

## Scenario 2: Book an Appointment
This workflow automates the scheduling process, creating an appointment for the selected time slot from the chatbot in Google Calendar without manual intervention, ensuring a streamlined experience for both the users and the service providers.

- Webhook Trigger: The scenario is initiated by a custom webhook that's set up to listen for a POST request from the chatbot.
- Google Calendar Action: The details for the event (start date, end date, user name and user email) are mapped from the processed webhook data to the relevant fields in the Google Calendar event creation form.
- Appointment Booking: The event is then automatically added to our Google Calendar (https://calendar.google.com/calendar/u/0?cid=cGhhcm1hY2Fpcmljb2xhQGdtYWlsLmNvbQ), effectively booking an appointment. The event can include all the necessary details, such as date, time, participants, and any notes relevant to the appointment.

## Integration with Camunda
<img width="396" alt="Bildschirmfoto 2023-11-23 um 19 54 43" src="https://github.com/DigiBP/Team-Ricola/assets/60508037/39cca1e1-5da3-4afc-a0e0-d01d608bf6db">

Upon completion of the chatbot's protocol, a POST request is sent to the Camunda Engine where a process definition is already deployed. The POST request starts a new process instance and all variables from the chatbot are transmitted in the request body for further handling in Camunda. 

___________

### Scenario
Scenario 1: Ordering medication 💊

The patient goes to the doctor and receives a prescription for his medication. On the way home, the patient can order the medication by communicating with our chatbot. The pharmacy checks whether it has the medication in stock and checks it using the dual control principle, then packs it and delivers it to the patient accordingly. 
If the patient is not sure which medication he would like to get, he can consult with the chatbot, who makes suggestions for the patient's symptoms based on the information in its knowledge base. If the patient wishes to order the suggested medication, he can do so directly via bot. 

Scenario 2: Booking an appointment/ teleconsult 👩🏻‍⚕️👨🏽‍⚕️

When a patient decides to arrange an appointment with the pharmacy via the chatbot, he opens the chatbot and enters his preferred day and selects the appropriate time. When a suitable appointment is found, the patient can choose between a face-to-face or virtual appointment (teleconsult). Furthermore, the patient can select the type of appointment he wishes to conduct (taking measurements, vaccination consult, corona testing, mediCheck for drug interactions, birth control pill consult, piercing of the ears or prescription consult). The appointment is confirmed by sending an email to the pharmacy and patient, as well as making an appoinment in the Google Calendar of both PharmacAI and the customer. In case of teleconsult, this appointment includes a link to Google Meet, where the teleconsult will be held.

## Fully automated process

## Conclusion
Under the leadership of Andreas Martin and Charuta Panda, we have been working on the development of PharmacAI, an innovative system for optimizing and digitizing the medication procurement process in Switzerland. Our goal was to make the process more user-friendly and efficient for both patients and employees.

The current medication procurement process requires patients to visit pharmacies in person, which is often associated with long waiting times, limited opening hours and challenges in consultation. Additional issues such as confidentiality concerns, cost and language barriers further complicate the process.

To overcome these challenges, we plan introduced a fully automated system supported by a chatbot. This chatbot is available 24/7 and allows patients to order medication quickly, efficiently and discreetly. The main advantages of this system include time savings, constant availability, a simple user interface, quick responses, automated order processing and discretion.

The project envisages two main use cases: Firstly, ordering medication via the chatbot (either after consultation which medication to get from the chatbot or after having received a prescription from a doctor) and secondly, arranging an appointment or teleconsultation via chatbot. These innovations aim to revolutionize the medication procurement process in Switzerland by improving efficiency, accessibility and user experience.

In the future, it would be exciting to integrate personalized medication recommendations and detailed information about side effects and drug interactions. These innovations will not only increase patient safety, but also significantly improve the efficiency of the system.

![image](https://github.com/DigiBP/Team-Ricola/assets/95039367/89074b44-a79e-43e7-828e-0cb6210f4f96)

