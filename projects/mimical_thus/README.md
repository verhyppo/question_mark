# MimicalThus

## Context  

The system we are going to create is called *MimicalThus* and allows users to search people which are similar in terms of 
- similar behaviour
- passions and hobbies

Each user is able to insert its data during the registration process and then, cannot update them anymore.

Each user can select up to 5 behaviors and 5 passions, with a total of 10 entries per user, and can assign a value to each of its entries from -10 to +10, where -10 means that hates that behavior or passion and +10 means that loves them very much

Once done so, the users are then provided with a list of paginated results of the most similar people by following this requirements:
- first, people with the highest number behaviors in common with the closest value
- second, people with the highest number interests in common with the closest value

The default number of result is 5 but the user can select the number of results to be displayed up to 20, with a step of 5, and navigate to see other people.

The list provided, allows the user to see other users information:
- the email
- behaviors and its values
- passions and its values
- common passions and behaviors needs to be highlighted

Allowed values for Behaviours are listed in [Behaviors](Behaviours.md) file and Passions are listed in [Passions](Passions.md)

A basic database schema to model the problem is provided in the [DB](DB.md) file.

## Outcomes

Deliverables expected

- Requirements as described above are satisfied

Feel free to provide diagrams or tests (integration or unit) to describe how do you plan to achieve the results.

## Bonus 
- Github project
- Wrap application into electron application. Electron is a js framework to build cross-platforms desktop applications: https://www.electronjs.org/
- The application uses OpenID authentication by using Microsoft Identity Platform, or a social login of choice
