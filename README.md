# Courses Tapestry

This repo contains some experimentations with the [Tapestry Tool](https://www.home.tapestry-tool.com/) - an open source system for building interactive graphs.

Our initial objective with the system was to construct a concept/knowledge graph formed with the courses taught at the Mathematics bachelor's programme at the [Faculty of Mathematics and Computer Science](https://fmi.unibuc.ro/) of the [University of Bucharest](https://unibuc.ro/), to help students understand _what_ they're learning and _why_ they're learning it.

## Setup

Tapestry is designed to work as a plugin for the popular [WordPress](https://wordpress.com/) CMS (Content Management System). You will first need a WordPress-based website hosted somewhere on the internet.

For local development / testing, you can also use WordPress running on your local machine. This repository contains a [Docker Compose](https://docs.docker.com/compose/) file which you can use to easily spin up a WordPress instance:

```bash
docker compose up
```

It will be available at `http://localhost:80`.

The latest built version of the [Tapestry plugin for WordPress](https://github.com/tapestry-tool/tapestry-wp) can be downloaded from [the "Releases" page](https://github.com/tapestry-tool/tapestry-wp/releases) of their GitHub repository. However, the latest beta version has a bug which makes it not work with newer versions of PHP / WordPress. The version contained in this repo is patched.

**Important**: for Tapestry Tool to work properly, you should switch [your permalinks format](https://wordpress.org/documentation/article/customize-permalinks/) to "Post name".

You can then go to the "_Modules_" page in the WordPress admin interface in order to search for and install the "Tapestry" plugin (by uploading the downloaded `.zip` file).

After installing and activating the plugin, you should see a new "Tapestries" section in the left bar. You can start creating tapestries by following [the official guides](https://www.home.tapestry-tool.com/guides).
