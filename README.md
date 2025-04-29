# LLM-Training-Data
<br></br>
After testing several open source llms, I noticed that there are a lot of questions that they consistantly get wrong (there are 3 r's in the word strawberry, not 2!), so I decided to try to fine tune a model, so it would be able to answer similar questons correctly.
<br></br>
I chose to use the alpaca format for my dataset, since it is easy to use and accepted by most programs and llms. For example:

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

<ul>
  <li>Some scenarios for training from <a href="https://arxiv.org/html/2405.19616v1#S9">https://arxiv.org/html/2405.19616v1#S9</a></li>
  <li>Includes some training data from <a href="https://github.com/gururise/AlpacaDataCleaned">https://github.com/gururise/AlpacaDataCleaned</a></li>
  <li>Includes some resaoning problems from <a href="https://www-formal.stanford.edu/leora/commonsense">https://www-formal.stanford.edu/leora/commonsense</a></li>
</ul>
This dataset is still in progress, so the files will be changing until it is more tested and finished.
