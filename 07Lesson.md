{% include "/header.md" %}

# Lesson Seven - Site Migration

Students Will...
* Understand how to make a successful Wordpress Site Migration

## Key Questions
* How do I move a wordpress build without taking down a website?
* How do I move a sql database from local to live?
* What Plugins Should I use to prepare myself for it?



## Demonstration
Before You Get Started Make Sure you Have
* FTP Login for hosting account
* SQL Login for mySQL server


1. Download and back up the current website, files and sql.
2. Upload the new website to a directory on the hosting site.
3. Export and Migrate your sql database using WP Migrate.
4. set up a new sql database on the sql server.
5. change the sql database info in the wp-config file
6. add a directory for the old website.
7. move the old website into the old director folder
8. move the new website directory contents into the main directory.


## Tips for a Successful Migration
1. Never do it during the day.(unless your on WP engine)
2. Evening migrations should happen on Thursday or Friday
3. Back up the original locally as well as on the server
4. Know where the website is going - triple check your install, passwords and sql
5. **Delete nothing** from the server just move files

# Project
Buy hosting and set up a website and migrate a website to your hosting. it can be on a sub domain if you already have one.

{% include "/footer.md" %}
