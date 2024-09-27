# Build an image from Dockerfile, docker-compose, and run a Multi-Container Project
----------------------------------------------------
I took the reference from the previous project, so the docker-compose file is same, but here I have created a Dockerfile to store all the changes in an image.

In this compose file I use 2 images to create 2 containers. 1 for Drupal which will be used for creating a CMS website and another one is Postgres which will be used to store the data.

To access the website on the Drupal container I assign port 8080 on my system and a default port of 80 on the drupal container.
