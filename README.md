# Project Description
The goal of this project is to develop an information extraction algorithm from pdf documents in chemical distributor industry to extract pre-defined attributes. Two algorithm is provided in this project- rule-based if loop+ regular expression and custom entity recognition model.
# Rule-based if loop+ Regular expression
This method requires users to first go through every pdf files to figure out the word patterns and rules of each attribute.

**1.** Separate attributes into two groups- **with or without uniform format**. For the attributes with uniform format, **Regular Expression** can be easily applied to extract the information. For the attributes without uniform format, rules for the attributes have to be defined.

**2.** Design the code based on the word patterns and rules.

**3.** Import the pdf files into the algorithm. The algorithm will first extract the text from the pdf file and extract the attribute information from the text.

**4.** The extracted information will then be saved as a dataframe, excel files, or forms that can be executed by SQL.
### Pros
* Low complexity
* No need for training model
### Cons
* Less flexible and scalable
* Might not work for every future document if the naming conventions or rules are different

# Custom Named Entity Recognition
This model stems from named entity recognition model, a context based information extraction algorithm that define attributes such as **Name**, **Location**, **Country**, and etc. Custom Named Entity Recognition allows users to target the entities based on **user-define tags**.

**1.** Separate pdf files into training and testing groups.

**2.** Extract text from the pdf files in the training group.

**3.** Annotate the user-defined named-entities.

![Alt text](https://github.com/ChengOscar/Information-extraction-algorithm-in-chemical-distributor-industry/blob/main/Annotation.png)

**4.** Export the annotation into json files and import the json files into the model.

**5.** Train the model with base_config.cfg file. The file can be downloaded here:  https://spacy.io/usage/training.
And the setting should be as the picture.
![Alt text](https://github.com/ChengOscar/Information-extraction-algorithm-in-chemical-distributor-industry/blob/main/base_config_cfg%20setting.png)

**6.** Once the training is finished, the testing pdfs can be imported. The model will automatically extract the attributes information and saved into dataframe.
### Pros
* Less restrictive to the format
* Dynamic
* Very scalable and flexible
### Cons
* Time consuming (training model takes 40 minutes with only 16 documents)
* Model performance is restrictive to the quality of training data
