Auth Cycles
  Session API requests
    sign in
      invoked from AuthForm onSubmit of SignInButton
      sends a post request to api/sessions
      callback set as receiveCurrentUser

    sign out
      invoked from SignOutButton on nav bar
      sends a delete request to api/sessions
      callback set as removeCurrentUser

    sign up
      invoked from AuthForm onSubmit of SignUpButton
      sends a post request to api/users
      callback set as receiveCurrentUser

    fetchCurrentUser
      invoked from AuthForm on componentDidMount
      sends a post request to api/sessions
      callback set as receiveCurrentUser

  Session API responses
    receiveCurrentUser
      invoked as callback from request
      the SessionReducer puts the current_user in the state

    removeCurrentUser
      invoked as callback from request
      the SessionReducer removes the current_user from the state

Language Cycles
  Language API requests
    fetchLanguages
      invoked from ChooseLanguage onSubmit
      GET /api/languages is called
      callback set as receiveLanguages

  Language API responses
    receiveLanguages
      invoked as callback from request
      the LanguageReducer puts selected languages in the state

Node Cycles
  Node API requests
    fetchNodes
      invoked from Nodes in componentDidMount
      GET /api/language/:languageId/nodes is called
      callback set as receiveNodes

    fetchNode
      invoked from Node in onClick
      GET /api/language/:languageId/node/:nodeId is called
      callback set as receiveNode

  NodeAPI responses
    receiveNodes
      invoked as callback from request
      the NodeReducer sets the language.nodes portion of the tree

    receiveNode
      invoked as callback from request
      the NodeReducer puts the selected node in the language.nodes portion of the tree
