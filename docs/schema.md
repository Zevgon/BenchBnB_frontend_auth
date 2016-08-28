Users
  column          data type         details

  id              integer           null: false
  username        string            null: false
  password_digest string            null: false
  session_token   string            null: false

Languages
  column          data type         details

  id              integer           null: false
  name            string            null: false

UsersLanguages
  column          data type         details

  user_id         integer           null: false
  language_id     integer           null: false

Nodes
  column          data type         details

  id              integer           null: false
  title           string            null: false
  language_id     integer           null: false, indexed
  completed       boolean           null: false, default: false
  unlocked        boolean           null: false, default: false

Words
  column          data type         details

  id              integer           null: false
  word            string            null: false
  translation     string            null: false
  node_id         integer           null: false, indexed
  completed       boolean           null: false, default: false
  unlocked        boolean           null: false, default: false
