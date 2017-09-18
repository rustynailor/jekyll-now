---
layout: post
title: Wide Words&#58; In the play store
---

So, Wide Words is up and in the Google Play Store - it's available here:

[https://play.google.com/store/apps/details?id=uk.co.rustynailor.widewords](https://play.google.com/store/apps/details?id=uk.co.rustynailor.widewords)

You can see the source at the initial point of release [here](https://github.com/rustynailor/wide-words/releases/tag/v0.2).

I originally made the app as the Capstone project for my Udacity Android Nanodegree - even thought it was only finished about 9 months ago, there have been loads of new developments in Android that I would like to incorporate.

One thing that is a little clunky in the app right now is the handling of screen rotation in the quiz activity - the new [Architecture Components](https://developer.android.com/topic/libraries/architecture/index.html) - notably the lifecycle aware components - look great for simplifying this. So I'm going to take a look at that next week.

This is the original spec of the project - it is competing in a very small field of Will Self based Android Apps :-)

### Description 

The writer Will Self is renowned for deploying his vast, esoteric vocabulary throughout his novels and newspaper columns. A self described sesquipedalian (lover of obscure language), he argues persuasively that we could all benefit from being less risk-averse in our choice of words. This app is designed to help the user do just that - embrace a wider world of words. 

### Problem:
Will Self writes columns for many newspapers and magazines in the UK, which are peppered with obscure words. The user enjoys reading these articles, but finds having to constantly reach for a dictionary to look up words disrupts the flow of their reading. They want to learn and retain some of the words so they can read with more confidence and pleasure.

### Proposed Solution
After analysing a range of Will Self columns, I have identified 50 uncommon words that frequently occur in his writing. This app will help the user learn those words with engaging presentation and a simple but compelling multiple choice game.

The app will have two modes - a learn mode, where the user is presented with the words as flashcards with a full definition, which they can review and learn at leisure.

Then there is a game mode, where the user has to select the correct definition of a word from four choices within ten seconds. These quizzes will go through batches of ten words at a time.  Once a user has successfully selected the correct definition of a word three times (in different quiz sessions), they have mastered that word, and it will not be presented again in the quiz.  The object of game mode is to have mastered all 50 words, at which point the user should be able to read a Will Self column with vastly increased ease and pleasure.

In learn mode, there are three choices of review - all words,  new words or mastered words. By selecting new words, the user can review only words that they have not yet mastered.

There will also be an option in settings to reset the list of mastered words.

Data will be persisted using a SQLite database. Sharing intents will be used to enable users to proudly display their achievements on Social Media.

Defintions for words will be sourced from the open source WordNet project: http://wordnet.princeton.edu/
Intended User

The intended user of the app is an English speaking  reader who is keen to expand their vocabulary with some interesting new words, or reinforce their knowledge.  It will be of particular interest to fans of Will Self, but also to general readers.

### Features

The main features of the app are:
  * Contains a SQLite dictionary of words with related definitions
  * Presents these words to the user with the correct definition in flashcard format in learn mode
  * Has a timed multiple choice quiz in Quiz mode
  * Saves user progress on the quiz and modifies questions accordingly
  * Displays ads on the home screen using Google Admob
  * Has google analytics embedded in the app 
  * Allows the user to share their progress with a sharing intent
  * The app supports Android 4.2 and higher
  * A word of the day widget which shows a random word and definition
  * An option to download the latest word list from a web service in the settings, via an Intent Service




