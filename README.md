# Cloudinary UI Extension

Uploader for images to [Cloudinary](https://cloudinary.com). 

## What's new in 2.0?
>Version 2.0 includes breaking changes.
* Cloudinary UI extension returns image ID instead of image safe url field.
* You must specify name of the field, that extension will save the image ID into.

## Installation and usage

Check you have the [requirements](https://github.com/contentful/extensions/blob/master/samples/README.md#requirements) needed to use extensions.

You must have:
 * Cloud name
 * Preset name

Optional:
  * Cloudinary Account
  
## Local development

Start a local server, changing the port if needed:

```bash
python -m SimpleHTTPServer 3030
```

Don't use the `extension.json` descriptor file but instead use 3rd party hosting from `localhost`

```bash
contentful extension update --force --src 'http://localhost:3030/index.html' --id cloudinary --name cloudinary --field-types Object -field-types Asset
```

The [same constraints](https://github.com/contentful/extensions/blob/master/samples/README.md#debugging-on-your-local-environment) apply to loading unsafe scripts.

## Using the extension in the Contentful web app

Enable the extension in the Contentful web app for a "JSON Object" field by opening the _Settings_ for a field and selecting the widget in the _appearance_ tab.

Fill fields for _Cloud name_ and _preset_.
