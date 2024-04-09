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
## Forked Repository link - [Prayer Times Menubar App](https://github.com/b0bdN/prayer-times-menubar-app/)
## Issues - [Opened and Available Issues](https://github.com/b0bdN/prayer-times-menubar-app/issues)

## Issue Labels
* Enhancement
* New feature
* Help wanted
* First issue

## Detailed Explanation of Issue
There are a few issues that have been worked on in the issue directory and some were stated in the repository readme.md like creating more language translations and getting reminders before prayer time.
On this issue: https://github.com/b0bdN/prayer-times-menubar-app/issues/4 You can let the method .toLocaleTimeString() get the default locale in store.js. To do this, you have to use an empty array: .toLocaleTimeString([], options)
If the local is needed, you can add a new argument to the function getTableTimings(). You'll have to add this argument before calling the function in main.js. You can use app.getLocale() in main.js to get the current locale.
```
// store.js
const getTableTimings = (locale, newMonth, newDate) => {...}

// main.js
const initData = () => {
  // ...
  const locale = app.getLocale()
  const tableTimings = store.getTableTimings(locale)
  // ...
}
```
In addition to the notifications, we can add an option to have the Adhan. Thanks to AlAdhan.com for providing us with adhans in MP3 format.
Here is the link: https://aladhan.com/download-adhans
Here's what we need:
* a checkbox to enable/disable the sound
* Options to choose between the different Adhans.
* The Adhan should be triggered at the same time as the notification

## Work Done
* I Forked and cloned the project to my machine.
* After that, I establish a new branch with the name oakintunde to work on the issue.
* Did research about using node fetch, renderer.js and ipinfo.io for node projects which were provided as references.
* Then after, I create a subfolder in locales with the name in the folders "pa, it and ng" and add everything relevant to the topic.
* Also, I made a contribution file under the name "contribution.md" to describe my contribution to this work.
* Then I commit and push all the content to GitHub.

## Code Review and Outcome
Code quality, consistency, and adherence to best practices are ensured via code review, which is an essential component of software development. The way that Basit Awofeso reviewed your documentation shows that you are working together to make improvements. You can improve readability and offer useful insights by including "Real-world examples" in your README, such as node-fetch and ipinfo for Angular projects. This procedure encourages ongoing learning and development within the development community in addition to validating your work. Robust and user-friendly software solutions are finally produced through transparent and cooperative code review and behaviour.

## Reflection on Success
Making a contribution to the Prayer Times Menubar App's GitHub issue proved to be beneficial. The app's accessibility was expanded by me by adding support for the Yoruba languages spoken in Nigeria, Italy, and Pakistan. By integrating node-fetch, the user experience was improved by the smooth reminders of prayer times. The utilisation of Aladhan.com's RESTful Prayer Times API guaranteed precise and current prayer timings. This fruitful effort enhanced functionality and added new language options, making the software more dependable and accessible for users all over the world. It made a significant impact on the app's capabilities by demonstrating the strength of creativity and teamwork in open-source development.

## Next Steps
My curiosity motivates me to conduct further research to develop a deeper understanding of this subject as I learn more about it. Moreover, my goal is to implement it so that I may personally witness its actual results.

## Project Contribution Links
* Project link - [Prayer Times Menubar App](https://github.com/b0bdN/prayer-times-menubar-app)
* Forked Repository - [Prayer Times Menubar App](https://github.com/oakintunde/prayer-times-menubar-app/tree/oakintundeDGL104PrayerTimesApp)

# Community Code Contribution Information - Part two
## Project - [Pattern Library](https://github.com/nic-dgl104-winter-2024/pattern-library)
## About Pattern Library
The "DGL 104 Pattern Library," includes implementing common software design patterns and describing architecture patterns in various programming languages. Contributions must adhere to open-source project standards, including pull request submissions and issue management for students to contribute and learn.

## Contribution Details - [Issue 1](https://github.com/nic-dgl104-winter-2024/pattern-library/issues/67)

## Forked Repository link -[ Pattern Library](https://github.com/oakintunde/pattern-library/tree/oakintunde)
## Selected Issue 1 - Add Javascript implementation of Strategy pattern
## About selected Issue 1
The GitHub issue intends to add a JavaScript implementation of the Strategy pattern to improve the project's usefulness. Development will be more flexible and scalable thanks to this improvement, which will also improve the maintainability and organisation of the code. The project may better separate its concerns and facilitate dynamic algorithm selection at runtime by applying the Strategy pattern, which will also increase its adaptability to changing requirements.

## Contributors
* ting-dev-coder Ting Yu Chen
* 8968sam Sam
* manasvi111
* and some unassigned contributors

## Work Done
* I choose this problem, apply some labels to it, fork it, and clone it into my machine.
* I then created a distinct workspace named "java template method" where I worked on this particular issue.
* I have submitted two pull requests for this issue: one for my solo effort and the other for the collective work.
* We got together, discussed the criticism of our initial pull request, and worked on the necessary adjustments to produce a new one.
* Then I pushed the work to Github after committing it.

## Code Review and Outcomes
Reviewing the code with Basit, Alina, and Swathy:
1. Examined the Strategy pattern's JavaScript implementation.
2. Verified that the code adhered to coding standards and was readable.
3. The merits of better code organisation and flexibility were discussed.
4. Potential duplication and optimisation opportunities were addressed as cons.
5. Efficiency-enhancing suggestions.
6. Worked together to guarantee code quality and handle problems.
Results: - Improved comprehension of JavaScript's Strategy pattern.
Enhanced code structure and quality.
- Improved cooperation and teamwork abilities.

## Reflection on success
Using JavaScript to implement the Strategy design pattern was a reflection of my development journey's success. Algorithms were divided into distinct classes and dynamic switching between them was allowed to make the code more scalable, adaptable, and manageable. The short lines of code showed the value of encapsulation and abstraction, improving code readability and cutting down on redundancy. This implementation revealed that design patterns are a useful tool for resolving complex issues and also enhanced the organisation of the codebase. It was a worthwhile educational experience that helped me develop reliable and effective software solutions.

## Contribution Details - [Issue 2](https://github.com/nic-dgl104-winter-2024/pattern-library/issues/68)

## Forked Repository link - [Php Strategy Design Pattern](https://github.com/oakintunde/pattern-library/tree/oakintunde/php_strategy_pattern) 

## About Strategy Design Pattern
A behavioural design pattern called the Strategy Design Pattern lets you define a family of algorithms, package them all, and make them interchangeable. The algorithm can change independently of the clients using it thanks to this pattern. The Strategy Pattern in PHP is very helpful for detaching algorithms from their clients or for constructing algorithms that can be changed at runtime.
This is a thorough explanation of the PHP Strategy Design Pattern:
### Goal:
* Specify a group of algorithms, package them all, and ensure that they may be used interchangeably. Differentiating the algorithm from the environment in which it is used is up to the clients.
The strategy algorithms' interface or abstract class is declared by the following participants:
* Strategy Interface/Abstract Class. It describes a technique or group of techniques that The tangible tactics will be put into practice.
* Concrete Strategies: Provides particular algorithm implementations for the Strategy interface/abstract class.
* Context: Contains a pointer to the abstract class/interface for strategy. It enables the client to dynamically transition between various strategies.
Example of Implementation: Suppose we have a payment system in which many payment modalities (strategies) are interchangeable.
* Interface for Strategy:
```
interface PaymentStrategy {
    public function pay(float $amount): void;
}
```

* Concrete Strategies:
```
class CreditCardPayment implements PaymentStrategy {
    public function pay(float $amount): void {
        // Implement credit card payment logic
    }
}

class PayPalPayment implements PaymentStrategy {
    public function pay(float $amount): void {
        // Implement PayPal payment logic
    }
}
```

* Context:
```
class PaymentContext {
    private $paymentStrategy;

    public function __construct(PaymentStrategy $paymentStrategy) {
        $this->paymentStrategy = $paymentStrategy;
    }

    public function setPaymentStrategy(PaymentStrategy $paymentStrategy): void {
        $this->paymentStrategy = $paymentStrategy;
    }

    public function processPayment(float $amount): void {
        $this->paymentStrategy->pay($amount);
    }
}
```

* **Usage:**
```
// Create payment strategies
$creditCardPayment = new CreditCardPayment();
$payPalPayment = new PayPalPayment();

// Initialize context with default payment strategy
$paymentContext = new PaymentContext($creditCardPayment);

// Process payments using different strategies
$paymentContext->processPayment(100); // Uses credit card payment
$paymentContext->setPaymentStrategy($payPalPayment);
$paymentContext->processPayment(50); // Uses PayPal payment
```

## The advantages of the strategy pattern
* Flexibility: Strategies don't need to update the client code to be added, removed, or altered during runtime.
Code management and maintenance are facilitated by the encapsulation of each method.
* Decoupling: By separating context and client code from particular algorithm implementations, code modularity and reusability are encouraged.
* Testability: The process of testing can be improved by the ability to test strategies separately.

By separating algorithms from their usage, offering flexibility, and encouraging code reuse, the Strategy Design Pattern in PHP, in general, helps to create a clear and manageable code structure.

## Selected Issue 2 - Develop PHP Strategy Design Pattern
* **Sign up page**
```
<?php
class SignUpForm {
    public function handleSignup(User $user, $username, $password) {
        $user->signup($username, $password);
    }
}
?>
```
* **Login Form**
```
<?php
class LoginForm {
    public function handleLogin(User $user, $username, $password) {
        $user->login($username, $password);
    }
}
?>
```

* **Index.php**
```
<?php
include_once 'User.php';
include_once 'strategies/EmailPasswordStrategy.php';
include_once 'strategies/SocialLoginStrategy.php';
include_once 'LoginForm.php';
include_once 'SignUpForm.php';

// Create user instance
$user = new User();

// Set email/password authentication strategy
$user->setAuthenticationStrategy(new EmailPasswordStrategy());

// Handle login using email/password
$loginForm = new LoginForm();
$loginForm->handleLogin($user, 'user@example.com', 'password');

// Set social login authentication strategy
$user->setAuthenticationStrategy(new SocialLoginStrategy());

// Handle login using social login
$loginForm->handleLogin($user, 'socialuser', 'socialpassword');

// Handle signup
$signupForm = new SignUpForm();
$signupForm->handleSignup($user, 'newuser@example.com', 'newpassword');
?>
```

* **User.php**
```
<?php
include_once 'strategies/AuthenticationStrategy.php';

class User {
    private $authenticationStrategy;

    public function setAuthenticationStrategy(AuthenticationStrategy $strategy) {
        $this->authenticationStrategy = $strategy;
    }

    public function signup($username, $password) {
        // Mocking signup logic
        echo "User signed up successfully.\n";
    }

    public function login($username, $password) {
        // Using the selected authentication strategy to authenticate
        if ($this->authenticationStrategy->authenticate($username, $password)) {
            echo "User logged in successfully.\n";
        } else {
            echo "Login failed. Invalid credentials.\n";
        }
    }
}
?>
```

## References
* Project link - [Pattern Library](https://github.com/nic-dgl104-winter-2024/pattern-library)
* Forked Repository link -[Pattern Library](https://github.com/oakintunde/pattern-library/tree/oakintunde)
* Forked Repository link - [Php Strategy Design Pattern](https://github.com/oakintunde/pattern-library/tree/oakintunde/php_strategy_pattern) 
* Issue 1 - [Add Javascript implementation of Strategy pattern](https://github.com/nic-dgl104-winter-2024/pattern-library/issues/67)
* Issue 2 - [Php Strategy Design Pattern](https://github.com/nic-dgl104-winter-2024/pattern-library/issues/68)
