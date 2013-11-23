# Heroku Buildpack Bower

A simple buildpack, designed to run with the [multi buildpack](https://github.com/ddollar/heroku-buildpack-multi),
which will run install bower and run `bower install`.

## Usage

1. Set your buildpack to the [multi buildpack](https://github.com/ddollar/heroku-buildpack-multi):

   ```bash
   $ heroku config:set BUILDPACK_URL=https://github.com/ddollar/heroku-buildpack-multi
   ```

2. Configure your `.buildpacks` file:

   ```
   https://github.com/heroku/heroku-buildpack-nodejs
   https://github.com/ejholmes/heroku-buildpack-bower
   ```

3. Ensure that npm installs bower:

   ```json
   {
     "dependencies": {
       "bower": "latest"
     }
   }
   ```
