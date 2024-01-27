[![tests](https://github.com/kevinquillen/ddev-meilisearch/actions/workflows/tests.yml/badge.svg)](https://github.com/kevinquillen/ddev-meilisearch/actions/workflows/tests.yml)

## About this add-on

[Meilisearch](https://www.meilisearch.com/) is a flexible and powerful user-focused search engine that can 
be added to any website or application.

This DDEV add on adds Meilisearch as a local service.

<img width="1723" alt="Screenshot 2024-01-27 at 11 15 42 AM" src="https://github.com/kevinquillen/ddev-meilisearch/assets/362176/958ae356-3254-43bf-99b6-59f6368712c2">

## Installation

With DDEV installed, run this command:

`ddev get kevinquillen/ddev-meilisearch`

## Configuration

The Meilisearch container is reached at hostname: "meilisearch", port: 7700.

Outside the container, you can visit `127.0.0.1:7700/health` in your browser to verify health status.

The default API key for Meilisearch is `ddev`. You can provide your own by 
adding to `.ddev/.env` in your project, and adding the `MEILI_MASTER_KEY` variable:

`MEILI_MASTER_KEY=my_master_key_value`

## Admin Dashboard

This DDEV addon also includes the admin dashboard by Ricco Xie:

https://github.com/riccox/meilisearch-ui

The admin dashboard is useful to navigate your collections, schema, and debug your search.

You can access the admin dashboard by navigating to this URL in your browser:

`http://meilisearch.(DDEV_HOSTNAME):8100`

To login, provide the configured API key, `127.0.0.1` as the hostname, and 
`7700` as the port.

# Drupal and Search API

If you are using Drupal, you can use Search API and the [Search API 
Meilisearch](https://www.drupal.org/project/search_api_meilisearch) 
modules to connect to the running Meilisearch instance.

**Originally Contributed by [kevinquillen](https://github.com/kevinquillen)**
