[![tests](https://github.com/kevinquillen/ddev-meilisearch/actions/workflows/tests.yml/badge.svg)](https://github.com/kevinquillen/ddev-meilisearch/actions/workflows/tests.yml)

## Installation

Uses the current stable release of the Meilisearch Docker image.

With DDEV installed, run this command:

`ddev get kevinquillen/ddev-meilisearch`

## Configuration

The Meilisearch container is reached at hostname: "typesense", port: 8108.

Outside of the container, you can visit `127.0.0.1:8109/health` in your browser to verify health status.

The default API key for Meilisearch is `ddev`. You can provide your own by 
adding to `.ddev/.env` in your project, and adding the `TYPESENSE_API_KEY` variable:

`TYPESENSE_API_KEY=my_api_key_value`

## Admin Dashboard

This DDEV addon also includes the admin dashboard by bfritscher:

https://github.com/bfritscher/typesense-dashboard

The admin dashboard is useful to navigate your collections and schema and debug your search.

You can access the admin dashboard by navigating to this URL in your browser:

`http://meilisearch.(DDEV_HOSTNAME):8109/#/login`

To login, provide the configured API key, `127.0.0.1` as the hostname, and `8108` as the port. Leave the path blank.

# Drupal and Search API

If you are using Drupal, you can use Search API and the Search API Meilisearch 
modules to connect to the running Meilisearch instance.

**Originally Contributed by [kevinquillen](https://github.com/kevinquillen)**
