footer: **_Kara Carrell_**  |  *TableXI 2020*   | [@KaraAJC](https://twitter.com/KaraAJC) | [kara.codes](https://kara.codes)
slidenumbers: true

^ OK everyone, I'm kara Carrell, I use she/they pronouns, and today I'm going to talk to you about the 5 things I do to make sites more accessible.
# A_11_y_OOOP_!

## _5_ things I do to make sites **more _accessible_**

---
## _1:_ I Google _a11y **(insert feature)**_ </br> whenever I build a feature.
^ Step one! It might sound obvious, but I know that since I've not yet gotten a handle on everything that makes a site accessible, I make sure that I google what I can do to make the thing i'm doing more accessible. This has been useful recently when doing work on SVGs that i'm still learning about in general, but I found a few things I can do to make them more accessible, like making sure there's a title, or a nearby label if it's an informational icon. Doing this is also me continuing to listen to the disability community about their needs, and doing right by that community is important.

|*HOW*                             |*WHY*                                     |
| :------------------------------: | :--------------------------------------: |
| _1:_ LMGTFY :smile:              | _1:_ I've learned from others' expertise |
| _2:_ find dev-specific resources | _2:_ To find a solution quickly          |
| _3:_ if it's an img, table, form, or layout, imma double check  | _3:_ Never hurts to check your own work|

---
## _2:_ I use HTML tags, _**Say NO to divs**_!

^ What I mean here is that much of what we are given with HTML5 is built with accessibility in mind, so using as much of that will give us what we need, without doing much at all! If I'm working on views especially if i'm writing haml, I double check that I'm not adding more divs where other tags could be used instead. It makes our code easier to maintain as well, because we're writing in context by using semantic HTML.

|*HOW*                             |*WHY*                                 |
|:--------------------------------:|:------------------------------------:|
| _1:_ in haml I always try to use `%tag`                     | _1:_ A11y is built in! |
| _2:_ If I see a div that can be better defined, I change it | _2:_ Makes code easier to read |
| _3:_ i.e. main, header, section                             | _3:_ ... and easier to change |


---
## _3:_ I add _titles_, _captions_, and _roles_ </br> to HTML tags that need em
^ Sometimes, divs still need to be used, and sometimes context is just not super clear, so in those cases, I try to make sure I'm using the appropriate html tags and attributes to give assistive technologies what they need to help someone get all the context they need. Role and title attributes can be vital when that context cant be derived from semantic HTML, and if there's ever a table in code, it should have a caption, sometimes images need captions too. we can't leave the information up to interpretation.

|*HOW*                                |*WHY*                                 |
|:-----------------------------------:|:------------------------------------:|
| _1:_ Add `role` attribute to div elements              | _1:_ Expressing intent helps assistive technologies |
| _2:_ i.e. img `role=presentation` or div `role=button` | _2:_ ...also helps other devs |
| _3:_ i.e. th `role=col/row`                            | _3:_ ...and helps the client! |


---
## _4:_ I Ask,</br>  _**"Is this information, or aesthetic?"**_
^ Now that I've been trying to do this, I've gotten into the habit of asking myself a few questions to check what I'm doing, so I know to look for the right answers in terms of what a11y implementation I should do. The biggest question is "is what I'm doing adding information, is it functional? or is this aesthetic? furthermore, will my aesthetic change be obfuscating information? sometimes alt tags for example, arent needed, for presentational background images, where others are trying to convey meaning, so it's important to make sure everyone's in on the joke, as they say. You'll also notice some testing guides will ask you questions instead of saying "this is the way" because it depends on your intent, and no one can know that but you (or in MANY cases, the client).

|*HOW*                              |*WHY*                                 |
|:---------------------------------:|:------------------------------------:|
| _1:_ For visual things like icons, images | _1:_ Semantic HTML requires meaning |
| _2:_ Ask clients for clarification        | _2:_ Folks can be missing out on info *OR* |
| _3:_ Implement accordingly                | _3:_ Folks can be overwhelmed with unnecessary info |


---
## _5:_ I run a11y testing in my browser
^ I've added this step to my PR template in github as well, but just as we have githooks like rubocop and linters to check if we semicoloned our lines and dotted our methods, there are tools you can use to run the page through to make sure there isnt more you can be doing to make the site more accessible. And that's all!!!

|*HOW*                        |*WHY*                                 |
|:---------------------------:|:------------------------------------:|
| _1:_ tota11y                | _1:_ Hammering in WHY something is wrong helps you learn |
| _2:_ AXE beta               | _2:_ Don't want to add to the problem |
| _3:_ Microsoft Insights     | _3:_ If I can fix something around the code I'm changing, why not? |

---
## *Bonus*: Here are things we should be<br/> keeping track of when we build:
^ GOTCHA!! there's much much more than 5 things! and systematically, now that i've had exposure to over 25 repositories internally, I think these are things that keep coming up for me that i want all of us to work on getting right before it ends up on my plate in maintenance, and though I love having the opportunities to learn, we're sending experiences out to folks every time we launch a project, and we want all of those experiences to be good ones.

  - `Page titles` are IMPORTANT!
  - `Set language`, it helps!
  - Don't let abstract writing cloud us from implementing a11y<br/> **Cough Haml, Cough React**
  - Good tip: `Zoom to 200%`, are things still workable?

---
# In Summary:
- Google Now To Remember Later
- Use HTML's built-in A11y
- Add attributes when you have to (particularly, `role & title`)
- Ask yourself: Is this `information`, or `aesthetic`?
- Use a linter to check yo'self, before you wreck yo'self & others!

---
# What Next?!
^ Join the channel in slack, and check out the work that folks have done internally so far, props to the brink team, props to alex, props to Matt, props to robin, props to Aly

- Join the [#accessibility](#) channel in Slack
- Check out the work that's been [documented so far](https://github.com/tablexi/brink-rn/wiki/Accessibility-Checklist).
- JUST DO IT.

### Thank You!
---
# Resources
## Tools:
- [a11y Tutorials by WCAG](https://www.w3.org/WAI/tutorials)
- [SiteImprove A11y checker](https://chrome.google.com/webstore/detail/siteimprove-accessibility/efcfolpjihicnikpmhnmphjhhpiclljc)
- [Tota11y](https://khan.github.io/tota11y/)
- [Img alt decision tree](https://www.w3.org/WAI/tutorials/images/decision-tree/)
