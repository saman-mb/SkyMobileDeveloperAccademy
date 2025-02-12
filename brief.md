# Project Brief
## Sky Go Training Project 
### App Brief
* Build an OTT VOD browsing and streaming app that uses native DRM protection. 
* Native Android and iOS applications
* Share code via a GraphQL service 
* Target architecture MVVM or MVP 
* Build UI using latest APIs (Swift UI / Jetpack Compose)

## Process 

The teams will work using an agile scrum model with 2 week sprints and the usual activities. 

### Sprint Structure

* Planning - [link](https://agile.at.sky/secure/RapidBoard.jspa?rapidView=22507&projectKey=QGOACAD&view=planning&issueLimit=100)
* Daily Stand Ups 
* Feature Development
* Code Review
* QA
* Merge Feature Code
* Sprint Review Presentation
* Retrospective

### Project Setup & CI
* Xcode / Android Studio / VSCode
* Git / Github 
* Branching strategy
* CI/CD - Jenkins

### Testing
<img src="./images/pyramid.png" width="500"/>

* Unit Testing (XCTest / JUnit)
* UI testing (XCUITest / Espresso)

## Epics and Stories 
### Splash Screen / App Startup 

<img src="./images/splash.jpeg" width="300"/>

Build an animated splash screen page which stays displayed until the app has finished carrying out the necessary startup processes before transitioning to the home page. 

* Download the applications config file and cache it using local storage 
* Handle application life cycle events 
* Build a animated splash screen UI

### Home Page

<img src="./images/home.jpeg" width="300"/>

Build a home page UI that presents VOD content to users allowing them to browse content.

* Integration with the QMS endpoint 
* Build a loading spinner / in page error message UI
* Build UI for home page content (different rail and cell templates)

### Show Page 

<img src="./images/showpage.jpeg" width="300"/>

Build a page UI which presents metadata for single and episodic programmes to the user in a modal context.  

* Integrate with the Sky "Ways to Watch API" 
* Present the show page with loading spinner or in page error if the API call fails
* Build the single programme or episodic content UI for the page

### Login Page

<img src="./images/login.jpeg" width="300" class="center"/>

* Integration with the Rango API with native UI (if possible)
* Otherwise integrate using SkyID website using a WebView

### Play VOD 

<img src="./images/player.jpeg" width="650"/>

Build a video player which is capable of playing both unencrypted and encrypted Sky VOD assets using Native DRM. (FairPlay, Widevine)

* If user isn’t logged in show login 	
* Initial version can use unencrypted test stream
* Final version can use OVP integration and native DRM (FairPlay, iOS / WideVine, Android) 
* Build the video player UI 
* Local bookmarks  

### Settings 

<img src="./images/settings.jpeg" width="300"/>

Build a page that displays useful app information and settings to the user in a modal context. 

* Terms and conditions page 
* Player settings 
* Persisting users selections across app sessions using local storage 
* Developer debug panel 

### Analytics 

Build a logging system that allows developers and analysts to debug problems and extract useful information about how customers are using the app. 

* Build generic modular logger (or use an off the shelf solution to keep things more simple)
* Log levels 
* Device log 
* Third parties: Firebase, Sentry, Adobe (needs some discussion as we want to keep things simple)
* Crash reporting 