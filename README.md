# Team-Ricola - *PharmacAI* 
## Team Members 👩🏽‍⚕️👩🏻‍⚕️👩🏻‍⚕️👨🏽‍⚕️

| Names  | Emails |
| ------------- | ------------- |
| Adrian Altermatt  | adrian.altermatt@students.fhnw.ch  |
| Jana Brzak  | jana.brzak@students.fhnw.ch  |
| Sarah Meyer  | sarah.meyer@students.fhnw.ch  |
| Shathvika Karunakaran  | shathvikashima.karunakaran@students.fhnw.ch  |

## Links 🔗
- API: https://deepnote.com/workspace/sarah-0641-c9908259-8add-4a78-8c29-a62d49bf7322/project/PharmacAI-46d040bc-851a-49ab-a8fb-23c965475dff/notebook/Notebook%201-54d9685dbc4145cdbc87804d1ff98b8b? (Version Sarah 11.11.)
- Chatbot: Voiceflow

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
<img width="1230" alt="image" src="https://github.com/DigiBP/Team-Ricola/assets/95039367/4d7c3c1b-e0b5-402d-9ba0-2036071f754c">

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

___________

### Scenario
Scenario 1: Ordering medication 💊

The patient goes to the doctor and receives a prescription for his medication. On the way home, the patient can order the medication by communicating with our chatbot. The pharmacy checks whether it has the medication in stock and checks it using the dual control principle, then packs it and delivers it to the patient accordingly. 

Scenario 2: Booking an appointment/ teleconsult 👩🏻‍⚕️👨🏽‍⚕️

The patient is not feeling well and decides to arrange an appointment with the pharmacy via the chatbot. To do this, he opens the chatbot and enters his available day and selects the appropriate time. When a suitable appointment is found, the patient can choose between a face-to-face or virtual appointment (teleconsult). The appointment is confirmed by sending an email to the pharmacy and patient.

## Fully automated process

## Conclusion
Under the leadership of Andreas Martin and Charuta Panda, we have been working on the development of PharmacAI, an innovative system for optimizing and digitizing the medication procurement process in Switzerland. Our goal was to make the process more user-friendly and efficient for both patients and employees.

The current medication procurement process requires patients to visit pharmacies in person, which is often associated with long waiting times, limited opening hours and challenges in consultation. Additional issues such as confidentiality concerns, cost and language barriers further complicate the process.

To overcome these challenges, we plan to introduce a fully automated system supported by a chatbot. This chatbot will be available 24/7 and will allow patients to order medication quickly, efficiently and discreetly. The main advantages of this system include time savings, constant availability, a simple user interface, quick responses, automated order processing and discretion.

The project envisages two main use cases: Firstly, ordering medication via the chatbot after receiving a prescription and secondly, arranging an appointment or teleconsultation via the chatbot. These innovations aim to revolutionize the medication procurement process in Switzerland by improving efficiency, accessibility and user experience.

In the future, it would be exciting to integrate personalized medication recommendations and detailed information about side effects and drug interactions. These innovations will not only increase patient safety, but also significantly improve the efficiency of the system.

![image](https://github.com/DigiBP/Team-Ricola/assets/95039367/89074b44-a79e-43e7-828e-0cb6210f4f96)

