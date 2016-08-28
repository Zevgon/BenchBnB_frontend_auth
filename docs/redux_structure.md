<h2> Auth Cycles </h2>
<h4> Session API requests </h4>
  * sign in
    * invoked from AuthForm onSubmit of SignInButton
    * sends a post request to api/sessions
    * callback set as receiveCurrentUser
  * sign out
    * invoked from SignOutButton on nav bar
    * sends a delete request to api/sessions
    * callback set as removeCurrentUser
  * sign up
    * invoked from AuthForm onSubmit of SignUpButton
    * sends a post request to api/users
    * callback set as receiveCurrentUser
  * fetchCurrentUser
    * invoked from AuthForm on componentDidMount
    * sends a post request to api/sessions
    * callback set as receiveCurrentUser

<h4> Session API responses </h4>
  * receiveCurrentUser
    * invoked as callback from request
    * the SessionReducer puts the current_user in the state
  * removeCurrentUser
    * invoked as callback from request
    * the SessionReducer removes the current_user from the state

<h2> Language Cycles </h2>
<h4> Language API requests </h4>
  * fetchAllLanguages
    * invoked from ChooseLanguage onSubmit
    * GET /api/languages is called
    * callback set as receiveAllLanguages
  * fetchUserLanguages
    * invoked from profile's LanguageIndex on componentWillMount
    * GET /api/users/:userId/languages is called
    * callback set as receiveUserLanguages
  * fetchLanguage
    * invoked from StudyButton in profile
    * GET /api/users/:userId/languages/:languageId is called
    * callback set as receiveLanguage

<h4> Language API responses </h4>
  * receiveAllLanguages
    * invoked as callback from request
    * the LanguageReducer puts selected languages in the state
  * receiveUserLanguages
    * invoked as callback from request
    * the LanguageReducer puts selected languages in the state
  * receiveLanguage
    * invoked as callback from request
    * LanguageReducer puts selected language in the state

<h2> Node Cycles </h2>
<h4> Node API requests </h4>
  * fetchNodes
    * invoked from Nodes in componentDidMount
    * GET /api/language/:languageId/nodes is called
    * callback set as receiveNodes
  * fetchNode
    * invoked from Node in onClick
    * GET /api/language/:languageId/node/:nodeId is called
    * callback set as receiveNode

<h4> NodeAPI responses </h4>
  * receiveNodes
    * invoked as callback from request
    * the NodeReducer sets the language.nodes portion of the tree
  * receiveNode
    * invoked as callback from request
    * the NodeReducer puts the selected node in the language.nodes portion of the tree
