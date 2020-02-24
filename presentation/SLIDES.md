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
- not a computer scientist nor engineer - I just like using code to make stuff
- not a mathematician nor a category theorist... don't need to know it to write reliable User Interfaces
- I love javascript TICK
- It would surprise my colleagues - running of js - equality, freedom it creates by having a core of universally supported standard on majority of our devices

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
- I don't like reading or writing javascript
- TICK: You're probably a lot better at writing javascript than I am - because don't do it very much
- TICK: Might think new tech is fun - but old tech is safer - new to you does not mean new.
- functional 1930's - React Elm 2014/ 2015
- You might think popular tech is reliable and niche tech is fragile
- TICK: Like me, you proably want to write reliable software that you can be proud of
- and feel confident when others collaboate with you on your code

+++

## This talk is not

IMG![](assets/images/functional-primer.jpg)<!-- .element class="fragment" data-fragment-index="1" -->
IMG![](assets/images/anti-js.jpg)<!-- .element class="fragment" data-fragment-index="1" -->
IMG![](assets/images/tools-choices.jpg)<!-- .element class="fragment" data-fragment-index="1" -->
IMG![](assets/images/true-story.jpg)<!-- .elementT class="fragment" data-fragment-index="1" -->

Note:
(3 min)
- A functional programming primer
- Intended to diss javascript
- Intended to make anyone feel bad about their tools and choices
- It's one possible experience

+++

## This talk is
IMG![](assets/images/humans-vs-computers.jpg)<!-- .element class="fragment" data-fragment-index="1" -->
IMG![](assets/images/react.jpg)<!-- .element class="fragment" data-fragment-index="1" -->
IMG![](assets/images/elm.jpg)<!-- .element class="fragment" data-fragment-index="1" -->
IMG![](assets/images/human-complication.jpg)<!-- .element class="fragment" data-fragment-index="1" -->

Note:
(4 min)
- Asking you to think about what humans are good and what computers are good at
- Exposing some of the benefits of functional, static typing
- Going to make some bad assumptions about react (I don't use it much)
- Going to talk about how and why I think Elm helps make happier, more productive teams
- I am going to tell you a little about Elm and why I like it, but this talk is more about how we can help each other write better code and have better conversations
- It's great that some brain types can process and retain info around complex networks and code connections - but if you are writing inclusive code remember that most of us can't.
- And if you are new to coding or new to the project, you probabably won;t even be aware that the complexity exists.
- Humans are awesome. We have imagination... but that can also lead to complication

---

<!-- .element id="app-venture" data-transition="zoom" data-background="#88d449" -->

## A Tale of 2 App-ventures

![](assets/images/elm-signpost.jpg)
![](assets/images/js-signpost.jpg)

### New project!

Note:
(5 min)
- A story about 2 teams of people who set off with same goal and took different paths
- A story around a brand new product - but Elm can also be used to add elements to an exisiting js project
- After the initial project is scoped and prototyped, we have choices to make
- What tech stack?
- Of course includes the frontend - we know react vs. we heard about Elm
- And of course typescript, angular, reason ml, etc... there are many
- In this story, 1 team intrigued by functional is a safe / predictable space
- The other team is sticking with React


+++

<!-- .element id="stage-1" data-transition="zoom" -->

## Stage 1 start

![](assets/images/elm-guilty.jpg)
![](assets/images/react-excited.jpg)

### Choose and initialise the stack

Note:
- React team Excited! They dive in and start scaffolding.
- The Elm tean is feeling a little guilty, they'll have to find out more.
- Common exp. in this room, but Obviously only happens on first Elm project.

+++

![](assets/images/elm-start-worries.jpg)<!-- .element class="large-img" -->

Note:
- Contray to popular belief, you don't have to throw out everything you know.
- You are already using many functional concepts
- Lots of big and small companies in all kinds of sectors all over the world are using it in production.
- 5 conferences (Japan, St Louis, Chicago, Paris, Oslo)
- More than a language, defines an architecture that helps us write good code

+++

### Strings, Math & Lists

```elm
"Hello " ++ "Norwich!"
> "Hello Norwich!" : String
```

```elm
5 / 2
> 2.5 : Float

5 // 2
> 2 : Int
```

```elm
names = ["Alex", "Shaun"]

List.reverse names
> ["Shaun", "Alex"] : List String

List.length names
> 2 : Int
```

Note:
- syntax confusing - Ironically, exp devs seem to have more trouble reading Elm than beginners
- Concatenate strings with `++`
- Division can be floating point / or integer //
- Lists must contain items of same type

+++

### Tuples & Records

```elm
myFailureTuple = (False, "Oh no!", HomePage)
mySuccessTuple = (True, "Yay!", NextPage)
```

```elm
event = { attendees = 50, name = "nor(DEV):con" }

event.name
> "nor(DEV):con" : String

.name event
> "nor(DEV):con" : String

{ event | attendees = 500 }
> { attendees = 500, name = "nor(DEV):con" }
    : { attendees : number, name : String }
```

Note:
- Tuples are fixed in number of values but can be mixed types
- Records are like objects but type safe
- Get value with dot or as a function
- Update a record

+++

### Functions!

<pre><code class="language-elm" data-line-numbers="1|2-3|5|6">addTwoString : Int -> Int -> String
addTwoString x y =
  toString x ++ "+" ++ toString y ++ "=" ++ toString (x + y)

addTwoString 2 3
> "2+3=5"
</code></pre>

Note:
- The type annotation
- The function definition
- Call the function
- The result is a string

+++

### Logic

```
if True then "yes" else "no"
> "yes"
```

```
case time of
    Morning ->
        "Hello"

    Evening ->
        "Goodbye"

    Midnight ->
        ""
```

Note:
- if then else has 2 branches determined by boolean
- case statement more than 2 possibilities
- Note that every branch of the case must return the same type

+++

## What's so great about static typing?

Note:
- Elm can make more complex apps safer but it's also a solid foundation for any UI

+++

<!-- .element id="stage-1" data-transition="zoom" -->

## Stage 1 end
#### Project Boilerplate

![](assets/images/elm-excited.jpg)
![](assets/images/react-powerful.jpg)<!-- .element class="wonk-img" -->

#### create-elm-app 20,960 lines<!-- .element class="fragment" -->
#### create-react-app 2,652,534 lines<!-- .element class="fragment" -->


Note:
(10 min)
- Elm team wander around exploring carefully - they feel excited - learning something new.
- They've been reassured by the great docs, easy set up and supportive community
- React team feeling powerful! They've got a clean new project to dive into.
- This is going to be the best engineered project ever - now they know what they are doing.
- Not advocate use, but popular way to tear up. Had a hunch about number of lines.
- TICK TICK - not wrong

---

## Stage 2 start

![](assets/images/elm-cautious.jpg)
![](assets/images/react-bored.jpg)

### Start to make the things

Note:
- The Elm team is feeling cautious. Many patterns are new to them.
- React team bored. Install some linting and build tools. 

+++

- Domain modeling in Elm
- What is this TEA you speak of?
- Elm UI? No more css
- html?
- What does the team look like?

![](assets/images/tea.png)


Note:
(13 min)
- model - your 'state'
- update function like a react redux reducer - unidirectional dataflow 
- view - display
- subscriptions for outside events like time

+++

## Stage 2 end
#### Initial domain model

![](assets/images/elm-exhilerated.jpg)
![](assets/images/react-huffy.jpg)


Note:
(15 min)
- Elm team exhilerated.
- They've figured out how the architeture works 
- React team Huffy they've been arguing a little and coding over each other's work.
- Both teams have come to an agreed model


---

## Stage 3 start

![](assets/images/elm-confident.jpg)
![](assets/images/react-annoyed.jpg)

### Change of plan

Note:
(17 min)
- Reach limits of the initial model
- Elm Team confident - they meet a dead end but they trust the compiler
- React Team annoyed - they meet a dead end and fear a refactor

+++

## Refactor time!

+++

## Stage 3 end
#### The 2 teams meet and find they've had same challenges

![](assets/images/elm-confident.jpg)
![](assets/images/react-confident.jpg)


Note:
(18 min)
- Elm team still confident. They can see they have good patterns.
- React team confident. They started to trust each other and have a new, more robust model.
- Made me reflect that we need to learn to trust each other's tech - and knowlegde & ability to evaluate and make choices in good faith

---

## Stage 4 start

![](assets/images/elm-excited.jpg)
![](assets/images/react-excited.jpg)

### Build & polish

Note:
(20 min)
- Elm Team Excited - they start writing the functionality they need
- React Team Excited - they know what they need, start installing libraries.

+++

## Holes start appearing

+++

## Stage 4 end
#### The alpha has landed!

![](assets/images/elm-confident.jpg)
![](assets/images/react-guilty.jpg)

Note:
(22 min)
- Elm team feeling confident. Their code feels robust. They don't have as many features as they wanted and some of them are a little rough... 
- React team feeling guilty. They delivered lots of features but less tests than they should have written and they are aware of some cracks.

---

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
(25 min)

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
- We have a finite amount of time. Try to spend it building, testing and designing features; not discovering, discussing and fixing bugs.
- Elm is a language based on functional programming principles that compiles to Javascript and defines an architecture that makes rapid prototyping, evolving and scaling web apps and maintaining a single source of truth easy.

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

