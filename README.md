Here is the link of notebook:
https://colab.research.google.com/drive/1OXJ3P8G7mQVq4l7jTar4oYO1uvuVN-f8?usp=sharing

Python Data Types-Basics
>>> my_number = 1
>>> type(my_number)
Output: int
>>> my_decimal_number = 0.1
>>> type(my_decimal_number)
Output: float
>>> my_char = ‘ABC’
>>> type(my_char)
Output: str

Built in data types



Python Libraries
External code base that we can use with functions and objects that’s not readily available in base Python
Internal: Math, String
External: Pandas, Keras, NumPy


Python Lists
Lists are mutable objects that wee can use and access by index.
my_list = [1, 20, 34, 63, 62, 21]
my_list[0]	-> returns 1 as index on python start on zero
my_list[3] 	-> this returns 63 as index 3 fetches the object from position 3 + 1
my_list[1:3]	-> this returns a new list with 2 elements 20, 34


Python Sets
Sets are objects that contain distinct elements
My_list = [1,1,1,2]	-> this list has 4 elements
>>> set(my_list)	-> if you call set on my_list you get the returning distinct elements of the list
Output: {1, 2}









Python Dictionaries
Key value pair objects that are extremely flexible in Python
>>> month_dictionary = {‘Jan’:1, ‘Feb’:2, ‘Mar’:3, ‘Apr’:4}
-> Dictionary with 4 elements that maps the name of the month to the respective number

>>> month_dictionary[‘Jan’]
-> Accessing the key returns the value of the dictionary

Important attributes:
.items()
.values()
.keys()


Python Tuples
Paired objects that can be accessed by it’s index.
>>> list_of_tuples = [(1,’A’),(2,’A’),(3,’A’)]	-> Creating a list of types
>>> list_of_tuples[0] 	-> Accessing the first tuple
Output: (1, ‘A’)


Python Control Flow
For loops
my_list = [1, 2, 3, 4]
For item in my_list:
	print(item**2)
Output: 
1
4
9
16
While loops
max = 10
i = 0
while i<=10:
	i = i + 1
	print(i)



If statements
if my_var == ‘Hello’
	print(‘Hi’)
else: 
	print(‘Please say Hello’)



Python functions

Functions enable you to create code that you can reuse and pass parameters(if you want to)

# defining the function say_hi that takes the argument name.
>>> def say_hi(name):
	print(‘Hello’ + name)

# calling the function with the argument John
>>> say_hi(‘John’)
Output: John



Numpy Overview
Linear algebra library that enables you to manipulate arrays inside Python
>>> import numpy as np
np.array([0,1,2])		-> 1D array
np.array([0,1,2], [3,4,5])	-> 2D array



Pandas Overview























String




















NLTK(Natural Language Toolkit)
First release: 2001
Developed by: Department of computer and information science at the University of Pennsylvania
Highlights: POS Tagging, Tokenization, Stemming, Lemmatization




Stemming
Stemming is a text normalization technique that helps you to reduce words into similar prefixes.
Eg: 
Creating -> create
Creation -> create

Pros: reduces your vocabulary, Saves space
Cons: Lose information


Lemmatization
Lemmatization is a text normalization technique that helps you to reduce words into the root of the word.
Eg:
Is -> be
Are -> be
Be -> be

Pros: reduces your vocabulary, Saves space
Cons: Lose information, Needs parts of speech













POS Tag
Part of speech tag relates to the function of a word in a text:
Eg: 























N-Grams




Tokenizer



NOTE: len(array_name)	-> gives the length of the array





Stemming

Getting to the root of the word means stemming. token means single word 
Eg: 	run -> run 
running -> run
There are mainly three stems techniques:
Porter: vanilla(basic one)
Snowball: advance
Lancaster: more aggresive(risk of over stemming)

word_2 = 'controversial'


print(porter.stem(word_2))
print(lancaster.stem(word_2))
print(snowball.stem(word_2))
Output: 
controversi
controvers
Controversi





Lemmatization
lemmatization is a normalization technique that we can apply to out sentences/tokens.

Eg:

We have to import it’s library
from nltk.stem import WordNetLemmatizer
then
Lemmatizer = WordNetLemmatizer()
porter.stem(‘worse’)
Output: wors
































NLP Pipeline
NLP pipeline is a set of steps followed to build an end to end NLP software.
NLP software consists of the following steps:
Data Acquisition: data gather karna
Text Preparation
Text Cleanup: remove spelling mistake and emojis
Basic preprocessing: tokenization, words by words alag karte hai
Advance preprocessing: Parts of speech tagging, chunking, co reference resolution:
Feature Engineering: jab hum machine learning ya deep learning algorithms apply karenge to uske liye hume correct format me data chahiye rahega
Modelling: Jab actual me algorithm apply ki jati hai use modelling kehte hai
Model Builing
Evaluation
Deployment
There are three steps of this:
Deployment: hum apne model ko kisi cloud service par deploy karte hai jaise(aws, azure)
Monitoring: hum apne model/software ko constantly monitor karte hai
Model update: current model ko update ya replace karna ho to


Points to remember
It is not universal
Deep learning pipelines are slightly different
Pipeline is non-linear


		
















Data Aquisition

1. When Data is Readily Available:

If the data is readily available in a table format or any structured form, it simplifies the process. You can directly use it for analysis or training models.

2. Available but Unorganized:

In cases where the data is available but unorganized, data engineers or data preprocessing tools can be employed.

3. Less Data Available:

Some techniques that can be applied to increase the amount of data when data is scarce. A data augmentation technique is applied to increase the diversity of Data.












Feature Engineering
(Text ko number me convert karna)
Sentiment analysis karne ke liye, ek sentences ke andar ke positive word ka count lelo, negative words ka count lelo, neutral words ka count lelo aur isse hum sentiment ka pata laga sakte hai



ML algo/ ML pipeline
Hume features batana padta hai
preprocessing->feature generate->algorithm


Hume features generate karne padenge
Domain knowledge hona chahiye
Deep learning/ deep learning pipeline
Khudse feature decide karke khudse sara kaam kar leta hai, hume pata nhi chalta ki backgroud me usne kounse feature lagaye hai.(automatic neural network features generate karke de dega)

preprocessing-> algo

Eg: spam email detect kar lega, lekin pata nhi chalega ki kounse words ko spam maan rha hai


Khudse features generate kar dega
Domain knowledge zaruri nhi hota(backgound me jo hora hai uska pata nhi chalta)



Modelling
Modelling:- 
Heuristic
ML algo
Deep Learning 
Cloud API
Evaluation


Modelling technique depends of amount of data and nature of problem.

Eg:- Spam classification: 
Heuristic approach:
1st approach) email id ko hi spam declare kardo
2nd approach) kisi email me “sale” word bahut jyaada aa rha ho to vo spam declare kardo


Machine Learning approach: 
No of positive and no of negative words ko count karlo

Kabhi kabhi koi problem par do approaches ko saath me laga sakte hai
Jaise spam classification me: email id ko spam declare kardo aur no of positive aur no. of negative words ko classify kardo

Deep Learning approach:
Bahut bada amount of data ho to use karte hai
Eg: BERT LLM hai uska use karke bhi koi problem solve kar sakte hai

Cloud API approaches:
Cloud service ka use kar sakte hai, cost jyaada lagti hai



Evaluation
Intrinsic evaluation:
Technical level par check karte hai model ka performance kaisa hai
Extrinsic evaluation
Model jab deploy ho jata hai aur jab user usko use karte hai tab business setting me usko test karte hai

NOTE:
perplexity-> iska matlab model kitna confused hai
Mujhe ye pata karna padega ki meine jitne suggestion dikhaye aur user ne kitne suggestion ko use kiya


Deployment
Teen steps:
Deploy
Monitor
Update

Deploy
Eg: email spam detection
Suppose if we have created a software email spam classifier(jo spam email check karta hai), and this is not a full fledged software.
To ye feature ko as a API(microservice) hume kisi cloud service pe deploye karna hoga
To jab usko jab bhi hit karenge matlab us api par email ka text bhejenge aur vo api check karegi ki vo email smap hai ya nhi.


Monitor: monitor karte rehna ki humara model theek se work kar rha hai ya nhi

Update: humara product/software hai usme koi update needed ho to phirse model ko train karke update karna padta rahega



Video - 3
Text Preprocessing
Lowercasing, remove html tags, remove url’s, remove punctuation, chat word treatment, spelling correction, removing stop words, handling emojis, tokenization, stemming, lemmatization
