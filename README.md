# Project-Athena
<br>
After recently watching some of the Iron Man movies, and realizing that I can run a llm locally on my computer, I thought it would be a really cool project to try and make something similar to JARVIS, with a fully customized computerized assistant. I plan on eventually making a system that allows me to connect to and use the assistant from anywhere in the world, but before that, I realized that there were some issues I wanted to fix with the model I decide on using.
<br>
After testing several open source llms, I noticed that there are a lot of questions that they consistantly get wrong, often with spelling or simple math, so I decided to try to fine tune a model so it would be able to answer more questons correctly.
<br>
I chose to use the alpaca format for my dataset, since it is easy to use and accepted by most programs and llms. For example:
<br></br>

``` json
{
  {
    "instruction": "",
    "input": "",
    "output": "",
  },
  {
    "instruction": "",
    "input": "",
    "output": "",
  }
}
```

The current dataset is not massive, but I will likely suppliment it with additional data, whenever I find something that the model struggles with.
<br></br>
I have not yet figured out how exactly I will connect to my computer to remotely access the ai; this will definitely be the most difficult part of the project, and I still have to decide on the exact features I would like, but there are some I know I will work on implementing.
<ol>
  <li>LLM model fine tuned to respond more accurately to some questions</li>
  <li>Give the LLM acces to either the internet, or an external database for a wider, more up to date knowledge base</li>
  <li>The ability to access the assistant from a seperate network, and eventually through a cellular connection</li>
  <li>The ability to have a camera that can send images back to the host computer, allowing the LLM to anylize them</li>
</ol>
<br>
Though most of the training data is my own, I used a couple external resources to help increase the diversity of training data.
<br></br>
<ul>
  <li>Some scenarios for training from <a href="https://arxiv.org/html/2405.19616v1#S9">https://arxiv.org/html/2405.19616v1#S9</a></li>
  <li>Includes some training data from <a href="https://github.com/gururise/AlpacaDataCleaned">https://github.com/gururise/AlpacaDataCleaned</a></li>
  <li>Includes some resaoning problems from <a href="https://www-formal.stanford.edu/leora/commonsense">https://www-formal.stanford.edu/leora/commonsense</a></li>
</ul>
<br>
This dataset is still in progress, so the files will be changing until it is more tested and finished.
