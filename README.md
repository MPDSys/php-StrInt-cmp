# StringInt Comparator
*mpd\Util\StrIntCmp*  
[![Packagist Version](https://img.shields.io/packagist/v/mpd/util-strintcmp)](https://packagist.org/packages/mpd/util-strint-cmp)
![Packagist Dependency Version](https://img.shields.io/packagist/dependency-v/mpd/util-strint-cmp/php)
![GitHub License](https://img.shields.io/github/license/MPDsys/php-StrInt-cmp)

Library to compare large integers with arbitrary precisions, provides own pure php
implementation, but can also use bcmath or GMP on background when available

# Installation
`not yet`

# Motivation
We have been in need to compare large numbers with arbitrary precision anywhere,
which is problematic on some hostings, and problems starts earlier than you might think.  

__platform (64bit scope)__  
When host system is 32bit php int is to, larger numbers silently become floats which 
sometimes results in incorrect results

__polyfill__  
you can easily solve this by using libraries like bcmath or gmp... but these are not
written in php, they are php extensions which needs to be installed physically in the system,
and most standard web hosting dost let you touch that, they are sometimes available, but you 
need to modify your code depending on which one is available and sometimes there is none.  
This library isolates you from this, you just call compare method, and receive result.
It has its own pure php implementation, but prefers to use gmp/bcmath when available
for better performance. 

__writing new__  
Research for similar library wasn't much successful, few pure php math implementations was
found, but they usually looks abandoned since php5 was new and tends to be very large, and
also don't act as "polyfill" 

__only comparators?__  
Idea of universal polyfill is tempting, but currently there is no need for more functionality
rather for things being quickly done, and it also allows this lib to be small.  
On internal or even external request it might become reality.

# Usage
TODO