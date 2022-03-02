[**Technote**](https://technote.giligar.xyz)

A personal tech blog, developed using the [Hugo](https://gohugo.io/) static site generator and deployed on [Netlify](https://www.netlify.com/)

[![Netlify Status](https://api.netlify.com/api/v1/badges/1c523bf5-c4ad-47a0-9e38-ce2db3b964e3/deploy-status)](https://app.netlify.com/sites/zen-euclid-cb1235/deploys)

Development

1. Install Hugo and add hugo to system/user environment variable
2. Clone the repo
3. Start the server with file watcher and hotreload using `hugo server -D -w -v`

Deploy to prefered CDN

1. Start with building it using `hugo`
2. It will build content and theme into html content and save it on `public` directory
3. Push it to prefered CDN

Deploy to Netlify

1. Push the code Github/Gitlab or keep it locally at your own risk!
2. Setup Netlify by adding project from Github/Gitlab or upload directly
3. Once deploy complete, you will get netlify subdomain where you can open the project

Create new post: using `hugo new post/post_file_name.md`

License: MIT