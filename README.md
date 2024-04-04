# MIST4610-Project-1

# Team name:

21479 Group 6

# Team Members:

1. Ireland Wellshear @21iwellshear

2. Jack Liskey @Jackliskey

3. Ryan Mai @Peaches124

4. Ashkon Mokhlesi  @AshkonMokhlesi

5. Karandeep Singh @KarandeepSingh23

# Problem Description

The task at hand is to model and build a relational database for the general operations of a tennis club. The central entity in the model is the Club entity, representing each physical club location owned and operated by the organization. The tennis club operates in conjunction with various things, such as racket rentals, tournaments, coaching sessions, court reservations, and shopping at the Pro Shop, to cater to its members and guests. We aim to accurately model these relationships, generate sample data, and populate the entities and their attributes with this sample data. Additionally, we are interested in performing functional queries on this data to gain valuable insights into the club's operations and member engagement.

# Data Model

Explanation of data model:

Our data model is based on our prestigious and well-equipped private tennis club organization. Beginning with the club entity, each individual club within the organization is assigned its own unique club id. Each individual club has many workers as a part of its staff but each staff member can only work at one club during their employment exhibited through the one-to-many relationship to the staff entity.


Each club also has numerous members who are connected through a one-to-many relationship from the club entity to the members entity. Every member is assigned a unique member id to identify them as well. You may notice through our queries that many members have home addresses in a different state that the location of the club and this is a testament to our prestige as an organization. We have many members who travel and temporarily relocate to become members and train at one of our clubs.


Members of our clubs can take part in a number of tournaments made available to them through their association with us. Shown by the many-to-many relationship between the tournaments entity and the members entity, a tournament can have many of our members playing in them and a member can take part in as many tournaments as they like. Each tournament also has a sponsor through various companies who use our tournaments as a means of product and service exposure. Each sponsor is given their own sponsor id to track which tournaments they sponsor.


To give our players confidence going into these tournaments we offer private coaching sessions to our members on the facilities of any of our clubs. This is a relationship our members value between them and their coaches, and is displayed as a many-to-many relationship between the two entities. Individual coaching sessions are logged and displayed as an associative entity between the member and coaches entities. For each session only one court can be reserved creating a one-to-one relationship with the coaching session entity and court entity.


To ensure that there are always coaches available to our members at each club, each coach can only work at one club, and of course, each individual club employs many top notch coaches exhibited through a one-to-many relationship from club to coaches.


Lastly, to provide the best service possible to our members each club has their own pro shop. At our pro shop members can purchase new equipment such as shoes, tennis balls, energy drinks, protein bars, and even a new racket (for sale not for rent). The relationship between these pro shop items and members is a many-to-many relationship as members can purchase many items and an item can be purchased by many members. Each purchase is recorded and logged as a transaction. The transactions entity is an associative entity between pro shop items and members.

 

![image](https://github.com/21iwellshear/MIST4610-Project-1/assets/150079987/a1778499-57f5-4f6d-a6bb-fcc5bb5faf5c)

 

# Date Dictionary:

 

![image](https://github.com/21iwellshear/MIST4610-Project-1/assets/150079987/6aaf2df7-a5a5-4c1a-9481-328f1d70ec3b)

![image](https://github.com/21iwellshear/MIST4610-Project-1/assets/150079987/c3ae632f-5d90-4b14-a291-e6e4f61f49fe)

![image](https://github.com/21iwellshear/MIST4610-Project-1/assets/150079987/55f9f4c4-c5c9-4409-8ccf-e609c062c201)

![image](https://github.com/21iwellshear/MIST4610-Project-1/assets/150079987/1a93f90f-6303-4720-86a5-db81e1631274)

![image](https://github.com/21iwellshear/MIST4610-Project-1/assets/150079987/ee2d034a-9348-4b17-9bec-039e6d712ac5)

![image](https://github.com/21iwellshear/MIST4610-Project-1/assets/150079987/b6a420e9-165b-4487-b586-e9dc0ac8a2de)

 

 

# Queries

![image](https://github.com/21iwellshear/MIST4610-Project-1/assets/150079987/99eaf859-75a4-49c0-9900-8940235ca816)

 

1. Description: Determine the total number of coaching sessions conducted by each coach as a percentage of all sessions.

   ![image](https://github.com/21iwellshear/MIST4610-Project-1/assets/150079987/48b85a0f-78c4-4e27-ac6d-e135393f205b)

   - Justification: Understanding the distribution of coaching sessions helps in workload balancing and identifying coaching resource needs.

   - Complexity: JOIN Operation, Aggregation Functions (COUNT), Subquery, GROUP BY Clause, Arithmetic Operations (Percentage Calculation)

2. Description: List of upcoming tournaments located in China.

     ![image](https://github.com/21iwellshear/MIST4610-Project-1/assets/150079987/e3923c90-76a1-4da8-8167-a08104b2b665)

     - Justification: Enables planning for hosting and promoting specific events for China.

     - Complexity: Simple WHERE

3. Description: Find all tennis courts with lighting.

      ![image](https://github.com/21iwellshear/MIST4610-Project-1/assets/150079987/af3c6e70-9141-4406-abc5-8a3ff9bda725)

     - Justification: To schedule evening or night games and training sessions.

     - Complexity: Simple WHERE

4. Description: List winners of tournaments, the prices they won, and the sponsor of the tournament.

      ![image](https://github.com/21iwellshear/MIST4610-Project-1/assets/150079987/2aabb458-5f65-4955-959e-f0de9501379e)

     - Justification: Highlights successful players and their rewards, useful for promotional materials and sponsor relations.

     - Complexity: Complex (Multiple Table Join, GROUP BY)

5. DescriptionL Find all coaches who specialize in training kids age groups and their pay rates.

      ![image](https://github.com/21iwellshear/MIST4610-Project-1/assets/150079987/a1539ab7-3be4-4e00-9bbf-8f31cfb1a633)

     - Justification: Helps allocate coaches based on demand for junior training sessions, optimizing staffing.

     - Complexity: Simple WHERE

6. Description: Find the most purchased items in the pro shop by quantity ordered.

      ![image](https://github.com/21iwellshear/MIST4610-Project-1/assets/150079987/55357c47-c647-4dce-a9cf-ebde485179f7)

   - Justification: Identifies best-selling items to manage stock levels effectively.

   - Complexity: Complex (Join, GROUP BY, ORDER BY)

7. Description: Identify Largest Spenders in the Pro Shop and Their Associated Clubs

      ![image](https://github.com/21iwellshear/MIST4610-Project-1/assets/150079987/4e6ca6b4-7dae-4b60-a232-db14d7232ddd)

   - Justification: For club managers and marketing teams, understanding who the largest spenders are and their club affiliations can inform a range of strategic decisions.

   - Complexity: JOIN, GROUP BY, CASE, Subquery

8. Description: Identify coaches whose trainees have renewed their memberships at the highest rates, suggesting high coach performance.

      ![image](https://github.com/21iwellshear/MIST4610-Project-1/assets/150079987/2eddf5ca-4c34-4d4f-90c3-4317fa2ccdc2)

   - Justification: Enables the club to identify and reward top-performing coaches, potentially using this information for marketing or compensation strategies.

   - Complexity: Complex (Join, Subquery, Window Functions)

9. Description: Calculate the total hours worked by each staff member in a given day, including details of their position.

      ![image](https://github.com/21iwellshear/MIST4610-Project-1/assets/150079987/5ede43f9-a800-42f1-91cc-60eb757f0fcd)

   - Justification: Provides insights into staff workload distribution, helping to identify under or overutilized staff for better resource management.

   - Complexity: (Join, Date Functions, Aggregate Functions)

10. Description: Calculate the total monthly payment received from all active members.

      ![image](https://github.com/21iwellshear/MIST4610-Project-1/assets/150079987/116a328e-a5a2-4209-8a25-18c6eaeff687)

   - Justification: Provides a quick overview of the club's primary income source, helping in financial planning.

   - Complexity: Simple (Aggregate Function).

 

# Database Information:

Name of the database: al_Group_21479_G6

 

Additional information: Each query listed above is marked in the database using stored procedures which can be called using the following format: CALL TP_Q1();
