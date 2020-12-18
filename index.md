# Can Twitter be Chill?
### Team "We Love You Bob (WLYB)" 
### Théophane Mayaud - Basile Spaenlehauer - Abed Alrahman Shabaan
____
## Basic Idea and Project Conception
As the original dataset argues for chilling effects on Wikipedia and shows that such effects may indeed exist and influence people's behaviour, we saw to inspect the extension of the original hypothesis to another online space.

We chose Twitter as a subject of study instead of Wikipedia having in mind the following differences between the two:
1. Wikipedia is mostly an intellectual space, people go to Wikipedia to learn about a certain subject, while Twitter is more of a Wild West of ideas and silly everyday thoughts, and not necessarily dedicated to a specific purpose
2. Wikipedia is more of a passive space, there isn't really a lot of interaction between users and each individual's behaviour on the website is pretty much independent from the others, while Twitter is mostly a slurry of conversations and people talking to (actually, more like yelling at) each other. So when we look into sensitive subjects (as we are to do in this small study), we can expect a lot of heated debate, and hence a lot of activity incited by recent events.

##  Research Question
we set ourselves two questions that we seek to answer in this work

**1. Do the chilling effects found in the original paper extend to Twitter?**

**2. Does Twitter show an inverse effect because of its discussion-oriented nature?**

## Used Data

To have a similar scope to the original paper, we chose to use all Tweets from the same studied period of the paper that contains one of the article titles studied in the paper (more accurately, all Tweets that show up in a Twitter search for those words)

To do so, we used the Python module `Twint` to scrape the Tweets described above, this choice introduces the following issues to our data:
* The module doesn't get Tweets from deleted, banned, or shadow-banned accounts, so the observed data will be missing some Tweets.
* How clean will the scraped data be? How many irrelevant Tweets will be introduced into the dataset?

## Waarming up (our CPUs)

We went on and recovered the data as planned (after a test run on Twitter Superstar Donald Trump's account), and retrieved about 25 GB of Twitter Data (Tweets, mentions, likes, etc. as well as metadata) containing the following keywords:

```abu sayyaf, agro, al-qaeda in the arabian peninsula, al-qaeda in the islamic maghreb, al-qaeda, al-shabaab, ammonium nitrate, biological weapon, car bomb, chemical weapon, conventional weapon, dirty bomb, eco-terrorism, environmental terrorism, euskadi ta askatasuna, extremism, farc, fundamentalism, hamas, hezbollah, improvised explosive device, iraq, irish republican army, islamist, jihad, nationalism, nigeria, nuclear enrichment, nuclear, palestine liberation front, plo, political radicalism, somalia, suicide attack, suicide bomber, taliban, tamil tigers, tehrik-i-taliban pakistan, terrorism, terror, weapons-grade, yemen```

The data recovery went on for several days, and was the biggest bottleneck in our operation.




```markdown
Syntax highlighted code block

# Header 1
## Header 2
### Header 3

- Bulleted
- List

1. Numbered
2. List

**Bold** and _Italic_ and `Code` text

[Link](url) and ![Image](src)
```

For more details see [GitHub Flavored Markdown](https://guides.github.com/features/mastering-markdown/).

### Jekyll Themes

Your Pages site will use the layout and styles from the Jekyll theme you have selected in your [repository settings](https://github.com/theophanemayaud/can-twitter-be-chill/settings). The name of this theme is saved in the Jekyll `_config.yml` configuration file.

### Support or Contact

Having trouble with Pages? Check out our [documentation](https://docs.github.com/categories/github-pages-basics/) or [contact support](https://github.com/contact) and we’ll help you sort it out.
