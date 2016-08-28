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
<h4> **Phase 1**: Setup (1 day) </h4>
  **Objective**: Have a functioning app with a styled splash page
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
  * style splash page
  * push to Heroku
  * review phase 1

<h4> **Phase 2**: Frontend Authentication (1 day) </4>
  **Objective**: Have a functioning sign-in/sign-up structure
  * password protection
  * session
    * SessionMiddleware
    * SessionReducer
  * edit application layout for user persistence

<h4> **Phase 3**: Selecting languages (1 day) </h4>
  **Objective**: Allow users to check boxes indicating which languages they want to learn and have the state update accordingly
  * ChooseLanguage component
    * LanguageChoice components
      * store choices in their own states
  * selector to get list of language names
  * LanguageMiddleware
    * intercepts dispatch to requestAllLanguages and sends back a list of the language names
  * LanguageReducer
    * takes a receiveLanguages dispatch and updates the state accordingly
  * create actions for requesting and receiving languages
  * NextButton sends user to tree page for first language in state
  * style choose language page
  * review phase 2

<h4> **Phase 4**: Tree page and nav bar (1 day) </h4>
  **Objective**: Get tree page to display, be able to click on nodes and go to node page, and have nav bar
  * Tree component
    * triggers fetchNodes request in componentWillMount
  * LanguageHeader subcomponent
  * Node subcomponents
  * set onClick on all nodes to send user to proper page (regardless of unlocked status for now)
    * dispatches fetchNode request
    * put placeholder content for node page
  * NodeMiddleware
    * catches requestNode and requestNodes dispatches
  * NodeReducer
    * catches receiveNode and receiveNodes dispatches
  * style tree page
  * create and style nav bar
    * Profile onClick sends user to profile page
    * LogOut onClick logs out user
  * review phase 2

<h4> **Phase 5**: Profile (1 day) </h4>
  **Objective**: Display languages that the user is learning and have a button next to each one that sends the user to the corresponding language tree
  * ProfileContainer
    * LanguageIndex component
      * triggers fetchUserLanguages in componentWillMount
      * onClick of items dispatches fetchLanguage request
  * style profile page
  * review phase 4

<h4> **Phase 6**: Node page (1 day) </h4>
  **Objective**: Have a styled node page
  * NodeContainer
    * ProgressBarContainer
      * ProgressPiece component
    * ForeignWord component
    * GuessField component
  * style node page
  * review phase 6
  * revisit previous phases and clean up

<h4> **Phase 7**: Finishing touches (3 days) </h4>
  **Objective**: Have a bug-free, visually pleasing web application!
  * Fix any remaining bugs
  * Touch up styling
  * Add bonus features
    * Be able to progress through questions in nodes
    * Be able to create custom nodes
    * Use Google API to translate custom content
