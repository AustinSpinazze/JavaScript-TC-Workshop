# Section 6 - Regular Expressions (Regex)

## What is Regex and what does it have to do with our job?

Regex, or regular expressions, are special sequences used to find or match patterns in strings. These sequences use metacharacters and other syntax to represent sets, ranges, or specific characters. For example, the expression `[0-9]` matches the range of numbers between 0 and 9, and `humor|humour` matches both the strings “humor” and “humour”. An example of a Regex pattern to validate the pattern for emails may look something like this `/^(([^<>()[\]\\.,;:\s@\"]+(\.[^<>()[\]\\.,;:\s@\"]+)*)|(\".+\"))@((\[[0-9]{1,3}\.[0-9]{1,3}\.[0-9]{1,3}\.[0-9]{1,3}\])|(([a-zA-Z\-0-9]+\.)+[a-zA-Z]{2,}))$/`

Pretty simple right? ...

![Gif of Jimmy Fallon](https://media4.giphy.com/media/xhN4C2vEuapCo/200.webp?cid=ecf05e47npcmjtr6diidw8o7ihon14r1v624lh5u4f6kmwyf&rid=200.webp&ct=g)

If you like Ron Swanson, have no idea what any of the above means don't despair! We are going to dive into the inner-workings of Regex shortly as well as some awesome tools to help us write it easier. Before we get into that though, lets talk about some real world use cases for Regex, some terminology, and ways we could use it in Technical Consulting here at HubSpot.

### Real World Use Cases

A few of the more common real world use cases of Regex include:

- Form input validation
- Web Scraping
- Search and Replace
- Filtering for information in massive text files such as logs

Although Web Scraping may not have a lot of use cases in our day to day form input validation, search and replace, and filtering for information in logs absolutely do.

### Terminology

In order to understand how Regex works we first have to understand the terminology:

- **Pattern**: regular expression pattern
- **String**: test string used to match the pattern
- **Digit**: 0-9
- **Letter**: a-z, A-Z
- **Symbol**: !$%^&*()_+|~-=`{}[]:”;'<>?,./
- **Space**: single white space, tab
- **Character**: refers to a letter, digit, or symbol

### Basics

Before we get started with the basics of Regex we are first going to take a look at our first tool [Regex101](https://regex101.com/). Regex101 is a regular expression tester with syntax highlighting, explanation, cheat sheet for PHP/PCRE, Python, GO, JavaScript, Java, C#/.NET. It is a tool I always turn to when initially trying to build a Regular Expression. The first thing you will need to do when you open Regex101 is switch the flavor to ECMAScript(JavaScript) (as every language's Regex although similar have slight variations). This can be done through the pane on the left side:

![Image of Regex101 left side](https://459248.fs1.hubspotusercontent-na1.net/hubfs/459248/JS%20Workshop%20Assets/Screen%20Shot%202022-06-21%20at%203.49.45%20PM.png)

Once that is done then we need to turn off the **global** and **multi line flags** (we'll cover what those do later on in this section). To do this click on the second backslash (`/`) at the end of the Regular Expression input. Then deselect the global and multiline flags in the drop down like below:

![Image of removing global and multiline flags](https://459248.fs1.hubspotusercontent-na1.net/hubfs/459248/JS%20Workshop%20Assets/Screen%20Shot%202022-06-21%20at%204.15.09%20PM.png)

Now that that is done we can use Regex101 as we work through some of the basics.

Lets start with the most basic regular expression we can build. In the regular expression input in Regex101 input `cat`. Then in the test string input `rat bat cat sat fat cats eat tat cat mat CAT`

![Missing Global Flag Example](https://459248.fs1.hubspotusercontent-na1.net/hubfs/459248/JS%20Workshop%20Assets/Screen%20Shot%202022-06-21%20at%204.19.00%20PM.png)

Take note that regular expressions in JavaScript start and end with `/`. If you were to write a regular expression in JavaScript, it would look like this: `/cat/` without any quotation marks. In the above state, the regular expression matches the string “cat”. However, as you can see in the image above, there are several “cat” strings that are not matched. Why is this 🤔 ?

Well if you are thinking that it may have something to do with the **global** flag we replaced earlier then you would be correct! By default, a Regex pattern will only return the first match it finds. If you'd like to return additional matches, you need enable the **global** flag, denoted as `g`. To be clear the **global** flag is not just a Regex101 feature but an actual feature in Regex. So, if have your Regex pattern `/cat/` and you want it to show you all matches then in would need to look like this `/cat/g` in your code. If you want to now go back to Regex101 and enable the **global** flag you should now see almost all the patterns now be highlighted. But why are they not all matches now?

![No Case Insensitive Flag Example](https://459248.fs1.hubspotusercontent-na1.net/hubfs/459248/JS%20Workshop%20Assets/Screen%20Shot%202022-06-22%20at%208.51.46%20AM.png)

Well as you can imagine there's a flag for that as well called the **insensitive** flag where it makes your pattern case insensitive. So, if you go ahead and turn that flag on you will see your pattern become `/cat/gi` and `CAT`. This then also matches the pattern for `CAT`.

![Case Insensitive Flag](https://459248.fs1.hubspotusercontent-na1.net/hubfs/459248/JS%20Workshop%20Assets/Screen%20Shot%202022-06-22%20at%209.20.13%20AM.png)

As you can see just the flags alone in Regex can be very powerful to help you make flexible and robust patterns. Below you will find a list of all the flag options in Regex:

|Flag|Description|
|--- |--- |
|global|Don't return after first match|
|multi line|^ and $ match start/end of line|
|insensitive|Case insensitive match|
|sticky|Anchor to start of pattern, or at the end of the most recent match|
|unicode|Match with full unicode|
|single line|Dot matches newline|
|indices|The regex engine returns match indices|

### Character Sets

In the previous example, we learned how to perform **exact** case-sensitive matches, but what if we wanted to match "bat", "cat", and "fat"? We can do this by using **character sets** that are denoted by square brackets `[]`. So for our "bat", "cat", and "fat" example we just adjust out Regex pattern with a prefix **character set** of `[bcf]` to then make `/[bcf]at/gi` and this will now pattern match with "bat", "cat", "fat" "cats", "cat", and "CAT".

![Character Set Example](https://459248.fs1.hubspotusercontent-na1.net/hubfs/459248/JS%20Workshop%20Assets/Screen%20Shot%202022-06-22%20at%2010.28.53%20AM.png)

**Character sets** also work with digits:

![Character Set digits example](https://459248.fs1.hubspotusercontent-na1.net/hubfs/459248/JS%20Workshop%20Assets/Screen%20Shot%202022-06-22%20at%2010.36.38%20AM.png)

### Ranges

Let's assume we want to match all words that end with `at`. We could supply the full alphabet inside the **character set**, but that would be tedious 😅 and look something like this `[abcdefgh...]at`. See I couldn't even be bothered write out the entire example. But like Dr. Ian Malcolm from Jurassic Park once said...

![Life finds a way](https://media1.giphy.com/media/eLpoGELHst13a/200w.webp?cid=ecf05e47rldmurrffuvi9ib83zfmxjfa9vge62ytuzyittpp&rid=200w.webp&ct=g)

But in this case instead of life, Regex finds a way through the use of **ranges**. A **range** in Regex matches a single character that is contained within the range defined in the brackets and can be in the forms of:

|Range|Description|
|--- |--- |
|Partial range|Selections such as `[a-f]` or `[g-p]`|
|Capitalized range|`[A-Z]`|
|Digit range|`[0-9]`|
|Symbol range| For example, `[#$%&@]`|
|Mixed range|For example, `[a-zA-Z0-9]` includes all digits, lower and upper case letters. Do note that a range only specifies multiple alternatives for a single character in a pattern.|

So in our example where we want to match all words that end with `at` we would do `/[a-z]at/gi`

![Range example](https://459248.fs1.hubspotusercontent-na1.net/hubfs/459248/JS%20Workshop%20Assets/Screen%20Shot%202022-06-22%20at%202.03.25%20PM.png)

Of if we want to find only numbers 3 - 7 we would do `/[3-7]/gi`

![Range digit example](https://459248.fs1.hubspotusercontent-na1.net/hubfs/459248/JS%20Workshop%20Assets/Screen%20Shot%202022-06-22%20at%202.13.45%20PM.png)
