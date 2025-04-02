Deployed to stat541.visruth.com (Cloudflare Pages) and uses Github Actions to render the site.

Need to clean up the rendering pipeline. Currently, what happens is

push commit -> GHA renders site (static files generated) && Cloudflare renders push (w/o the updated static files) -> GHA pushes static website -> Cloudflare renders GHA's push (initial push's changes are finally rendered and deployed to the web)