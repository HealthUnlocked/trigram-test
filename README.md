# trigrams

A trigram is sequence of 3 words in any given text. Let's take an example sentence: "the cat sat on the other cat on the mat on the floor" - its trigram map will look like this:
```clj
{["the" "cat"]   ["sat"]
 ["cat" "sat"]   ["on"]
 ["sat" "on"]    ["the"]
 ["on" "the"]    ["other" "mat" "floor"]
 ["the" "other"] ["cat"]
 ... etc.
 }
 ```

To generate a new sequence of text, start with a key at random, say `["on" "the"]`, and then pick a value at random, say `"other"`, now you have a trigram `["on" "the" "other"]`. For the next trigram, you look up `["the" "other"]` and get a value at random - in this case there will only be one, `"cat"`. Continue ad infinitum.

Using a book of your choosing from [Project Gutenberg](https://www.gutenberg.org/) and the process described above, please complete the following:

1. Ignoring punctuation marks, generate a sequence of 50 words.
2. Generate 10 full sentences (sentences start with a capital letter and end in a punctuation mark).
3. Given a word from the text, generate a sentence which contains it anywhere inside it (i.e. not just the start).

