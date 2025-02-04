## How to Add a Sitemap to Next.js App

To add a sitemap to your Next.js application, you can follow these steps:

1. Install the `next-sitemap` package by running the following command:

   ```bash
   npm install next-sitemap
   ```

2. Create a `next-sitemap.config.js` file in the root of your project with the following content:

   ```javascript
   module.exports = {
     siteUrl: <your_site_name>,
     generateRobotsTxt: true,
   };
   ```

3. Building sitemaps

   In your package.json add build script to generate sitemap.

   ```javascript
   {
       "build":"next build",
       "sitemap":"next-sitemap --config next-sitemap.config.js"
   }

   ```

4. In your `next.config.js` file, add the following code to enable the sitemap generation:

   ```javascript
   const withSitemap = require("next-sitemap");

   module.exports = withSitemap({
     sitemap: {
       hostname: <your_site_name>,
     },
   });
   ```

5. Run your Next.js application and verify that the sitemap is generated by visiting `https://sitename.com/sitemap.xml`.

That's it! You have successfully added a sitemap to your Next.js application.

Hope this helps!
