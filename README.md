# Introduction 
Effortlessly set up and deploy interactive ChatGPT UIs (built in Next.js) on IIS with seamless Microsoft authentication integration.

# Getting Started
After going through following steps you will have fully working app.
1.	Download code
2.	Open repo in your favorite code editor (for me MS code)
3.	Run npm i to install all dependencies of project
4.	Run npm run dev to test its working fine locally
5.	Run npm start to run it on custom server
6.	Now for deployment on IIS, first configure your IIS server
7.	Replace your openAI key in .env.local
8.	Create your app in azure portal through which you want authorize your organization user access,  get client id and tenant id, and redirect uri (this should be same as you mentioned in azure app registration portal) here in services/msal.ts file.
9.	You have option to use google authentication as well, you can do this by simply replacing in # Google GOOGLE_API_KEY=YOUR_API_KEY GOOGLE_CSE_ID=YOUR_ENGINE_ID  env.local file.

10.	Next we have to install few packages
•	Rewrite URL from here (https://www.iis.net/downloads/microsoft/url-rewrite)
•	IIS node from (https://github.com/tjanczuk/iisnode)

Your deployment requirements are completed, now on IIS manager create a simple site and its physical path refer a deployment folder with following files and folders
•	Web.config
•	.next (folder)
•	Node_module(folder)
•	Server.js file
•	next-i18next.config


# Build and Test
TODO: Describe and show how to build your code and run the tests. 

# Contribute
A big shout to 
- https://github.com/mckaywrigley/chatbot-ui
- https://www.youtube.com/watch?v=HLsx0iraA-Y
