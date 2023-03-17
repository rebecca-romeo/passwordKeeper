Password Keeper Project
=========

## Project Description
Password Keeper
A storage system for passwords for organizations. An organization, like Lighthouse labs, has many different accounts which need to be shared between users. This app will let an authorized user access all the passwords of the organization. The app will also let a user generate a new password for a specific account (just like LastPass). Users will be able to generate a password based on the options the form will provide. Some of the options are: password length, contains lowercase, contains uppercase, contains numbers, and contains symbols.
If a user needs to log in to a specific website (e.g. Facebook) they can go into the app, find the appropriate password, click a button which copies the password into the clipboard, and log in.

## Final Product

!["screenshot of sign in page"](https://github.com/rebecca-romeo/PasswordKeeper/blob/master/docs/pwk1.png)


!["screenshot of viewing all accounts"](https://github.com/rebecca-romeo/PasswordKeeper/blob/master/docs/pwk2.png)


!["screenshot of adding a new account"](https://github.com/rebecca-romeo/PasswordKeeper/blob/master/docs/pwk3.png)


## Getting Started

1. Create the `.env` by using `.env.example` as a reference: `cp .env.example .env`
2. Update the .env file with your correct local information
  - username: `labber`
  - password: `labber`
  - database: `midterm`
3. Install dependency: `npm i cookie-session`
4. Install dependency: `nnpm i bcryptjs`
5. Install remaining dependencies: `npm i`
6. Fix to binaries for sass: `npm rebuild node-sass`
7. Reset database: `npm run db:reset`
  - Check the db folder to see what gets created and seeded in the SDB
8. Run the server: `npm run local`
  - Note: nodemon is used, so you should not have to restart your server
9. Visit `http://localhost:8080/`

## Warnings & Tips

- Do not edit the `layout.css` file directly, it is auto-generated by `layout.scss`.
- Split routes into their own resource-based file names, as demonstrated with `users.js` and `widgets.js`.
- Split database schema (table definitions) and seeds (inserts) into separate files, one per table. See `db` folder for pre-populated examples.
- Use helper functions to run your SQL queries and clean up any data coming back from the database. See `db/queries` for pre-populated examples.
- Use the `npm run db:reset` command each time there is a change to the database schema or seeds.
  - It runs through each of the files, in order, and executes them against the database.
  - Note: you will lose all newly created (test) data each time this is run, since the schema files will tend to `DROP` the tables and recreate them.

## Dependencies

- Node 10.x or above
- NPM 5.x or above
- PG 6.x
