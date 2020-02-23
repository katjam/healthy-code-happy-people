# Healthy Code, Happy People
![](assets/images/elm.png)
### An introduction to Elm

---

<!-- .element id="me" data-background="#8fcbdc" -->

## Katja Mordaunt

![](assets/images/neontribe-logo.png)
 
- &nbsp;katja&#64;neontribe.co.uk<!-- .element class="icon-envelop"-->
- &nbsp;@neontribe<!-- .element class="icon-twitter" -->
- &nbsp;katjam<!-- .element class="icon-github" -->
- &nbsp;elmlang: katjam<!-- .element class="icon-slack" -->

Note:
(1 min)
- Developing software in small teams over decade with Neontribe. Work with non-profits to build digital tools that compliment their over-stretched services
- I'm not a computer scientist or engineer - I just like using code to make stuff
- I love javascript TICK

---

## Assumptions

**Your skills & knowledge** are not the same as mine

**You might think**<!-- .element class="fragment" data-fragment-index="2"-->
- New is fun & old is safe<!-- .element class="fragment" data-fragment-index="2"-->
- Popular is reliable & niche is fragile<!-- .element class="fragment" data-fragment-index="2"-->

**You probably value**<!-- .element class="fragment" data-fragment-index="3"-->
- Safety & efficiency<!-- .element class="fragment" data-fragment-index="3"-->
- Client trust<!-- .element class="fragment" data-fragment-index="3"-->
- Un-stressful collaboration<!-- .element class="fragment" data-fragment-index="3"-->

Note:
(3 min)
- It would surprise my colleagues - running of js - equality, freedom it creates by having a core of universally supported standard on majority of our devices
- I don't like reading or writing javascript
- You're probably a lot better at writing javascript than I am
- Might think new tech is fun - but old tech is safer - new to you does not mean new.
- You might think popular tech is reliable and niche tech is fragile
- Like me, you proably want to write reliable software that you can be proud of
- and feel confident when others collaboate with you on your code

+++

## This talk is not

IMG![](assets/images/functional-primer.jpg)<!-- .element class="fragment" data-fragment-index="1" -->
IMG![](assets/images/anti-js.jpg)<!-- .element class="fragment" data-fragment-index="2" -->
IMG![](assets/images/tools-choices.jpg)<!-- .element class="fragment" data-fragment-index="3" -->
IMG![](assets/images/true-story.jpg)<!-- .element class="fragment" data-fragment-index="4" -->

Note:
(4 min)
- A functional programming primer
- Intended to diss javascript
- Intended to make anyone feel bad about their tools and choices
- It's one possible experience

+++

## This talk is
IMG![](assets/images/humans-vs-computers.jpg)<!-- .element class="fragment" data-fragment-index="1" -->
IMG![](assets/images/react.jpg)<!-- .element class="fragment" data-fragment-index="2" -->
IMG![](assets/images/elm.jpg)<!-- .element class="fragment" data-fragment-index="3" -->
IMG![](assets/images/human-complication.jpg)<!-- .element class="fragment" data-fragment-index="4" -->

Note:
(6 min)
- Asking you to think about what humans are good and what computers are good at
- Exposing some of the benefits of functional, static typing
- Going to make some bad assumptions about react (I don't use it much)
- Going to talk about how and why I think Elm helps make happier, more productive teams
- I am going to tell you a little about Elm and why I like it, but this talk is more about how we can help each other write better code and have better conversations
- It's great that some brain types can process and retain info around complex networks and code connections - but if you are writing inclusive code remember that most of us can't.
- Humans are awesome. We have imagination... but that can also lead to complication

---

<!-- .element id="app-venture" data-transition="zoom" data-background="#88d449" -->

## A Tale of 2 App-ventures

![](assets/images/elm-signpost.jpg)
![](assets/images/js-signpost.jpg)

### New project!

Note:
(7 min)
- A story about 2 teams of people who set off with same goal and took different paths
- After the initial project is scoped and prototyped, we have choices to make
- What framework etc - we know react vs. we heard Elm 
- Funtional is a safe / predictable space
- Someone mentioned Elm

+++

<!-- .element id="stage-1" data-transition="zoom" -->

## Stage one start

![](assets/images/elm-guilty.jpg)
![](assets/images/react-excited.jpg)

### Choose and initialise the stack

Note:
- React team Excited! They dive in and start scaffolding.
- The Elm tean is feeling a little guilty, they'll have to find out more.

+++

![](assets/images/elm-start-worries.jpg)<!-- .element class="large-img" -->

Note:
- Contray to popular belief, you don't have to throw out everything you know.
- You are already using many functional concepts
- Lots of big and small companies in all kinds of sectors all over the world are using it in production.
- 5 conferences (Japan, St Louis, Chicago, Paris, Oslo)

+++

## Syntax too confusing?

Note:
- syntax confusing - Ironically, exp devs seem to have more trouble reading Elm than beginners
- Elm can make more complex apps safer but it's also a solid foundation for any UI

+++

## What's so great about static typing?

+++

<!-- .element id="stage-1" data-transition="zoom" -->

## Stage one end

![](assets/images/elm-excited.jpg)
![](assets/images/react-powerful.jpg)<!-- .element class="wonk-img" -->


### Project Boilerplate

Note:
(12 min)
- React team feeling powerful! They've got a clean new project to dive into.
- Elm team wander around exploring carefully - they feel excited - learning something new.
- Made me reflect that we need to learn to trust each other's tech - and knowlegde & ability to evaluate and make choices in good faith

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
- What is this TEA you speak of?
- Elm UI? No more css
- What does the team look like?


Note:
(18 min)

<!-- INITIAL RELASE AND TESTING (5) - Try it out, Show it off -->
<!-- js CAUTIOUS Realise they don't need some of the features ANNOYED -->
<!-- Elm PROUD Are able to go through the code with client PROUD -->
<!-- Test with users and demo to client -->

---

- features (made it & not)
- share with clients
- mutable objects
- elm storytelling

Note:
(23 min)

<!-- MAKING CHANGES (6) Tweaks and leads step back a little now the architecture is done -->
<!-- js CONFIDENT Mess up the css. Can't tweek the 3rd party library. Don't realise they've made a big hole in the wall. ANXIOUS -->
<!-- Elm ANXIOUS Amend the 'shelter' feature with no problems. Good error messages. PROUD -->
<!-- Tweaks and a couple new features -->


---

- Need ports?
- Code review strategy
- Dive in and change something (would you let and intern do that?)
- Alter elm-ui vs css

Note:
(28 min)

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

Note:
(33 min)

<!-- CONCLUDE AND SUMMARY -->

---

## Now what?

If programming is your job, it isn't supposed to be fun...

IMG![](assets/images/yay-got-this.png)<!-- .element class="fragment" data-fragment-index="1"-->

but it should make you feel proud.<!-- .element class="fragment" data-fragment-index="1"-->


Note:
(34 min)
- Our ultimate goal is reliable apps
- Your job should not include unneccessary stress
- If you are writing code that's hard for some of your team to understand, you won't feel proud.
- We have a finite amount of time. Try to spend it building, testing and designing features; not discovering, discussing and fixing bugs

---

<!-- .element id="thanks" data-background="#ffb700" -->

## Thank you

![](assets/images/neontribe-logo.png)
![](assets/images/elm.png)

- &nbsp;katja&#64;neontribe.co.uk<!-- .element class="icon-envelop"-->
- &nbsp;@neontribe<!-- .element class="icon-twitter" -->
- &nbsp;katjam<!-- .element class="icon-github" -->
- &nbsp;elmlang: katjam<!-- .element class="icon-slack" -->

Note:
(35 min)
- Support of Neontribe and the Elm community
- Come find me later with questions or get in touch

