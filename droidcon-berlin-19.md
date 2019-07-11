# Droidcon Berlin 2019

* Date: July 1-3  
* [Website](https://www.de.droidcon.com/)
* Venue: [CityCube Berlin](https://goo.gl/maps/sMQuMb5LkviEG6iZA)

# Talks

## Hiring from Both Sides of the Table (Panel)

* **Speakers**: Carrie Hall, Hasan Hosgel, Anastasia López, Stefan Hoth,  Miriam Busch, Martin Bernard

* Be clear about the position:
    * Job description
    * Define which skills are mandatory
    * Info about the company
* Long processes are bad for everyone
* The “no-gos” for a candidate:
    * Companies looking for “jedis” or “ninjas”
    * No diversity
    * Positions that doesn’t specify the their context properly
    * Company value proposition
* All the information must be available to the candidate in upfront
* Diversity, ethics and value are important things to display
* Invest on a clear and smooth hiring process
* Provide candid feedback
* Take care with pair programming (it can be intimidating)
* “Take home challenges”
    * No for week-long challenges
    * Onsite seems to be better but can be intimidating
    * Create a challenge that is relevant for the job

## ADB Command: Life is too short to not use it

* **Speaker**: [Zhenlei Ji](https://twitter.com/zhenleiji)
* **Slides**: https://speakerdeck.com/zhenleiji/droidconberlin-life-is-too-short-not-to-use-adb-commands

 
* adb devices -l
* adb install/uninstall <APK>
* adb -s (specifies which device will answer the commands)
* adb push/pull (send/retrieve files)
* adb shell pm (package manager)
    * clear <package> (clear data)
    * grant/revoke (permissions)
    * dump <package>
* adb shell am (activity manager)
    * start [options] [intent]
    * start-service [options][intent]
    * force-stop
    * kill
    * kill-all
* adb shell wm (windows manager)
    * size (changes the screen size)
    * density (changes screen density)
    * No way to test notches =(
* adb shell getprop/setprop (system properties)
    * debug.hwui
    * Look for more properties here: https://android.googlesource.com/platform/frameworks/base/+/master/libs/hwui/Properties.h
    * adb shell input keyevent/tap/swipe (simulate hw events)
* Tip: create alias and scripts to make your development flow easier (examples: https://github.com/zhenleiji/AndroidScripts)


## What Will We Be Developing in 5 Years? (Panel)

* **Speakers**: Erik Hellman, Juhani Lehtimäki, Pascal Welsch, Stacy Devino, Danny Preussler

* Android is not likely to die (at least the way that Blackberry did)
* Will Fuschia replace Linux? Is Flutter coming to strong? The answer is: always follow the money
* Cross-platform already exists for a long time: WEB
* Cross-platforms frameworks and sdks always tend to fade
* How to deal with UX across platforms?
* Flutter is already good on Android but how about iOS?
* Small teams? Rapid prototyping? Use Flutter!
* PWAs and Web Apps are not “apps” (native)
* Browsers are always a greenfields (always updated when compared with phones OS)
* In five years…(predictions)
    * UI/UX will take our jobs
    * Faster builds and hot reload are going to be a thing
    * Everything will be automated (linting, testing and maybe coding)
    * Apps will be developed as flowing states
    * Assistants will rise
Wearables are a bet (WearOs who?) but how about augmentations?
* Rule of a thumb for technologies: don’t disrupt social interactions (e.g. google glass, phones, etc)
* How about embracing one-handed UI?
* Learn multiple skills (designer + developer, backend + apps dev, etc)
* Soft skills for the win
    * Bring more value for your life
    * Build relationships
    * Help on working together
* Be open minded for web technologies and new languages
* Learn concurrency (RX won’t solve all your problems)
* Skills are transferable from one tech to another
* Community matters!


## Designing for Sustainable GROWTH/Digital Well Being

* **Speaker**: Purnima Kochikar (Google)

* 10 years of Android
* Google wants your feedback
* Priorities:
    * Sustainable Growth
    * Safety and Trust
    * Digital Wellbeing
* A subscription means that your user sees the value provided by your app/service
* References for best practices: Google Play Medium and Academy for App Success
* Android Q: improvements on Permissions and Background Processing
* Users needs to trust us
* Why to ask for many permissions?
* Improved App Review Process:
    * Submission -> ML Review -> Human Review -> Publish decision
    * More changes:
        * Device Id
        * Location
        * Third Party SDKs
        * Family Safe content
* CTA
    * Review Permissions
    * Stay in touch with Google
    * Use latest Android SDK
* Apps and Games shouldn’t cause regret, they should make users happy. (regrets of wasting time)
* Everything is created to establish habits
* “Regret test” your apps
* Are we being ethical with our apps?
* Great technologies should improve lives, not distract from them
* Good example of app: WYSA
* Which impact we are causing? Are we making the users regret?
* Everyone in app ecosystem is responsible for the safety of the users

## Jetpack Compose — Next Gen Kotlin UI Toolkit for Android

* **Speaker**: [Ragunath Jawahar](https://twitter.com/ragunathjawahar)
* [Slides](https://speakerdeck.com/ragunathjawahar/jetpack-compose-next-gen-kotlin-ui-toolkit-for-android-7f94e1f2-d99c-427c-a09e-e0d219d1aa22 ) 

* UI Evolution followed Requirements evolution
* Architecture sets expectations between devs
* Many archs: choose yours wisely!
* View <-> ? <-> ?
* Everything is about states now!
* RecyclerView can sometimes bring a lot of inconsistencies
* Compose
    * UI = f(state) (UI is a function of state)
    * No reference to views
    * Composable functions
* Smallest reusable unit is a function
* Stateless widgets/components
* Single source of truth
* Structure of code is the same of the view hierarchy
* UI built from leaf to node
* State pushed as close to the root as possible
* “One of the hardest things to know is when something is "unfamiliar, but better" when you have something equivalent that is "familiar, and good".” - [Leland Richardson](https://twitter.com/intelligibabble)


## Navigation and the Single Activity: Learnings from a Skeptic

* **Speaker**: [Ash Davies](https://twitter.com/askashdavies)
* [Slides](https://speakerdeck.com/ashdavies/navigation-and-the-single-activity-learnings-from-a-skeptic) 

* Lifecycles are different (activities, fragments and views)
* FragmentManagers o.O
* Bundles (FragmentFactory?)
* Give a chance to Android X Fragments
* Jetpack FTW: Let’s Make Navigation Great Again
* Jetpack Navigation
  * Libraries
  * Plugin
  * Tooling
* Principles of Navigation
  * Fixed start (start and finish at the same place)
  * State as Stack
  * Deep link should simulate manual navigation
* Navigation
    * Graph
        * Default Destination types: Activities, Fragments, Dialogs
        * Customizing: https://developer.android.com/guide/navigation/navigation-add-new 
    * Controllers
        * findNavController() (Activities, Fragments and Views)
        * Navigation actions 
    * Deep Links
    * Navigation Styles
        * Toolbar
        * Bottom
        * Drawer
    * Navigation UI
    * Destination Changed Listener
    * Bundles 
        * Honorable mention: https://github.com/Takhion/android-extras-delegates
        * Jetpack provides safe args by code generation (needs to apply a plugin)
* Migrating
    * Move screen behaviours away from activities
    * Create new activity for fragments
    * Move existing activity logic for fragment
    * Initialise fragment in host activity
    * Create navigation graph
    * Profit!
* No activity result for now… (issue in place: https://issuetracker.google.com/issues/79672220)
* LiveData (https://medium.com/androiddevelopers/livedata-with-snackbar-navigation-and-other-events-the-singleliveevent-case-ac2622673150)
* Dynamic Features coming soon
* Video recommendation: https://www.youtube.com/watch?v=2k8x8V77CrU

## The Art of Code Reviews

* **Speaker**: [Fred Porciúncula](https://twitter.com/tfcporciuncula)
* [Slides](https://speakerdeck.com/tfcporciuncula/the-art-of-code-reviews)
* Values (from [Martin Fowler Refactoring book](https://martinfowler.com/articles/refactoring-2nd-ed.html)):
    * Spread knowledge
    * Improve understanding of codebase aspects
    * Enforce more clear code
    * Collaboration and exchange of ideas
* [Thread from @hillelogram about code review](https://twitter.com/hillelogram/status/1120495752969641986)
* The talk is about how Blinkist Android team does Code Review:
    * How they made it more efficient
    * Rationale about their process
    * Making developer's life more easy
* Good readings:
    * [Frustration-Free Code Reviews](http://adavis.info/2018/09/frustration-free-code-reviews.html) from [Annyce Davis](https://twitter.com/brwngrldev)
    * [How to write the perfect pull request](https://github.blog/2015-01-21-how-to-write-the-perfect-pull-request/) from [Keavy McMinn](https://twitter.com/keavy)
* WIP PRs
    * Make everyone aware of what you are doing
    * People interested could follow up on what you are doing
    * Could provide early feedback from your peers
    * How to do in...
        * Github: Draft PRs, Tags or Naming
        * Gitlab: Draft MRs
        * Bitbucket: :disappointed:
    * Good to read: [The WIP Pull Request](https://ben.straub.cc/2015/04/02/wip-pull-request/) from [Ben Straub](https://twitter.com/benstraub)
* Small PRs
    * Small PRs are easier to spot problems
    * Huge PRs = No proper reviews ("Looks good to me")
    * Squash? Merge? Rebase?
        * Depends on the team
        * Squash will make you lose the commit history but it's not a problem if your PRs are small enough
* Commit-by-commit reviews
    * More efficient
    * Easier to read and review
    * PRs as presentations (commits = slides)
    * Gives more contexts than reading all changes
    * Advice: put formatting on other commits
    * Helps with Big PRs
    * Achieving it:
        * Build it from the beginning of your work
        * Rewrite commit history before opening PR
    * Save time from reviewers
    * Possible problems:
        * Rebasing while reviewing
        * "I'm fixing that in my next commit"
        * Works better on change intense PR
        * Takes time to get used
* Extra tips
    * Have greta descriptions
    * Have a good PR template
    * EMBRACE SELF REVIEW
    * Keep PR list clean (Broken Window Theory)
    * Emoji driven comments
        * Reduce cognitive load
        * Easier to scan
* Keep things clean!
* **Everyone** must to be involved!

## Mobile Test Automation at the BBC: Then, Now and Next
* **Speaker**: [Jitesh Gosai](https://twitter.com/jitgo)
* BBC had 2 apps sharing the same media component: Sounds and iPlayer
* How to reduce testing time? Automation!
* Use the testers time better (battery, performance, etc)
* Automation can't replace testers
* Even with automation it was taking 1-3 days to test all the releasestwitter
* What dtwitterere testing?
* The cotwitteras not the same for everyone
* Unit ttwitterng
* Hexagotwitterr Ports & Adapters
* "Tripltwitterlopers + Tester to develop features
* Fast Ttwitter
* Rely otwitterisolate the proper places that need to be testetwitter
* Investtwitter
    * Smtwitterue
    * Betwitters
* Contratwitterinteractions between consumers and producertwitter

## Why wtwitterrizing our app. An honest retrospective.
* Speaketwitter](https://twitter.com/orbycius)
* [Slidetwitterdeck.com/marcosholgado/why-we-ftwittering-our-app)
* "Commotwittermon" - Voltaire
* First twitterer country => Long builds, Painful challengtwitter
* Convintwitterry hard (specially the ones that out of your teatwitter
* What itwitter
    * Fetwitter
    * Cotwitter
* Featurtwitter
    * Intwitter
    * Outwitter
    * Litwitter
* What itwitterto decide)
* First module, bad decisions:
    * Complicated feature
    * Hard deadline
    * Only one developer
* Should we start with the easiest? A: No, no, no, no...
* **Start with the most valuable**
* Integrate ASAP
* Use feature toggles to protect
* Don't compromise the quality of your modules
* Dependency Injection: use the one that you really want to dig in!
* SODD: Stack Overflow Driven Development
* Understand what you are doing and share knowledge!
* KISS (Keep it simple, stupid)
* If the team doesn't understand, you failed
* Don't overcomplicate
* Do you really need a core module?
* Treat each module as an independent library
* Testing modules: create a showcase/sample app 
* Prefer Sample modules for each module
* Resouce conflicts ("top" dependency will always prevail)
* Use resources prefix
* Android Studio scopes: narrow the project view to modules
* Take aways:
    * App is a glue that holds everything together
    * Features as libraries
    * "Everything should be made as simple as possible, but no simpler." - Albert Einstein

## Tacling Android at Scale
* **Speaker**: [Fabio Carballo](https://twitter.com/fabiocarballo)
* [Slides](https://speakerdeck.com/fabiocarballo/tackling-android-at-scale)
* Scale: Tech Readiness, Recruiting, Onboarding, Automation, Releases, Culture
* How do approach with code?
* Broken windows theory: Good looking code has more chance of keeping quality
* Defining architecture:
    * Reduce number of discussions
    * Embrace evolution
    * Favour testability
    * Protect from making mistakes
    * REDUCE AMBIGUITY
* Current approach:
    * Reactive
    * Layered
    * Dependency Injection (Dagger to deal with compiling time)
* Defining tech stack:
    * What problems is it solving?
    * What is the impact?
    * Is actively maintained?
* Wrapping 3rd party libs behind interfaces is actually good
* Don't rely on releases to control features modules
* Workflow
    * How to streamline work for 20+ ppl?
    * Branch out and branch in small chunks
    * Feature flags
* Commit messages
    * Use scripts to automatize commit tagging
* Modularisation
    * Complexity increases over time (hidden coupling appears)
    * Breaking down features into modules
    * Independent modules
    * Build times?
        * Increases with complexity
        * New hardware can help
        * Using feature launcher apps to make things smoother and fast
        * Go  bottom-top, not top-bottom
    * Why modularize?
        * Independent teams
        * Refactor with more safety
        * Creativity and innovation
* Testing to release with trust
    * Unit tests
    * Functional ui tests
    * Automated regression
    * Create script that considers git diff to run contextual tests, avoiding slower UI testing
* Design systems
    * Avoid ambiguity
    * Single source of truth
    * Align definitions between teams
    * Live documentation
    * System Glossary (reference app that contains all the specs from design system)
    * Language for defining app
* Allow people to innovate
    * Discreet mode (start small and involve everyone when needed)
    * Hide/Show Balance feature: developed by 2 ppl

## Better Together

* **Speaker**: [Niamh Power](https://twitter.com/niamh__power)

* iOS vs Android doesn't make sense for developers
* POs and Designers often are iOS oriented
* Why should we care about it?
* Users matter!
* Why to work across platforms/domains?
    * Quality
    * Communication
    * Teamwork
    * BIG picture
* Teams formed by discipline: 🙄
* Cross disciplinary squads promote more efficiency
* Increased feedback loop
* Diversity increase creativity
* Communication play a important role
* Embrace async communication (remote people with thank)
* Using semantic emojis to improve communication (scan and contextual chats)
* Using emojis to disclaim commits sizes!
* Stack overflow for teams (or a repository for knowledge)
* Proposals to help with improvements and suggestions
* Kotlin and swift are really close in terms of syntax
* Moving to Kotlin Native or Flutter? O.o
* Native is always best.
* Fabric and Firebase
* Buddybuild and Circleci
* Release process
    * Once a week
    * Rotation between ppl
    * Release stand-up
    * Requires a lot of collaboration with product and QA
* Following platforms ui/ux guidelines improves the experience
* Working together benefits everyone
* Product and design must to be aboard too

##  The Silver Bullet That Wasn’t - the story of Hubs

* **Speaker**: [Elin Nilsson](https://twitter.com/hejelinnilsson) (Spotify)
* The Hub Framework
    * Business Logic -> Data -> UI -> Events -> Business Logic
    * Data, UI and Events on the fly provided by hubs
* There isn't a silver bullet
* Why to build it? More dynamic playlists!
* GLUE = Visual language for Spotify
* Backend (UI)=> Framework => Screen
* Seeemed a success at the beginning:
    * Less code
    * Backend driven UI
    * Faster to ship
* How about making the whole app to use it? o.O
* #hubitup = peak of inflated expectations
* iOS version was open sourced at 2016 and deprecated on 2018
* Expectations: solve everything wit it!
* Realisation: initial features were similar, the rest was different
* New requirements:
    * Animation
    * Backend driven style
    * New components on the fly
    * Fallbacks and edge cases
    * No backend versioning
* Let's implement everything!
* iOS and Android versions were doing different things!
* Rethink, rewrite and reship it!
* No alignment between Android and iOS
* Full rewrite: 50% of the code wasn't being used anymore
* Backend was resistant with changes
* Hubs renderer: new version
* Using and profiting:
    * Use only when it makes sense
    * Stable framework with clear value proposition
    * Differences between platforms are recognized
* We should embrace the hype curve but minimize the side effects
* Make adoption smooth
* Always ask why you should start/use something
* SET CLEAR EXPECTATIONS
* Validate assumptions
* Measure success (using good metrics, of course)
* Embrace constraints and limitations
* Priorize maximum impact with minimum efforts
* Constraints liberates, liberties constrain
* Solving everything is not a solution



## Building SDKs - The Kotlin Way
* **Speaker**: [Jossi Wolf](https://twitter.com/jossiwolf) 
* [Slides](https://speakerdeck.com/jossiwolf/building-sdks-the-kotlin-way)
* Release notes aren't enough
* Use `@Experimental` to denote that API can change
* Use `@Deprecated` to indicate that API will be removed
* Both annotations provide visual cues and guidance to SDK users 
* Custom annotations to bring scoping to the game
* Typealias can help during the phaseout of deprecation
* Class delegation can be useful as well

## Flowing into Deep
* **Speakers**: [Hannes Dorfmann](https://twitter.com/sockeqwe) and [Gabriel Ittner](https://twitter.com/gabrielittner)
* [Slides](https://speakerdeck.com/sockeqwe/flowing-in-the-deep-event-streams-in-kotlin)

##  Incorporating Material Theming into Custom Views
* **Speaker**: [Nick Rout](https://twitter.com/ricknout)
* [Slides](https://speakerdeck.com/ricknout/incorporating-material-theming-into-custom-views)

## Step Up your tooling
* **Speaker**: [Pascal Welsch](https://twitter.com/passsy)
* [Slides](https://speakerdeck.com/passsy/step-up-you-tooling)

##  Modularization for dynamic delivery
* **Speaker**: [Ben Weiss](https://twitter.com/keyboardsurfer)
* Articles: https://medium.com/@keyboardsurfer

## Migrating to Paging Library
* **Speaker**: [Florina Muntenescu](https://twitter.com/fmuntenescu)

##  Iterative Mobile Development
* **Speaker**: Andrea Falcone

# Talks that I couldn't attend but want to watch later

##  Minimalism Driven Development
* **Speaker**: [Miguel Beltran](https://twitter.com/MiBLT)
* [Slides](https://speakerdeck.com/miquelbeltran/minimalism-driven-development)

## Developing Themes with Style
* **Speakers**: [Nick Butcher](https://twitter.com/crafty) and [Chris Banes](https://twitter.com/chrisbanes)
* [Slides](https://speakerdeck.com/nickbutcher/developing-themes-with-style-7d0571e3-6008-4ec5-99c6-aa5669520124)

##  Going edge-to-edge with Gesture Navigation
* **Speaker**: [Chris Banes](https://twitter.com/chrisbanes)
* [Slides](https://chris.banes.dev/talks/2019/going-edge-to-edge-berlin/)

##  I have no idea what my app is doing ¯\_(ツ)_/¯
* **Speaker**: [Nicola Corti](https://twitter.com/cortinico)
* [Slides](https://speakerdeck.com/cortinico/i-have-no-idea-what-my-app-is-doing-nicola-corti-android-dev)

## Let your design evolve, adopt a Design System!
* **Speaker**: [Jean-Baptiste Vincey](https://twitter.com/JBVincey)
* [Slides](https://speakerdeck.com/jbvincey/deezer-design-system)

## Inclusive Craft
* **Speaker**: [Joe Birch](https://twitter.com/hitherejoe)

## Lessons I Wish I Knew When Starting Android Development
* **Speaker**: [Frank Tamre](https://twitter.com/tamrefrank)

##  Write awesome tests
* **Speaker**: Jeroen Mols
* [Article](https://jeroenmols.com/blog/2017/02/16/unittests/)

##  Customer Driven Development : What, Why & How?
* **Speaker**: [Ishan Khanna](https://twitter.com/droidchef)

## Kotlin Not-to-Do List - What we should avoid doing in Kotlin
* **Speaker**: [Marcin Moskała](https://twitter.com/marcinmoskala)

## Think of the next billion users: Building for Low End devices
* **Speaker**: [Frank Tamre](https://twitter.com/tamrefrank)
* [Slides](https://docs.google.com/presentation/d/1YuO62Du3pVnoz3dtrU0XSYgcrzF77S4yygca_yiJDtM/edit#slide=id.g5c78377107_0_101)

##  Fearless Deploys on Friday Evening. Wait; what?!
* **Speaker**: [Oleksii Fedorov](https://twitter.com/waterlink000)
