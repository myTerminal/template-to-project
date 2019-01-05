# template-web-webpack

## Layout

- Blank out *README.md* and mention the right project name and mark the file as incomplete
- In file *configs.json*, origin would be either
  - `'/'` for web applications running under their own domain
  - `'/liquid/'` for web applications hosted in a group like as on GitHub
- Update *package.json* with all references of project name and remove any dependency that would not be required
  - Properly update the `main` field with starter file
  - Update the `repositories`, `bugs` and `homepage` fields if hosting outside GitHub
  - Update the `keywords` field with correct keywords
  - Remove the scripts `start`, if not required
- Update or remove the *starter.js* file depending on whether is needs one
- Update the variable called `sourceDir` in *webpack.common.js*, *webpack.dev.js* and *webpack.prod.js*
  - Check for startup file name and extension
  - Verify and remove all loaders and static files mentioned
  - Check if `publicPath` under `output` is correct and whether it needs to be updated
- Check if *data* directory is required under *source*
- Make a reminder to update the *favicon.ico* file under *src* directory
- Make a reminder to update icon files under *src* directory
- Update meta tags, title, etc. in *index.html* in *src* directory
- Update details in file *manifest.json* in *src* directory
- Take care of the chores in *scripts* and *styles* directories in *src* directory
  - Update links of attached stylesheets if required
- Try running the application and figure out the required files listed in *sw.js* in *src* directory

## Changing values

- Update the following values as required
  - value of `start_url` in *manifest.json*, to specify the final URL to get manifest information and resources
    - `/` for regular projects
    - `/liquid/` for GitHub hosted projects
  - value of `origin` in *configs.json*, to specify the origin for service workers
    - `/` for regular projects
    - `/liquid/` for GitHub hosted projects
  - value of `publicPath` under `output` in *webpack.common.js* as necessary
    - `/` for regular projects
    - `''` for GitHub hosted projects
