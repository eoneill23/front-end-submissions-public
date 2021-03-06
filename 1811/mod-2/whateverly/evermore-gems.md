# Whateverly 
* Students:
* Evaluator:
* Repo: https://github.com/IsaacSunoo/whateverly-evermore-gems

# Rubric

## Specification Adherence

* [ ] Novice - README is missing or incomplete. Codebase is not organized. User stories from group are never submitted. Application does not solve the presented problem.

* [ ] Advanced Beginner - README is complete. Codebase is organized. User stories are completed; however, may be late. Some user stories may be unclear or hard to understand. Application is close to solving presented problem.

* [X] Proficient - Developers turn in user stories on time and iterate on user stories throughout the life of the project, as needed. User stories have enough detail - such that an outside developer could jump right in and help with user stories/tickets. Application solves the presented problem.

* [ ] Exceptional - Meets all expectations for `Proficient`. Developers may use personas to help guide their user stories. Developers may also incorporate other tools to assist in planning - workflow diagrams, story maps, etc.



------------------------------------------------------------------

## UI/UX

* [ ] Novice - The application is confusing or difficult to use. The final project presents an interface that is incomplete.

* [ ] Advanced Beginner - The application may be confusing or difficult to use at times. The application shows effort in the interface, but the result is not effective because UX and/or UI still present an application that is incomplete or difficult to use. It is not clear that the user stories helped to guide UX.

* [ x ] Proficient - The application has many strong pages/interactions. The application can stand on its own to be used by instructor without guidance from a developer on the team.

* [ ] Exceptional - Meets all expectations for `Proficient`. In addition, the application is fully responsive, and has clearly had special consideration around usability on devices. There no holes in functionality.


Comments:

* Filtering works well with just one exception -- if I type in a gem name in the search bar, then I select to filter by a color that does *not* match that of the gem name I filtered by, the gem list repopulates to only prioritize the color filter and completely nixes the search bar. I would either have that list reflect results from both filter categories combined, or, clear out that search bar text when someone filters by color to make it more obvious that we're now only filtering by color and no longer by name.

* A cool UI feature to add would be some sort of step-by-step "breadcrumbs" or signifier that there are multiple steps to complete before viewing your results. Think of filling out an online application that has multiple phases -- it usually tells you you're on step 1 and you have 4 to go. I could see a top nav bar that says something like "Select Your Gem > Select Your Metal > View Results" where the step you're currently on is highlighted.

* On the results page, I'd swap the image from the left to the right side of the page -- it's a more common convention to have the important information on the left as people have a tendency to ignore the right side of the page (usually the right column is full of ads and other garbage so we've been conditioned to ignore it.)












------------------------------------------------------------------

## CSS/Sass Style

* [ ] Novice - There are several (10+) instances of duplication and one or two major bugs. Developers write code with unnecessary selectors or tags which do not increase clarity.

* [ ] Advanced Beginner - There is some duplication (5-10 instances) in the codebase. There may be one to two minor bugs. There may be some unnecessary selectors or tags. Application adds organization for the whole stylesheet and within rules.

* [ x ] Proficient - Application is thoughtfully put together with comments to help guide organization. There may be some duplication (fewer than 5 instances) present. Comments are present to assist with organization of code.

* [ ] Exceptional - Meets all expectations for `Proficient`. The application has exceptionally well-factored CSS/Sass with all styles separated out into logical stylesheets. There are zero instances where an instructor would recommend taking a different approach.


Comments:


* Nitpick, but there are lots of indentation/formatting issues throughout the CSS that make it a bit more difficult to read. Make sure those types of things get cleaned up just like we do with our javascript.

* The transitions [here](https://github.com/IsaacSunoo/whateverly-evermore-gems/blob/master/src/scss/_MetalCardStyle.scss) would be a good use case for a mixin so you can avoid writing all that repeat CSS that's long-winded and complex


* Are there any other elements with a class of [header-title](https://github.com/IsaacSunoo/whateverly-evermore-gems/blob/master/src/scss/_Header.scss#L2)? If not, we probably don't want this nested (unecessarily bloats the CSS) and an ID is usually better.



------------------------------------------------------------------

## JavaScript / React Style

* [ ] Novice - There is a significant amount of duplication and one or two major bugs. JavaScript does not follow the principles of `DRY` (Don't Repeat Yourself)

* [ ] Advanced Beginner - There is some duplication and there may be one or two major bugs. The application has large components and logic could be broken apart into smaller, stateless components. JavaScript may be hard to read/follow.

* [x] Proficient - Application has little to no duplication and no major bugs. Application has several components built out that logically break apart the functionality. JavaScript may be hard to follow at times but is generally easy to read/understand. 

* [ ] Exceptional - Application has exceptionally well-factored code with little or no duplication and all components separated out into logical components. There are zero instances where an instructor would recommend taking a different approach to design and component architecture. DRY and SRP (Single Responsibility Principle) practices are incorporated, making JavaScript very easy to follow/read.


Comments:


* Nice job breaking apart components for things like `Header` and `Greeting`. With using `Header` in multiple locations, it would be nice to see this made dynamic for different titles/heading levels - it's a bit strange to see a component for headings when you are still ysing heading levels in the same areas, like [here](https://github.com/IsaacSunoo/whateverly-evermore-gems/blob/master/src/components/MetalsPage.js#L17-L18) 
* Don't name components as pages. The component name should reflect that is a small part of the overall layout -> ex: `GemsPage` can just be `Gems`
* Opportunities for refactoring due to duplication. For instance - `GemCard` and `MetalsCard` could be refactored into a `Card` component.


------------------------------------------------------------------

## GitHub Collaboration/Workflow

* [ ] Novice - Developers do not tag instructors in the two required PRs by due dates listed in the project outline or tagged PR has fewer than 200 lines of code. The developer creating the PR does not summarize the changes or why the changes were made. Reviewers are not leaving line-by-line feedback/comments _or_ are merging the PR before changes are made.

* [ ] Advanced Beginner - Developers tag instructors in both required PRs by due dates _or_ in one of the two required. PR has less than the required lines of code in PR. Reviewers do not leave line-by-line feedback. May be merging PR before feedback is incorporated.

* [ x ] Proficient - Developers tag instructors in both required PRs by due dates. PR is between 350 - 450 lines of code. The developer creating the PR summarizes the changes made, why those changes were necessary, and asks for insights. Reviewers leave line-by-line comments/feedback and wait to merge PR until feedback is incorporated.

* [ ] Exceptional - Meets all expectations for `Proficient`. The feedback is both kind _and_ insightful. There may be numerous threads of conversation where developers go back and forth to find the best solution to the problems they are solving together.


Comments:

Contribution breakdown:  
 _Rachael: <x> 18 commits  1,391 ++  163 --_  
 _Kristen: <x> 14 commits  911 ++  505 --_  
 _Isaac: <x> 16 commits  19,720 ++  1,956 --_  


* Overall as a group you probably need a bit more commits -- 71 likely means that each commit is doing too much work and includes more changesets than a single piece of functionality or work. I'd always aim to be well over 100 commits on projects of this size. e.g. don't combine changes for a [test and css](https://github.com/IsaacSunoo/whateverly-evermore-gems/commit/9320d105c91824b45f582a7543f11b0ff7ffcd98) in the same commit. They are unrelated pieces of work.

* Mostly a readable git history, though I would make sure the formatting of your commit messages is a bit more consistent (e.g. always start with a capital letter, never include punctuation, always write in the imperative tense, etc.)






------------------------------------------------------------------

## Testing

* [ ] Novice - There is little or no evidence of testing in the application.

* [ ] Advanced Beginner - Project has sporadic use of tests at multiple levels. The application contains numerous holes in testing and/or many features are untested.

* [ x ] Proficient - Project has a running test suite that tests multiple levels but fails to cover some features.

* [ ] Exceptional - Project has a running test suite that exercises the application used Enzyme. The test suite covers almost all aspects of the application.


Comments:


* You should move that App.test.js file into your tests directory so it can sit alongside all the other ones.

* [These methods](https://github.com/IsaacSunoo/whateverly-evermore-gems/blob/master/src/App.test.js#L77-L85) would also need to test that the display state is changed as they are both invoking that changeDisplay method

* Missing tests for metalsCard which should be spying on a mock function passed through as a prop







------------------------------------------------------------------

## Presentation

* [ ] Novice - Not all presenters speak. Presenters give too much or too little information about the application. Presenters do not use audio/visual aids or media.

* [ ] Advanced Beginner - Everyone in the group speaks. Presenters do a live demo of the application. The group may speak about the planning/challenges/rewards of the project; however, the delivery does not seem thought out/well-planned. 

* [X] Proficient - Everyone in the group has an opportunity to speak during the presentation. The group has a visual of the application to demo (e.g. slides, recordings of interactions, live demo). The group talks about the app, speaking to the challenges, rewards, and collaborative aspects of the project.

* [ ] Exceptional - Meets all expectations of `Proficient`. In addition, the presentation runs smoothly w/no hiccups - indicating that it was planned/rehearsed/polished. The presentation is so engaging that there is no time that the evaluators find themselves checking the time/clock.


Comments:

* Intro was great - the background was a bit long, wanted to get to the point of the problem being solved a little sooner
* Could take one of the challenges and go into depth about it - make it into a quick teachable moment
* Great to hear about divide and conquer and making working remotely successful







