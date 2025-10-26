# mist4610groupproject
MIST 4610 Group Project: Group 7

Team Name and Members:

Team Members:

Audrey Staples - https://github.com/audreystaples/mist4610groupproject

Angela Ren - https://github.com/angelaaa456/mist4610groupproject

Sammy Effron - https://github.com/Seffron/mist4610groupproject

Tanner Sutherland - https://github.com/tannersutherland/mist4610groupproject

Tyler Schildkraut - https://github.com/tylerschildkraut/mist4610groupproject

Scenario Description:
We wanted to construct a data model that organizes key information used to navigate the NCAA college football landscape. The ultimate goal for our model is to represent the various relationships that exist among Coaches, Teams, Players, Rosters, Games, etc. in a way that mirrors how real NCAA programs operate. Although our data is hypothetical, it represents pertinent information that would meet managerial requirements within the NCAA ecosystem. From surveying game statistics to determining player status on a roster, our database provides insights that would prove highly useful to NCAA stakeholders. Ultimately, we aimed to create a database that would effectively aid managerial decision making within essential business units such as logistics management, decision-making, and reporting within an ever evolving industry.

Data Model:

MIST 4610 GP Data Model
Explanation: 

Our database is based on the NCAA with hypothetical data included for ease of data insertion. For instance, instead of the University of Georgia the record is the Athens Bulldogs.

Beginning with the Teams entity, we made teamID our identifier and included attributes such as teamName and conference. This entity relates to our Coaches entity with a one-to-many relationship because teams have many coaches, but those coaches are linked to only one team. Our Coaches entity is identified by the primary key coachID and contains attributes such as name, role which describes their specific coaching position (Head Coach, Offensive Coordinator, etc.), yearsOfExperience describing the amount of years of coaching experience they have, as well as a foreign key being teamID. Rosters represent the associative entity connecting the many-to-many relationship between Teams and Players as players can be on many teams and teams are composed of many players. Rosters are identified by rosterID, and they have attributes such as a foreign keys playerID and teamID. Additionally, Rosters display the startDate of a player’s commitment to a team as well as the endDate which could be null if the player is still playing on that team playing. Rosters also display the player’s position on that specific team as well as their jersey number on that specific team. The Players entity is identified by a unique playerID which is the primary key of that entity. In addition to that, the Players entity has attributes such as name, the player’s yearInSchool, their height in inches, their weight in pounds, and the status of their scholarship, if applicable. Additionally, the Players entity has a one-to-many relationship with the entity named Injuries as players can have many injuries but a specific instance of an injury can only occur once in one player. Injuries have the primary key injuryID along with attributes such as injuryName, lengthOfRecovery, surgery name if needed, as well as the foreign key playerID which specifies the one-to-many relationship.

Moving on to another key entity, we have Games. Games are identified by their primary key which is called gameID. Our Teams table has two one-to-many relationships with the Games entity meaning that one instance of a team (the home team) has many games but those games only have one home team. Additionally, another instance of a team (the away team) also has many Games but those specific games are only related to one away team. For that reason, our Games entity contains two foreign keys from the Teams table, one being homeTeamID and the other being awayTeamID. Another foreign key in the Games table is the stadiumID. The last attribute in the Games table is the date attribute which specifies the date the game occurred on. Our Stadiums table is connected to the Games entity by a one-to-many relationship. Stadiums house many games but those games can only be played at one stadium at a time. Stadiums are also identified by attributes such as stadiumName, city, and capacity. Stadiums also have a one-to-many relationship with Seats because a stadium has many seats but a seat can only be in one stadium. Seats have the primary key seatID as well as attributes like section, row, seatNumber, seatType, and the foreign key stadiumID. Seats also have a one-to-many relationship with Tickets as a seat can be sold by many tickets but tickets only are attached to one seat. Tickets are identified by ticketID, and have attributes such as price, ticketHolderName, the foreign key gameID, and the foreign key seatID. This then brings about the relationship between Games and Tickets being one-to-many as games have many tickets but a specific ticket is only attached to one game. The last entity that needs describing is our Statistics entity. Statistics has a many-to-one relationship with Players as Players have many statistics but a specific statistic is only connected to one player. Another relationship that exists with Statistics is a many-to-one relationship with Games. Statistics are present in many games, but a game only has one instance of a specific player statistic. Statistics are identified by a statID, a foreign key of playerID, yards if applicable, touchdowns if applicable, tackles if applicable, interceptions if applicable, receptions if applicable, fieldGoals if applicable, as well as the foreign key gameID.


<img width="638" height="700" alt="Screenshot 2025-10-22 at 10 09 00 PM" src="https://github.com/user-attachments/assets/a28ac496-6830-4f2a-96cf-64cd652cd0d6" />

Data Dictionary:

<img width="902" height="295" alt="Screenshot 2025-10-22 at 10 13 45 PM" src="https://github.com/user-attachments/assets/be3afe6d-085d-4152-a56d-11718f81a2e7" />

<img width="879" height="244" alt="Screenshot 2025-10-22 at 10 14 05 PM" src="https://github.com/user-attachments/assets/0e5cb177-19b1-4c5b-8178-3bfad7b5c5d5" />

<img width="862" height="360" alt="Screenshot 2025-10-22 at 10 14 22 PM" src="https://github.com/user-attachments/assets/f7c89cbb-760e-4270-b73d-127cf0b00cbf" />

<img width="933" height="406" alt="Screenshot 2025-10-22 at 10 14 48 PM" src="https://github.com/user-attachments/assets/68f128f5-99c6-4afe-8e35-c9d26210eec1" />

<img width="948" height="342" alt="Screenshot 2025-10-22 at 10 15 07 PM" src="https://github.com/user-attachments/assets/590900da-c8b4-4675-ad55-2ef51ff074e9" />

<img width="654" height="284" alt="Screenshot 2025-10-26 at 7 21 06 PM" src="https://github.com/user-attachments/assets/7345fffc-4e22-4aa2-8438-6c2c648c7fdc" />

<img width="656" height="448" alt="Screenshot 2025-10-26 at 7 21 21 PM" src="https://github.com/user-attachments/assets/2df615c6-b661-4f57-b121-3c74ff0675d3" />

<img width="660" height="274" alt="Screenshot 2025-10-26 at 7 21 34 PM" src="https://github.com/user-attachments/assets/d8a8f872-4506-4252-8596-61087e2202bf" />

<img width="675" height="357" alt="Screenshot 2025-10-26 at 7 21 50 PM" src="https://github.com/user-attachments/assets/c8033cc4-55d1-4f24-add9-608bb4c292d5" />

<img width="663" height="213" alt="Screenshot 2025-10-26 at 7 22 00 PM" src="https://github.com/user-attachments/assets/48b6c101-7b36-4a48-b58b-6db86a1b5e3f" />

Queries:

<img width="662" height="316" alt="Screenshot 2025-10-26 at 7 23 57 PM" src="https://github.com/user-attachments/assets/b32eadd2-a490-426f-8528-ec413c9e0d16" />



1. Query 1 shows every team and counts how many players are currently listed on their roster. It joins the Teams and Rosters tables using the teamID to associate players with their teams, then groups the results by each team name.


<img width="553" height="175" alt="Screenshot 2025-10-26 at 7 25 15 PM" src="https://github.com/user-attachments/assets/9ae5e49e-3c11-4872-985e-d3a4cfb3c7fe" />\


<img width="421" height="609" alt="Screenshot 2025-10-26 at 7 25 32 PM" src="https://github.com/user-attachments/assets/7f8ee285-89f6-43b8-b6e7-680684240f3c" />


Text Results: Execute:

SELECT teamName, COUNT(playerID) AS PlayerCount FROM Teams JOIN Rosters ON Teams.teamID = Rosters.teamID GROUP BY teamName

------------- + ---------------- + | teamName | PlayerCount |
------------- + ---------------- + | Athens Bulldogs | 3 | | Madison Badgers | 3 | | Columbus Buckeyes | 2 | | Ann Arbor Wolverines | 2 | | State College Nittany Lions | 3 | | East Lansing Spartans | 2 | | Minneapolis Gophers | 2 | | Lincoln Huskers | 2 | | Iowa City Hawkeyes | 2 | | Champaign Illini | 2 | | Evanston Wildcats | 3 | | Piscataway Scarlet Knights | 2 | | College Park Terrapins | 2 | | Seattle Huskies | 2 | | Eugene Ducks | 2 | | Los Angeles Bruins | 2 | | Los Angeles Trojans | 2 | | Bloomington Hoosiers | 2 | | West Lafayette Boilermakers | 2 | | Austin Longhorns | 2 | | Norman Sooners | 2 | | Tuscaloosa Crimson Tide | 2 | | Baton Rouge Tigers | 2 |
------------- + ---------------- + 23 rows


Managerial Justification: Roster size directly affects scholarship budgeting, recruiting needs, and practice planning. Athletic departments can use this information to verify roster compliance with NCAA limits (e.g., 85 scholarship players in Division I football) and identify whether certain teams are under- or over-staffed. It also provides insights for coaching staff to balance positional depth across the roster.

2. Query 2 calculates the total number of offensive yards gained by each player across all games using the Statistics table. The query groups by player name and sums their yards column, returning players in descending order of total yardage.

<img width="612" height="152" alt="Screenshot 2025-10-26 at 7 26 23 PM" src="https://github.com/user-attachments/assets/48a9d17c-c0f4-4a07-a8af-17c433bb1376" />\

<img width="312" height="643" alt="Screenshot 2025-10-26 at 7 26 37 PM" src="https://github.com/user-attachments/assets/41e2f66c-f9e0-4016-ae35-901e6f5704fc" />

Text Results: Execute:

SELECT name AS PlayerName, SUM(yards) AS TotalYards FROM Players JOIN Statistics ON Players.playerID = Statistics.playerID GROUP BY name

--------------- + --------------- + | PlayerName | TotalYards |
--------------- + --------------- + | Tyler Moore | 526 | | Connor Davis | 303 | | Noah Lewis | 153 | | Zach Moore | 322 | | Connor White | 480 | | Aaron Jones | 65 | | Connor Martinez | 260 | | David Harris | 147 | | James Anderson | 157 | | John Miller | 289 | | Ethan Wilson | 461 | | Luke Moore | 521 | | Alex Smith | 449 | | Logan Martinez | 331 | | Michael Taylor | 447 | | Justin Davis | 168 | | Jordan Moore | 324 | | Ryan White | 195 | | Josh Johnson | 579 | | Nick Lewis | 251 | | Matt Jones | 350 | | Ethan Smith | 148 | | Michael Walker | 67 | | Zach Harris | 190 | | John Johnson | 282 | | Michael Thomas | 159 | | Michael Harris | 20 | | Aaron Thomas | 40 | | Dylan Walker | 77 | | James Clark | 112 |
--------------- + --------------- + 30 rows


Managerial Justification: Tracking cumulative yardage helps offensive coordinators evaluate player impact and consistency. This data is key for determining award nominations, highlighting top performers in media relations, and identifying players who may deserve more playing time or position adjustments based on productivity.

3. Query 3 identifies all players who have not yet recorded any game statistics by checking which player IDs are not present in the Statistics table.

<img width="618" height="707" alt="Screenshot 2025-10-26 at 7 27 19 PM" src="https://github.com/user-attachments/assets/7848cd18-238a-429c-bc8e-7a0b6c030bbe" />


Text Results: Execute:

SELECT name FROM Players WHERE playerID NOT IN (SELECT playerID FROM Statistics)

--------- + | name |
--------- + | Noah Johnson | | Josh Thomas | | Jordan Garcia | | Nick Thomas | | Chris Harris | | Noah Smith | | Josh Smith | | Michael Moore | | Alex Walker | | Luke Brown | | David Clark | | Tyler Garcia | | James Thompson | | Kyle Davis | | Kyle Martinez | | Zach Jones | | Logan Brown | | Ryan Jones | | Zach Clark | | Zach Garcia |
--------- + 20 rows


Managerial Justification: This helps coaching staff and analysts find players who have not appeared in any games and make decisions about those players accordingly. Managers can use this information to determine which players may need more opportunities to play or to address what to do with those players in the future.

4. Query 4 displays all players who have sustained more than one recorded injury. It joins Players and Injuries using playerID, groups the results by player, and filters using a HAVING clause.

<img width="579" height="652" alt="Screenshot 2025-10-26 at 7 28 16 PM" src="https://github.com/user-attachments/assets/47642145-9c67-4777-addc-1f4a2929cb92" />

Text Results: Execute:

SELECT name, COUNT(injuryID) AS TotalInjuries FROM Players JOIN Injuries ON Players.playerID = Injuries.playerID GROUP BY name HAVING COUNT(injuryID) > 1

--------- + ------------------ + | name | TotalInjuries |
--------- + ------------------ + | Tyler Moore | 2 | | Jordan Moore | 2 | | Ethan Smith | 3 | | Michael Taylor | 3 | | Alex Walker | 3 | | Zach Moore | 2 | | James Anderson | 3 | | Ethan Wilson | 2 | | Kyle Martinez | 2 | | Logan Brown | 4 | | James Clark | 2 |
--------- + ------------------ + 11 rows


Managerial Justification: Identifying players with frequent injuries allows medical staff to implement personalized recovery or training programs. Coaches can use this information to manage playing time and avoid re-injury, which reduces long-term risk and protects the team’s investment in scholarship athletes.

5. Query 5 finds the average weight of players for each position across all rosters. It joins Rosters and Players and groups the results by position.

<img width="600" height="572" alt="Screenshot 2025-10-26 at 7 29 27 PM" src="https://github.com/user-attachments/assets/c57b2557-f756-4a20-adeb-91f370fd0570" />

Text Results: Execute:

SELECT position, ROUND(AVG(weight (in lbs)), 1) AS AvgWeight FROM Rosters JOIN Players ON Rosters.playerID = Players.playerID GROUP BY position

------------- + -------------- + | position | AvgWeight |
------------- + -------------- + | QB | 243.7 | | RB | 222.1 | | WR | 223.2 | | LB | 198.3 | | TE | 238.7 | | CB | 255.0 | | DL | 238.8 | | S | 245.0 | | OL | 206.0 |
------------- + -------------- + 9 rows


Managerial Justification: Weight and conditioning benchmarks are crucial for maintaining competitiveness. This data helps strength and conditioning coaches monitor whether players at each position (e.g., linemen, receivers, linebackers) meet desired physical standards and make training adjustments if a position group is under or over target weight ranges. AI was utilized here to locate the backticks function which allowed for the system to not confuse the parentheses in the column title with SQL script parentheses.

6. Query 6 shows the number of total games each team has participated in—both home and away. It joins Teams and Games and counts how many times a team appears as either the home or away team.

<img width="620" height="121" alt="Screenshot 2025-10-26 at 7 29 57 PM" src="https://github.com/user-attachments/assets/3ccba3fc-5fe3-4922-884b-2f3e84fda8ec" />\


<img width="394" height="657" alt="Screenshot 2025-10-26 at 7 30 13 PM" src="https://github.com/user-attachments/assets/8ccba44e-c80e-4e23-ad98-29eacfb5e661" />

Text Results: Execute:

SELECT teamName, COUNT(gameID) AS TotalGames FROM Teams JOIN Games ON Teams.teamID = Games.homeTeamID OR Teams.teamID = Games.awayTeamID GROUP BY teamName

------------- + --------------- + | teamName | TotalGames |
------------- + --------------- + | Athens Bulldogs | 2 | | Madison Badgers | 2 | | Columbus Buckeyes | 2 | | Ann Arbor Wolverines | 2 | | State College Nittany Lions | 2 | | East Lansing Spartans | 2 | | Minneapolis Gophers | 2 | | Lincoln Huskers | 2 | | Iowa City Hawkeyes | 2 | | Champaign Illini | 2 | | Evanston Wildcats | 2 | | Piscataway Scarlet Knights | 2 | | College Park Terrapins | 2 | | Seattle Huskies | 2 | | Eugene Ducks | 2 | | Los Angeles Bruins | 2 | | Los Angeles Trojans | 2 | | Bloomington Hoosiers | 2 | | West Lafayette Boilermakers | 2 | | Austin Longhorns | 2 | | Norman Sooners | 2 | | Tuscaloosa Crimson Tide | 2 | | Baton Rouge Tigers | 2 | | Athens Classic Dawgs | 2 | | Gainesville Gators | 2 | | Knoxville Volunteers | 2 | | Oxford Rebels | 2 | | Starkville Bulldogs | 2 | | Fayetteville Razorbacks | 2 | | Columbia Gamecocks | 2 | | College Station Aggies | 2 | | Lexington Wildcats | 2 | | Nashville Commodores | 2 | | Tallahassee Seminoles | 2 | | Clemson Tigers | 2 | | Chapel Hill Tar Heels | 2 | | Durham Blue Devils | 2 | | Raleigh Wolfpack | 2 | | Blacksburg Hokies | 2 | | Charlottesville Cavaliers | 2 | | Coral Gables Hurricanes | 2 | | Winston-Salem Demon Deacons | 2 | | Syracuse Orange | 2 | | Pittsburgh Panthers | 2 | | Berkeley Golden Bears | 2 | | Boulder Buffaloes | 2 | | Salt Lake City Utes | 2 | | Tempe Sun Devils | 2 | | Tucson Wildcats | 2 | | Provo Cougars | 2 |
------------- + --------------- + 50 rows


Managerial Justification: Tracking total games played helps administrators measure team activity levels across the season and can highlight scheduling imbalances. Operations teams can use this data to evaluate travel frequency, ensure scheduling fairness, and make logistical improvements for future seasons.

7. Query 7 lists all players who currently receive full athletic scholarships, ordered alphabetically by name.

<img width="445" height="159" alt="Screenshot 2025-10-26 at 7 30 48 PM" src="https://github.com/user-attachments/assets/227b1e31-8b8b-43aa-99e7-c4962033b83f" />\


<img width="466" height="616" alt="Screenshot 2025-10-26 at 7 31 05 PM" src="https://github.com/user-attachments/assets/735d06cf-26fa-4c8a-9b1b-074dec6f64d3" />

Text Results: Execute:

SELECT name, yearInSchool, scholarship FROM Players WHERE scholarship = "Full Scholarship" ORDER BY name

--------- + ----------------- + ---------------- + | name | yearInSchool | scholarship |
--------- + ----------------- + ---------------- + | Aaron Jones | 5th Year | Full Scholarship | | Alex Smith | 4th year | Full Scholarship | | Connor Davis | 4th Year | Full Scholarship | | Connor White | 5th Year | Full Scholarship | | David Clark | 4th Year | Full Scholarship | | Dylan Walker | 2nd Year | Full Scholarship | | James Anderson | 3rd Year | Full Scholarship | | Josh Johnson | 5th Year | Full Scholarship | | Luke Brown | 3rd Year | Full Scholarship | | Michael Moore | 4th Year | Full Scholarship | | Nick Lewis | 1st Year | Full Scholarship | | Noah Johnson | 2nd Year | Full Scholarship | | Noah Smith | 4th Year | Full Scholarship | | Tyler Garcia | 2nd Year | Full Scholarship | | Tyler Moore | 3rd Year | Full Scholarship | | Zach Clark | 2nd Year | Full Scholarship | | Zach Garcia | 1st Year | Full Scholarship |
--------- + ----------------- + ---------------- + 17 rows


Managerial Justification: Scholarship allocation is one of the largest financial responsibilities for athletic programs. This query helps compliance officers ensure that scholarship funds are properly assigned and enables administrators to monitor financial obligations and renewal cycles.

8. Query 8 displays the injuries in the database with the longest reported recovery times, ordered from longest to shortest.


<img width="547" height="143" alt="Screenshot 2025-10-26 at 7 31 36 PM" src="https://github.com/user-attachments/assets/f796ad2d-0789-4a70-a123-5f019c2cd98f" />\

<img width="399" height="618" alt="Screenshot 2025-10-26 at 7 31 54 PM" src="https://github.com/user-attachments/assets/44cd5f97-09c2-4536-bcd7-e45d7d225e8e" />

Text Results: Execute:

SELECT injuryName, lengthOfRecovery FROM Injuries ORDER BY CAST(lengthOfRecovery AS UNSIGNED) DESC

--------------- + --------------------- + | injuryName | lengthOfRecovery |
--------------- + --------------------- + | Turf Toe | 12 weeks | | Groin Pull | 12 weeks | | Wrist Fracture | 12 weeks | | Fractured Rib | 12 weeks | | Shoulder Dislocation | 12 weeks | | Neck Strain | 12 weeks | | Torn Achilles | 10 weeks | | Shoulder Dislocation | 10 weeks | | MCL Sprain | 8 weeks | | Wrist Fracture | 8 weeks | | Elbow Dislocation | 8 weeks | | Elbow Dislocation | 8 weeks | | Torn Rotator Cuff | 8 weeks | | Groin Pull | 8 weeks | | Hip Flexor Strain | 6 weeks | | Elbow Dislocation | 6 weeks | | Hip Flexor Strain | 6 weeks | | Foot Fracture | 6 weeks | | Neck Strain | 6 weeks | | Elbow Dislocation | 6 weeks | | Shoulder Dislocation | 6 weeks | | Broken Collarbone | 6 weeks | | Turf Toe | 4 weeks | | Back Spasms | 4 weeks | | Groin Pull | 4 weeks | | Elbow Dislocation | 4 weeks | | Neck Strain | 4 weeks | | Torn Achilles | 4 weeks | | Fractured Rib | 4 weeks | | Wrist Fracture | 2 weeks | | Hand Fracture | 2 weeks | | Neck Strain | 2 weeks | | ACL Tear | 2 weeks | | Bruised Lung | 2 weeks | | Back Spasms | 2 weeks | | MCL Sprain | 2 weeks | | Neck Strain | 2 weeks | | Torn Achilles | 2 weeks | | Elbow Dislocation | 2 weeks | | Torn Rotator Cuff | 2 weeks | | Elbow Dislocation | 2 weeks | | Neck Strain | Season-ending | | Ankle Sprain | Season-ending | | Neck Strain | Season-ending | | Bruised Lung | Season-ending | | Broken Collarbone | Season-ending | | Back Spasms | Season-ending | | Broken Arm | Season-ending | | Hip Flexor Strain | Season-ending | | Bruised Lung | Season-ending |
--------------- + --------------------- + 50 rows


Managerial Justification: Provides insight into which types of injuries are most severe and time-consuming to heal. This allows sports medicine staff to plan future prevention programs, identify potential insurance or cost implications, and communicate expected recovery timelines to coaches and media. Although we had not yet learned this feature, we utilized AI to accomplish this query as the VARCHAR() data format is not compatible with the ORDER BY DESC or ASC capabilities. Utilizing CAST and UNSIGNED, our string data values were converted to numbers effectively.

9. Query 9 calculates the average price of tickets sold for each game by joining the Games and Tickets tables and grouping results by gameID.

<img width="587" height="97" alt="Screenshot 2025-10-26 at 7 32 37 PM" src="https://github.com/user-attachments/assets/3db45916-d0fb-49a9-9eaa-63e780319ce1" />\

<img width="264" height="611" alt="Screenshot 2025-10-26 at 7 32 50 PM" src="https://github.com/user-attachments/assets/763653f9-0c59-468f-9523-239241c4cb46" />


Text Results: Execute:

SELECT Games.gameID, ROUND(AVG(CAST(REPLACE(price, '$', '') AS DECIMAL (10,2))), 2) AS AvgPrice FROM Games JOIN Tickets ON Games.gameID = Tickets.gameID GROUP BY Games.gameID

----------- + ------------- + | gameID | AvgPrice |
----------- + ------------- + | 24 | 83.00 | | 8 | 217.50 | | 2 | 151.00 | | 34 | 183.00 | | 39 | 180.00 | | 21 | 90.67 | | 1 | 162.00 | | 11 | 39.00 | | 49 | 115.00 | | 31 | 64.00 | | 23 | 247.00 | | 40 | 191.00 | | 28 | 205.50 | | 36 | 61.00 | | 33 | 207.00 | | 12 | 143.00 | | 4 | 237.00 | | 6 | 161.00 | | 19 | 143.00 | | 20 | 163.00 | | 7 | 183.50 | | 43 | 101.50 | | 30 | 71.00 | | 16 | 132.50 | | 13 | 129.50 | | 41 | 187.00 | | 5 | 94.00 | | 44 | 26.00 | | 29 | 92.00 | | 32 | 104.00 | | 3 | 102.00 | | 10 | 124.00 | | 27 | 62.00 |
----------- + ------------- + 33 rows


Managerial Justification: Understanding average ticket prices helps the marketing and sales department assess revenue potential per game. It also reveals which matchups draw higher-paying audiences, allowing pricing strategies to be adjusted for rivalry or high-demand games to maximize profits. Similarly as before, we utilized the CAST function so that we could convert the original VARCHAR value of the price attribute in the Tickets entity to DECIMAL data formats so that we would be able to perform aggregations on the values.

10. Query 10 lists the five players with the highest total touchdowns recorded across all games.


<img width="565" height="512" alt="Screenshot 2025-10-26 at 7 33 25 PM" src="https://github.com/user-attachments/assets/b8fc6a67-c382-4d74-aa37-f76986c91eb4" />

Text Results: Execute:

SELECT name, SUM(touchdowns) AS TotalTouchdowns FROM Players JOIN Statistics ON Players.playerID = Statistics.playerID GROUP BY name ORDER BY TotalTouchdowns DESC LIMIT 5

--------- + -------------------- + | name | TotalTouchdowns |
--------- + -------------------- + | Alex Smith | 15 | | Logan Martinez | 9 | | Luke Moore | 8 | | Dylan Walker | 7 | | Zach Harris | 7 |
--------- + -------------------- + 5 rows


Managerial Justification: This helps highlight standout offensive players for performance evaluations, awards, and media recognition. Teams can also use this information for recruiting promotions and identifying which athletes consistently contribute to scoring. The LIMIT 5 function, which we learned through use of AI, allowed us to locate the top 5 players worth considering.



