# Google Fonts Attribution

The [Google Fonts API](https://developers.google.com/fonts/docs/developer_api) doesn't include license or copyright information which is frustrating if you want to programmatically include this information in your application.

- https://github.com/google/fonts/issues/2799

This repo include a small script that scrapes the Google Fonts [attribution page](https://fonts.google.com/attribution) and loads it into a JSON object. The format closely resembles the official API.

## Installation

```
bundle install
```

## Usage

```
irb
require './google-fonts-attribution'
GoogleFontsAttribution.new.execute
```

## Sample

```JSON
{
  "kind": "webfonts#webfontList",
  "items": [
    {
      "family": "ABeeZee",
      "license_name": "SIL Open Font License, 1.1",
      "license_url": "http://scripts.sil.org/OFL",
      "copyright": "Copyright (c) 2011 by Anja Meiners, with Reserved Font Name 'ABeeZee'"
    },
    {
      "family": "Abel",
      "license_name": "SIL Open Font License, 1.1",
      "license_url": "http://scripts.sil.org/OFL",
      "copyright": "Copyright (c) 2011, Matthew Desmond (http://www.madtype.com | mattdesmond@gmail.com), with Reserved Font Name Abel."
    },
    {
      "family": "Abhaya Libre",
      "license_name": "SIL Open Font License, 1.1",
      "license_url": "http://scripts.sil.org/OFL",
      "copyright": "Copyright (c) 1996-2015 Pushpananda Ekanayake (pushpanandae@gmail.com) Copyright (c) 2015 Sol Matas (sol@sonnenshine.com.ar) Copyright (c) 2015 Mooniak (hello@mooniak.com)"
    }
  ]
}
```
