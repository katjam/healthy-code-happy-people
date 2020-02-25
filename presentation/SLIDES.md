# Healthy Code, Happy People
![](assets/images/elm.png)
### An introduction to Elm

---

<!-- .element id="me" data-background="#8fcbdc" -->

## Katja Mordaunt

![](assets/images/neontribe-logo-pink.png)
 
- &nbsp;katja&#64;neontribe.co.uk<!-- .element class="icon-envelop"-->
- &nbsp;@neontribe<!-- .element class="icon-twitter" -->
- &nbsp;katjam<!-- .element class="icon-github" -->
- &nbsp;elmlang: katjam<!-- .element class="icon-slack" -->

Note:
(1 min)
- Developing software in small teams over decade with Neontribe. Work with non-profits to build digital tools that compliment their over-stretched services
- I don't identify as a computer scientist or engineer - I just like using code to make stuff
- not a mathematician nor a category theorist... sometimes I wish I was, but you don't need to know it to write reliable User Interfaces
- I love javascript
- It would surprise my colleagues - clarify - universally supported & flexible target as standard on majority of our devices

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
- It's also pretty neat how small the initial learning curve is. I don't like reading or writing javascript
- TICK: You're probably a lot better at writing javascript than I am - because don't do it very much
- TICK: Might think new tech is fun - but old tech is safer - new to you does not mean new.
- functional 1930's, ML syntax 1973 - React Elm Typescript Webpack 2012/ 2013 - graphql, redux 2015
- You might think popular tech is reliable and niche tech is fragile - carefully engineered specialist equipt
- TICK: Like me, you proably want to write reliable software that you can be proud of
- and feel confident when others collaboate with you on your code

+++

## This talk is not

![](assets/images/functional-primer.png)<!-- .element class="fragment" data-fragment-index="1" -->
![](assets/images/anti-js.png)<!-- .element class="fragment inline" data-fragment-index="2" -->
![](assets/images/tools-choices.png)<!-- .element class="fragment inline" data-fragment-index="2" -->

Note:
(3 min)
- TICK: A functional programming primer
- TICK: Intended to diss javascript
- Intended to make anyone feel bad about their tools and choices

+++

## This talk is
IMG![](assets/images/humans-vs-computers.jpg)<!-- .element class="fragment" data-fragment-index="1" -->
![](assets/images/react-lang.png)<!-- .element class="fragment inline" data-fragment-index="2" -->
![](assets/images/elm-lang.png)<!-- .element class="fragment inline" data-fragment-index="3" -->

Note:
(4 min)
- TICK Asking you to think about what humans are good and what computers are good at
- Great that some brain types can process and retain info around complex networks and code connections - but if you are writing inclusive code remember that most of us can't.
- And if you are new to coding or new to the project, you probabably won;t even be aware that the complexity exists.
- Humans are awesome. We have imagination... but that can also lead to complication particularly during a creative collaboration
- TICK Probably going to make some wrong assumptions about modern react
- TICK Because my focus is to tell you little about why I like Elm and how it helps make happier, more productive team 
- And more improtant, how we can help each other write better code and have better conversations
- Exposing some of the benefits of functional, static typing along the way

---

<!-- .element id="app-venture" data-transition="zoom" data-background="#8fcbdc" -->

## A Tale of 2 App-ventures

![](assets/images/elm-signpost.jpg)
![](assets/images/js-signpost.jpg)

### New project!

Note:
(5 min)
- A story about a brave team of people who set off down an unknown path. As they go, they reflect on experience of an earlier react project
- A story around a brand new product cycle - but Elm can also be used to add elements to an exisiting js project
- After the initial project is scoped and prototyped, we have choices to make
- What tech stack? Of course includes the frontend - we know react vs. we heard about Elm
- also typescript, angular, reason ml, etc... there are many
- In this story, our team intrigued promises of Elm
- Elm is a language based on functional programming principles that compiles to Javascript and defines an architecture that makes rapid prototyping, evolving and scaling web apps and maintaining a single source of truth easy.
- It's ecosystem is steadily growing & as advertised is a delightful language for reliable webapps, with friendly error messages and no runtime errors, is also for data vizualisation, for 3D graphics

+++

<!-- .element class="stage-card" -->

## Choose and init the stack

![](assets/images/elm-guilty.jpg)
![](assets/images/react-excited.jpg)


Note:
- If they were using react Excited! They be able to dive in and start scaffolding.
- But instead, Elm team is feeling a little guilty, they'll have to do some learning before they get started.
- Common exp. in this room, but Obviously only happens on first Elm project.

+++

![](assets/images/elm-start-worries.jpg)<!-- .element class="large-img" -->

Note:
- Contray to popular belief, you don't have to throw out everything you know to switch to a more functional paradigm.
- Many languages have support for functions as first class citizens, so you probably already use concepts without realising
- Elm helps ease you in to it without needing the theory behind it. Understanding comes later.
- More than a language, a community & defines an architecture that helps us write good code
- Lots of big and small companies in all kinds of sectors all over the world are using it in production.
- 5 conferences (Japan, St Louis, Chicago, Paris, Oslo)

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
- demo that this is not a lisp based syntax
- uses comments, variables, functions, math and logic
- in a REPL XXX
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
- Update a record XXX 

+++

### Functions!

<pre><code class="language-elm" data-line-numbers="1|2-7|9|10">addTwoString : Int -> Int -> String
addTwoString x y =
    String.fromInt x 
        ++ "+" 
        ++ String.fromInt y 
        ++ "=" 
        ++ String.fromInt (x + y)

addTwoString 2 3
> "2+3=5" : String
</code></pre>

Note:
- The type annotation
- The function definition
- Call the function
- The result is a string

+++

### Logic

```elm
if True then "yes" else "no"
> "yes"
```

```elm
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

<!-- .element class="stage-card" -->

## Project Boilerplate

![](assets/images/elm-excited.jpg)
![](assets/images/react-powerful.jpg)<!-- .element class="wonk-img" -->

#### create-elm-app 20,960 lines<!-- .element class="fragment" -->
#### create-react-app 2,652,534 lines<!-- .element class="fragment" -->

Note:
(10 min)
- First milestone: Elm team feel excited - they are exporing carefully and learning something new.
- Reflect that if React they'd be feeling powerful! With clean new project to dive into.
- With the confidence that it'd the best engineered project ever - now they know what they are doing.
- They've been reassured by the great Elm docs, easy set up and supportive community
- Not advocate use, but popular way to tear up. Had a hunch about number of lines.
- TICK TICK - not wrong

---

<!-- .element class="stage-card" -->

### Start to make the things

![](assets/images/elm-cautious.jpg)
![](assets/images/react-bored.jpg)

Note:
- The Team is feeling cautious. Many patterns are new to them. They need to figure out how to render and alter stuff.
- Reflect that if using react they'd be maybe a little bored, installing some linting and build tools. 

+++

## Html?

```elm
div [ class "list-of-stuff" ]
[
  h2 [] [ text "Short list of stuff"],
  ul []
    [
      li [] [ text "Item one"],
      li [] [ text "Item two"],
      li [] [ text "Item three"]
    ]
]
```
![](assets/images/list-of-stuff.png)<!-- .element class="fragment" -->

Note:
- We often have artifacts after discovery that tell us what the view should be like
- It's fair to start there and add stuff to the model and update as you need them

+++

## ... and buttons and links
### it's all just functions

```elm
button [ onClick DoThing ] [ text "Do thing" ]

a [ href "/my-path" ] [ text "Follow the high road" ]
```

<span class="fragment">

```js
React.createElement(
  "button",
  { onClick: this.doThing },
  "Do thing"
);

React.createElement(
  "a",
  { href: "my-path" },
  "Follow the high road"
);
```
</span>

Note:
- html5 elements fully implemented & is easy to make your own too
- TICK Much like how jsx works under the hood

+++

## Html?
### Using elm-format

```elm
div [ class "list-of-stuff" ]
    [ h2 [] [ text "Short list of stuff" ]
    , ul []
        [ li [] [ text "Item one" ]
        , li [] [ text "Item two" ]
        , li [] [ text "Item three" ]
        ]
    ]
```

- elm-format -> One agreed standard
- Machine can parse with confidence
- No one forgets the commas
- Don't need trailing commas to eliminate bad diffs

Note:
- I lied a little - it looks like this.
- But elm-format does that for you... so if it takes your muscle memory a while to retrain - don't worry.
- Like prettier but without the arguments over spaces, tabs and semicolons.

+++

## CSS?

- Elm UI? No more css
- IMG packages

Note:
(13 min)
- What does team look like?
- Already have some css - can import as a sheet or use sass
- Can use elm-css which is a little like styled components
- elm ui define responsive behaviours in a more obvious / logical way in the same place as other code
- When every thing is functions, your team can be more flexible
- accessibility package etc

+++

### The Elm architecture

![](assets/images/tea.jpg)<!-- .element class="large-img" -->

Note:
- model - your 'state'
- update function like a react redux reducer - unidirectional dataflow 
- view - display
- subscriptions for outside events like time
- 3 types of Main progamme supplied by the core Browser package. element, document and application

+++

Difference approaching domain model components vs...

- model
- update
- view


Note:
- Don't prefer shorter files
- Don't try to model everything from the beginning, let it grow organically and refector with confidence
- Assume everything is unique until it isn't. Often we mistake similar for the same in order to save effort, but it often is a false economy.
- Build your modules around types rather than types of functionality.
- Don't think in terms of visual components - it's tempting to break stuff down into - local state and methods, but that's the object trap and it adds a layer of management complexity.

+++

<!-- .element class="stage-card" -->

## Initial domain model

![](assets/images/elm-exhilerated.jpg)
![](assets/images/react-huffy.jpg)

Note:
(15 min)
- Elm team exhilerated.
- They've figured out how the architeture works 
- Remember when React were Huffy they've been arguing a little over how to model things and coding over each other's work.

---

<!-- .element class="stage-card" -->

## The plan hasn't worked

![](assets/images/elm-confident.jpg)
![](assets/images/react-annoyed.jpg)

Note:
(17 min)
- Reach limits of the initial model
- Elm Team confident - they meet a dead end but they trust the compiler
- React Team annoyed - they meet a dead end and fear a refactor

+++

## Refactor time!

+++

## What's so great about static typing?
## What's are custom types?

Note:
- Elm can make more complex apps safer but it's also a solid foundation for any UI

+++

<!-- .element class="stage-card" -->

## There will always be challenges, misunderstandings and mistakes

![](assets/images/elm-confident.jpg)
![](assets/images/react-confident.jpg)

Note:
(18 min)
- The 2 teams meet and find they've had same challenges
- Elm team still confident. They can see they have good patterns.
- React team confident. They started to trust each other and have a new, more robust model.
- Made me reflect that we need to learn to trust each other's tech - and knowlegde & ability to evaluate and make choices in good faith

---

<!-- .element class="stage-card" -->

## Build & polish

![](assets/images/elm-excited.jpg)
![](assets/images/react-excited.jpg)

Note:
(20 min)
- Elm Team Excited - they start writing the functionality they need
- React Team Excited - they know what they need, start installing libraries.

+++

## Holes start appearing

Notes:
- React memories of discovering how to manage state and lifecycle methods.
- Benefits of pure functions

+++

<!-- .element class="stage-card" -->

## The alpha has landed!

![](assets/images/elm-confident.jpg)
![](assets/images/react-guilty.jpg)

Note:
(22 min)
- Elm team feeling confident. Their code feels robust. They don't have as many features as they wanted and some of them are a little rough... 
- React team feeling guilty. They delivered lots of features but less tests than they should have written and they are aware of some cracks.

---

<!-- .element class="stage-card" -->

## Initial release

![](assets/images/elm-proud.jpg)
![](assets/images/react-cautious.jpg)

Note:
- The Elm team feeling proud and confident to go through the features & code with client
- The React team are feeling cautious - they realise some of their features are fragile

+++

- features (made it & not)
- share with clients
- mutable objects
- elm storytelling

+++

<!-- .element class="stage-card" -->

## Try it out & show it off

![](assets/images/elm-proud.jpg)
![](assets/images/react-annoyed.jpg)

Note:
(25 min)
- Testing with users and getting acceptance signed off by client
- The elm team proud of what they have and all works as expected
- The React team are annoyed, they realise they don't need some of the features they built after all

---

<!-- .element class="stage-card" -->

## Making changes

![](assets/images/elm-anxious.jpg)
![](assets/images/react-confident.jpg)

Note:
- Leads can step back now architecture is done
- Elm team feel anxious about adding a new feature
- React team confident - but then things start going wrong unexpected effects

+++

- Need ports?
- Code review strategy
- Dive in and change something (would you let and intern do that?)
- Alter elm-ui vs css

+++

<!-- .element class="stage-card" -->

## Maintenance

![](assets/images/elm-confident.jpg)
![](assets/images/react-anxious.jpg)

Note:
(28 min)
- Elm team feel proud, they added the features and nothing broke
- React team feel anxious, they've had to patch something at the last minute
- The project hasn't been worked on for a while
- Security patches
- A new feature request
- Elm team confident they make the changes and follow the compiler
- React team feeling anxious and not sure how to approach.
- The things they try feel fragile

+++

- Unbreakable means no stress
- Project grows, people churn
- Read code
- Amend code
- js libraries moved on - Elm no undeclared breaking changes

Note:

+++

<!-- .element class="stage-card" -->

## New feature added to mature code base

![](assets/images/elm-proud.jpg)
![](assets/images/react-lucky.jpg)

Note:
(33 min)
- Elm team feel proud, even though they weren't original it feels like the thing they added is sound
- React team feel lucky and discuss a complete rewrite if ever they are asked to add another feature

---

<!-- CONCLUDE AND SUMMARY -->

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
- Hear people say stuff that sounds sensible and repeat it. We ought to stop and think for ourselves?

---

<!-- .element id="thanks" data-background="#8fcbdc" -->

## Thank you

![](assets/images/neontribe-logo-pink.png)
![](assets/images/elm.png)

- &nbsp;katja&#64;neontribe.co.uk<!-- .element class="icon-envelop"-->
- &nbsp;@neontribe<!-- .element class="icon-twitter" -->
- &nbsp;katjam<!-- .element class="icon-github" -->
- &nbsp;elmlang: katjam<!-- .element class="icon-slack" -->

Note:
(35 min)
- Support of Neontribe and the Elm community
- Come find me later with questions or get in touch
