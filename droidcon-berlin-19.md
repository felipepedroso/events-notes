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

## Other talks

Migrating to Paging Library
Speaker: Florina Muntenescu (Google)
Paging library brings some perks to load paged lists like placeholders and customization. Since it had lots of code, I decided to not take notes... The slides were not provided afterwards.




https://speakerdeck.com/fabiocarballo/tackling-android-at-scale


