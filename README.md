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
## Current As-Is Process
<img width="1230" alt="image" src="https://github.com/DigiBP/Team-Ricola/assets/95039367/4d7c3c1b-e0b5-402d-9ba0-2036071f754c">

#### Description for the Use Case when the patient knows what kind of drug he needs and has a prescription for it 
Upon visiting the pharmacy, the pharmaceutical assistant inquires about the patient's needs. If the patient is aware of the required medication, the assistant requests a prescription for verification. Once the specialist's prescription is validated, the assistant prepares the medication, ensuring it is properly packaged. Depending on circumstances, further verification by the specialist may occur. Following this, the medication is dispensed to the patient.

#### Despription for the Use Case when the patient knows what kind of drug he needs but does not have a prescription
When visiting the pharmacy, the pharmaceutical assistant enquires about the patient's needs. If the patient knows what medication they need, the assistant asks for a prescription that they can check. If the patient needs a prescription, the pharmaceutical assistant must tell the patient to bring it with them on their next visit. 
The pharmaceutical assistant prepares the medication and ensures that it is properly packaged.  The medication is checked by the specialist before it is dispensed to the patient. If the medication is not in stock, the pharmacy will order the medication and notify the patient when the medication arrives. 

#### Despription for the Use Case when the patient does not know what kind of drug he needs
When visiting the pharmacy, the pharmaceutical assistant enquires about the patient's needs. If the patient does not know which medication they need, the pharmaceutical assistant asks about the symptoms. Depending on the symptoms, she checks whether the medication is available without a prescription or whether it requires a visit to the doctor. If it is over-the-counter, the pharmacy assistant prepares the medication and ensures that it is properly packaged.  The medication is checked by the specialist before the medication is dispensed to the patient. If the medication is not in stock, the pharmacy orders the medication and notifies the patient when the medication arrives. 

#### Despcription for the Use Case when the patient needs a prescrption for the drug 
When visiting the pharmacy, the pharmaceutical assistant enquires about the patient's needs. If the patient does not know which medication they need, the pharmaceutical assistant asks about the symptoms. Depending on the symptoms, she checks whether the medication is available without a prescription or whether it requires a visit to the doctor. If it requires a prescription, the pharmacy assistant advises the patient to go to their GP. 

___________

### Issues with the current As-Is Proces 🚩
**Waiting times:** Pharmacies can have long waiting times, especially at peak times. This can be inconvenient, especially if you need urgent medication.

**Limited opening hours:** Pharmacies often have limited opening hours, which means patients may have difficulty getting their medication outside of regular business hours or on weekends.

**Personal presence required:** To pick up medication, patients usually have to physically go to the pharmacy. This can be a challenge for people with limited mobility or chronic illnesses.

**Confidentiality and stigma:** Some patients may feel uncomfortable asking for or picking up prescription or sensitive medications at the pharmacy due to privacy concerns or stigma.

**Medication errors:** Although pharmacies strive to avoid medication dispensing errors, occasionally errors in dosing, medication selection or labeling can occur.

**Limited consultation:** In busy pharmacies, the time pharmacists have available for consultation may be limited. This can lead to patients not being adequately informed about the correct use and side effects of their medication.

**Cost:** Prices for medications can vary in different pharmacies and some medications can be expensive, especially if they are not covered by health insurance.

**Language barrier:** Several languages are spoken in Switzerland and this can lead to communication problems, especially if the pharmacist or staff do not speak the patient's native language.
___________

## To-Be Process
<img width="539" alt="image" src="https://github.com/DigiBP/Team-Ricola/assets/95039367/bb5adcf1-55fe-43b4-9e1b-4a0608e35785">


### Benefits ✔️

**Time-saving:** Ordering medication through the chatbot is quick and convenient, eliminating the need to visit a pharmacy in person and saving time. 

**24/7 availability:** The chatbot is accessible round the clock, making it particularly helpful for those who require medication outside regular business hours. Ease of use: With an intuitive user interface and clear instructions, the chatbot enhances the user experience and simplifies the ordering process. 

**Quick responses:** The chatbot can promptly answer queries, provide medication information, and offer recommendations, improving the overall customer experience. 

**Automated order processing:** By automating the ordering process, the chatbot minimizes human error and streamlines the purchasing process, making it more efficient. 

**Discretion:** The chatbot provides a private and discreet setting for people who prefer to discuss their health issues confidentially. 

**Personalized recommendations:** By analyzing previous orders, the chatbot can make personalized medication recommendations, enhancing customer satisfaction. 

**Information on side effects and interactions:** The chatbot can provide information on medication side effects and drug interactions to ensure customer safety. 

**Scalability:** The chatbot can handle multiple user interactions simultaneously, making it more scalable than relying solely on human staff.

___________

### Scenario
Scenario 1: Ordering medication 💊
The patient goes to the doctor and receives a prescription for his medication. On the way home, the patient can order the medication by communicating with our chatbot. The pharmacy checks whether it has the medication in stock and checks it using the dual control principle, then packs it and delivers it to the patient accordingly. 

Scenario 2: Booking an appointment/ teleconsult 👩🏻‍⚕️👨🏽‍⚕️
The patient is not feeling well and decides to arrange an appointment with the pharmacy via the chatbot. To do this, he opens the chatbot and enters his available day and selects the appropriate time. When a suitable appointment is found, the patient can choose between a face-to-face or virtual appointment (teleconsult). The appointment is confirmed by sending an email to the pharmacy and patient.

## Fully automated process

## Conclusion
