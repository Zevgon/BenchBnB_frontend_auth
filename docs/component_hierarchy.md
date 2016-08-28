<h3> AuthFormContainer
  * AuthForm

<h3> ChooseLanguage
  * LanguageChoice
  * NextButton

<h3> NodeContainer
  * ProgressBarContainer
    * ProgressPiece
  * ForeignWord
  * GuessField
  * CheckButton

<h3> ProfileContainer
  * LanguageIndex
    * LanguagePercentage
    * StudyButton

<h3> TreeContainer
  * LanguageHeader
  * Stats
  * Nodes
    * Node

<h3> NavBar



# Routes
| Path | Component     |
| :------------- | :------------- |
| '/sign-up-sign-in' | AuthFormContainer |
| '/users/:userId/choose' | ChooseLanguage |
| '/users/:userId/languages/:languageId/node/:nodeId' | NodeContainer |
| '/users/:userId/profile' | ProfileContainer |
| '/users/:userId/languages/:languageId' | TreeContainer |
