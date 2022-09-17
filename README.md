# Zoom Apps JavaScript Sample

This Zoom App Sample uses Node.js + Express to build a simple Hello World Zoom App.

1. Go to [zoom develop page](http://marketplace.zoom.us/develop)
2. Click on `Zoom Apps`
3. Enter App Name and select your preferred distribution and continue.
4. You will now be redirected to your apps page where you need to fill additional details. Lets park that for now.
5. Go back to this app and run `npm install`
6. Run `ngrok http 3000`
7. Copy the generated ngrok url. Should look like `https://xxx.ngrok.io`
8. Go back to te page from step 4.
9. Paste the url from step 7 into the field `Home URL`
10. Create a `.env` file on the root of this project.
11. It should have the contents

```shell
ZM_CLIENT_ID="<ur zoom client id from step 8>"
ZM_CLIENT_SECRET="<ur zoom client id from step 8>"
ZM_REDIRECT_URL="ur ngrok url from step 7/auth"
```

12. Go back to page from step 8 and fill redirect url for oauth. Should look like `https://xxx.ngrok.io/auth`
13. You can ignore the `production` section for now
14. You can fill the same value from step 12 in the oauth allow list field
15. Add the domains to the allow lists - `appssdk.zoom.us` & `xxx.ngrok.io`
16. Ignore the warning because of using ngrok url. Click continue
17. Fill ur develop information and click continue
17. Click `Add API's` under the zoom sdk section.
18. Enable `shareApp` feature and click done.
19. Click continue to go to the next section
20. Add `zoomapp:inmeeting` scope if needed and click continue
21. You should now be at the test app locally page with the add button enabled. Wait let go back to the app and run `npm run start`
22. Do not click the add button from the previous page. It doesn't generate a state value in the url which breaks the app.
23. Instead go to the install path via ur ngrok url. Should look like `https://xxx.ngrok.io/install`
24. You should now be redirected to a window asking u to open/install ur app on ur zoom client.
25. Hopefully ur client is open now showing `Hello Zoom`
