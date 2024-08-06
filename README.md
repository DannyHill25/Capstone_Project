# Capstone_Project
 **Digital Futures Academy Capstone project on sentiment analysis for Hearing Centre**

Welcome to my capstone project code! This code was developed as a result of all the skills and knowledge I acquiered during my time at Digital Futures' Academy. Originally, this was a project I had personally worked on using Excel and VBA coding, which had severy limitations in application and scope. Now, it's not only a more sustainable product, it also scalable and provides better and deeper insights than before.

***PLEASE NOTE***: this code only works on my local system, as the end-point connection was tested locally as a proof of concept. If you want to test the code, you will need to change end-point link to whatever you have access to.

## Code Improvements

### Obtaining the data
At first, you had to go to each centres website back-end and manually download the most recent submission form data. Once you had download the data, you had to make sure that it was stored in the same folder as the processing Excel file, and had to have a specific name structure.

With this code, you simply need to set up the end-point API access link to download the data automatically. The link itself in the code has been set up to loop through all listed centres, meaning that you can get other new centre information by simply adding the name to the list.

***Optiomisation point*** One thing that I would like to address in the future is that we it's only downloading the data needed. User email is one of them to ensure the code filters out duplicate messages and spam; however, this information should be annonymised during the extraction process, instead of later down the pipeline (as we will see further down).

### Processing the data
Before the capstone, I developed a piece of VBA code to handle 'spam filtering' annd remove duplicate messages. Duplicate messages are those that the same user sends back-to-back in a short amount of time, due to users clicking the submit button on the form multiple times (it's more frequent than you think). 'Spam filter' was a simple check for keywords in the messages and if they are, remove the message enterily.

Post capstone, 'spam filter' has been developed using a count vectorizer model to determine the likelyhood of a message being spam or not. This model is trained agaisnt a csv file containing samples of non-spam and spam messages. The main advantage of this system is that it's much easier to maintain, as you don't have to manually add new keywords for new forms of spam. What's more, once the dataset grows larger, you can add sample messages from the dataset into the csv filter file to ensure you capture latest forms of spam, while also tunning the model to the form submissions.

As mentioned before, this code also annonymises users emails and then performs a duplicate check to remove duplicates.

### Analysing the data
For this step, previously I used a Pivot Table to develop some simple graphs illustratring in what predefine category a message was submitted for, and shows a timeline of count of messages, distribution and quartely performance.

Now, using a sentiment-analysis model, we can organicly develop categories based on users forms and keyword frequency, while also developing the same time analysis performed before.

***Optiomisation point*** Due to time constraints, this code only outputs the results of the sentiment analysis model. No other outputs are presented. To have a more complete report, several distribution graphs of unique messages, different types, keyword frequencies, etc per centre per timeframe should be available and developed at the end of the codes runtime.


## Closing

I hope you enjoyed and appreciate my work. It's been a very enjoyable journey, and being able to have a direct comparison between before and after learning more about coding and Data Analysis has been an incredible experience.

Please feel free to use my code, and suggest any improvements or alternative methods to optimise further.
