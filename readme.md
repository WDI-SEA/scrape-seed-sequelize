# Scrape and Seed using Sequelize

This lab uses the project created in the [data scraping lesson](https://gawdiseattle.gitbooks.io/wdi/content/02-js-jquery/js-data-scraping/readme.html).

## Storing the Scraped Data

So you can run the `gethoods.js` file and output the data in the console, but what if we want to store this data for later use?

### 1. Set up sequelize
* install `pg`, `pg-hstore`, and `sequelize`
* create a database called `seattlehoods`
* configure database in `config.json` file

### 2. Create neighborhood model
* `name:string`
* `link:string`

### 3. Run the migration

### 4. Store scraped data

In `gethoods.js`:
* import your models
* inside the callback of the `request`, after getting the data, use a `forEach` loop on the `neighborhoods` array to write each neighborhood to your `neighborhoods` table.
* run this file and check postico to see if the data populated correctly
