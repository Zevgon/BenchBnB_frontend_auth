<h2> HTML endpoints </h2>
  * Root
    * `GET / ` triggers React components to load

<h2>  JSON endpoints </h2>
  * Users
    * `POST /api/users`
    * `GET /api/users`
  * Session
    * `POST /api/sessions`
    * `GET /api/sessions`
    * `DESTROY /api/sessions`
  * Trees
    * `GET /api/trees`
    * `GET /api/users/:userId/trees`
    * `GET /api/users/:userId/trees/:treeId`
  * Nodes
    * `GET /api/trees/:treeId/nodes`
      accepts node[language_id] as a param
    * `GET /api/trees/:treeId/nodes/:nodeId`
      accepts node[language_id] and node[id] as params
