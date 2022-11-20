# modify_requirements_file

Add a personal access token to your requirement.txt file in build phase.

# Usage
1- create your personal access token in your Github account 
you can use: https://docs.github.com/en/authentication/keeping-your-account-and-data-secure/creating-a-personal-access-token

2- Add the buildpack to your Heroku app:
```
$ heroku buildpacks:add https://github.com/Ashraf-Khaled-BE/modify_requirements_file.git -i 1
```
Keep in mind that the buildpack order is important. If you'll specify this buildpack after your default one (e.g. heroku/nodejs) it'll not work.
See https://devcenter.heroku.com/articles/using-multiple-buildpacks-for-an-app for details.

3- Set GITHUB_AUTH_TOKEN to Your Personal access token from github :
```
$ heroku config:set GITHUB_AUTH_TOKEN=<your personal access token from github>
```

4- Deploy Your App!
