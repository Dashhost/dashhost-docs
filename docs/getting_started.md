# Getting Started

## Open Dashhost's dashboard

Dashhost is a flutter web app running within Dashhost. Visit [https://my.dashhost.app/](https://my.dashhost.app/) to get started.

## Creating your account

### Github Sign-up / Sign-in
Dashhost currently supports signup with Github only. Simply click on the `Sign in with Github` button to create your account. You'll be prompted to agree to our Terms & Conditions and Privacy Policy. 

Dashhost only requests read-only access to your email address personal information for account creation.

### Email Sign-in
Note: there is a `Login with Email & Password` option, but this is only for existing accounts.

## Adding your first app


### Connect Repo(s)
Just click the `New App` button which will bring you to the list of your repos. Then click the `Connect Repo(s)` button to beging the process. You'll be redirected to Github where you can choose specific repo(s) from your account.

### Choose Repo
You'll be redirected back to the previous screen where you can select the repo of your choice (since you may have connected multiple). 

### Choose Branch
Select the branch you wish to use. It default to your repo's default main branch (which is generally main or master) but you can choose any branch.

### App Settings
Be sure to set your flutter version accordingly. You can find out what version you are using locally by running `flutter --version` in your console. These settings can be changed at anytime, so don't worry!

### Deploy?
If you have a fairly simple app, you can just click `Deploy Now` but keep in mind, if you app requires any additional build commands and/or environment variables, it's better just to click `Maybe Later` so you can fine-tune your settings.

Either way, you'll be redirected to the app detail screen where you can see a summary of your app with some options that these docs will cover in greater detail as your read along.

#### Primary Actions
* `Edit`: Edit your app's settings
* `Duplicate App`: Create a new instance of your app connected to a different branch.
* `Deploy Now`: Trigger a manual deploy

#### Latest Deployment
Shows the most recent and/or active deployment. You can click on it to review the logs in realtime. You can also click `View All` (if there is at least one) to view a history of your deployments.

#### Magic Routes
Dashhost's secret sauce. More to follow on this topic of course.

### View Your App
Assuming your deploy went through successfully, you can visit your app using the following url pattern: `https://{YOUR_APP_SLUG}.dashhost.app`. There is also a button in the top right corner to launch your app's link in a new domain.