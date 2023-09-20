# Data-Scientist-Challenge
Data Scientist Challenge for Nimble Gravity
by Juan Pablo Estavillo


# Description
The goal of this repository is to present the technical challenge given by Nimble Gravity, 
providing with evidence of my proficiency in python and my ability to extract
meaningful insights from complex data, and my creativity in approaching open-ended questions.


The challenge consist of 3 challenges, one mandatory and two optional, reffered in:
* task 1 Understanding User Journeys
* task_2  Longest Way to TripAdvisor
* task_3  User Engagement and Retention Analysis

These 2 files should be runned in this order, given that all tha data cleaning and transformation happens in
file 1


## Instalation

### Requirements
In order to run the task notebooks, we must install the libraries used to solve the challenges from the file 
'requirements.txt'using the following
command in your terminal.

```
pip install -r requirements.txt
```


## Data


### Download AWS CLI
First we have to download the data, to do so we are going to use AWS cli, since 
it is mantained at optimal levels and it uses multi threading to copy multiple files simultaneously,
so the copy operation takes less elapsed time.


Follow the instruction to have it installed in the wizard.

### Configure  AWS Keys

After the instalation, it is required to configure given challenge keys
under the terminal, run the command.
```
AWS configure
```


This will follow up with 4 parameters to fill:
the first one is the access key from the challenge
```
* AWS Access Key ID: ****************7SAA
* AWS Secret Access Key: ****************PQr3
* Default region name: us-west-2
* Default output format: json
```
* For security reasons, full keys are not shown


### Download Data
The data is stored in parquet format. Apache Parquet is an open source, 
column-oriented data file format designed for efficient data storage and retrieval.
To download, just go to the terminal, and use the following command to download the data,
changing the path with the location of the project and the LocalFolderName with the data folder

```
aws s3 cp s3://BUCKETNAME/PATH/TO/FOLDER LocalFolderName --recursive
```

## Additional tools to get you started
about parquet apache
https://parquet.apache.org/
about aws cli
https://docs.aws.amazon.com/cli/latest/userguide/getting-started-install.html
https://docs.aws.amazon.com/cli/latest/userguide/cli-chap-configure.html


## How To Use The Project

### Data Cleaning
The first thing to do is work with the data, to clean it and transform it to extract more meaningful insights
Thats where the functions of data cleaning come in handy, just by running the cell of get_clean_data,
the data is cleaned for further uses applying:

* ordering
* extracting domain
* extracting sub domain

### Data Transformation

in order to we know the user journeys, it is neccesary to transform the data into sequence, with get_user_journeys
the cleaned data can be transformed into a sequence of domains visited by the user ending in tripadvisor in 
a selected timeframe.


## License
 
The MIT License (MIT)

Copyright (c) 2023 Juan Pablo Estavillo

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.

