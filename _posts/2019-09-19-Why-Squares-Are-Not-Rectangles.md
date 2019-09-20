Week 1 Day 4 Homework

by Ethan Miller

# Homework

A rectangle is not a good superclass to a square because it violates Liskov Substitution Principle. (A basetype should be able to be replaced by a subtype.) If a Tesla is a subtype to a Car, and `drive()` is a method of Car, than I should be able to drive a Tesla.

The rectangle class has two methods:

1. `changeHeigh()`
1. `changeWidth()`

The expected behavior is that when we invoke `changeHeight`, the `height` property will change. If we replace the rectangle with a square, the behavior of `changeHeight` will change the `height` and `width` properties since all sides of a square must be equal. Because of this, a rectangle (would-be basetype) cannnot truly be replaced with a square (would-be subtype) and should not have a direct inheritence relationship.

# Journal

## Restore master branch to initial commit

Today when I tried to `git checkout master` to clear my answers from my working branch, I recieved the following error:

``` bash
C:\source\JSquire>git checkout master
Switched to branch 'master'
Your branch is ahead of 'origin/master' by 3 commits.
  (use "git push" to publish your local commits)
```

It turns out it wasn't an error at all. It succesfully switched me to my master branch. I still had all of my answers showing up in my files, though. Alex showed me the following steps to troubleshoot the problem:

``` bash
# Show a list of commits
$ git log
# Quit log
$ q
```

This shows me the first commit and the lastest commit.

``` git
commit 4a54a23ee4b50ee08b0e3a9824b61f4a825af989 (HEAD -> master)
Author: Ethan Miller <Ethan.Miller@improving.com>
Date:   Wed Sep 18 13:03:06 2019 -0500


    201909171300


commit 93439ec83fcb3fa8467281ca9a8e381ba885698c (upstream/master, 201909171300)
Author: Tim Rayburn <tim@timrayburn.net>
Date:   Mon Sep 16 19:49:51 2019 -0500
```

Copy the commit you want to reset your HEAD to, and insert the following command:

``` bash
$ git reset --hard 93439ec83fcb3fa8467281ca9a8e381ba885698c
# Copy master branch into working directory
$ git checkout master
# Check status
$ git status
```

The reason `git checkout master` wasn't producing the desired result is because I accidentaly committed my code to master instead of putting it on a new branch with `git cb <name>`. If I ran `git branch`, the result showed that I was in the master branch. So why wasn't my code reset to the original stubs without answers? Because I committed them to master. (Oops!) So Alex's solution had me overwrite my master branch with Tim's original version. It wasn't that `git checkout master` wasn't working after all. My master branch was just pollutted with my answers.

## Homework Preview

Tim gave us a preview of our homework for tonight. It will be to explain why `Quadralateral > Rectangle > Square` is not a good example of inheritence. (Specifically why square is not a good example of inheriting all proporties of rectangle.)

He explained that `Freezer > Ice Maker > Ice` is an example of `has` rather than `inherits`. A freezer has an ice maker, but not all things that are true of a freezer are true of an ice maker.

`Lemonade > Drink > Consumables`

## Random Notes

Our local repositroy has a master branch. Our remote repository (Origin) has a master branch.

``` bash
# Show remote repositories (associated links)
$ git remotes
# Create a branch
$ git checkout -b ioc
# Show list of commits
$ git lg
$ git lga
$ git log --all
# Change branch using the hash associated with the branch name
$ git checkout 94b9343

```

Version control is like save points in a video game.

## Lunch

Lunch was a lot of fun. We played that game from the interview and I met another Improver named Thomas. We didn't win, but we had some pretty bad cards.

Today was the first time in over 10 years that I've used a Microwave. I brought a Banquet meal-- Chicken Fingers and Macaroni and Cheese. It's definately a lot cheaper than eating out. Still wish we had a toaster oven though.

### Inheritence, Rectangles, and Squares

Rachel accomplished her homework early by Googling, "Why a square and a rectangle is a bad example of class inheritence." I'm anxious to hear the answer from the horses mouth. Ben and Thomas both knew immediately why. As far as I can tell, all things that are true about a rectangle are true about a square.

### Pro Tip!

Extract Method with `Ctrl + Alt + M`.

## Interfaces allow polymorphism

The reason you use an interface is to enable you to use a signature

``` java
public interface Command {
    boolean isValid(String input); // This is the signature for the isValid method.
    void execute(String input); // This is the signature for the execute method.
}
```

in multiple different ways:

``` java
// Implement Command for an abstract class
public abstract class BaseEmoteCommand implements Command {
    private String cmdText;
    private String cmdResponse;

    public BaseEmoteCommand(String cmdText, String cmdResponse) {
        this.cmdText = cmdText;
        this.cmdResponse = cmdResponse;
    }

    @Override
    public boolean isValid(String input) {
        return input.equals(cmdText);
    }

    @Override
    public void execute(String input) {
        System.out.println(cmdResponse);
    }
}

// Implement Command for a class
public class demoCode implements Command {
    private int count = 0;
    @Override
    public boolean isValid(String input) {
        return input.endsWith("ing");
    }

    @Override
    public void execute(String input) {
        count++;
        System.out.println("We have 'ing'ed " + count + " times.");
    }
}
```

In the base class `isValid()` checks for an input from the user that matches a string (`return input.equals(cmdText);`), while in the demoCode class, the same method `isValid()` checks if the user input ends with the string "ing". That's pretty cool! One method, two different implementations of it. An interface is like a template for other classes to populate with functionality. And the functionality is up to you!

It's like those drink dispensers at Wendey's. Let's say it has two methods, `chooseFlavor(input)` and `dispense()`, and based on user input it dispenses a different flavor. `dispense()` might have implementation that says, `sout drink(flavor)`. That's all fine and good, but what if we want to dispense ice instead of a drink? Now we're out of luck, because our `dispense()` method only handles drinks. To solve this, we could make `dispense()` a property of an interface called Dispenser, and then implement that interface with two seperate classes, `Drink` and `Ice`. One souts `drink(flavor)` and the other souts `ice`. So even though we're using the same method `dispense()`, it's going to behave differently based on whether it's invoked by the Drink class or the Ice class.