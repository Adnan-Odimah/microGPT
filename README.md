# Learning how to create a GPT Model

Attempting to create a Generative pre-trained transformer model. This will be utilised in Project Athena as a replacement for OpenAI API when complete enough. This is also a great learning experience and will help me satify my interest and curiosity in learning about AI and it's limits.

I will be following a tutorial to start, in order to get a general foundation but plan on adding my own customisation's whether to get a specified outcome, to do it in a way that I understand more or a way I _think_ may be more efficient.

The plan is to initially use a smaller dataset, (Maybe the Shakespeare one) in order get a deeper understanding of how the model works exactly then get new data from various sources to improve the model.

Thing's I have yet to think about:
- How to classify sarcasm and jokes. (Since in Athena, there will be a setting for this)

Next steps:
- Figure out how to add the input encoding and fine-tuning for the model in order to assist it in generating relevant texts. Initially, I think I will ask questions relevent to Shakespeare as that dataset is already available.
- Optimization, look into the maths and possible work-arounds in order to improve computing efficiency and speed.
- Get a better understanding of each components relevance to how the model operates.

Currently, this generates a relatively english-like text in shakespeare-ian english. It is slightly inaccurate due to the limitations of my machine with batch sizes etc. The text is non-sensicle but is mostly english words. This is because the model currently uses tokens to figure out what letters should show after each other. Basically it is guessing which of the letters in the vocab can be used to make a word that is english with no purpose behind the generation.

In order to add this 'purpose' we need to fine-tune it such that it utilises relevant data according to an inputted text. This is currently a decoder only model and would require the encoder module in the paper in order to achieve this prompt-like fashion.
