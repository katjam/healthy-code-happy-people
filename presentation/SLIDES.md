# Healthy Code, Happy People
![](assets/images/elm.png)
### An introduction to Elm

---

<!-- .element id="me" data-transition="zoom" data-background="#60b5cc" -->

## Katja Mordaunt

![](assets/images/neontribe-logo.png)
 
- &nbsp;katja&#64;neontribe.co.uk<!-- .element class="icon-envelop"-->
- &nbsp;@neontribe<!-- .element class="icon-twitter" -->
- &nbsp;katjam<!-- .element class="icon-github" -->
- &nbsp;elmlang: katjam<!-- .element class="icon-slack" -->

Note:
- Developing software in small teams over decade with Neontribe. Work with non-profits to build digital tools that compliment their over-stretched services
- I'm not a computer scientist or engineer - I just like using code to make stuff

---

## Assumptions about you

- you want to make reliable web apps
- TODO grab some stff from tech exeter? or drop

+++

## This talk is not

- a functional programming primer
- intended to diss javascript
- intended to make anyone feel bad about their tools and choices
- a true story

+++

## This talk is

- Asking you to think about what humans are good and what computers are good at
- Exposing some of the benefits of functional, static typing
- Going to make some bad assumptions about react (I don't use it much)
- a story about 2 teams of people who set off with same goal and took different paths

Note:
- Going to talk about how and why I think Elm helps make happier, more productive teams
- I am going to tell you a little about Elm and why I like it, but this talk is more about how we can help each other write better code and have better conversations
- It's great that some brain types can process and retain info around complex networks and code connections - but if you are writing inclusive code remember that most of us can't.
- Humans are awesome. We have imagination... but that can also lead to complication

---

## A Tale of 2 App-ventures

IMG: Welcome banner with 2 signposts / paths

New project!

Note:
- After the initial project is scoped and prototyped, we have choices to make
- What framework etc - we know react vs. we heard Elm 
- Funtional is a safe / predictable space
- Someone mentioned Elm

<!-- CHOOSE and Init Stacks (1) -->
<!-- js EXCITED dive in start scaffolding - swim across lake POWERFUL-->
<!-- Elm GUILTY learn syntax, explore model - wander round lake slowly EXCITED -->
<!-- Project boiler plate -->

+++

-  Syntax too confusing?
-  What is static typing for anyway?
-  What is this TEA you speak of?
-  Can I use webpack?

Note:
- syntax confusing - Ironically, exp devs seem to have more trouble reading Elm than beginners
- Made me reflect that we need to learn to trust each other's tech - and knowlegde & ability to evaluate and make choices in good faith
- I tried to explain that - yes Elm can make more complex apps safer but it's also a solid foundaiton for any UI

+++

## What does it look like in production?

- Real world
- Create- apps
- Is anyone using it?

<!-- MODEL (2), PLAN (3) and CODE (4) -->
<!-- (2) Start to make the things -->
<!-- js BORED Install some linting and build tools. Argue a little but agree standards. HUFFY -->
<!-- Elm CAUTIOUS Sort out data model and figure out update code EXHILERATED -->
<!-- Agreed initial domain model -->
<!-- (3) Reach the limits of the initial model -->
<!-- js ANNOYED - dead end - meet round the campfire CONFIDENT -->
<!-- Elm CONFIDENT - dead end - meet round the campfire CONFIDENT  -->
<!-- Realise need new model -->
<!-- (4) Build and Polish -->
<!-- js EXCITED Come across and old cabin. In the morning they realise the roof leaky. shrug it off, they have a lot of features GUILTY -->
<!-- Elm EXCITED Build own shelter. In the morning they admire their shelter. It's a bit rough, but perfectly sound. They have less features CONFIDENT -->
<!-- MVP prototype -->

---

- Domain modelling in Elm
- The Architecture
- Elm UI? No more css
- What does the team look like?

<!-- INITIAL RELASE AND TESTING (5) - Try it out, Show it off -->
<!-- js CAUTIOUS Realise they don't need some of the features ANNOYED -->
<!-- Elm PROUD Are able to go through the code with client PROUD -->
<!-- Test with users and demo to client -->

---

- features (made it & not)
- share with clients
- mutable objects
- elm storytelling

<!-- MAKING CHANGES (6) Tweaks and leads step back a little now the architecture is done -->
<!-- js CONFIDENT Mess up the css. Can't tweek the 3rd party library. Don't realise they've made a big hole in the wall. ANXIOUS -->
<!-- Elm ANXIOUS Amend the 'shelter' feature with no problems. Good error messages. PROUD -->
<!-- Tweaks and a couple new features -->


---

- Need ports?
- Coed review strategy
- Dive in and change something (would you let and intern do that?)
- Alter elm-ui vs css


<!-- MAINTENANCE (7) project not been worked on for a while -->
<!-- js CONFUSED wander through the underground cave system - many dead ends and rockslides LUCKY -->
<!-- Elm CONFIDENT Have a map and get straight through PROUD -->
<!-- New feature added to mature code base -->

---

- Unbreakable means no stress
- Project grows, people churn
- Read code
- Amend code
- js libraries moved on - Elm no undeclared breaking changes

<!-- CONCLUDE AND SUMMARY -->

---

## Now what?

If programming is your job, it isn't supposed to be fun...

but it should make you feel proud.<!-- .element class="fragment" -->


Note:
- Our ultimate goal is reliable apps
- Your job should not include unneccessary stress
- If you are writing code that's hard for some of your team to understand, you won't feel proud.
- We have a finite amount of time. Try to spend it building, testing and designing features; not discovering, discussing and fixing bugs

---

## Thank you
