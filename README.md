
# Team-Ricola - *PharmacAI* 
- [Team Members](#team-members-👩🏽‍⚕️👩🏻‍⚕️👩🏻‍⚕️👨🏽‍⚕️) 
- [How to run](#how-to-run) 
- [Coaching](#coaching) 
- [Introduction](#introduction) 
- [Technologies](#Technologies) 
- [As-Is Process](#as-is-process) 
- [To-Be Process](#to-be-process) 
- [Chatbot](#chatbot) 
- [Integration with Camunda](#integration-with-camunda) 
- [Make Scenarios](#make-scenarios) 
- [Customer Scenarios](#customer-scenarios) 
- [Medication Stock REST API](#medication-stock-rest-api) 
- [Conclusion](#conclusion)

## Team Members 👩🏽‍⚕️👩🏻‍⚕️👩🏻‍⚕️👨🏽‍⚕️

| Names  | Emails |
| ------------- | ------------- |
| Adrian Altermatt  | adrian.altermatt@students.fhnw.ch  |
| Jana Brzak  | jana.brzak@students.fhnw.ch  |
| Sarah Meyer  | sarah.meyer@students.fhnw.ch  |
| Shathvika Karunakaran  | shathvikashima.karunakaran@students.fhnw.ch  |

## How to run
1. Start [Medication Stock API Notebook 'Medication API'](https://deepnote.com/workspace/sarah-0641-c9908259-8add-4a78-8c29-a62d49bf7322/project/PharmacAI-46d040bc-851a-49ab-a8fb-23c965475dff/notebook/Notebook%202-73dce108c691468dbef96242504c074b?) (! Watch out, it sometimes stopps on its own!).
2. Open [Chatbot: Voiceflow](https://digibp.github.io/Team-Ricola/).
3. Depending on your interaction with the Chatbot user tasks are created in [Camunda](https://digibp.herokuapp.com/). (Username: sarahmeyer, Password: password)
4. Check the PharmacAI Google Docs, where the Invoice information is written in a [Google Sheets](https://docs.google.com/spreadsheets/d/1m85WdAdZekZGYzg_zqUK3-oxw_vHrMGVca3PIfGTiGI/edit#gid=0) and an [Invoice](https://docs.google.com/document/d/1RQujRKo-LbhSIdR-f65h1rv7RCbUMfGgSWIspmm3TJ0/edit) is automatically generated.

Google Account:
E-Mail: pharmacairicola@gmail.com
Password: PharmacAI_01

*Find all invoices in Google Drive.*

*The first medication order starts the reordering process because Amoxicillin is low on stock.*

### Links 🔗
- [Camunda](https://digibp.herokuapp.com/)
- [Medication Stock API](https://deepnote.com/workspace/sarah-0641-c9908259-8add-4a78-8c29-a62d49bf7322/project/PharmacAI-46d040bc-851a-49ab-a8fb-23c965475dff/notebook/Notebook%202-73dce108c691468dbef96242504c074b?)
- [Chatbot: Voiceflow](https://digibp.github.io/Team-Ricola/)
- [PharmacAI Accounting: Google Sheets](https://docs.google.com/spreadsheets/d/1m85WdAdZekZGYzg_zqUK3-oxw_vHrMGVca3PIfGTiGI/edit#gid=0)
- [PharmacAI Invoice: Google Docs](https://docs.google.com/document/d/1RQujRKo-LbhSIdR-f65h1rv7RCbUMfGgSWIspmm3TJ0/edit)
- [PharmacAI Google Calendar](https://calendar.google.com/calendar/u/0?cid=cGhhcm1hY2Fpcmljb2xhQGdtYWlsLmNvbQ)
- [PharmacAI Apps Script](https://script.google.com/u/0/home/projects/1oZgKnxqsioHXGj6jILQQhcJkjZK_xmdxESsNL-3TSOj9LsOHmKzSZcob/edit)

## Login - Information
- Make: E-mail sarah.meyer@students.fhnw.ch, Password PharmacAI_01
- Google Account: E-Mail pharmacairicola@gmail.com, Password PharmacAI_01
- Camunda: Username sarahmeyer, Password password

## Coaching
- Andreas Martin
- Charuta Pande

## Introduction
The drug and pharmacy system in Switzerland is similar to those in other countries, but with some differences. Medicinal products that promise to cure specific ailments can only be purchased in pharmacies or rarely in "Drogerien". The drugs are categorized based on whether they require a prescription or are available over-the-counter (OTC). Commonly used drugs for minor ailments such as headaches and coughs can be purchased without a prescription. However, prescription from a medical doctor is required for drugs like antibiotics, pain relievers with high dosage, and drugs used in treating cancer.

### Goal 🎯
Our aim in this project is to optimize and digitalize the process of obtaining medication. The tool should be user-friendly for patients and employees.

## As-Is Process
<img width="1544" alt="image" src="https://github.com/DigiBP/Team-Ricola/assets/60508037/eefdff95-c0d4-43d2-ad28-63252eec582d">


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

### Issues with the As-Is Proces 🚩

**Waiting times:** Pharmacies can have long waiting times, especially at peak times. This can be inconvenient, especially if you need urgent medication.

**Limited opening hours:** Pharmacies often have limited opening hours, which means patients may have difficulty getting their medication outside of regular business hours or on weekends.

**Personal presence required:** To pick up medication, patients usually have to physically go to the pharmacy. This can be a challenge for people with limited mobility or chronic illnesses.

**Confidentiality and stigma:** Some patients may feel uncomfortable asking for or picking up prescription or sensitive medications at the pharmacy due to privacy concerns or stigma.

**Language barrier:** Several languages are spoken in Switzerland and this can lead to communication problems, especially if the pharmacist or staff do not speak the patient's native language.
___________

## To-Be Process

<img width="1308" alt="image" src="https://github.com/DigiBP/Team-Ricola/assets/95039367/db3e3545-51f3-40d2-87b6-24508758cefb">



1. **Service Start:**
- The process begins when the customer interacts with the chatbot.

2. **Determining Service Type:**
- The chatbot determines whether the customer needs medication or an appointment.

3. **Consulting a Prescription:**
- If medication is required, the chatbot assesses whether a prescription is necessary.
- If a prescription is needed, the chatbot proceeds to check the prescription.

4. **Prescription Checking and Drug Preparation:**
- Upon confirmation of the prescription, the system prepares the drugs.
- If the prescription is not required, the system directly prepares the drugs.

5. **Inventory Management:**
- The system checks if the medication is in stock.
- If the stock is sufficient, the order continues.
- If the stock is insufficient, the system triggers a reorder flow, which includes reordering low stock, restocking, and updating the inventory.

6. **Appointment Handling:**
- If an appointment is needed, the chatbot helps to book the appointment.

7. **Order Verification and Packaging:**
- The system verifies the order.
- If the order is correct, the package is prepared for shipping.

8. **Invoice Preparation:**
- The system prepares an invoice for the customer.

9. **Order Completion:**
- The order is finalized, and the process concludes with the customer being notified that their order has been processed.

10. **Automatic Storage System:**
- This API facilitates monitoring low stock items, deducting sold medications, and restocking items in the pharmacy inventory through specific endpoints.

### Benefits ✔️

**Time-saving:** Ordering medication through the chatbot is quick and convenient, eliminating the need to visit a pharmacy in person and saving time. 

**24/7 availability:** The chatbot is accessible round the clock, making it particularly helpful for those who require medication outside regular business hours. Ease of use: With an intuitive user interface and clear instructions, the chatbot enhances the user experience and simplifies the ordering process. 

**Quick responses:** The chatbot can promptly answer queries, provide medication information, and offer recommendations, improving the overall customer experience. 

**Automated order processing:** By automating the ordering process, the chatbot minimizes human error and streamlines the purchasing process, making it more efficient. 

**Discretion:** The chatbot provides a private and discreet setting for people who prefer to discuss their health issues confidentially. 

**Scalability:** The chatbot can handle multiple user interactions simultaneously, making it more scalable than relying solely on human staff.

**Automatic reordering:** The API makes the reordering process automatic, can save time and give structure to this process.

## Technologies
- Camunda
- Voiceflow
- Voiceglow
- Make
- Google Calender
- Google Forms
- Google Apps Script
- Flask


## Chatbot

<img width="1439" alt="image" src="https://github.com/DigiBP/Team-Ricola/assets/95039367/6be5f733-4aef-424a-8e9a-76eee79aa58e">

The flowchart outlines a structured process for a pharmacy or medical service to handle customer needs. It starts by assessing whether the customer knows the drug they need. If they do, the service can directly order the medication, or set up an appointment or teleconsult. In cases where over-the-counter medication is sufficient, patient data is collected, verified, and an invoice is sent, concluding the interaction. For prescription medications, symptoms are discussed, a drug is recommended, and upon confirmation, either an over-the-counter drug is provided or a prescription is requested, followed by data collection and invoicing.

For unknown drugs, the process involves checking the medication request, verifying patient identity, and then either confirming the drug recommendation or proceeding to prescription if necessary.

Separately, for appointments or teleconsults, a date is requested, and upon finding a suitable slot, it is confirmed. Types of appointments vary from general measurements to vaccinations, COVID testing, general health checks, prescription of birth control pills, ear piercing, or a prescription consultation. Each service pathway concludes with patient data collection, invoicing, and ends the conversation, ensuring a clear and efficient resolution to the customer's needs.



### Knowledge Base
<img src="https://github.com/DigiBP/Team-Ricola/assets/60508037/36abee9b-4171-4201-b583-a7bf12359bf3" alt="alt text" width="30%">
<img src="https://github.com/DigiBP/Team-Ricola/assets/60508037/31c145f3-5de9-4aca-81e8-633e62dadc78" alt="alt text" width="29%">


#### Objective:
The knowledge base serves as a foundational resource for the chatbot and includes data on common symptoms, associated therapies, and details regarding the prescription status and pricing of medications. This base is structured to facilitate the efficient retrieval and dissemination of information, supporting the chatbot in delivering accurate and relevant responses to user inquiries.




### Booking an Appointment through the Chatbot 👩🏻‍⚕️👨🏽‍⚕️
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
7. Workflow Management with Camunda: The Voiceflow component POST to Camunda is called.
Camunda handles the necessary steps to ensure the appointment is held successfully (User Task: Hold Appointment) and triggers the invoice generation (Service Task: Prepare Invoice) after the appointment.



### Ordering Medication via Chatbot 💊
![Bildschirmfoto 2023-12-03 um 11 31 59](https://github.com/DigiBP/Team-Ricola/assets/60508037/89d80475-ba46-4cac-befd-c64bcd47b44e)


#### Objective:
To assist the customer in ordering medication and submit the order to Camunda for processing.

#### Process Flow:

1. Patient-Chatbot Interaction: The patient starts the conversation with the chatbot by requesting to order medication.
2. Medication Known: The customer is asked whether he knows, which medication he wishes to order.
3. Knowledge Base: If the user does not yet have a specific medication in mind, he is queried for his symptoms and the chatbot will suggest a medication for his symptoms.
4. Medication Confirmation: The user is asked to confirm the medication he wants to order.
5. Medication Price: The bot checks the price for the selected medication in its knowledge base and saves it in the variable price, which is later transmitted to Camunda and from there to Make for invoice processing.
6. Prescription Status: If the medication needs a prescription (which is determined in the knowledge base of the chatbot), the user is prompted to upload both the prescription and some form of identification (ID, passport or driver's licence).
7.  Workflow Management with Camunda: The Voiceflow component POST to Camunda is called.
   

![Bildschirmfoto 2023-12-03 um 11 38 20](https://github.com/DigiBP/Team-Ricola/assets/60508037/2dfef1b1-69d9-4620-b892-641314be7b3f)
File Upload System for Prescription Medication

___________

## Integration with Camunda

### Voiceflow Component "POST to Camunda"

<img src="https://github.com/DigiBP/Team-Ricola/assets/60508037/997f5d8c-53ca-4d4b-b797-08d4f50051ee" alt="alt text" width="50%">

#### Objective:
This Voiceflow component serves as the end-point for all pathways in the chatbot, gathers the customer's billing information sends all the gathered variables in a POST request to the Camunda API. By implementing it as a component, reusability of this subprocess was granted.

#### Process Flow:

1. Billing Information: The customer's full name, address and e-mail are collected and saved in variables.
2. Current Date: The current date is saved in a variable so the billing date and due date can later be calculated correctly.
3. POST Request to Camunda: A POST request is made to the URL "https://digibp.herokuapp.com/engine-rest/process-definition/key/Process_0g7objr/tenant-id/MI18/submit-form", which starts a new process instance of the already deployed process definition. All the necessary variables for the process are included in the body of the request. 
   
### Process Instance in Camunda
<img src="https://github.com/DigiBP/Team-Ricola/assets/60508037/c2c12ffa-d526-4892-84f4-f12bb8312472" alt="alt text" width="50%">

Once the process instance is started via POST request, it is displayed in the Camunda Engine with all the variables that were gathered in the conversation of the chatbot.
From here, the To-Be-Process is run. 


___________

## Make Scenarios
### Make Scenario 1: Invoice Generation
This workflow automates the process of capturing data from the chatbot via a webhook and directly inputting that data into a Google Sheets document, from which an invoice can be generated. 
- Webhook Trigger: This is the starting point of the workflow. We have set up a custom webhook that waits for a POST request that is sent from the chatbot. When the webhook receives the JSON data, it triggers the automation.
- Google Sheets Action: The processed data is then sent to the Google Sheets document [PharmacAI Accounting](https://docs.google.com/spreadsheets/d/1m85WdAdZekZGYzg_zqUK3-oxw_vHrMGVca3PIfGTiGI/edit#gid=0). The workflow takes the data from the webhook and adds a new row to the Google Sheets document with the data mapped to the appropriate columns.
- Google Apps Script Execution: After the data is entered into Google Sheets, a [Google Apps Script](https://script.google.com/u/0/home/projects/1oZgKnxqsioHXGj6jILQQhcJkjZK_xmdxESsNL-3TSOj9LsOHmKzSZcob/edit) is triggered via "On Changed" trigger action. . The script processes the data in the new Google Sheets row and fills out our Google Docs invoice template [PharmacAI Invoice](https://docs.google.com/document/d/1RQujRKo-LbhSIdR-f65h1rv7RCbUMfGgSWIspmm3TJ0/edit). 
- Invoice Generation: The Google Docs invoice templates placeholers are populated with the data to produce a finished invoice.

### Make Scenario 2: Book an Appointment
This workflow automates the scheduling process, creating an appointment for the selected time slot from the chatbot in Google Calendar without manual intervention, ensuring a streamlined experience for both the users and the service providers.

- Webhook Trigger: The scenario is initiated by a custom webhook that's set up to listen for a POST request from the chatbot.
- Google Calendar Action: The details for the event (start date, end date, user name and user email) are mapped from the processed webhook data to the relevant fields in the Google Calendar event creation form.
- Appointment Booking: The event is then automatically added to our [Google Calendar](https://calendar.google.com/calendar/u/0?cid=cGhhcm1hY2Fpcmljb2xhQGdtYWlsLmNvbQ), effectively booking an appointment. The event can include all the necessary details, such as date, time, participants, and any notes relevant to the appointment.


___________

## Customer Scenarios
Scenario 1: Ordering prescription medication 💊

The patient goes to the doctor and receives a prescription for his medication. On the way home, the patient can order the medication by communicating with our chatbot. The user has to upload his prescription and identification. The pharmacy then checks whether it has the medication in stock, deducts the medication package from the stock and checks it using the dual control principle, then packs it and delivers it to the patient accordingly. 
Video Link: [Prescription Medication Order](https://drive.google.com/file/d/1DLCgkwElCej7nbeA2HfAzzDQ3rzXbGkL/view?usp=drive_link)

Scenario 2: Medication Consult & Order 

The patient has fallen ill and wishes to order medication, but does not know which medication to get. The chatbot asks for the user's symptoms and checks for a fitting medication in his knowledge base and suggests it (only Over-The-Counter medication, as the customer would not have a prescription in this case). The patient can then confirm the medication or ask for another recommendation. Upon confirmation, a medication order can be placed directly via bot.
Video Link: [Medication Consult](https://drive.google.com/file/d/1jGsJAijKZFvoeLmTRvMVCVM9rXVAoX7L/view)

Scenario 3: Booking an appointment/ teleconsult 👩🏻‍⚕️👨🏽‍⚕️

When a patient decides to arrange an appointment with the pharmacy via the chatbot, he opens the chatbot and enters his preferred day and selects the appropriate time. When a suitable appointment is found, the patient can choose between a face-to-face or virtual appointment (teleconsult). Furthermore, the patient can select the type of appointment he wishes to conduct (taking measurements, vaccination consult, corona testing, mediCheck for drug interactions, birth control pill consult, piercing of the ears or prescription consult). The appointment is confirmed by sending an email to the pharmacy and patient, as well as making an appoinment in the Google Calendar of both PharmacAI and the customer. In case of teleconsult, this appointment includes a link to Google Meet, where the teleconsult will be held.
Video Link: [Appointment Booking](https://drive.google.com/file/d/1Qu6Tp09XltZ7QVgK8HluyKGdLfSfDgy7/view?usp=sharing)

___________
## Medication Stock REST API
This API facilitates monitoring low stock items, deducting sold medications, and restocking items in the pharmacy inventory through specific endpoints. The database operates on a simple CSV structure. Notably, changes made within the API aren't directly written to the CSV. Instead, for showcasing purposes, the stock resets upon API restarts. While in an optimal scenario, changes should reflect in the CSV, this method serves demonstration needs effectively.

When the API detects a low stock item, it initiates a reorder process. This action prompts the creation of a manual task in Camunda. Upon the arrival of the medication, personnel can restock the shelves and fill out a form in Camunda, specifying the restocked quantity. The submission of this form updates the running database without directly modifying the CSV file.

#### Routes:

##### 1. Order Low Stock Medication

-   **Route:** `/stock/order` (GET)
-   **Purpose:** Retrieves items low on stock and not yet ordered.
-   **Action:**
    -   Finds items with stock levels below a threshold (`stock_low_threshold`) and not marked as ordered.
    -   Marks these items as ordered (`'ordered'` column in CSV).
-   **Response:**
    -   If no items need reordering, it returns `{"reorder_started": False}`.
    -   If items are reordered, it returns `{"reorder_started": True}`.

##### 2. Deduct Medication Amount

-   **Route:** `/stock/<name>/deduct` (POST)
-   **Purpose:** Deducts sold medication amount from the stock.
-   **Action:**
    -   Takes the medication name from the URL and deducts the specified amount from the stock if available.
    -   If the medication doesn’t exist or the requested amount exceeds stock, it provides appropriate responses.
-   **Example Payload:**
	- ```{ "amount": 5 }```
	- This payload deducts 5 units of the specified medication.
-   **Response:**
    -   `"Success"` (with status code 200) if the deduction is successful.
    -   `"Not enough left"` if the requested amount exceeds available stock.
    -   `"Medication not tracked"` if the medication isn't in the system.

##### 3. Restock Medication

-   **Route:** `/stock/restock` (POST)
-   **Purpose:** Restocks medication in the inventory.
-   **Action:**
    -   Accepts a JSON payload containing medication names and their restock amounts.
    -   Increases the stock levels for specified medications and marks them as not ordered.
-   **Example Payload:**
	- ```{ "Aspirin": 10, "Ibuprofen": 20 }```
	- This payload indicates restocking 10 units of Aspirin and 20 units of Ibuprofen. Adjust the medication names and quantities as needed.
-   **Response:** `"Success"` (with status code 200) after successful restocking.

#### CSV Database Structure:

-   **Fields:** `id`, `name`, `stock`, `prescription_needed`, `ordered`.
-   `id`: Unique identifier for each medication.
-   `name`: Name of the medication.
-   `stock`: Current stock level.
-   `prescription_needed`: Indicates if a prescription is required.
-   `ordered`: Boolean indicating whether the medication has been ordered.

___________

## Conclusion
Under the leadership of Andreas Martin and Charuta Pande, we have been working on the development of PharmacAI, an innovative system for optimizing and digitizing the medication procurement process in Switzerland. Our goal was to make the process more user-friendly and efficient for both patients and employees.

The current medication procurement process requires patients to visit pharmacies in person, which is often associated with long waiting times, limited opening hours and challenges in consultation. Additional issues such as confidentiality concerns, cost and language barriers further complicate the process.

To overcome these challenges, we introduced a fully automated system supported by a chatbot. This chatbot is available 24/7 and allows patients to order medication quickly, efficiently and discreetly. The main advantages of this system include time savings, constant availability, a simple user interface, quick responses, automated order processing and discretion.

The project envisages two main use cases: Firstly, ordering medication via the chatbot (either after consultation which medication to get from the chatbot or after having received a prescription from a doctor) and secondly, arranging an appointment or teleconsultation via chatbot. These innovations aim to revolutionize the medication procurement process in Switzerland by improving efficiency, accessibility and user experience. The Workflow also automatically checks for items low on stock and reorders them if necessary to further make the pharmacists life easier. 

In the future, it would be exciting to integrate personalized medication recommendations and detailed information about side effects and drug interactions. These innovations will not only increase patient safety, but also significantly improve the efficiency of the system.

![image](https://github.com/DigiBP/Team-Ricola/assets/95039367/89074b44-a79e-43e7-828e-0cb6210f4f96)

## On a less serious note: 

We really put our chatbot through the wringer, here is a visual representation of the immense number of tokens - we even bought Voiceflow Pro - we invested to creating our chatbot, symbolizing the extensive effort and dedication invested in its development. 


<img width="50%" alt="image" src="https://github.com/DigiBP/Team-Ricola/assets/60508037/f0aa8c1c-4872-481c-b3ed-db9e2c4e0172">

![Bildschirmfoto 2023-12-06 um 19 58 05](https://github.com/DigiBP/Team-Ricola/assets/60508037/fe8332f8-87f6-4735-987e-c3f398833ac6)

