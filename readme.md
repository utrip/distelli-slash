#Distelli-Slash
Build, test and deploy your app entirely from Slack w/ the Slash command: `/distelli`.
![Alt text](http://try.distelli.com/hubfs/slack.gif)

##Installation:

###Setup within Distelli
1. Fork this repository.
2. Log into Distelli and create a new Distelli application named **DistelliSlash** (https://www.distelli.com/username/app/new).
3. If you haven't done so already, connect a GitHub account.
4. Connect your application to your forked repository.
5. Create an environment named **DistelliSlash-Prod**, add a server to that environment.
6. Update the first line of your distelli-manifest.yml file to use your Distelli username instead of **distelli** and push the repository.
7. Build your application **DistelliSlash**.
8. Add a server and deploy the latest release of **DistelliSlash** to environment **DistelliSlash-Prod**.
9. Create an apiToken. (https://www.distelli.com/username/settings?section=API)
10. Create the following environment variables on environment **distellislash-prod**: `USERNAME=your-userName` & `APITOKEN=your-apiToken` (https://www.distelli.com/username/envs/distellislash-prod)

###Setup within Slack
1. Navigate to https://username.slack.com/services/new/slash-commands
2. In the choose command textbox, enter **/distelli** and hit the green **Add Slash Command Integration** button.
3. In the URL textbox, enter the IP you deployed your app to with **:3000** at the end to specify port 3000.

It should look something like this when you're done:
![Alt text](https://monosnap.com/file/IEcnSl09wWXPaHDTEAMpPpXxBXqayz.png)

##Things you can do:
1. `List Apps`: List all apps associated with your Distelli account. Use the command `List Apps After [AppName]` to see the next page of results.
2. `List Builds`: List all builds associated with your Distelli account. Use the command `List Builds After [BuildNum]` to see the next page of results.
3. `List Servers`: List all servers associated with your Distelli account. Use the command `List Servers After [ServerName]` to see the next page of results.
4. `List Servers for Env [EnvName]`: List all servers associated with an app enviroment.
5. `List Releases for App [AppName]`: List all releases associated with an app.
6. `Create App [App Name]`: Create a Distelli application.
7. `Create Env [Env Name]`: Create a Distelli environment.
8. `Restart Env [Env Name]`: Restart an existing environment.
9. `Latest release for app [appName]`: Get information on the latest release associated with an app.
10. `Deploy latest to env [envName]`: Deploy the latest release to an environment.

Shoot me an email (alex at distelli.com) if you need a hand with setup!
