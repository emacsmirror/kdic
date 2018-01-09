# Kanji Dictionary

Practice your Kanji using a dictionary.

The big benefit of [kdic.el](kdic.el) is that it uses existing
dictionaries. See below.

I abandoned this package when I switched to *Flashcard* by Jorgen
Schaefer. It was later maintained by Damien Elmes, who rewrote it
using Python, and in the end it turned into
[Anki](https://apps.ankiweb.net/).

Sadly, *Flashcard* seems to be no longer available.

This particular package, however, is still available!

## How to use it

Use `kdic.el` to self-administer a *multiple-choice* test. Emacs
presents a kanji and five possible meanings. When you fail to choose
the correct answer, Emacs will remember these mistakes (and save them
to a file). As you continue, the kanji you missed have a high
probability of popping up again.

Alternatively, Emacs presents a meaning and five possible kanji, or
Emacs presents a kanji and five possible readings. The number of
choices you are presented with is customizable.

## Features

* List of missed entries is automatically maintained and trained. It
  is saved to a file at the end of session and reused the next time
  kdic is started.

* Training is customizable: Number of answers per question, percentage
  for picking a question from the missed entries.

* Three modes available: Give the correct meaning for a Kanji, give
  the correct pronounciation for a Kanji, give the correct Kanji for a
  meaning. Or switch between them at random.

* Allows sorting and selecting of Kanjis from the dictionaries (since
  the dictionaries are huge). This selection can be stored in a cache
  for faster restart times.

## Other languages, writing your own dictionary files

If you are looking for a vocabulary trainer that quizzes you on
vocabulary files you write yourself, see VocabTest, or write your file
in the EDICT format: Every line should match one of these:

    word [] meaning
    word [more info] meaning
    word [more info] meaning/meaning/meaning
    some words [] meaning
    some words [more info] meaning
    some words [more info] meaning/meaning/meaning

All these variations match the regexp `"\\(.*\\) \\[\\(.*\\)\\] /\\(.*\\)/"`.

## Getting Dictionaries

If you are looking for dictionary files, you might want to start here:

* http://ftp.monash.edu.au/pub/nihongo/00INDEX.html

Examples:

* kanjidic (more than 6000 Kanji in the JIS X 0208 Standard)
* kanj212 (more than 5000 Kanji in the JIS X 0212 Standard)
* edict (more than 90000 Japanese/English entries)
* jddict.v02 (more than 11000 Japanese/German entries)

Failed:

* JMdict (XML file incorporating all the other dictionary files)

Somebody would have to write an XML parsing wizard.

## Flashmaker

*Flashmaker* is Emacs Lisp code to create a flashcard file from from a
number of electronically distributed dictionaries in the KANJIDIC and
EDICT format (this includes JDDICT for Japanese-German, ENAMDIC for
Japanese proper names, and COMPDIC for Japanese-English computing and
communications vocabulary) for *Flashcard*. But as I said above,
*Flashcard* is abandoned and thus *Flashmaker* is useless.
