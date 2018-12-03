# Character-Traits-Internet-Usage



# Overview

In a typical business scenario, one would want to understand their customers better on demographics, culture, and their interests scale by their previous purchasing records and the kind of products they would be investing in future. This will in turn help improve the business process and overall customer satisfaction. My interest builds upon the fact that our behavior can be drilled down to the minimalist characteristic traits of our nature, our culture, our beliefs, and our habits. I have selected the Young people survey dataset, as it has the necessary set of features to study the character traits along with the demographics of young people. With this young people survey dataset, I was curious to know if we can describe the character traits of young people based on their Internet usage levels.

The Internet has made life a lot easier by making information more accessible to all and creating connections with different people around the world[1]. However, it has also led a lot of young people to spend a considerable amount of time on the internet every day and it has become an integral part of their lives. 

# Dataset Studied[3]
In 2013, students of the Statistics class at FSEV UK were asked to invite their friends to participate in this survey. The survey was presented to participants in both electronic and written form. The original questionnaire was in Slovak language and was later translated into English. All participants were of Slovakian nationality, aged between 15-30.
Source URL : Kaggle (https://www.kaggle.com/miroslavsabo/young-people-survey)

# Description of & Structure of the Data

The survey was taken on a Likert scale and It is the most widely used approach to scaling responses in survey research, such that the term is often used interchangeably with the rating scale.
The variables can be split into the following groups:
Music preferences (19 items)
Movie preferences (12 items)
Hobbies & interests (32 items)
Phobias (10 items)
Health habits (3 items)
Personality traits, views on life, & opinions (57 items)
Spending habits (7 items)
Demographics (10 items)
The dataset was in .csv format and for convenience, the original variable names in the dataset were shortened in the data file. Another file columns.csv file was used to match the data with the original names. The data file (responses.csv) consists of 1010 rows and 150 columns (139 integer and 11 categorical). The dataset contains few missing values in almost every column.
The integer features are in the range of 1 to 5 as either of the follows:
Strongly disagree 1-2-3-4-5 Strongly agree
Don't enjoy at all 1-2-3-4-5 Enjoy very much
Not interested 1-2-3-4-5 Very interested
Not afraid at all 1-2-3-4-5 Very afraid of

# Notes on Exploration of the Dataset

There were some blanks in almost all the features. We do not know why people did not fill or maybe there was a post-processing error (how the data was transferred to the digital form) in the dataset. If people did not fill the data, then leaving a survey question also tells something about the respondent’s character trait. Therefore, the blank values were kept as it is and were counted to find if it would reveal any interesting observation at a later point.

There were 1010 responses for the survey which had 150 questionnaires (139 integer and 11 categorical). My goal was to analyze the internet usage level – Internet usage level as a categorical feature which could be either of the following : Few Hours a Day, Most hours of Day, Less than an hour and no time at all. The internet usage column has no blanks and only 3 responses correspond to “no time at all” internet usage, which implies that almost everyone uses the internet these days daily[7].

Now, with this knowledge on data, I can examine questions like “ Of the people who used the internet few hours a day, what percentage of them have strongly agreed to have healthy lifestyle” To categorize the character traits at each level, I have filtered the responses for each of the character traits and separated them into separate sheets in excel for percentage calculations of each trait. After calculating the percentages of people who have responded strongly agreed/agreed/neutral/strongly disagreed in personality traits features across the internet usage levels of few hours, most hours, less than an hour, no time at all and measuring the majority of the opinions for each trait revealed an interesting pattern that young people irrespective of the number of hours spent on internet exhibit similar behaviors (45 out of 57-character traits). However, the opinions of people who used the internet most number of hours a day exhibited contrasting personality traits. 

Following were the 12 contrasting traits of a majority of respondents who spent most of the hours on the internet: 
I try to do tasks as soon as possible and not leave them until last minute. Strongly Disagree(32.6%)
I always make a list, so I don't forget anything.         Strongly Disagree(31.45%)
I often study or work even in my spare time.	      Strongly Disagree(30.65%)
I look at things from all different angles before I go ahead.	Agree(25.81%)
I believe bad people will suffer one day and good people will be rewarded.      Strongly Disagree(%)
I can fall for someone very quickly and then completely lose interest.	Agree(22.58%)
I would rather have lots of friends than lots of money.	Neutral(33.87%)
I often think about and regret the decisions I make.	Strongly Agree(39.52%)
I try to give as much as I can to other people at Christmas.	Strongly Disagree(27.42%)
My moods change quickly.	Agree(29.84%)
I am not afraid to give my opinion if I feel strongly about something.	Agree(31.45%)
I cry when I feel down, or things don't go the right way.	Strongly Disagree(25%)

Next, I took 11 categorical features and made similar classification as done for numerical features. However, the data descriptions must be analyzed across each category of categorical variables for each internet usage level. Since the data was structured, using excel features and formulas, I was able to get summaries for each categorical variable quite easily to look for any patterns in them.  There were more female respondents (593) than male respondents (411) and most respondents have secondary school(621) as their highest education level and bachelors come next (212 respondents). Most of them have at least one sibling. Most live in the block of flats(595) rather than in an independent house(411). However, a majority of the people who spent less than an hour on the internet live in independent houses. A majority of respondents have accepted that they lie sometimes and a majority of them are social drinkers and have tried smoking. People who spend most of the hours on the internet are perhaps drinkers - either social drinkers or those who drink a lot. The dataset had too many variables to analyze and to have fun exploring. However, it is important to stick to the goals rather than knowing the facts from dataset just because they are interesting. Therefore, with the new observations from the dataset, the goals had to be adjusted by putting them through pragmatic filter What is possible? What is valuable? What is efficient?

# Questions to Ask of the Dataset

As mentioned in the textbook by Godsey, every question has assumptions, and if those assumptions don’t hold, it could spell disaster for your project. It’s important to think about the assumptions that your questions require and decide whether these assumptions are safe.
The assumptions that below questions had were, the character traits could either be positive or negative traits at a very basic level that are universally accepted by the general audience irrespective of cultures or beliefs. 

-->Looking at the above responses by the people who spent most number of hours a day using the internet, tend to have more negative traits but is there any correlation?

Correlation describes the degree of relationship between the two variables. However, it tells nothing about the causality. Just a small example, the anti-violent gaming policies say that there is a correlation between time spent on playing violent computer games and a violent behavior. In fact, we do not know if the computer games make a person violent or a violent person would play more violent games.

-->Do a majority of the people who spend most of the hours a day using internet exhibits character traits which are classified under one of the Big 5 personality traits[2]?

Openness, Conscientiousness, Extraversion, Agreeableness, and Neuroticism or OCEAN
Openness - People who like to learn new things and enjoy new experiences usually score high in openness. Openness includes traits like being insightful and having a wide variety of interests.
Conscientiousness - People that have a high degree of conscientiousness are reliable and prompt. Traits include being organized, methodical, and thorough.
Extraversion - Extraverts get their energy from interacting with others, while introverts get their energy from within themselves. Extraversion includes the traits of energetic and talkative.
Agreeableness - These individuals are friendly, cooperative, and compassionate. People with low agreeableness may be more distant. Traits include being kind, affectionate, and sympathetic.
Neuroticism - This dimension relates to one’s emotional stability and degree of negative emotions. People that score high on neuroticism often experience emotional instability and negative emotions. Traits include being moody and tense.

# Adjusting Goals 
Now that I have a better understanding of the data and the interesting observations made from the dataset, there was a new hypothesis that I could come up with “ People who spend most number of hours a day using internet classify under neuroticism personality trait”. In the presence of the new information I had as a result of the early exploratory stages of the project and the kind of questions asked to the dataset, revisiting the same process here to answer these questions again:
# What is possible?
There should be relevant data that could map personality traits to one of the 5 Big personality traits. However, mapping them to the exact questionnaires in the survey is challenging.
#What is valuable?
The values of the goals of the project haven’t changed much and classification would simplify the personality traits variables by grouping them. Features of interest in the dataset are a group of numerical variable questionnaires pertaining to personality traits, views on life, & opinions.
# What is efficient?
Start with the negative connotation traits of 5 Big Personality traits and try mapping them into responses that have high Internet usage levels.

# Strategy to Process the Data
The Big 5 model requires a special set of items. However, we can try to develop a new psychometric model from the data. Starting with factor analysis[4] from personality items and then try to look at the interpretation of the factors found. Maybe the factors found will be very similar to those from the Big 5. Or maybe we might spot something new. If unsuccessful, revisit the goals and consider whether it is worth spending more time on this one.

# Summary
This dataset had Likert[6] scale type questionnaires, though a little confused on how I would analyze several aspects of the dataset if the number of questionnaires was this huge. However, eventually, I learned how to derive descriptive statistics from these kinds of surveys. Although the survey was taken by students of a class, the data and their responses could be biased towards that region’s culture and since it was translated, maybe some of the data could be misinterpreted. The missing values in the dataset could perhaps be due to the conversion errors while converting the survey to English. This dataset could potentially be used for further research for knowing how interests and traits can speak up to a broader spectrum of every individual’s opinions. This project was an eye-opener for me as I got to know how creative and patient one must be to become a true data scientist, the deliberate process will come in hand to make informed decisions while processing the data. Data scientists need to have awareness about the data to go further into the project, there could be several pitfalls during the initial days of becoming a data scientist, however, with enough experience, it could be avoided. The skills one would require to have a successful career in data science is to have both analytical, computer tools/technologies know-how and the most important component of this entire process that is the awareness of the subject matter and to have a mathematical approach all along. Effective ways of using and exploring the data could be learned through knowing any scripting language like Python, R or MATLAB. Big data technologies to store and process huge amounts of structured, unstructured or semi-structured data. Data mining knowledge to analyze patterns in the data and Machine learning algorithms to predict things in the future or to calculate the likelihood and classify things. The process of following the deliberative approach and working with data on regular intervals over several weeks did help me to look at data differently and get different perspectives and creative ideas to explore the dataset.

# References
1.	Abd. Rahman Ahlan & Naeem Atanda Balogun (2013) , Internet usage and personality traits: Finding relationship in learning institution, Transnational Journal of Science and Technology March 2013 edition vol.3, No.3, ISSN 1857-8047 https://www.researchgate.net/publication/261310710_Internet_usage_and_personality_traits_Finding_relationship_in_learning_institution
2.	Big Five personality test traits
https://www.123test.com/big-five-personality-theory/
3.	Dataset owner : Miroslav Sabo, Bratislava, Slovak Republic https://www.kaggle.com/miroslavsabo/young-people-survey
4.	https://www.kaggle.com/miroslavsabo/analyzing-gender-differences/comments
5.	Godsey, B. (2017). Think like a Data Scientist: Tackle the data science process step-by-step. Shelter Island, NY: Manning
6.	Presenting-Likert-data-pdf
https://www.cmu.edu/gcc/handouts/presenting-likert-data-pdf
7.	How to tabulate, analyze, and prepare graph from Likert Scale questionnaire https://www.youtube.com/watch?v=iawmdLDTJqM
8.	O1 – A2: Definition of Desirable Situations: Report of survey results in United Kingdomhttps://inscreenmode.eu/results
