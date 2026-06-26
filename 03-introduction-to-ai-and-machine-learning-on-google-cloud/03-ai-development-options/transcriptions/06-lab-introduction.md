SPEAKER: Now it's time for some hands-on practice.
00:02
In the following lab, you'll use the Natural Language API to analyze text.
00:08
Specifically, you'll identify entities and analyze sentiment with code.
00:13
Before you begin, let's briefly review the main features of the Natural Language API you learned in the previous lesson.
00:21
You can identify entities, which are subjects in the inputted text, such as Google as a company name and Mountain View as a location.
00:30
You can identify the sentiment, which indicates emotion at both the overall document and individual subject level.
00:38
You can analyze syntax and extract linguistic information, such as the relationship between words.
00:45
And you can also classify the text to categories based on topics or keywords, similar to assigning a tag to a piece of text.
00:54
You perform all of this analysis through a UI, which is a quick and efficient way to demonstrate and test these features.
01:02
However, if you want to incorporate these features in production, you must embed the APIs into code.
01:09
Using APIs in your code is similar to ordering a sandwich at a deli.
01:14
You order from the menu and get your food without worrying about how it was made in the kitchen.
01:18
The same concept applies to using APIs.
01:21
You only need to know three things, the features, the menu, the input, the order, and the output, the sandwich.
01:30
Like a menu, features are the types of requests that you can make to the Natural Language API.
01:36
Like a food order, the input is how you construct the request.
01:40
Then the sandwich you receive after you place the order is the response or output.
01:45
With this, you can determine next steps.
01:48
So, what are different types of requests that you can make?
01:52
The Natural Language API provides several methods for performing analysis and annotation on your text.
01:59
You'll practice with most of them in the lab.
02:01
For entity analysis, you can use the analyze entities method.
02:06
The sentiment analysis is performed through the analyze sentiment method at the entire text level and analyze entity sentiment at the individual, entity, and subject level.
02:17
The syntax analysis is performed with the analyze syntax method.
02:22
And the content classification is performed by using the classify text method.
02:28
Now, how do you construct those requests?
02:31
The Natural Language API is a REST API and consists of JSON requests and responses.
02:38
A simple JSON request for entity analysis looks like the code shown here, where you define the type of the document, for example, plain text, the language, like
02:48
EN, which stands for English, the content, which can be the text itself, or the file location in Cloud Storage, and finally, the encoding type, like UTF 8.
03:01
After you construct the request, you need to call the API, just like, after you decide
03:05
what you want at a deli, you need to place the order with the counter person.
03:11
Here's an example to call the API with curl.
03:14
Curl stands for Client URL and is a command line tool to transfer data between client and server.
03:21
You can also use other programming languages, such as Python and Java SDKs, to call the APIs.
03:28
Typically, the vendors of the product and services you're using define the APIs and provide the SDKs in different languages for you to choose.
03:37
In this example, you call the Natural Language API feature analyze entities, pass the request.json file that you just constructed, and save the response to result.json file.
03:51
Finally, how should you handle the responses?
03:54
You can review the result by using a command like cat result.json, or parse it for further usage.
04:02
Equipped with the technical details, in this lab, you'll use the Natural Language API to extract entities, analyze sentiment, and analyze syntax.
04:14
By completing the lab, you'll get practice creating a Natural Language API request and calling the API with curl, extracting entities
04:21
and running sentiment analysis on text, performing linguistic analysis on text, and creating a Natural Language API request in a different language.
04:33
Let's start.