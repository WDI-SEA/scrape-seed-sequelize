# Scrape and Seed using Sequelize

This lab uses the project created in the [data scraping lesson](https://gawdiseattle.gitbooks.io/wdi/content/02-js-jquery/js-data-scraping/readme.html).

---

## Storing the Scraped Data

So you can run the `gethoods.js` file and output the data in the console, but what if we want to store this data for later use?

### 1. Set up sequelize
* install `pg`, `pg-hstore`, and `sequelize`
* create a database called `seattlehoods`
* configure database in `config.json` file

### 2. Create neighborhood model
* `name:string`
* `link:string`
* `photo:string`
* `description:string`

### 3. Run the migration

### 4. Store scraped data

In `gethoods.js`:
* import your models
* inside the callback of the `request`, after getting the data, use a `forEach` loop on the `neighborhoods` array to write each neighborhood to your `neighborhoods` table.
* run this file and check postico to see if the data populated correctly

---

## Use this data in an Express App

You now have a database of Seattle Neighborhoods, let's use it! Turn this project into an Express app.

Your app should include:
* **Home View:** A landing page that welcomes you to the website and has an `explore seattle` link that takes you to the index view.
* **Index View:** A list of Seattle Neighborhoods with a text input box that functions as a search/filter (like your dinosaurs app). Each neighborhood in the list should have an "explore" button that links to the show view for that neighborhood.
* **Show View:** A page that displays the neighborhood name, photo, description, and link to the seattle neighborhoods website page corresponding to that neighborhood.

## Let's get CRUDdy

Add a **New Neighborhood** view that has a form for users to enter their own made-up neighborhood. Make sure to create a `POST` route that posts the new neighborhood data to the database.
