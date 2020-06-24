# Simple_RecSys


# Simple Category Based Cold Start Recommender


I am trying to find the 3 most similar to a name by sorting combinations of a 2 set of dummies(get_dummies) plus a column. Or find the name of the top 3 matchings (most in common) of the combinations of column data - herotype, weapons, and spells.

# Data that we have

  - name 
  - herotype
  - weapons
  - spells
  - backgroundstory

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
