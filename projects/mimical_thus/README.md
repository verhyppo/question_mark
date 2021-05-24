# MimicalThus

## Context  

The system we are going to create is called *MimicalThus* and allows users to search people which are similar in terms of 
- similar behaviour
- passions and hobbies

Each user is able to insert its data
- name
- surname
- email
- birthdate
- list of behaviour and value
- list of passions and value

during the registration process and then cannot update them anymore.

Each user can select up to 5 behaviors and 5 passions, with a total of 10 entries per user, and can assign a value to each of its entries from -10 to +10, where -10 means that hates that behavior or passion and +10 means that loves them very much

Once done so, the users are then provided with a list of paginated results of the most similar people by following this requirements:
- first, people with the highest number behaviors in common with the closest value
- second, people with the highest number passions in common with the closest value

The default number of result is 5 but the user can select the number of results to be displayed up to 20, with a step of 5, and navigate to see other people.

The list provided, allows the user to see other users information:
- the email
- behaviors and its values
- passions and its values
- common passions and behaviors needs to be highlighted

Allowed values for Behaviours are listed in [Behaviors](Behaviours.md) file and Passions are listed in [Passions](Passions.md)

A basic, not comprehensive, database schema to model the problem is provided in the [DB](DB.md) file, feel free to modify it.

## Outcomes

Deliverables expected
- Requirements as described above are satisfied
- (Basic) Authentication is in place
- Postman collection to:
  - retrieve paginated list of similar users
  - registration process

Feel free to provide diagrams or tests (integration or unit) to describe how do you plan to achieve the results.

## Bonus 
- Github project
- Authentication via OpenID authentication by using Microsoft Identity Platform or other social login of choice
- Liquibase Integration
