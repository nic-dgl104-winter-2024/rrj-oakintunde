# External Community Contribution Guidelines for selected Project - Part one
## Contributor Covenant Code of Conduct
The Prayer Times Menubar App repository on GitHub has principles for inclusive and courteous behaviour that can be found in the Contributor Covenant Code of Conduct. It fosters an inclusive atmosphere for all participants, regardless of their identities or backgrounds. To promote a cooperative and happy community, this code places a strong emphasis on accountability, constructive communication, and respect for one another. Following this code makes sure that everyone working on the project has a safe and encouraging environment, which improves collaboration and overall development.

## Contribution guidelines
The "Prayer Times Menubar App" repository at https://github.com/b0bdN/prayer-times-menubar-app has concise and understandable contribution instructions. They describe how to contribute, which includes forking the repository, putting changes into a new branch, committing code that complies with coding guidelines, and requesting pull requests. The recommendations also stress how crucial it is to follow the project's code of conduct, test changes rigorously, and provide thorough commit statements. In general, the guidelines encourage a cooperative and structured approach to contributions, making sure that those who make them are aware of the procedures and standards for efficiently improving the Prayer Times Menubar App.

##  Step by Step Procedure to contribute
* You will need a TOKEN from IPinfo.io.
* ```
  // config.js

const TOKEN = 'your.token'
exports.TOKEN = TOKEN

---
// main.js

function geolocation () {
  console.log('Fetch geolocation via IPinfo.io.')
  // NOTE: Enter your TOKEN from IPinfo.io
  const TOKEN = config.TOKEN

  fetch(`https://ipinfo.io/json?token=${TOKEN}`)
    .then(res => res.json())
    .then(json => {
      // console.log(json.ip, json.city, json.country)
      store.setCityCountry(json.city, json.country)
    })
    .catch(err => console.log(err))
}
```
* node-fetch v2.x is used because the ES Modules are not in use in this app.
* Follow these steps to translate the app in your language:
1. Create a folder with the 2 letters of your language in ./locales/
2. Copy this file (./locales/en/translation.json) in your folder

* Note: the words between braces (e.g.:{{api}}) shouldn't be translated.
### Available translations:
* Arabic 
* বাংলা (Bangla)
* English
* Français (French)
* Türkçe (Turkish)
* O'zbek (Uzbek)

## References
* Prayer Times Menubar App ReadMe.md (https://github.com/b0bdN/prayer-times-menubar-app/blob/master/README.md)
* Ipinfo.io - https://ipinfo.io/
* Menubar - https://github.com/max-mapper/menubar
* Node Fetch - https://nodejs.org/dist/latest-v18.x/docs/api/globals.html

# Community Code Contribution Information - Part one

## Project - Prayer Times Menubar App
## About Prayer Times Menubar App
With the help of the Prayer Times Menubar App, you can easily view the precise times of prayer based on the location of your city. It provides several features to improve customisation and user experience, including:
1. **Actual Times from Any Location:** With precision and dependability guaranteed, the software calculates prayer times in real time for any location.
2. **Custom Calculation Method:** Following their inclinations or religious precepts, users can alter the calculation technique or the angles for the Fajr and Isha prayers.
3. **Create Custom Methods:** Users can also customise their approaches by changing the times of various prayers to meet their requirements.
4. **Show extra Times:** The app shows extra times like Imsak, Sunrise, and Midnight in addition to prayer times. 
5. **Dark and Light Mode:** The application provides users with the option to select their favourite theme or utilise either the dark or light mode, which defaults to the system settings.
6. **Geolocation:** By inputting their city and country in the settings box, users can quickly configure their location. For convenience, the software supports alpha-2 code ISO 3166 or complete country names.
7. **Geolocation Button:** Using the IPinfo.io API, the app retrieves the user's nation and city via the geolocation button, guaranteeing precise prayer times based on the user's current location. This function needs to be connected to the internet.
8. **Keyboard Quick Links:** Keyboard shortcuts are available in the program for easy access and use, such as a global shortcut (Ctrl or Cmd + Alt + P) to easily display or hide the application.

* Up to 50k queries per month are permitted under the ipinfo.io Free plan, which is used by the app. This guarantees unrestricted access to precise prayer times for users.

All things considered, the Prayer Times Menubar App helps people with their regular prayer routines by providing a user-friendly design, customisable choices, and accurate computations. The [Prayer Times Menubar App](https://github.com/b0bdN/prayer-times-menubar-app/tree/master?tab=readme-ov-file) allows you to get further into the app and view its source code.

# Contribution Details
## Forked Repository link - Prayer times menubar app

## Choose Issue - More clarity on what including compodoc does?

## Issue Labels

## Detailed Explanation of Issue

## Work Done

## Code Review and Outcome

## Reflection on Success

## Next Steps

## Project Contribution Links

# Community Code Contribution Information - Part two

## Project - Pattern Library

## About Pattern Library

## Contribution Details - Issue 1

## Forked Repository link - Pattern Library

## Selected Issue 1 - Add Java Template Method for Design Pattern 

## About selected Issue 1

## Contributors


## Work Done


## Old pull request outcome

## New Pull Request


## Code Review and Outcomes

## Reflection on success

## Contribution Details - Issue 2

## Forked Repository link - Php Strategy Design Pattern 

## Selected Issue 2 - Write the definition of the Template pattern in README.md

