# Word Mine

Word Mine is a web application inspired by Duolingo. It uses a Postgres database and a React frontend, implementing a Redux framework for controlling data flow.

<h2> Implementation </h2>
Users' information is kept extremely secure. Word Mine uses BCrypt to hash users' passwords and create password_digests and uses SecureRandom.url_safe.base64 to create session tokens. Passwords themselves are never stored anywhere and session tokens only live in the database and are kept off the front end.
<br />
<h3> Models and Controllers </h3>
Word Mine has the following models:
  * User
  * Language
  * Node
  * Word

Each model validates the presence of its most important info. The controllers are:
  * UsersController
  * SessionsController
  * LanguagesController
  * NodesController

JSON is set as the default format for responses from controllers. Requests to the controllers are triggered by React components and sent in the form of $.ajax requests. Responses are formatted using JBuilder. <br /><br />
A WordsController was not necessary because requests to the NodesController's show method sends back a node which contains an array of the words that belong to it:

  ```
  @words = Word.where({node_id: params[node][id]})
  ```

<h3> Associations </h3>
Since users can study many languages and languages can be studied by many users, Word Mine sets up a many-to-many relationship between the two. To accomplish this, the database has a join table to connect the users table and the language table. It includes user_id and language_id foreign key columns. Languages also have many nodes and nodes have many words.

<h3> Languages </h3>
The languages table has a `name` and an `id` column. After a user signs up, the ChooseLanguage component is rendered, which queries the database for all the names in the language table. Since the store's state includes only objects (with the exception of the nodes portion containing an array of words), a selector is used to extract only the names of the languages.

<h3> Nodes </h3>
The nodes table has columns for `id`, `title`, `language_id`, `completed`, and `unlocked`. The `completed` and `unlocked` attributes are used to determine the background color of the nodes when they get rendered on the tree page. When a user clicks on a node, it triggers a request to the database for all the words that belong to that node:


<h3> Styling </h3>
All styling in Word Mine is done with CSS.

<h2> Next Steps </h2>
Some features that I plan on adding to Word Mine are:
  * Pictures for user profiles
  * Option to create custom node, using Google API to translate words
  * Be able to unlock the next node by answering all questions correctly in the current node
