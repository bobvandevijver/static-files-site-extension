# Enable common static files for Azure App Service

By default some common static files (site.webmanifest, *.woff2, *.woff and *.ttf) are not served by IIS in Azure App Service. This extension simply add MIME types for these font files.

This will work with:

* *.webmanifest
* *.woff2
* *.woff
* *.ttf

# How to add this extension

Locate your **App Service** in Azure portal, in the blade, you'll find the "Extensions" tab, in the right pane, click "Add", find "Enable Static Web Files", click OK. Then **restart App Service**, that's it.

When using ARM, you can add this extension by adding the following to your template:
```
  {
      "name": "App",
      "apiVersion": "2018-02-01",
      "type": "Microsoft.Web/sites",
      "resources": [
        {
          "name": "AzureAppServiceStaticFiles",
          "type": "siteextensions",
          "apiVersion": "2018-02-01",
          "dependsOn": ["App"]
        }
      ]
    }
```

# Credits

This repository was forked from https://github.com/johnnyqian/enable-font-awesome-site-extension and extended to also support some other types.
