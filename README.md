Not Found Cacher
================

A simple cacher module for ProcessWire that's caches the contents for the 404 page (since ProCache doesn't support that).

Installation
------------

Do these in your project's composer.json:

1) Add `"AvoineOy/notfoundcacher": "dev-master"` to your requires

2) Add the repository as follows:

```
  "repositories": [
    {
      "type": "vcs",
      "url": "https://github.com/AvoineOy/notfoundcacher"
    }
  ],
```

3) Add these scripts:
```
    "scripts": {
      "post-install-cmd": [
        "rm -fr public/site/modules/NotFoundCacher",
        "mkdir -p public/site/modules/NotFoundCacher",
        "cp vendor/AvoineOy/NotFoundCacher/NotFoundCacher.module public/site/modules/NotFoundCacher"
      ],
      "post-update-cmd": [
        "rm -fr public/site/modules/NotFoundCacher",
        "mkdir -p public/site/modules/NotFoundCacher",
        "cp vendor/AvoineOy/NotFoundCacher/NotFoundCacher.module public/site/modules/NotFoundCacher"
      ]
    },
```

4) Add /public/site/modules/NotFoundCacher to .gitignore
