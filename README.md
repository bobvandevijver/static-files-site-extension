# Enable common static files for Azure App Service

By default some common static files (site.webmanifest, *.woff2, *.woff and *.ttf) are not served by IIS in Azure App Service. This extension simply add MIME types for these font files.

This will work with:

* site.webmanifest
* woff2
* .woff
* .ttf

# How to add this extension

Locate your **App Service** in Azure portal, in the blade, you'll find the "Extensions" tab, in the right pane, click "Add", find "Serve common static files", click OK. Then **restart App Service**, that's it.

# Credits

This repository was forked from https://github.com/johnnyqian/enable-font-awesome-site-extension and extended to also support some other types.
