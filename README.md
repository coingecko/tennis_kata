Tennis Game Kata Refactoring
============================

This repo contains an exercise for refactoring a ruby code based on a Tennis game. This is a forked repo callunity/tennis-kata which is based on Emily Bache's Tennis-Refactoring-Kata repo.

We've restructured the repository to provide a quick-start introduction to refactoring techniques and to mimic the setup we used last time. The code to be refactored is found in the ``lib/`` directory, and we have supplied unit tests in the ``spec/`` directory.

### Setup

Here are the steps to get you started with the repo. We assume, naturally, that you have a working development machine with Ruby 1.9 or better on it. We've included some optional elements - just skip them if you're using rvm or are not versioning your Ruby.

```sh
% git clone git@github.com:k00ka/tennis-kata.git
% cd tennis-kata
% gem install bundler
Fetching: bundler-1.7.4.gem (100%)
Successfully installed bundler-1.7.4
1 gem installed
% bundle
Fetching gem metadata from https://rubygems.org/.........
Resolving dependencies...
Installing rake 10.3.2
...
Using bundler 1.7.4
Your bundle is complete!
Use `bundle show [gemname]` to see where a bundled gem is installed.
```
##### Note: if you use rbenv...
```sh
% rbenv rehash
```
You are (almost) there!

### Rules and Specification

Tennis has a rather quirky scoring system, and to newcomers it can be a little difficult to keep track of. The tennis society has contracted you to build a scoreboard to display the current score during tennis games.

Your task is to write a ``TennisGame`` class containing the logic which outputs the correct score as a string for display on the scoreboard. When a player scores a point, it triggers a method to be called on your class letting you know who scored the point. Later, you will get a call ``score`` from the scoreboard asking what it should display. This method should return a string with the current score.

You can read more about [Tennis scoring](https://www.liveabout.com/simple-introduction-to-tennis-scoring-for-beginners-3207375), which is summarized below:

1. A game is won by the first player to have won at least four points in total and at least two points more than the opponent.
2. The running score of each game is described in a manner peculiar to tennis: scores from zero to three points are described as "love", "fifteen", "thirty", and "forty" respectively.
3. If at least three points have been scored by each player, and the scores are equal, the score is "deuce".
4. If at least three points have been scored by each side and a player has one more point than his opponent, the score of the game is "advantage" for the player in the lead.

You need only report the score for the current game. Sets and Matches are out of scope.

### Your Mission (Should You Choose to Accept It)

1. Do whatever you need in order to complete this virtual scoreboard. (method names are provided as guideline, feel free to have any additions/deletions/modifications as you like)
2. Be sure to include appropriate test cases.
3. Refactor your code, the commit history will tell us your approach to solving problems, make sure to utilize that.

### Running the tests
To run our virtual scoreboard against the code in ``tennis.rb``, do the following:
```sh
rspec ./spec/tennis_spec.rb
.

Finished in 0.00115 seconds
1 example, 0 failures
```
The text ``0 failures`` means you're ready for the main event.
