```javascript
//
//
//
===> install nodemon as a dependecy and not globally by doing ==> npm install nodemon
===> go to google and search 'node gitignore' copy the gitignore code from their Github then create a gitignore file in your
        backend folder and paste all you copied from there.
===> create a procfile with a capital P 'Procfile' and insert the following line of code ==> web: node ./index.js
===> create a .env file '.env' and put your secret keys and the rest e.g

        PORT = 5000
        MONGOBD_URL = mongodb+srv://kelvintony:qwertyuiop@cluster0.ql55m.mongodb.net/project-x?retryWrites=true&w=majority

===> in the script object of the package.json write only this code ==> "start": "nodemon index.js"
===> add this piece of code in your index.js to know if the server has been deployed properly

        //this displays when we hit the home route of the deployed server
        app.get('/', (req, res) => {
            res.send('Welcome to netrone blog');
        });

===> Remember to save everything
===> login and create an account in heroku, => 'click on new' to add a create new project, => 'click on settings' 
        => 'Reveal Config Vars', add environmental variables appropriately
        e.g KEY:  MONGOBD_URL
            VALUE: mongodb+srv://kelvintony:qwertyuiop@cluster0.ql55m.mongodb.net/project-x?retryWrites=true&w=majority
        NB: if there are other environment variables like api key, put everything here.

===> then go back and click on 'deploy', download and install 'heroku CLI For windows', in your terminal run
        => npm install -g heroku, run this to check if the CLI is installed properly => 'heroku --version'
        it should show you the version if installed properly
===> make sure you are already logged in the browser
===> type this following commands in the terminal from the deploy tab you entered:

        => heroku login
        => git init
        => heroku git:remote -a backend-test-2 //this is the name of the project you created so choose your own project name
        => git add .
        => git commit -am "make it better"
        => git push heroku master

===> Done!!!
===> you can copy the url and replace in your frontend.



