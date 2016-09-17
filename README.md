# sentiment-analysis

## Document vs Sentence Level Classification

Say we have some business review with 4 sentences and we want to classify the review as positive or negative. One approach is to classify each sentence as positive or negative and then aggregate those classifications to determine if the overall review is positive or negative.

## Important Features of Opinions

- terms
- the rarity of a word used
- the position of a word in the text (e.g., n-gram)
- the presence of negation words and other so-called opinion shifters
- the parts of speech present in a text


## Vocabulary

##### Terms

Terms include words and phrases, but could also include punctuation, emojis, and emoticons as those can also imply mood or feeling. Words that we determine indicate positive or negative sentiment are called **sentiment words, or opinion words.**

#### Negation Words / Opinion Shifters

Words like *not*, can have a big impact on the overall tone of a text.

Examples:

"I do like this movie" vs "I do ***not*** like this movie"

"This movie ***could have*** a better plot and the dialogue is ***hardly*** intelligent"

#### Subjectivity Classification

Some sentiment analysis research focuses on first identifying and removing non-subjective sentences, since those may not be relevant to the overall sentiment determination. This task of determining whether a sentence has enough subjective material in it to be considered an opinion.

#### Target

Each opinion has a **target** (sometimes called an **entity**). If we read the sentence, "This was the worst movie I ever saw," the target of that opinion is the movie.

#### Aspect

Each entity present in an opinion can also have **components**, or sub-parts, and **attributes**, or descriptors for the entity or component. If we see an opinion like "The amateurish ending of the plot was the worst part of the movie," the overall target of the opinion is still the movie, but we notice that there are additional components: **the movie has a plot, which itself had an ending, which was described as being amateurish.** These components and attributes are generically called **aspects** of the opinion.

#### Implicit vs Explicit

The writer may express an opinion about entities, components, and aspects either implicitly or explicitly. The following sentences demonstrate the difference in an explicit and implicit expression of an opinion about the entity, movie:

Case 1: "That was the worst movie I ever saw"

Case 2: "Well that movie was a total waste of $10"

In the first case, we identified an entity, movie, and the sentence clearly describes that entity as the worst. In the second case, a negative opinion can be inferred from the statement that the movie was a waste of money.

Understanding that this is a negative opinion requires understanding that movies cost $10, and that this person views wasting money as a bad thing. Teaching a computer to understand implicit opinions can be difficult.

## Trouble Spots

### Sarcasm & Idiomatic Statements

Consider statements like the following:

"You should go see The Little Mermaid if you have nothing better to do on a Saturday night, but you might be better off washing your hair or re-organizing your sock drawer"

"Has anyone else used the The Little Mermaid script to line a bird cage?"

These statements make sense if you know that washing your hair or re-organizing your sock drawer are considered boring activities, and lining a bird cage is what you do with worthless papers. The conditional statement "you should go" sounds positive, but is immediately offset by the "but" in the next clause. Sometimes questions are assumed to be neutral, in that they are designed to elicit information, but in this case, the second question is definitely meant to be negative.

### Comparative Opinions

A comparative opinion is one that tries to distinguish two or more items based on their shared characteristics. Consider the following comparative opinions:

Statement 1: "The songs in Beauty and the Beast were better than The Little Mermaid"

Statement 2: "Beauty and the Beast and The Little Mermaid both had some good music"

Statement 3: "The Little Mermaid has the best soundtrack of any animated film"

Statement 4: "Beauty and the Beast was funnier, but The Little Mermaid had better music"

Statement 1 is a direct comparison of the two movies in terms of the songs present in each, and one movie is considered superior to the other. Notice that the reviewer stops short of saying that the songs were good or bad, rather the two sets of songs are simply compared to each other and one came out on top.

Statement 2 compares the two movies to each other on the same "music" aspect, and finds that they are equally good.

Statement 3 finds that one movie is better than all other movies on the "soundtrack" aspect.

Statement 4 compares the two entities on two different aspects.

### Domain Specific Word Meaning

An example would be the word *unpredictable* which, when used in a movie review could be a positive descriptor (unpredictable plot), but when used in a car review could be a negative comment (unpredictable steering).

## Algorithms
