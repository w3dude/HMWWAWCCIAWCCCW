# HMWWAWCCIAWCCCW
How Many Wordle Words Would A Wordle Word Chucker Chuck If A Wordle Word Chucker Could Chuck Wordle Words?

README content below comes from Wordle-words, a private project created by Dan Hagler. (Access granted by permission only.)

Wordle-words - by Dan Hagler.
Copyright 2022. All rights reserved.
* Wordle-words is on GitHub using the MIT License, for now.
  * I'm planning to work out the License and Copyright, when I have time for that. (Not now!)
  * For the time being I reserve all rights, but allow for MIT License use by those I share this code with.
  * I don't intend to battle anything out in court, with the exception of if some powerful entity tries to screw me in some way.
  * I'm not sure about what I'm opening myself up to by putting this code and it's output on GitHub.
  * I'm putting this out here for now and crossing my fingers and hoping for the best.
* Wordle-words examines a list of valid Wordle words. (See Wordle-words-data/Wordle-words-sorted.)
* Wordle-words organizes and finds useful sets of words. (See various output files in Wordle-words-data.)
* Wordle-words optionally finds solutions given clues for letters used.
* Wordle-words takes one optional command line parameter. (See Usage section below.)
  * The command line parameter should be 1 to 5, or 6 characters long.
  * Lower case characters are looked for anywhere in the possible solution words.
  * Upper case characters must be in the given position in the possible solution words.
  * A question mark (?) can be used for unknown letters in any position in the solution.
  * An exclamation mark (!) can be used to prevent Wordle word exploration. (Time saver.)

Notes:
--------------------------------------------------------------------
* This code works with 5 letter English Wordle words.
* Parts of this code only works with lower case letters.
* Parts of this code only works with 5 letter words.
* This code is sloppy hacky quickly churned out code, but it works.
* No apologies. Code provided as is. Improvements to come...
* Built and tested with Visual Studio Code Version: 1.74.1

Coming soon, or whenever, as time permits:
----------------------------------------------------------------------------------
* More code cleanup and tweaks
  * Especially a few excessively long functions that do a ton of work.
* Performance improvements.
* Code to generate the README.md and LICENSE file.
* Command line parameter handling enhancements.
  * Make output of source code optional, along with other output.
* Who knows what I'll think of. :-)
  * I've thought of more things to do, but didn't write them down.
  * I'll add them when I think of them again. :-)

Longer term goal / purpose:
------------------------------------------------------------------------------------
See: Wordle-guesses-25-letters.old.txt
This is older generated output (from earlier code) that used a subset of starting words.
```
/******************************************************************************
 * Wordle-words - by Dan Hagler.
 * Copyright 2022. All rights reserved.
 *****************************************************************************/
bemix clunk grypt vozhd waqfs!!!!! j
bling jumpy treck vozhd waqfs!!!!! x
blunk cimex grypt vozhd waqfs!!!!! j
brick glent jumpy vozhd waqfs!!!!! x
brung cylix kempt vozhd waqfs!!!!! j
brung kempt vozhd waqfs xylic!!!!! j
chunk fjord gymps vibex waltz!!!!! q
clipt jumby kreng vozhd waqfs!!!!! x
clunk bemix grypt vozhd waqfs!!!!! j
fjord chunk gymps vibex waltz!!!!! q
fjord gucks nymph vibex waltz!!!!! q
glent brick jumpy vozhd waqfs!!!!! x
glent jumby prick vozhd waqfs!!!!! x
jumby pling treck vozhd waqfs!!!!! x
vozhd bemix clunk grypt waqfs!!!!! j
vozhd bling jumpy treck waqfs!!!!! x
vozhd blunk cimex grypt waqfs!!!!! j
vozhd brick glent jumpy waqfs!!!!! x
vozhd brung cylix kempt waqfs!!!!! j
vozhd clipt jumby kreng waqfs!!!!! x
vozhd glent jumby prick waqfs!!!!! x
vozhd jumby pling treck waqfs!!!!! x
waqfs bemix clunk grypt vozhd!!!!! j
waqfs bling jumpy treck vozhd!!!!! x
waqfs blunk cimex grypt vozhd!!!!! j
waqfs brick glent jumpy vozhd!!!!! x
waqfs brung cylix kempt vozhd!!!!! j
waqfs clipt jumby kreng vozhd!!!!! x
waqfs glent jumby prick vozhd!!!!! x
waqfs jumby pling treck vozhd!!!!! x
```

Usage:
--------------------------------------------------------------------

Run Wordle-words from a command prompt with optional parameter.
```
Wordle-words [kop?E][!]
```
This example passing kop?E! solves the given Wordle puzzle and produces the following output:
```
/***** Wordle-words output starts here! *****
Hello Wordle!
Parameter: 'kpo?E!'
14855 Wordle words found.
8401 words found using 5 letters not shared with other words.
5650 words found consisting of 5 unique letters.
2399 words found consisting of 4 unique letters.
340 words found consisting of 3 unique letters.
12 words found consisting of 2 unique letters.
2060 words found consisting of 5 unique letters and just one vowel.
3043 words found consisting of 5 unique letters and just two vowels.
Finding matches for puzzle 'kpo?E':
kopje
pekoe
poake
pokie
pouke
proke
spoke
Skipping Wordle word exploration per optional parameter containing exclamation mark!
***** Wordle-words output ends here! *****/
```
Note that by adding the exclamation mark (!), the Wordle-word exploration was skipped.

* When run without various data files present in the Wordle-words-data subdirectory, Wordle-words creates the desired data files.
  * This can take a long time, as in hours, up to days, depending on the speed of your computer and remaining exploration to do.
* Wordle-words produces a lot of output to the console that can be redirected to a file.
  * Be careful when directing the output to overwrite the souce in src/Wordle-words.cpp. The file will be destroyed.
  * A destroyed src/Wordle-words.cpp file can be restored from the Wordle-words file. (See source and Wordle-words files.)
* Wordle-words also creates a bunch of output files in the Wordle-words-data subdirectory.
* Wordle-words uses the data files it produces in the Wordle-words-data subdirectory to run much faster on subsequent runs.

Run Wordle-words from a command prompt with no parameter.
```
Wordle-words
```
This example passing no parameter produces the following output:
Note: This output was produced after running and interrupting the code multiple times. The code was interrupted here, to capture the output, rather than letting the code run for many hours. If you look over the output, there are a few sets of 5 Wordle words found that use 25 of the 26 letters of the English alphabet.
```
/***** Wordle-words output starts here! *****
Hello Wordle!
14855 Wordle words found.
8401 words found using 5 letters not shared with other words.
5650 words found consisting of 5 unique letters.
2399 words found consisting of 4 unique letters.
340 words found consisting of 3 unique letters.
12 words found consisting of 2 unique letters.
2060 words found consisting of 5 unique letters and just one vowel.
3043 words found consisting of 5 unique letters and just two vowels.
No puzzle provided to solve.
Searching for sets of 5 words using 25 unique letters... (This can take hours...)
abysm <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
acryl <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
acyls <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
advts <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
adyts <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
alkyd <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
ambry <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
amply <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
amyls <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
angry <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
angst <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
ankhs <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
antsy <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
aptly <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
artly <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
artsy <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
aryls <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
awdls <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
awmry <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
azyms <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
bachs <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
backs <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
backy <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
badly <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
bafts <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
baghs <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
bagsy <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
bahts <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
balds <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
balks <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
balky <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
balms <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
balmy <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
bancs <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
bandh <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
bands <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
bandy <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
bangs <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
banks <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
banky <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
bants <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
banty <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
bantz <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
bards <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
bardy <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
barfs <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
barfy <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
barks <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
barky <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
barms <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
barns <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
barny <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
barps <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
batch <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
bawds <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
bawdy <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
bawks <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
bawls <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
bawns <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
bawrs <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
bawty <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
bayts <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
bdays <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
becks <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
belch <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
belts <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
bench <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
bends <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
bendy <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
bents <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
benty <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
bergs <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
berks <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
berms <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
berth <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
beryl <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
beths <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
bewdy <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
bhang <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
bhels <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
bhuts <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
bicky <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
bight <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
bigly <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
bilks <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
binds <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
bings <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
bingy <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
binks <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
binky <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
bints <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
birch <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
birds <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
birks <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
birls <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
birsy <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
birth <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
bitch <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
bitsy <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
black <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
blags <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
blahs <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
blanc <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
bland <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
blank <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
blart <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
blast <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
blawn <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
blays <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
blend <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
blent <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
blert <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
bleys <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
blimp <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
blimy <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
blind <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
bling ----- ----- ----- -----
bling jumpy treck vozhd waqfs!!!!! x
blink <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
blins <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
bliny <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
blips <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
blist <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
blitz <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
block <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
blocs <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
blogs <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
blond <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
blonx ----- ----- ----- -----
blonx chawk fritz gyved jumps!!!!! q
blonx fritz gyved jacks whump!!!!! q
blots <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
blown <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
blows <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
blowy <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
bluds <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
bludy <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
blunk ----- ----- ----- -----
blunk cimex grypt vozhd waqfs!!!!! j
blunt <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
blurs <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
blurt <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
blush <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
blype <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
bocks <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
bodgy <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
bolds <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
bolks <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
bonds <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
bongs <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
bonks <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
bords <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
borks <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
borms <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
borts <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
borty <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
bortz <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
bosky <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
botch <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
bothy <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
bowrs <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
boxty <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
boyfs <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
boygs <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
brach <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
brack <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
bract <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
brags <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
brahs <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
brand <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
brank <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
brant <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
brast <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
brawl <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
brawn <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
braxy <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
brays <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
breds <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
brens <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
brent <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
brews <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
breys <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
brick ----- ----- ----- -----
brick glent jumpy vozhd waqfs!!!!! x
brigs <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
brims <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
bring <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
brink <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
brins <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
briny <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
brits <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
broch <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
brock ----- ----- ----- -----
brock judge miltz phynx waqfs!!!!! v
brogh <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
brogs <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
bronc <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
brond <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
brosy <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
broth <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
brown <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
bruck ----- ----- ----- -----
bruck gizmo phynx veldt waqfs!!!!! j
bruck glent jimpy vozhd waqfs!!!!! x
bruck glitz moved phynx waqfs!!!!! j
bruck goved miltz phynx waqfs!!!!! j
brugh <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
bruhs <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
brung ----- ----- ----- -----
brung cylix kempt vozhd waqfs!!!!! j
brunt <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
brusk <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
brust <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
bruvs <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
bucks <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
bufty <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
bulgy <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
bulks <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
bulky <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
bumfs <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
bumph <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
bumps <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
bumpy <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
bunch <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
bundh <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
bunds <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
bundt <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
bundy <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
bungs <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
bungy <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
bunjy <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
bunks <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
bunts <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
bunty <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
burds <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
burgs <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
burly <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
burns <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
burps <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
bushy <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
busky <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
busty <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
butch <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
butyl <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
bydes <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
byked <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
bykes <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
bylaw <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
byrls <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
bytes <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
cadgy <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
calfs <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
calks <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
calms <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
calmy <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
calps <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
calyx <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
camps <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
campy <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
candy <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
cangs <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
canst <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
canty <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
caphs <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
carbs <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
carby <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
cards <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
cardy <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
carks <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
carls <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
carns <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
carny <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
carps <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
carts <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
carvy <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
casky <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
cawks <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
celts <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
cents <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
certs <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
certy <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
cetyl <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
chads <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
chaft <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
chalk <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
chals <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
champ <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
chams <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
chang <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
chank <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
chant <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
chapt <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
chard <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
chark <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
charm <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
chars <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
chart <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
chary <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
chats <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
chavs <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
chawk ----- ----- ----- -----
chawk blonx fritz gyved jumps!!!!! q
chawl <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
chaws <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
chays <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
chefs <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
chelp <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
chems <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
chert <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
chest <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
chevy <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
chews <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
chewy <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
chibs <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
chiks <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
child <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
chimb <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
chimp <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
ching <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
chink <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
chins <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
chips <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
chirk <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
chirl <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
chirm <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
chirp <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
chirt <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
chits <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
chivs <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
chivy <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
chogs <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
choky <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
chomp <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
chons <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
chops <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
chord <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
chowk <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
chows <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
chubs <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
chugs <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
chump <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
chums <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
chunk ----- ----- ----- -----
chunk fjord gymps vibex waltz!!!!! q
churl <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
churn <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
chuts <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
chyle <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
chyme <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
chynd <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
cinqs <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
cirls <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
clads <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
clags <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
clamp <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
clang <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
clank <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
clans <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
clapt <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
clart <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
clast <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
claws <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
clefs <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
cleft <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
clegs <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
clems <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
clept <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
clerk <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
clews <-- skipping - already rejected. (See: Wordle-start-guesses-producing-less-than-25-letters-in-5-words)
clift jumpy krang vozhd wexes bq <--letters not used>
climb kraft pungy vozhd wexes jq <--letters not used>
cling pyxed thumb waqfs zokor jv <--letters not used>
clink grypt jambu vozhd wexes fq <--letters not used>
```
Execution interrupted with ^C.
I plan to make more performance improvements and let it run to completion. Updates will be coming...
