#  Svelte + Parcel + CI/CD to Github Pages

#### Make your ideas with [Svelte](https://svelte.dev/), [Parcel](https://parceljs.org/), [Github Pages](https://pages.github.com/) and [Github Actions](https://github.com/features/actions)


### Docs
#### Local Dev
1. `yarn` or `npm i`
2. `yarn dev` or `npm run dev`
####  Preparations for autodeployment to [Github Pages](https://pages.github.com/)
1. Create new branch on Github (skip if it's already done)
2. Link remote repo to your local git repo (skip if it's already done)
3. Create empty branch with name **gh-pages** and remove all files in this branch
4. Switch to **master** and update **homepage** and **repository** properties in **package.json**
5. Go to your **Github Developer Settings** -> **Personal access tokens** and create new token for your CD process. Don't forget to check all checkboxes in **repo** section
6. After the key is created, copy it to a safe place, we'll need it
7. After go to the **Your Repo Settings** -> **Secrets** and past value from prev step into **Value** input. Set secret name to **MY_DEPLOY_KEY** (you can use any name but be sure to use your own name in next steps)
8. Go to page of your repo, click on **Github Actions** and click on **Set up a workflow yourself**
9. Copy instructions from **workflow.example.yml** in your repo and update **YOUR_GITHUB_EMAIL**, **YOUR_GITHUB_USERNAME**, **YOUR_REPO_NAME** values. Also update **MY_DEPLOY_KEY** to your own name (if it was changed in prev steps).
10. Commit your changes. Deployment will start soon

Autodeployment will trigger on each push to **master** branch.
After a little while **(be patient)** your application will be available on https://YOUR_GITHUB_NAME.github.io/YOUR_REPO_NAME url.
