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

Most of the implementations use [semantic versioning](http://semver.org/);
previously some of them used the Perl style floating point versioning scheme
(the Perl implementation used it until v0.42; Python until v1.06). The Java
version still uses a Perl style version number, but this will change eventually.
