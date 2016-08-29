<h2> Users </h2>

| column    | data type | details |
| :------------- | :------------- | :------------- |
| id | integer | null: false |
| username | string | null: false |
| password_digest | string | null: false |
| session_token | string | null: false |

<h2> Languages </h2>

| column    | data type | details |
| :------------- | :------------- | :------------- |
| id | integer | null: false |
| name | string | null: false |

<h2> UsersLanguages </h2>

| column    | data type | details |
| :------------- | :------------- | :------------- |
| user_id | integer | null: false |
| language_id | integer | null: false |

<h2> Nodes </h2>

| column    | data type | details |
| :------------- | :------------- | :------------- |
| id | integer | null: false |
| title | string | null: false |
| language_id | integer | null: false, indexed |
| completed | boolean | null: false, default: false |
| unlocked | boolean | null: false, default: false |

<h2> Words </h2>

| column    | data type | details |
| :------------- | :------------- | :------------- |
| id | integer | null: false |
| word | string | null: false |
| translation | string | null: false |
| node_id | integer | null: false, indexed |
