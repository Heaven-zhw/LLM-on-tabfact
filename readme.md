

# Are Large Language Models Table-based Fact-Checkers?

20240201 Share the result files of ChatGPT and LLaMA on tabfact small test 

## Result File Description

### Results of ChatGPT 

All ChatGPT results are TSV files. In each row:

- The first element is ID number

- The second element is the full response of ChatGPT

Notice: There are in 2024 samples in original small test. But in the preprocessing of [original paper](https://github.com/wenhuchen/Table-Fact-Checking), the authors exclude samples containing "=", so the actual number of small test split they use is 1998. Here we show the results of all 2024 samples, but in evaluation we just consider 1998 samples which don't contain equals sign. 

###  Results of LLaMA

All LLaMA results are JSON files. The descriptions are as follow:

- _id：sample ID
- table_file: table file name in original Tabfact dataset
- instruction: instruction info in prompt to guide the models
- input: input content of a sample,  i.e. , table and statement
- output: golden label of the sample
- table_type: table type, tables in Tabfact are all "vertical"
- task_type: task name
- dataset: dataset name 
- response: the output content of LLAMA, the new generated content is after the last [\/INST]
- [history]：dialogue history

Notice: The numbers in `_id` of samples are not continuous increment, because we exclude the samples containing equals sign.  They are corresponding to the number in  "_id" of ChatGPT results.