# Simple_RecSys





# Simple Hybrid Cold Start Recommender System
###### Now to Combine the 3 all together

What started out as a simple category based recommender system has since grown into a hybrid system which I believe could possibly bring more life into the results. Which alread make sense from a categorical sense but I belive can be improved using both topic modeling and sentiment analysis.

![](header.png)

##  1. Simple Category Based Cold Start Recommender System

I have completed two verisons both work

##  2. Simple Sentiment Anaylysis

I have also completed this

##  3. Simple Topic Modeling


I have also completed this


##  4. Simple Dummy Data For Above


I have also completed this.

The File is a excell file that include all the data needed to do a simple test to make sure everything works as needed.
> Short blurb about what your product does.




## Installation

OS X & Linux:

```sh
npm install my-crazy-module --save
```

Windows:

```sh
edit autoexec.bat
```

## Usage example

A few motivating and useful examples of how your product can be used. Spice this up with code blocks and potentially more screenshots.

_For more examples and usage, please refer to the [Wiki][wiki]._

## Development setup

Describe how to install all development dependencies and how to run an automated test-suite of some kind. Potentially do this for multiple platforms.

```sh
make install
npm test
```

## Release History

* 0.2.1
    * CHANGE: Update docs (module code remains unchanged)
* 0.2.0
    * CHANGE: Remove `setDefaultXYZ()`
    * ADD: Add `init()`
* 0.1.1
    * FIX: Crash when calling `baz()` (Thanks @GenerousContributorName!)
* 0.1.0
    * The first proper release
    * CHANGE: Rename `foo()` to `bar()`
* 0.0.1
    * Work in progress

## Meta

Your Name – [@YourTwitter](https://twitter.com/dbader_org) – YourEmail@example.com

Distributed under the XYZ license. See ``LICENSE`` for more information.

[https://github.com/yourname/github-link](https://github.com/dbader/)

## Contributing

1. Fork it (<https://github.com/yourname/yourproject/fork>)
2. Create your feature branch (`git checkout -b feature/fooBar`)
3. Commit your changes (`git commit -am 'Add some fooBar'`)
4. Push to the branch (`git push origin feature/fooBar`)
5. Create a new Pull Request






I am trying to find the 3 most similar to a name by sorting combinations of a 2 set of dummies(get_dummies) plus a column. Or find the name of the top 3 matchings (most in common) of the combinations of column data - herotype, weapons, and spells.

# Data that we have

  - name 
  - herotype
  - weapons
  - spells
  - backgroundstory
  
  ```
name	               type	      weapons	                                           spells
------------------------------------------------------------------------------------------------------------------------------
bam	                 Bard	      Dagger, sling, club	                               Transmutation, Enchantment 
niem	               Sorcerer	  light crossbow, battleaxe	                         Necromancy 
aem	                 Paladin	  Greataxe	                                         Abjuration, Conjuration
yaeks	               Rogue	    club, battleaxe	                                   Conjuration, Evocation, Transmutation
jeeks	               Druid	     Dagger, Greataxe	                                 Evocation, Transmutation, Necromancy 
aez	                 Sorcerer	   club, light crossbow	                             Evocation, Enchantment 
sax	                 Bard	       light crossbow, battleaxe, Dagger, sling, club    Necromancy 
eert	               Bard	       Greataxe	                                         Transmutation, Necromancy 
wuc	                 Sorcerer	   light crossbow, battleaxe	                       Necromancy 
yac	                 Sorcerer    Greataxe	                                         Conjuration, Evocation, Transmutation
Jocelyn Churchill    Paladin	   club	                                             Evocation, Enchantment 
Robert Perry	       Rogue	     Dagger, sling, club	                             Abjuration, Conjuration
Tim Carlton	         Rogue	     light crossbow, sling	                           Necromancy 
Rolf Rylan	         Paladin	   light crossbow, battleaxe	                       Necromancy 
Manfred Watsons	     Rogue	     Greataxe	                                         Evocation, Enchantment 
```

I made a simple data frame example using some random DnD data.

I have a data frame loaded from CSV it has the id a name, herotype, weapons, and spells.

name there is only one so its unique

herotype can only be one choice but many names can have the same herotype

weapons a name can have one or many combinations weapons

spells a name can also have one or many combinations weapons

Now that I got the Simple recommender to work

# Data that we discovered

I Decide to take the background stories and get 7 topics to group them by to add a extra level that brings in there background story.

```

for index, topic in enumerate(nmf_model.components_):

    print(f"The Top 15 words Per topic # {index}")

    print([tfidf.get_feature_names()[i] for i in topic.argsort()[-15:]])

    print(f"\n")

The Top 15 words Per topic # 0
['friendly', 'alive', 'relationship', 'works', 'human', 'friend', 'adventurer', 'neutral', 'instantly', 'musical', 'discovered', 'day', 'picked', 'play', 'instrument']

```
