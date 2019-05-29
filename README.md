# NewsScraper

This app utilizes MongoDB/mongoose to store web-scraped articles and respective notes and comments a user may make on the article. It also uses express for routing and cheerio for DOM manipulation.

The intended usage for the app was a forum-like implementation, where an article could be linked to numerous notes, all of which could be edited and deleted. Due to time constraints, the multiple notes per article feature was not implemented. Additionally, there is a bug where clicking an article after a note has been deleted from it will result in the note text fields to note show up momentarily.

To implement the multi-note feature, a check could be done to see if a note exists. If a note already exists, present that note for editing, but then append a blank note field to accept a new note.

Currently, the app route /scrape must be visited to scrape the article data into the MongoDB, but the ideal app would use axios and cheerio on app load to scrape the articles.
