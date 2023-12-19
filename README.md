render-frontend-backend
# Render - Frontend &amp; Backend

Based on "How to deploy frontend and backend on Render?" at https://community.render.com/t/how-to-deploy-frontend-and-backend-on-render/7449

# 100 - Introduction

Hi there,

Thanks for reaching out.

[Our docs are full of Quickstart guides for various languages/frameworks](https://render.com/docs), which is often the best place to start.

# 200 - Requirements

# 300 - Building Our Application

Every project is different, so you will know what commands are required to get your app up and running. If you have a frontend and backend in the same repo, that’s a “monorepo” and Render has support for that: Monorepo Support

In general terms - and this may not be specific to your projects - a common pattern for what you’ve described would be to have the frontend app as a Static Site and the backend as a Web Service, using the Node Native Environment. So two services, both linked to the same repo with settings like (but amended to your required values):

A Web Service for the backend

Root Directory: “your_backend_dir”
Build Command: “npm install; npm run build;” (some backends don’t need to be built - will depend on what you’ve built)
Start Command: “node server.js” (or whatever file within “your_backend_dir” that starts your backend app)
A Static Site for the frontend

Root Directory: “your_frontend_dir”
Build Command: “npm run build” (static sites auto-install dependencies)
Publish Directory: “public” (this is Create React Apps default build directory, amend as required for your own project/framework)
Try getting something deployed and if you come across any issues, then reach out for assistance. If doing so, please elaborate on the issue in as much detail as possible, e.g. service name/ID, URLs, any logs/error messages, reproduction steps, screenshots, etc., to show the problem you’re experiencing, and the community may be able to offer advice.

# 400 - Conclusion

Hope that helps

Alan
