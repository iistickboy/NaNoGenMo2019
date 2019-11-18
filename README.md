# NaNoGenMo2019
This repository contains copies of the two Google Colab notebooks I used for my NaNoGenMo project.

I generated a manuscript inspired by my favorite subreddit, Writing Prompts. The manuscript consisted of a series of GPT-2-generated writing prompts and GPT-2-generated responses to those writing prompts.

OpenAI’s GPT-2 gave me access to a superpowered language model trained with a data set of 8 million webpages, all human-curated outbound links from Reddit. So much of the internet flows in and out of Reddit, it provides the scale of information needed to make a really sensible-sounding AI text generator.

Over at Reddit, the great u/disumbrationist trained an army of bots to create an entire Subreddit Simulator populated entirely by GPT-2 language models that were trained on the most popular subreddits. Following that example, I will create two large data sets.

Writing prompts seemed like the best way to work toward narrative coherence with GPT-2. 

After 17 days of text generation, my two GPT-2 language models have generated a 51,422-word manuscript filled with computer generated writing prompts and computer generated responses to those prompts.

The writing prompts were written by a fined-tuned GPT-2 language model I named “Jane Doe” after a character in one of the generated texts. The writing prompt responses were written by a fine-tuned GPT-2 language model I named “Mr. Output” after a character in another one of the generated texts.

MY STEPS

I created a dataset of writing prompts.
Using a Google’s BigQuery tool and the enormous archive of Reddit data archived at Pushshift.io, I saved thousands of individual writing prompts in a handy CSV file—each separated with <|startoftext|> and <|endoftext|> tokens.  I also used a Reddit search tool from Pushshift to collect hundreds of AI related writing prompts to add to the dataset. 

I love science fiction and technology-inspired writing prompts, so I wanted plenty of examples in my training set. At the end of my collecting, I had a writing prompt dataset with 1,065,179 tokens. GPT-2 is a massive language model, and you need a comparatively big dataset to finetune the model effectively. 

I collected a dataset of responses to writing prompts.
Using the same tools and lots of Reddit searches, I collected the highest rated and greatest writing prompts I could find online. I added lots of AI-focused responses, including my own writing prompt responses I’ve written over the years. I ended up with 1,947,763 tokens in this training dataset.

I structured my writing prompt response dataset. 
This step is really important for output. I wanted to give my AI the most uncluttered and high quality learning data possible, so I used a series of simple markers to teach GPT-2 the shape of a writing prompt response. I added <|startoftext|> and <|endoftext|> tokens to match the writing prompt dataset, but I also made sure each response had the original writing prompt marked [WP] and the response itself marked [RESPONSE].

While this was a huge time consuming effort, it made my output infinitely more interesting. I trained writing Ress Prompt prompter. 

I finetuned two separate GPT-2 models. I used the medium-sized 355M version of GPT-2 because it was large enough to handle my data set but small enough that it would run on Google Colab. I trained both models with 42,000 steps each. I broke the training into 10K chunks, because Google Colab won’t run longer than 12K steps.

I ran the finetuned version of Writing Prompt Prompter (Jane Doe) to generate between 10 and 20 pages of writing prompts every day.

I picked my favorite writing prompts, and fed them to Writing Prompt Responder (Mr. Output) to generate between 100 and 125 pages of writing prompt responses.

I repeated this processs for the first 17 days of November.  I combed through hundreds of pages of text that Jane Doe and Mr. Output generated, picking the most compelling stories. 

For every 350 words of compelling computer-generated writing that I gathered for NaNoGenMo, I had to plow through around 10,000 words of strange, confusing, repetitive, or just plain incomprehensible computer-generated text.

It was worth it. NaNoGenMo was a great writing and coding experience. There have never been so many resources available to amateurs like me and GPT-2 is truly powerful when trained finetuned. I'll be reading these GPT-2 generated stories for the rest of the year!

