# Apps built using web map config versus programmatic config

Read more about these apps in the following blog articles:

- [Good, better, best—Simplify your web app development with Map Viewer](https://www.esri.com/arcgis-blog/products/js-api-arcgis/developers/good-better-best-simplify-your-web-app-development-with-map-viewer/)
- [Web maps—the foundation of ArcGIS web applications](https://www.esri.com/arcgis-blog/products/js-api-arcgis/developers/web-maps-the-foundation-of-arcgis-web-applications/)

This repo contains 3 versions of the same application with different approaches to how the data is configured.

1. [js-only](https://ekenes.github.io/portal-vs-scratch/js-only.html) - This app builds an app using only the core ArcGIS JS API. All configurations for symbology, popups, map layers, etc. are made inline in JavaScript. This approach is not scaleable as the config code is verbose and is not easily shared between apps.
2. [viewer-only](https://ekenes.github.io/portal-vs-scratch/viewer-only.html) - This is the same app as `js-only`, except all map configurations were made in ArcGIS Online's Map Viewer. They are saved as a web map portal item and loaded using a portal item id. This makes the configuration easily shareable and easy to load in multiple applications. App layout is also handled using web components, making this code more clean and concise.
3. [item-with-slider](https://ekenes.github.io/portal-vs-scratch/item-with-slider.html) - This app builds on the `viewer-only` app, by adding a time slider component for exploring how the data changed over time. It starts with loading a web map using map components, then uses the core ArcGIS JS API for adding the customizations.
