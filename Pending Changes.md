# Pending Changes

These are some accepted changes to the RiveScript specification that have yet
to be implemented in all of the primary implementations.

The Working Draft will only be updated to document these changes when all of the
primary implementations support them.

In the following lists of implementations that support each feature, the GitHub
commit that implements the feature is linked. In the case where there isn't an
associated commit, it means that implementation included the feature from the
beginning or the commit that added the feature hasn't been found yet.

## UTF-8 Support

Allows using foreign characters in triggers, loosens up the filtering of input
messages, and allows for the user to tell the bot their e-mail address without
the @ and dot symbols being removed.

Support:

- [x] Go
- [ ] Java
- [x] JavaScript ([@0ea7741](https://github.com/aichaos/rivescript-js/commit/0ea77415419b941ce6cadc3ab3743810104c2fe3))
- [x] Perl ([@884708a](https://github.com/aichaos/rivescript-perl/commit/884708a4acf788a30274c62c3890d4587020a669))
- [x] Python ([@2239fe6](https://github.com/aichaos/rivescript-python/commit/2239fe6b1c333f77937cbb319e583b4238ce2cc9))

Last updated: 2016-02-11

## Punctuation Stripping in UTF-8 Mode

Strips common punctuation symbols from input messages when UTF-8 mode is active.
Provides a way for the user to override the regexp if they need to change the
definition of what a punctuation character is.

Support:

- [x] Go
- [ ] Java
- [x] JavaScript ([@789c5c2](https://github.com/aichaos/rivescript-js/commit/789c5c21acb7f957187b5f5966c6688659428087))
- [x] Perl ([@cffc087](https://github.com/aichaos/rivescript-perl/commit/cffc08763a08e6a5b85c0c06b19e1f76bd0c93ca))
- [ ] Python

Last updated: 2016-02-11

## Shortcut Tags for `<input>` and `<reply>` in Triggers

Shortcuts for `<input1>` and `<reply1>`, respectively. This is for triggers
only, not replies. For example, `+ <input>`

Support:

- [x] Go
- [ ] Java
- [x] JavaScript
- [x] Perl
- [x] Python

Last updated: 2016-02-11

## Setter Tags for `<bot>` and `<env>`

Lets you use `<bot name=value>` or `<env name=value>` to set bot and global
variables, respectively, similar to the `<set>` tag.

Support:

- [x] Go
- [x] Java ([@e09049e](https://github.com/aichaos/rivescript-java/pull/7/commits/e09049e1b24abf912aab46bb54fb302eff9ec9ff))
- [x] JavaScript
- [x] Perl
- [x] Python

Last updated: 2016-02-11

## Multiple Redirects

Similar to multiple replies; puts redirects and replies in the same bucket for
random selection. Acts as a shortcut to using `- {@trigger}`

Support:

- [ ] Go
- [x] Java
- [ ] JavaScript
- [ ] Perl
- [ ] Python

Last updated: 2016-02-11

## Arrays in Responses

This repurposes arrays to be usable in responses. A tag like `(@array)` is
expanded into `{random}ARRAY{/random}`, where "ARRAY" is the pipe-delimited
contents of the array.

Example:

```
! array greek = alpha beta gamma

+ say a greek letter
- Here you go: (@greek)

// This is equivalent to:
+ say a greek letter
- Here you go: {random}alpha|beta|gamma{/random}
```

Support:

- [ ] Go
- [ ] Java
- [x] JavaScript ([@fdc33ea](https://github.com/aichaos/rivescript-js/commit/fdc33eaa1a607113efc16cacb73cabf5a9928f38))
- [ ] Perl
- [ ] Python

Last updated: 2016-02-11

## Recursive Load Directory

This makes the `loadDirectory()` function search recursively for RiveScript files.

Support:

- [ ] Go
- [ ] Java
- [x] JavaScript ([@07e4e93](https://github.com/aichaos/rivescript-js/commit/07e4e932b0a69111fd797ec2a81393fbf3448ae7))
- [ ] Perl
- [ ] Python

Last updated: 2016-03-08

## Nested Arrays

This makes arrays able to embed each other, like `!array colors = @primary @chromatic orange brown pink`. Arrays are only expanded at reply fetching time, so they can be defined in any order in any file.

Support:

- [ ] Go
- [ ] Java
- [ ] JavaScript
- [x] Perl
- [x] Python ([#22](https://github.com/aichaos/rivescript-python/pull/22))

Last updated: 2016-10-27
