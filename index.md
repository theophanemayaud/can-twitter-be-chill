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

## Warming Up (our CPUs)

We went on and recovered the data as planned (after a test run on Twitter Superstar Donald Trump's account), and retrieved about 25 GB of Twitter Data (Tweets, mentions, likes, etc. as well as metadata) containing the following keywords:

```abu sayyaf, agro, al-qaeda in the arabian peninsula, al-qaeda in the islamic maghreb, al-qaeda, al-shabaab, ammonium nitrate, biological weapon, car bomb, chemical weapon, conventional weapon, dirty bomb, eco-terrorism, environmental terrorism, euskadi ta askatasuna, extremism, farc, fundamentalism, hamas, hezbollah, improvised explosive device, iraq, irish republican army, islamist, jihad, nationalism, nigeria, nuclear enrichment, nuclear, palestine liberation front, plo, political radicalism, somalia, suicide attack, suicide bomber, taliban, tamil tigers, tehrik-i-taliban pakistan, terrorism, terror, weapons-grade, yemen```

The data recovery went on for several days, probably used enough energy for us to feel bad, and was the biggest bottleneck in our operation.

As a matter of fact, as of the time this datastory is being written, the two biggest Dataframes haven't really finished downloading (`pakistan` and `attack`).

Nonetheless, we were able to retrieve the other 46 dataframes and had millions of Tweets to work with.

## Cleaning Up (our DFs)

Having a quick look at the Dataframes left us with some (expected, but nonetheless hurtful) findings, the data is less than desirably clean, we have Tweets in more than 20 languages (although our work is restricted to English content). This can be handled rather easily as the returned metadata contains the Tweet's language so we can use that to filter our data down, doing that reduced the size of our dataframes by 25% on average.

The more fun to see but less fun to solve problem is the inclusion of irrelevant Tweets in the dataset. Some of them were wholesome like

_Happy New Year everybody !! may 2012 be full of success , love and peace to everybody in the US, Iraq, Middle East and everywhere !!_ in the Dataframe `Iraq`, although some of them were, let's say less savoury:

_"I'm not a dirty whore, I bathe and I don't get paid. I'm a nice lady who gives bomb ass blowjobs " well folks, there you have it ; )_ in the Dataframe `dirty bomb`.

We tried removing those through detecting "positive" words specific to each Dataframe, but that lead to the elimination of many relevant Tweets as well (eliminating tweets contatining the word `bath` in `dirty bomb` eliminates all Tweets mentioning a `bloodbath` for example), so the procedure seemed to do more harm than good and we made the choice of leaving those funny Tweets in the dataset as they represented a minority that shouldn't really affect the conclusion. 



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
