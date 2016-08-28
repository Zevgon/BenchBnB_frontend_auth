<h3> AuthFormContainer
  * AuthForm

<h3> ChooseLanguage
  * LanguageChoices
  * NextButton

<h3> NodeContainer
  * ProgressBarContainer
    * ProgressPiece
  * ForeignWord
  * GuessField
  * CheckButton

<h3> ProfileContainer
  * LanguageListContainer
    * LanguagePercentage
    * StudyButton

<h3> TreeContainer
  * LanguageHeader
  * Stats
  * Nodes
    * Node




# Routes
| Path | Component     |
| :------------- | :------------- |
| '/sign-up-sign-in' | AuthFormContainer |
| '/users/:userId/choose' | ChooseLanguage |
| '/users/:userId/language/:languageId/node/:nodeId' | NodeContainer |
| '/users/:userId/profile' | ProfileContainer |
| '/users/:userId/language/:languageId' | TreeContainer |
