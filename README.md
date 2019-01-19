# DeveloPassion's Website

This is the code behind DeveloPassion's official Website: https://www.developassion.be.

## Build

-   execute `yarn install`
-   execute `npm run build` to run the development version locally
-   execute `npm run build:prod` to build the production version (put under public/)

GraphiQL: http://localhost:8000/___graphql

## Publish

-  execute `npm run deploy`

## Metadata

Adapt metadata.js

## Conditions

-   Add new PDF to `static`
-   Adapt metadata
-   Update `terms.tsx`

## Images

Loaded through GraphQL with Gatsby Image. Generates various sizes etc automatically.

Plugin used:

-   https://www.gatsbyjs.org/packages/gatsby-image/
-   https://codebushi.com/using-gatsby-image/
-   https://using-gatsby-image.gatsbyjs.org/
-   https://www.gatsbyjs.org/packages/gatsby-plugin-sharp/

SVGs:

-   Under `src/assets/images/svg`
-   Loaded using a require call and a specific Webpack loader (requires a tslint ignore)

## TODO

-   Remove path prefix once domain available: package.json deploy script, gatsby-config.js
-   Find solution for the Loading (StaticQuery) issue when using StaticQuery for contact and footer pages
    * https://github.com/gatsbyjs/gatsby/issues/6350
    * https://github.com/gatsbyjs/gatsby/issues/5473
    * https://github.com/gatsbyjs/gatsby/issues/10098
    * https://github.com/gatsbyjs/gatsby/issues/10016
-   i18n
    ** https://www.npmjs.com/package/gatsby-plugin-i18n
    ** https://www.npmjs.com/package/react-intl
-   Add news support
    ** https://github.com/gatsbyjs/gatsby-starter-blog
    ** markdown support with remark: https://github.com/gatsbyjs/gatsby/tree/master/examples/using-remark
    \*\* inspiration: https://github.com/scttcper/gatsby-casper (reading time, tag page, subscribe, author page)
    \*\* https://www.npmjs.com/package/gatsby-remark-responsive-iframe
-   GDPR and privacy policy

Blocked by domain acquisition:

-   Enable GH pages: https://github.com/DeveloPassion/website/settings
-   Create GH pages branch
-   Build: push public/ to GH pages branch
-   Sec headers (CloudFlare)
-   Google analytics: gatsby-plugin-google-analytics

Blocked by Gatsby:

-   CSP: https://github.com/gatsbyjs/gatsby/issues/10890
-   PWA
    ** https://www.gatsbyjs.org/docs/add-offline-support-with-a-service-worker/
    ** https://github.com/gatsbyjs/gatsby/issues/10036

Other:

-   Continue Lighthouse audit: https://developers.google.com/web/tools/lighthouse/
-   Check pagespeed: https://developers.google.com/speed/pagespeed/insights/
-   Check structured data: https://search.google.com/structured-data/testing-tool/u/0/
-   Add GreenKeeper
-   Improve 404, add image
    ** link \*** import {Link} from 'gatsby';
    \*\*\* <Link to="/" className="logo"><strong>DeveloPassion</strong></Link>
-   SEO: https://www.gatsbyjs.org/docs/add-seo-component/
-   Add testing: https://www.gatsbyjs.org/docs/testing/
-   Add typechecking for graphql queries: https://www.gatsbyjs.org/docs/static-query/
    \*\* do it using io-ts
-   Add "tslint-sonarts", to tslint.json once this is fixed: https://github.com/AdamLeBlanc/gatsby-plugin-ts-loader/issues/2
    -   and adapt package.json tslint script
    -   and remove tslint-npm.json
-   add keyboard support on services page (go from one block to the next): https://www.npmjs.com/package/react-hotkeys
-   Condense a bit (reduce top/bottom margins on desktop)
