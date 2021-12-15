## Sigma Shopify Boilerplate app

### Setup steps:
1. Download and setup `ngrok`: https://dashboard.ngrok.com/get-started/setup
2. Run ngrok with command from the folder you downloaded `./ngrok http 8080` or use any free port
3. Go back to repo and run `npm install`
4. While packages installing, go back to ngrok console and copy the next url, i.e. `https://a829-188-190-227-143.ngrok.io` from the last line. Pay attention to which port url is associated, i.e. `https://a829-188-190-227-143.ngrok.io -> http://localhost:8080`
5. Paste copied url to `.env` file to the field `SHOPIFY_APP_URL`
6. Go to `https://partners.shopify.com/` and create new app with the name you want
7. It the field App URL place your ngrok link `https://a829-188-190-227-143.ngrok.io`. And in Allowed redirection URL(s) field place your url + `/auth/callback`, i.e. `https://a829-188-190-227-143.ngrok.io/auth/callback`
8. After app is created go to its page in partners website and find the next two lines `API key` and  `API secret key`. Place them into `SHOPIFY_API_KEY`  and  `SHOPIFY_API_SECRET` fields in `.env` file, respectively.
9. In console click `shopify login` and login to the store you want to install the app
10. When you logged in successfully run in the console command `npm run dev`. If this command running without errors, you should see `> Ready on http://localhost:8080` message.
11. Go to the partners website. Select Stores section and Log In to the store where app will be installed.
12. Go back to the partners website. Select Apps section and click on your app.
13. At the bottom, you should see the section `Test your app`, click the `Select Store` button
14. Select the store you previously logged in and click `Install App` then in appeared modal `Install Unlisted App`
15. If the proccess finished successfully you will see opened app in your store with 'Hello!' message.