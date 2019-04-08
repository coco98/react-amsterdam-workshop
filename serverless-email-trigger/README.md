
### This function does the following:
1. Receives an event from the `profile` table that has an `email_id` column
2. Sends the email via sparkpost using the `SPARKPOST_API_KEY` env var
3. (Optional): Updates the database with knex using the `POSTGRES_CONNECTION_STRING` env var to set the `email_set` column to true

### Requirements
1. Table structure:
  - Table name: profile
  - Columns: `id (any), email_id (text), email_sent (boolean)`
2. Env var: `SPARKPOST_API_KEY`: This is necessary
1. Env var: `POSTGRES_CONNECTION_STRING`: Optional if you want to update the db
