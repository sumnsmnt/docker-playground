# Build a Compose File For a Multi-Container Project
----------------------------------------------------
In this compose file I use 2 images to create 2 containers. 1 for Drupal which will be used for creating a CMS website and another one is Postgres which will be used to store the data.

To access the website on the Drupal container I assign port 8080 on my system and a default port of 80 on the drupal container.

docker compose up
ctrl+c

or

docker compose up -d

docker compose down

to delete the volumes as well use,

docker compose down -v
