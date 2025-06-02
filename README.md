# Project-Athena
<br>
<p>
  After recently watching some of the Iron Man movies, and realizing that I can run a llm locally on my computer, I thought it would be a really cool project to try and make something similar to JARVIS, with a fully customized computerized assistant. I plan on eventually making a system that allows me to connect to and use the assistant from anywhere in the world, but before that, I realized that there were some issues I wanted to fix with the model I decide on using.
</p>
<p>
  After testing several open source llms, I noticed that there are a lot of questions that they consistantly get wrong, often with spelling or simple math, so I decided to try to fine tune a model so it would be able to answer more questons correctly.
</p>
<p>
  I chose to use the alpaca format for my dataset, since it is easy to use and accepted by most programs for training llms. For example:
</p>

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

<p>
  Because of the amount of data needed for a quality fine tune of an LLM, It would have taken me way too long to create every example by hand. To speed it uo, I created examples and the had GPT-4o create more based on my data. I then checked all of the date for any incorrect answers, to make sure I did not have any bad data. This still took a while though, so the current dataset is not massive, but I will likely suppliment it with additional data, whenever I find something that the model struggles with.
</p>
<p>
  Fine tuning is a bit of a challenge, since I am using an AMD GPU, which is not as supported for this use, especially on Windows. ROCm, the platform for running AI software on AMD hardware, is designed for Linux, so I have not been able to find any software for training AI models on Windows with my hardware. To get around this, I am going to try WSL for running any Linux software.
</p>
<p>
  After fine tuning the model, my next goal is to set up the LLM to automatically call on tools to get up-to-date information for certain questions, such as getting the current weather. I expect this to be a bit of a challenge, because my current base model (Llama 3.2 vision 11b) is not supported for tool calling by Ollama. Many examples of tool calling also need the tool calling information in the prompt, which I want to avoid because I am planning on getting this to work as a voice assistant, which needs to function with less formatted inputs. I will be doing some more research on this, but if I am unable to get this project to work with Ollama, I am likly going to use the Llama API, since it should support tools with my model. I am currently on the waitlist for access, so that will hopefully go through soon so I can continue testing.
</p>
<p>
  I have not yet figured out how exactly I will connect to my computer to remotely access the ai; this will definitely be the most difficult part of the project, and I still have to decide on the exact features I would like, but there are some I know I will work on implementing.
</p>
<ol>
  <li>LLM model fine tuned to respond more accurately to some questions</li>
  <li>Give the LLM acces to either the internet, or an external database for a wider, more up to date knowledge base</li>
  <li>The ability to access the assistant from a seperate network, and eventually through a cellular connection</li>
  <li>The ability to have a camera that can send images back to the host computer, allowing the LLM to anylize them</li>
</ol>
<p>
  Though most of the training data is my own, I used a couple external resources to help increase the diversity of training data.
</p>
<ul>
  <li>Some scenarios for training from <a href="https://arxiv.org/html/2405.19616v1#S9">https://arxiv.org/html/2405.19616v1#S9</a></li>
  <li>Includes some training data from <a href="https://github.com/gururise/AlpacaDataCleaned">https://github.com/gururise/AlpacaDataCleaned</a></li>
  <li>Includes some resaoning problems from <a href="https://www-formal.stanford.edu/leora/commonsense">https://www-formal.stanford.edu/leora/commonsense</a></li>
  <li>Data for moral exceptions from <a href="https://arxiv.org/abs/2210.01478">https://arxiv.org/abs/2210.01478</a> Undar a <a href="https://creativecommons.org/licenses/by-nc-sa/4.0/">CC BY-NC-SA 4.0 International License.</a></li>
</ul>
<p>
  This dataset is still in progress, so the files will be changing until it is more tested and finalized.
</p>
