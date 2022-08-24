```javascript
//
//
===> STEP 1:
//
//
===> SIMPLY BACKEND SERVER

=> First do " npm init " to intialize repository, " npm install -g nodemon " you have to install this once and not install again
=> Packages installed ==> npm install express morgan cors mongoose
=> In the package.json, add this to the script==> "dev":"nodemon index.js"
=> also in the same package add ==> "type": "module", this enables you to do import statment
=> Then to start up server you do ==> npm run dev

=> Not really necessary, NB: one thing i saw Dave Gray do is that he installed nodemon as a dev dependency...
		And you do that by doing ===> npm install nodemon -D

===> start of index.js ||

		import express from 'express';
		import cors from 'cors';
		import morgan from 'morgan';
		import mongoose from 'mongoose';

		const app = express();

		app.use(morgan('dev'));
		app.use(express.json({ limit: '30mb', extended: true }));
		app.use(express.urlencoded({ limit: '30mb', extended: true }));
		app.use(cors());

		const PORT = 5000;

		app.listen(port, () => {
			console.log(`server is running on port ${PORT}`);
		});

		app.get('/', (req, res) => {
			res.send([
				{
					name: 'Victor Ekon',
					program: 'full stack web development',
					period: '3 months'
				},
				{
					name: 'Aisha Tilbert',
					program: 'full stack web development',
					period: '3 months'
				},
				{
					name: 'Godwin Gate',
					program: 'full stack web development',
					period: '3 months'
				}
			]);
		});

===> End of index.js ||
//
// Test
//Test2
