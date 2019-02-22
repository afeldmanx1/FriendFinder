# Friend Finder - Node and Express Servers

### Heroku Link
https://salty-brook-83678.herokuapp.com/

### Overview

This is a  FriendFinder application that takes in results from your users' surveys, and compare their answers with those from other users. The app will then display the name and picture of the user with the best overall match.

Express is used to handle routing. 

### Instructions 

1. The survey has 10 questions. Each answer is on a scale of 1 to 5 based on how much the user agrees or disagrees with a question.

2. The `server.js` file requires the basic npm packages we've used in class: `express` and `path`.

3. The `htmlRoutes.js` file includes two routes:

   * A GET Route to `/survey` which displays the survey page.
   * A default, catch-all route that leads to `home.html` which displays the home page.

4. The `apiRoutes.js` file contains two routes:

   * A GET route with the url `/api/friends`. This is used to display a JSON of all possible friends.
   * A POST routes `/api/friends`. This is useds to handle incoming survey results. This route will also be used to handle the compatibility logic.

5. The application's data is saved inside of `app/data/friends.js` as an array of objects following the format below.

```json
{
  "name":"Ahmed",
  "photo":"https://media.licdn.com/mpr/mpr/shrinknp_400_400/p/6/005/064/1bd/3435aa3.jpg",
  "scores":[
      5,
      1,
      4,
      4,
      5,
      1,
      2,
      5,
      4,
      1
    ]
}
```