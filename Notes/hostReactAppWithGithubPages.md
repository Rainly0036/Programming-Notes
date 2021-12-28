## Host a React App With Github Pages
### Note
Im using visual studio code (IDE) and windows 10.
<br /> <br />

### Start
1. Open a repo in github
2. Open the folder where you want to host your React App
3. Open VSC terminal 
4. Run the following command in terminal:
```
git init 
git remote add origin <YOUR-GITHUB-REPO-LINK>
git add -A
git commit -m "Initial commit"
git push -u origin master
```
5. Add this text in your `package.json` file:
```
"homepage": "https://[USERNAME].github.io/[YOUR REPO NAME]",
```
6. Run the following command in terminal:
```
npm install gh-pages --save-dev
```
7. Change this text to your `package.json` file:
**Original**
```
"scripts": {
    "start": "react-scripts start",
    "build": "react-scripts build",
    "test": "react-scripts test",
    "eject": "react-scripts eject"
},
```
**New**
```
"scripts": {
    "predeploy": "npm run build",
    "deploy": "gh-pages -d build",
    "start": "react-scripts start",
    "build": "react-scripts build",
    "test": "react-scripts test",
    "eject": "react-scripts eject"
},
```
8. Commit all your file and push to your repo
9. Run the following command in terminal:
```
npm run deploy
```
10. Open github and go to your repo. Click on the `Settings` tab and click on the `Pages` tab.
11. Change the source from `none` to `gh-pages`
![Images](./Assets/source.jpg)
12. Run the following command in terminal:
```
npm run deploy
```

### End 
Now you can see your react app in this websites
: `https://[USERNAME].github.io/[YOUR REPO NAME]`

Any problem, please contact me at Discord
Discord Tag: `Rainly36#0306`
