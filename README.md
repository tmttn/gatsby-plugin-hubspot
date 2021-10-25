# gatsby-plugin-hubspot-tracking

[![Build Status](https://travis-ci.com/tmttn/gatsby-plugin-hubspot-tracking.svg?branch=master)](https://travis-ci.com/tmttn/gatsby-plugin-hubspot-tracking) [![Current npm package version](https://img.shields.io/npm/v/@tmttn/gatsby-plugin-hubspot-tracking.svg)](https://www.npmjs.com/package/@tmttn/gatsby-plugin-hubspot-tracking)

A Gatsby plugin to easily add a HubSpot embed code to your site.

**This repository is originally forked from [hutsoninc/gatsby-plugin-hubspot](https://github.com/hutsoninc/gatsby-plugin-hubspot) and is kept up-to-date with the latest Gatsby version (unlike the original repo).**

## Installing

`npm install --save @tmttn/gatsby-plugin-hubspot-tracking`

## How to use

```js
// In your gatsby-config.js
module.exports = {
  plugins: [
    {
      resolve: "@tmttn/gatsby-plugin-hubspot-tracking",
      options: {
          trackingCode: "1234567",
          respectDNT: true,
          productionOnly: true,
          region: "eu1"
      },
    },
  ]
}
```

## Options

### trackingCode

>Type: `string`  
>Default: `undefined`

*This value is required. Fill in the correct tracking code from your Hubspot account. (Settings > Tracking Code)*

### respectDNT

>Type: `boolean`  
>Default: `false`

*By enabling this option, visitors with "Do Not Track" enabled will have a `__hs_do_not_track` cookie placed in their browser. This prevents the HubSpot tracking code from sending any information for the visitor.*

More information about HubSpot cookies and privacy can be found in the [HubSpot Tracking Code API documentation](https://knowledge.hubspot.com/reports/install-the-hubspot-tracking-code).

### productionOnly

> Type: `boolean`  
> Default: `true`

*Only load the script when `process.env.NODE_ENV` is set to `production`.*

### region

>Type: `string`  
<Default: `undefined`

*Fill in this value if you want to use another region or the tracking script. The default script points to `js.hs-scripts.com/12345678.js` Change the region to `eu1` to point to the eu tracking script: `js-eu1.hs-scripts.com/12345678.js`*

## License

MIT © [Hutson Inc](https://www.hutsoninc.com)
