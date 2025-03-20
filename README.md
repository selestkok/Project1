# MIST 4610 Group Project 1: Team 1

## Team Members
1. Emily Jackson [@edj69332](https://github.com/edj69332)
3. Parker Jackson [@jcp39649](https://github.com/jcp39649)
4. Selest Kok [@selestkok](https://github.com/selestkok)
5. Paola Diaz [@paoladiaz1](https://github.com/paoladiaz1)
6. Lukas Farris [@Lafarris824](https://github.com/Lafarris824)

## Scenario Description
Our team was tasked with modeling and building a relational database that represents the operations and management of a pet shelter organization. The central entity in this model is the Pets entity, which keeps track of animals available for adoption, their species, breeds, medical history, and shelter location. The organization operates multiple locations, each of which manages its own inventory and staff. The shelters facilitate the care of animals by employing various staff members who help maintain the well-being of the pets and ensure they are matched with suitable adopters. A key part of this system is the adoption process, where potential adopters apply to adopt pets, and their details are stored for record-keeping. We aim to accurately model the relationship among these entities, generate sample data, and populate the database with realistic information. Furthermore, we will execute queries on this data to gain valuable insights about the shelter’s operations. 

## Data Model + Explanation
<img width="972" alt="AGV_vUdnPxkjxGlE1blPXQi7eTtysyPK_Zh-PFpIQXBgEIKy3AI6SY1skOSH4JL9tKiv1BHbU2g-j5-j2s1DoF7Ozgdn1ifqnJlwByMQMmRjr95z2aQpgAabo5OT" src="https://github.com/user-attachments/assets/b1d88391-5b98-4d61-b1d5-900692e9dbae" />

Our model is based on the structure of a hypothetical pet shelter organization. The shelter locations entity is representative of the locations this organization operates. Within this entity, we store the ID of each location, along with its address and phone number. Inside of each location, we keep track of many different products, pets, and employees. This is represented by the one-to-many relationships shown in our model between shelter locations and inventory, pets, and employees. Within our inventory entity, we store details about each product, such as a short description, quantity, and price. 

Within our entity for employees, we keep track of each employee’s ID, name, phone number, what shelter location they work at, and their specific role. This is represented by a one to many relationship shown in our model between roles and employees, since one role can be taken on by many different employees. Within our role entity, we keep track of each name and description of each role within the organization. Additionally, we added a one to many relationship between employees and medical records to represent that one employee can work on many different medical records. Within medical records, we keep track of each record and its entry description, date, and treatment plan. 

In order to store details about individuals who have adopted, we have created an entity for adopters. Here, we keep track of each adopter’s ID, email, name, phone number, and address. In order to store details about which pets adopters have adopted, we unintentionally created an associative entity for our many to many relationship between pets and adopters, called adoption records. Within this entity, we keep track of each application ID and the date adopted. We represented it this way since an adopter can apply for many different pets, and a pet may be applied for by many different adopters. 

Within our central entity, pets, we store data such as each pet’s name, age, gender, arrival date, species, shelter location, and breed. We also represent 2 more one to many relationships between species and pets, as well as breeds to pets. We represent it this way since one species accounts for many different pets, and one breed accounts for many different pets. Within these entities, we store information such as the species name and description, and the breed name. We added one more one to many relationship here between species and breeds, because one species has many different breeds. 

## Data Dictionary
<img width="656" alt="Screenshot 2025-03-20 at 11 37 32 AM" src="https://github.com/user-attachments/assets/1067a533-3eae-402f-901b-f7de59cdadff" />
<img width="641" alt="Screenshot 2025-03-20 at 11 38 01 AM" src="https://github.com/user-attachments/assets/a1c7cf4b-d2eb-4612-b00c-0501dba78458" />
<img width="634" alt="Screenshot 2025-03-20 at 11 38 46 AM" src="https://github.com/user-attachments/assets/5623d2f1-d366-4350-8fb2-dbb6a60af3a1" />
<img width="652" alt="Screenshot 2025-03-20 at 11 39 50 AM" src="https://github.com/user-attachments/assets/28438160-9b36-464b-b2ee-d1e0471c3727" />
<img width="705" alt="Screenshot 2025-03-20 at 11 40 30 AM" src="https://github.com/user-attachments/assets/51db4808-af68-41e9-9125-b10e6eacf733" />
<img width="703" alt="Screenshot 2025-03-20 at 11 40 57 AM" src="https://github.com/user-attachments/assets/698a72f2-6ff8-45dc-8342-fd2f9f4b2bde" />
<img width="659" alt="Screenshot 2025-03-20 at 11 41 28 AM" src="https://github.com/user-attachments/assets/84abcbd6-cc97-4e64-89df-d7f8aa9956b7" />
<img width="649" alt="Screenshot 2025-03-20 at 11 41 58 AM" src="https://github.com/user-attachments/assets/7271abfa-b80b-4970-99a7-f016d3a1ecae" />
<img width="640" alt="Screenshot 2025-03-20 at 11 42 39 AM" src="https://github.com/user-attachments/assets/bf2f6c4d-7ebf-435a-baa4-95e9cf9aa236" />

## Queries
<img width="651" alt="Screenshot 2025-03-20 at 11 56 35 AM" src="https://github.com/user-attachments/assets/59c95299-9db3-4eb1-80be-2b4e6764e055" />

### Complex
1. Select the names of pets who have been worked on by a Veterinarian
![AD_4nXdCGh5RrxNi71L5Kt46BsxVhvLL-yjeXE-ezl8i1HxNoF10VANE6NzPftPe0uYoBQn4q-TUhDAu0fbh6rya5Nfbb70-ya7TxT1F9KP1oUoTEKxxPDa7T6tD](https://github.com/user-attachments/assets/fdbcff25-1c55-4982-9fa8-ee334a0494af)
Explanation: This query allows shelter managers to easily see Pets who have been worked on by a Veterinarian, and therefore shows pets who are more prone to medical issues. The shelter manager should make sure a veterinarian is on site at the shelters these pets are located at.

2. Select the names of pets who have more than the average number of medical records
![AD_4nXdwfsNyyoXBCWUALxM1jT8XtNpoaQBi608j5h6Lag0JMv4bP89Q-tw3rfLwmIYJwd5E4MwEiRa5TWgrHoMtBaStmHV-WLCXjdHBOSLzfRlYepNLyZ9pMo6N](https://github.com/user-attachments/assets/0de2ff3d-16c9-4bd7-ad95-f1160d2f6f56)
Explanation: This query provides a similar insight to the first query, but outputs a different set of information. This query shows the user pets that are more likely to need some sort of medical examination. Unlike the first query however, these examinations could be performed by employees other than Veterinarians.

3. Print the Shelter location with the most inventory
![AD_4nXc_FCnnRFDxuIn-FzyOOO85Z53idN0poDr-tCPGagdIb8f6ptgQg0Jl0mi1CI9MxxFM4OHX-PZeBLksaSt5A2xnnnCJrvMc2kPHCEtf-ma-S_iF8qjp3Vyp](https://github.com/user-attachments/assets/5f360a39-416f-4547-b567-8d33e5273b2b)
  Explanation: This query allows the user to see the shelter with the most inventory. The user could use this information to know what   shelter they could get inventory from if another shelter is running low. This query could also easily provide the shelter with the least inventory by replacing ‘max’ in the subquery with ‘min’. This could be used to know what shelter needs to order inventory.

4. Print the number of pets for each employee who has worked on more than the average number of pets
![AD_4nXftwFAfqENgdUJLBwE1Mr_9UfskYFyBavSqmmu9lu7s_5mZ7HQZq9WjRhM0l1FQeK9DGAORU0pCzafJYzsXcSvkDzzSZrFVkBcaf95w9NMkBGTcnvVjwRoJ](https://github.com/user-attachments/assets/0b8f1486-25b8-46a1-ac78-b30b0de8787e)
  Explanation: This query could be useful in knowing which employees are doing the most work with the most pets, and therefore could be a factor in deciding employee wages, bonuses, or raises.

5. Print the number of employees by role in all Shelter Locations in Texas
![AD_4nXf8uo-RbdIPtwlMKs0ThVDBTtmF8wZyNLtXRi1vpt9pX4-htFS0trrD2ak5LOxsg_erXbsLNiIfZDi-6TeFMBXu3ShTETlV_aA9STzwBdl6iVjY_aah1Rn-](https://github.com/user-attachments/assets/12160be3-30aa-4564-a133-3ab433a2f83d)

  Explanation: This query allows the user to see how many of each type of employee is located in texas. This table could be even more useful by looking at what it does not output vs what it does, because based on what is not in this list, a manager could know what roles they need to hire for shelters in texas.


6. Print the names of Adopters who have adopted pets at multiple shelter locations
![AD_4nXfSB95jEAnsJfqanarCCI6USl_WVT-BFo8ox_Rfe9pJ6Fu1_xeuc5pBtgOKwEazPySnDovi_GRFDTPLODt4EvmtoAD46DS5P9IeSbe5B0mmnbPsJcQjrh5e](https://github.com/user-attachments/assets/861ebb56-8536-4543-bd63-13a39947d558)

  Explanation: This query provides a list of adopters who have adopted at multiple locations, and are therefore the best customers. Shelter Locations should take extra care of these adopters in order to keep them happy.

 ### Simple
7. Print out pet names at a shelter number 1
![AD_4nXfhujLcgWd2FUmKjKC28wZFcztC4OMQnIeAYDSxHC8wgYmwjZp2BfQ9FvSb_SeHg-IeSiR_Pe2R2UsfGNAtDVjtpYBTsVu-pZ6l7fgnzqvb_fFbPv-zMuRp](https://github.com/user-attachments/assets/33d151e9-5171-4b11-80a8-2c26fd791333)

  Explanation: This query helps shelter managers quickly identify and track the pets housed at a specific location. It is useful for monitoring shelter capacity, facilitating adoption events, and coordinating medical treatments. A manager can use this query to assess real-time pet availability and make operational decisions accordingly!

8. Find total value of inventory per shelter location.
![AD_4nXemE4kztc-rejPspjCt_pBC85UYxP6_RKnGzxA6XVraY9yMl41T3J-FnxDgXfyA809tLG8n62yW6sbVen2O9BIWMZ2pDU_Q5PxepiTm5aQQz6_CTkMeCw39](https://github.com/user-attachments/assets/5410f8aa-2982-4ecd-bdfd-e0bec15ba750)

  Explanation: This query helps managers understand the total financial value of inventory at each shelter, which is crucial for budgeting and financial planning, resource allocation, and preventing overstocking or shortages. Here, we can identify shelters that may have too much or too little stock. We can ensure shelters that have the right balance of supplies. By analyzing inventory value across shelters, we can optimize purchasing decisions and reduce waste, ensuring shelters operate efficiently.

9. List all adopters with their contact information.
![AD_4nXcPgqL0D445NwTfSPrrxqaf_7DTQqv5v8ogjPQdi8RACQnAzdZwHsuG2nt_Dk9J89BiSbthtF1vd8phS4WbmhP42Sd4nm7JsPTDcJx3v5Js0Pyw1rvPp5Qq](https://github.com/user-attachments/assets/49c351f2-104b-4261-b379-da3ba8f973f1)

  Explanation: This query is crucial for post-adoption support and shelter relations. It helps managers follow up on pet well-being, encourage future adoptions, and organize adoption events. Building long-term relationships with adopters enhances the reputation and sustainability of the shelter.

10. List all of the dogs
![AD_4nXcyu2rPHYhjeC9NFJA2wSCrC-6PHPYg-Y8l515xp7VaeGJs9XYBbXrY1hSqKx6v85zH4-R2KyiQsLNUukL1IVLztGVaXryXoW65Sc8B3FJVjRkjGoknSSon](https://github.com/user-attachments/assets/56336289-bb79-421e-a967-6e4f9421c2b6)

Explanation: Tracking all dogs in the shelter is critical for efficient shelter management and adoption planning. This helps managers plan adoption events, monitor shelter capacity, and assist breed specific rescues. By keeping an updated list of all dogs, shelters can ensure they provide the best care and find homes faster.
