# Minimum Viable Product
  Word Mine is a web application inspired by Duolingo. Users can choose a language and learn the most common words in that language.

  * Hosting on Heroku
  * User Profiles
  * Trees
  * Nodes
  * New account creation, user/guest login
  * Production README

# Design Docs
  * [Api Endpoints](api_endpoints.md)
  * [React Components](component_hierarchy.md)
  * [Redux Structure](redux_structure.md)
  * [Sample State](sample_state.md)
  * [Schema](schema.md)
  * [Wireframes](wireframes/)

# Implementation Timeframe
  <h4> **Phase 1**: Setup and Authentication (2 days) </h4>
  **Objective**: Create a working sign in/sign out structure and put some data in the database
  * Rails New (postgresql)
  * add gems (better_errors, binding_of_caller, annotate, table_print, pry-rails, byebug)
  * webpack.config.js
  * install react, redux, etc. in package.js
  * create models
    * User
    * Language
    * Node
    * Word
  * create controllers
    * api/users
    * api/sessions
    * api/languages
    * api/nodes
    * api/static_ages
  * configure server routes
  * set up frontend folder
  * seed database with at least one language, two nodes, and 15 words in each node for testing
  * style sign in/sign up page
  * review phase 1
  * **redux frontend authentication**

  <h4> **Phase 2**: Selecting a language to learn (1 day) </h4>
  **Objective**: Allow users to check boxes indicating which languages they want to learn and have the state update accordingly
  * ChooseLanguage component
    * LanguageChoices component
  * selector to get list of language names
  * LanguageMiddleware
    * intercepts dispatch to requestLanguages and sends back a list of the language names
  * LanguageReducer
    * takes a receiveLanguages dispatch and updates the state accordingly
  * create actions for requesting and receiving languages
  * send requests to API and send JSON back
  * NextButton sends user to tree page for first language in state
  * style choose language page
  * review phase 2

  <h4> **Phase 2**: Tree page, part 1 (1 day) </h4>
  **Objective**: Get tree page to display
  * create tree component
  * style tree page
  * style nav bar
