# [TOPIC 1.2] SERVERLESS CLOUD DEPLOYMENT WALKTHROUGHS

## [A] INFORMATION & DOCUMENTATION

**SERVERLESS / STATIC HOST:** Cloudflare Pages - https://pages.cloudflare.com/:

  - Cloudflare Pages on Vite deployment: https://developers.cloudflare.com/pages/framework-guides/deploy-a-vite3-project/

  - Vite & Cloudflare Pages hosting: https://vitejs.dev/guide/static-deploy.html#cloudflare-pages-with-git

&nbsp;

## [B] BASIC STEPS

**1. Create new Local Repo & Publish to GitHub**

  - Using GitHub Desktop, Add or Create New **LOCAL** Repo from your existing portfolio project

  - One Git setup, publish the repo to GitHub

  - Set the GitHub repo to private, unless you are happy for code to be viewed by anyone!

&nbsp;

**2. Sign up to Cloudflare, Login to Dashboard & Navigate to Pages section**

&nbsp;

**3. Create a New Project via GitHub**

  - Create a new project & connect to Git provider (*allow access to all GitHub repos*)

  - Select the Repo you wish to deploy & hit "Setup"
  
  - **NOTE:** You can just give it access to one, but you may choose to change in future, so access to ALL gives more flexibility

&nbsp;

**4. Setup your deploy settings**

  - Preset framework: N/A (*no Vite preset*)

  - Build command: `npm run build`

  - Build output directory: `/dist`

  - **IMPORTANT:** You need to set the node version, as default Cloudflare is 12.18.0.  We are currently at 18.16.0.  

    - Check your node version in CLI: `node -v`

    - Set the Environmental Variable to this node version: `NODE_VERSION` to `<YOUR VERSION>` (e.g. `18.16.0`)

  - Hit Save & Deploy (*no need for OTHER ENVs or Root configs for this static site*)

&nbsp;

**5. Build your Site**

  - You can watch it build in the in-browser terminal

  - Review your dashboard & domain settings after setup as well (see `Explore settings` & `Set up custom domain` link)