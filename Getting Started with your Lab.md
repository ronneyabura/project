# Getting Started with your Lab Sandbox

## What tools are already installed in this environment?
- Ruby 2.7
- Rails 7.0.3
- sqlite3 
- libsqlite3-dev
- Git version 2.25.1 & gh command line tool (for Github commands): https://cli.github.com/

## How can I execute code through the terminal and command line?
1. First, open Terminal: Navigate to your VSCode menu >> Terminal >> New Terminal 
(or use the shortcut Shift + CTRL + `)
2. You will run most of your Ruby code in the terminal for this course as you follow along with your instructors.

## How can I execute my code through the VSCode editor?
1. Ensure all of your code files have the appropriate file extension type.
2. To execute your code >> right click on file name >> Run code 
   or navigate Run >> Run without Debugging in your VSCode menu

## How can I push my Ruby App code to a Github Repository?
You can use Github's command line tool,  <a href="https://cli.github.com/">gh cli</a> to push your code to Github.
This is preinstalled in your lab sandbox environment. 

#### Preparing Git within Github:
1. To use this, you'll first need to set up a developer token
within your Github account to allow for appropriate authentication. You can do this through the <a href="https://docs.github.com/en/authentication/keeping-your-account-and-data-secure/creating-a-personal-access-token">instructions listed here on Github's site. </a> Please keep your token handy as you'll need it momentarily. 
Please also set minimum "scopes" of `repo`, `read:org`, and `workflow`.

#### Preparing Git within your Lab Sandbox:
2. Next authenticate your Github account within your lab. `Open Terminal -> New Terminal`
3. Type `gh auth login` and follow the prompts provided, inputting the following options:
- What account do you want to log into?: `GitHub.com`
- What is your preferred protocol for Git operations?: `HTTPS`
- Authenticate Git with your GitHub credentials: `Yes`
- How would you like to authenticate GitHub CLI: `Paste an authentication token`
- Paste your authentication token: `Copy/Paste this from your Github account Developer Settings at https://github.com/settings/tokens`

1. Create your app folder and `git init` within it.
2. After making changes to your app follow the `git add .` `git commit -m "your commit message"` and `git push` flows.
3. When you push you may be asked to set global git config values. For this, choose your Github user email and user name.


## The following commands are used frequently in this course and are provided for your reference: 

- Please click on **Terminal** and click on **New Terminal** for typing your commands.

- To create a new Rails project, please use:
```
rails new <app>
```
> Note: Here, 'app' is the name of the project that will be created

**Please run all the below commands in the app root directory**

- To install the gems specified in the Gemfile, please use:
```
bundle install
```

- To check the gems installed, please use:
```
bundle check
```

- Please use the below command to start the server & view your app.
```
rails server
```
> Note: The Rails server home page may appear different from the one shown in the course videos.
This is due to differences in an upgraded Rails version. You can proceed further correctly without any issues.
Please note that there have also been other changes to Ruby and Rails commands where we'd recommend 
referencing Ruby documentation if you hit any errors. One example is that `rake routes` has converted to `rails routes`

- Please use the below command to apply migrations to your database
```
rake db:migrate
he below command to run any new Ruby files that you create. Here the file name is '<your_filename.rb>'.
```
ruby <yourfilename>.rb
```

- There are 2 different commands for using a Ruby shell:

1. For opening a general Ruby interpreter shell/command line:
```
irb
```
2. To manipulate your Rails app using the shell/command line:
```
rails console
```

- To see the Rake tasks available, please use:
```
rake -T
```

- If you face any errors while running the 'rake routes' command, you can use the below one instead:
```
rails routes
```

#### View your Ruby App quickly in VSCode's built-in Live Server Extension:
- Click on the ***Browser Preview*** Icon from the left menu of the lab environment.
- A browser preview window will open for you.
- Please start your server using either ***rails server*** or ***rails s***. 
- Please enter your server running path ie. **localhost:3000** on the address bar to see the app home page.
- You can navigate to the other app routes from here by adding the respective routes.

### Viewing your lab files within a new Browser Tab Preview (for full access to Browser Developer Tools):
- ***Important!*** Before running the app, please run the below command in the app root directory for setting the route URL:
```
export ROOT_URL=http://localhost:3000/serve/
```
- Please start your server using either ***rails server*** or ***rails s***. This will set the app to run at:  **http://localhost:3000/serve/**

> Note: **If you wish to run the app at http://localhost:3000 like earlier, please enter the below command in the terminal:**
```
export ROOT_URL=http://localhost:3000/
```
- Input the following in your URL browser toolbar:
```
https://<your lab id>.labs.coursera.org/serve
```
> **Note: Please replace <your lab id> with the lab ID value that you see after clicking on the "Help" icon from the top of the Lab frame.**

- You can preview your web page content using the following path- https://<your lab id>.labs.coursera.org/serve/ in a new browser tab by adding the routes.
eg:  If you create a scaffold with the path '/posts' please enter the following route in the new browser tab:
```
https://<your lab id>.labs.coursera.org/serve/posts
```
You can fully access the dev tools on your local system browser as above.

## How can I create an ERD Diagram in this Lab?
To draw an ERD diagram there is an extension installed in VSCode with the name "ERD Editor". 
Follow the steps below to create an ERD diagram:

1. Under the project folder create a file with name <file name>.vuerd.json 
(A sample file test.vuerd.json is added under project folder for your reference.)
1. Open this json file with ERD editor by right clicking on this file and selecting "Open ERD Editor".
2. To add any component in the file >> Navigate to ERD editing area >> right click >> add the component required. To learn more about the ERD Editor extension visit - https://marketplace.visualstudio.com/items?itemName=dineug.vuerd-vscode

