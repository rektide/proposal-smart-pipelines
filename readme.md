# Smart pipelines
ECMAScript Stage-0 Proposal. Living Document. J. S. Choi, 2018-02.

Don't do any of this.

This would murder the language.

The additions of syntax to this deep a level is an overwhelming affront to the simplicity and understandability of JavaScript.

The scope and scale of things I see here makes me believe that the pipeline-operator must be entirely rejected. The original proposal seems deeply lacking & impotent by looking at this spec, but "solving" those problems results in a monstrous, undecypherable language that would be outright hostile to many many users of the language and which would present ongoing deeply rooted comprehension problems.

The real fix is to abandon the "points-free" style of programming demonstrated frequently in the "with smart pipelines" AND frequently in the "status quo" examples. Rather than trying to write "concise" but deeply nested javascript, users should be encouraged to step by step create variables for the expressions they make, and to compose them. By not relying on implicit variables and deep syntax, JavaScript can be easier to read, compose, and maintain, while greatly simplifying the amount of mental state a developer has to hold to undersatnd the code.

# Reasons

I find the "goals" section of the document to be illuminating and horrifying. An incredibly sharp mind, high on power, but using this power for vast evil. The extremely high falutin language of this document, it's essential non-decypherability to anyone but langauge geeks with a robust and comprehensive mastery of computer science principles, serves as a fundamental representation to me of for whom this drastic expansion of power targets: the wonks. Like this proposal's audience (wonks), this set of capabilities would exclude and deny access and understandability to any but sophisticated users.

## Don't break my code

This section is more or less fine. This proposal indeed does no great injury to existing code.

## Don't make me overthink

Somehow going full post-modern Perl is the answer to "don't make me overthink". Instead of having some normative paths, we're told that "expressive versatility" (which to me is the heart of this proposal) can "untangle deeply nested expressions into flat threads" but it does so by creating a wide array of new syntaxes and implicit variables that presents a bedazzling and confusing soup of options one can reach for and which one must carefully understand when reading code. While the structure of the program may be un-nested, one now how to chase variables backwards through steps in these deeply compacted implicit forms through remarkably terse and complicated new syntaxes.

## Make my code easier to read

> Making JavaScript expressions more ergonomic for humans is the prime, original purpose of this proposal. 

I appreciate that there is some significant improvement to the previous pipeline operator proposals.

However I rarely find the examples throughout this proposal to be easier to read.

### Untangled Flow

The author uses a points free, deeply nested construction to try to make a point.

However their alternative points-free example is barely improved, in my mind. It still relies on chasing a complex understanding of what is being passed where through multiple complex levels.

Alternatively, one could write

```
let say= await promise,
  doubled= doubleSay( say),
  capitalized= capitalize( doubled),
  msg= new User.Message( capitalized)
```

And it would be perfectly human & clear what is going on.

The author is using bad, evil programming styles used by bad people who write bad code that's hard to understand. And they have created a spec to "untangle" the same style while preserving it's essential bad-ness.

### Terse parthensis

> Parentheses are a prominent example: as long as operator precedence is clear, then reducing parentheses always would JavaScript code more visually terse and less cluttered.

Lol. Fucking no. Adding some extra parenthesis to clear things up is fine. Don't accept this rotgut poison.

### Terse variables

> Similarly, terseness of code may also be increased by removing variables where possible. This in turn would increase the data-to-ink visual ratio of the text and the distinguishability of important symbols. 

This doesn't make code easier to read. You are insane. Stop poisoning the language. Points-free style is a crime against the future readers, demanding that they hold the entire state of the code, the data flowing through it, in their head in platonic form and in totality. You have to be fucking insane to buy that maximizing data-to-ink increases understandability.

This is one of the most overtly high-flying pretentious user-hostile statements I have read about programming anywhere. It's a baldfaced powerplay against humans, and human understandability. Fuck this.

### Terse function calls

This paragraph is justification for the n-ary capabilities, which radically expand and unconstrain the proliferation of chasing implicit variables through the deeply nested pipelines.
