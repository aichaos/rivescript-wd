# Frequently Asked Questions

Questions and answers about RiveScript.

# Primary Implementations

FAQs about the primary implementations of RiveScript (the Perl, Python, Java,
and JavaScript versions).

## How are the projects versioned?

The RiveScript implementations are versioned in a similar scheme as the Perl
programming language: versions that end with an odd number are
*development versions* and those with an even number are *stable versions*.

For example, `1.0.5` would indicate a development version and `1.0.6` would be
the stable version that follows. Development versions are considered bleeding
edge and will get new features arbitrarily with no change in version number
until the next stable release.

The JavaScript version uses [semantic versioning](http://semver.org/) (the
"three number" notation) whereas the Perl, Python and Java versions use a
[Perl-style](http://perldoc.perl.org/perlmodstyle.html#Version-numbering)
versioning scheme (for example, `1.36`, because changing it now will cause
issues with packaging tools in those languages and some versioning schemes
[don't work well](http://www.dagolden.com/index.php/369/version-numbers-should-be-boring/)
in some programming languages).
