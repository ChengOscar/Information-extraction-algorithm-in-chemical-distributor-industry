# Project Description
The goal of this project is to develop an information extraction algorithm from pdf documents in chemical distributor industry to extract pre-defined attributes. Two algorithm is provided in this project- rule-based if loop+ regular expression and custom entity recognition model.
# Rule-based if loop+ Regular expression
This method requires users to first go through every pdf files to figure out the word patterns and rules of each attribute.

**1.** Go through every pdf files to define the word patterns and rules of each attribute.

**2.** Design the code based on the word patterns and rules.

**3.** Import the pdf files into the algorithm. The algorithm will first extract the text from the pdf file and extract the attribute information from the text.

**4.** The extracted information will then be saved as a dataframe, excel files, or forms that can be executed by SQL.
### Pros
* Low complexity
* No need for training model
### Cons
* Less flexible and scalable
* Might not work for every future document if the naming conventions or rules are different
