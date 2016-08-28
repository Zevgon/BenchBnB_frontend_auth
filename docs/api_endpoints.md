<h2> HTML endpoints </h2>
  * Root
    * ```GET / ``` triggers React components to load

<h2>  JSON endpoints </h2>
  * Users
    * ```POST /api/users```
    * ```GET /api/users```
  * Session
    * ```POST /api/sessions```
    * ```GET /api/sessions```
    * ```DESTROY /api/sessions```
  * Languages
    * ```GET /api/languages```
    * ```GET /api/users/:userId/languages```
    * ```GET /api/users/:userId/languages/:languageId```
  * Nodes
    * ```GET /api/languages/:languageId/nodes```
      accepts node[language_id] as a param
    * ```GET /api/languages/:languageId/nodes/:nodeId```
      accepts node[language_id] and node[id] as params
