# portfolio-react





## Notes
### General Q&A
1. What is the purpose of 
   1. tsconfig.json?
      - Answer: 
   2. tsconfig.app.json?
   3. tsconfig.spec.json?
   4. angular.json?
   5. package and package-lock.json?
   6. Node.js and npm?

### React Pre-Req

### React notes
1. to start a new react application


### Typescript and Javascript Notes

### Django notes

### Host React App on GitHub
1. Make sure the app is ready for prod by building it.
2. Install `gh-pages` package <br>
`npm install --save-dev gh-pages`
3. Update `package.json` <br>
   1. Add a homepage field: <br>
   ```json
   {
       "homepage": "https://srt-developer.github.io/portfolio-react/"
   }
   ```
   2. Add deployment scripts
   ```json
   {"scripts": {
        "predeploy": "npm run build",
        "deploy": "gh-pages -d build" //publishes build directory to gh-pages branch
   }}
   ```
4. Create a Production build <br>
Run the build command to create a production build of your React app: <br>
`npm run build` <br>
5. Deploy to GitHub Pages <br>
Deploy your app to GitHub Pages using the following command: <br>
`npm run deploy` <br>
This command will: <br>
   - Create a gh-pages branch in your repository (if it doesn’t exist).
   - Push the contents of the build directory to the gh-pages branch. <br>
6. Enable GH Pages
   1. Go to Github repo
   2. Click on Settings tab
   3. Scroll down to Github Pages section
   4. Under "Source", select main branch and /docs folder.
   5. Click Save
7. Access site
   1. After few minutes, site is hosted on <br> 
   `https://developer-srt.github.io/portfolio-react/`
8. Troubleshooting
   - 404 Error: If you encounter a 404 error when navigating directly to a route (e.g., https://<username>.github.io/<repository-name>/about), 
   - you may need to create a 404.html file that redirects all unknown routes to index.html. This is similar to the Angular setup.
   - Ensure Repository Name Matches: The homepage field in your package.json must match the exact name of your repository.