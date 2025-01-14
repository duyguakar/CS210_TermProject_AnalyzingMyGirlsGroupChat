# **Analyzing My Girls Group Chat CS210 Project**

## **Description**

This project aims to profile the texting habits of participants in a sample Girls Whatsapp Groupchat and calculate their correlation to engagement. Through the exploration of various texting styles, and high frequency periods, the project aims to offer suggestions to maximize engagement.

Potential questions that will be inspected throughout the analysis are the comparison between the message activity and the time of the day to find out if the group activity peaks at certain hours; the frequency of the keywords such as "sorry" and "congrats" to map group dynamics; and the count of media files as well as the follow-up messages they generate to explore if media files lead to higher engagement in the form of replies.

In a greater context, profiling participants according to their previous interactions, texting styles, and keyword use might help constitute and manage groups that will maximize engagement. Please open the ipynb files on google collab through the link. Enjoy!

## **Tools**

**Pandas** - For data cleaning and manipulation. 

**Matplotlib** - For basic visualizations like bar and line charts. 
Seaborn - For advanced visualizations like heatmaps and box plots. 
NetworkX - For social network and centrality analysis. 
NumPy - For numerical computations and data handling. 

**NLTK (Natural Language Toolkit)**- For text processing and word frequency analysis.

**Regex (Regular Expressions)**- For cleaning and preprocessing chat data. 

**Data Preprocessing Libraries** - For formatting and preparing data. 

**WhatsApp Chat Export Tool** - For extracting raw chat data. CSV/Excel - For storing and accessing processed data.

## **Table of Contents**

- [**Motivation**](#motivation)
- [**Data Source**](#data-source)
- [**Data Processing**](#data-processing)
- [**Data Visualizations and Analysis**](#data-visualizations-and-analysis)
  - Findings: Centrality Measures
  - Monthly Activity Trends
  - Top Words Used
  - Message Timing Patterns
  - Response Time Distribution
  - Message Length Distribution
  - Day vs. Night Activity
  - Outgoing-to-Incoming Ratios to Analyze Group Dynamics
- [**Limitations**](#limitations)
- [**Future Work**](#future-work)


## **Motivation**

I aimed to choose a project as personal as possible to make sure the analyzing process was fun. My Girls group chat, active day and night, has nearly been a support group for me and my high school friends over the years. As we opened up a new group to keep each other updated as one of our friends moved abroad, the opportunity of using the chat to analyze our dynamics for this project arised. I couldn’t think of a better source of consistent, reliable source of personal data. Through the motivation of this analysis, I plan to gain a greater perspective on our group dynamics, whether it’s the type of language used, or the textual habits that each member has established. As I am curious about gaining insights about each members’ texting behavior and habits, I plan to discover ways to improve engagement, and establish to tools increase the activity levels. Certainly this analysis will be our trend-topic in the upcoming meetings.

## **Data Source**

My main source of data was the Whatsapp Chat export.The raw Whatsapp chat export without the preprocessing is stored inside [raw_data](https://github.com/duyguakar/CS210_TermProject_AnalyzingMyGirlsGroupChat/blob/main/_chat.txt). While the main source of data used is the Whatsapp Group Chat export, it can be categorized in the following subtitles:

**Timestamps:** When each message was sent. Senders: Names or identifiers of the participants who sent messages. 

**Message Content:** Text, images, videos, and other media shared in the group. 

**System Messages:** Notifications about group creation, user addition, or changes (e.g., "User X created the group"). Media Indicators: Placeholder tags for attachments like photos, videos, stickers, or other media files, e.g– explain further in the future work part

Just like a typical Whatsapp group chat export the non-processed data contains metadata and message content. While the metadata contains the system messages and information such as group creation, and changes to the group names and descriptions, the message content includes the text messages as a whole. Particularly useful fields include the time stamp of the messages, the sender and the message body, emojis are included as a part of the message body.

# **Data Processing**

The data preprocessing is documented [here](https://github.com/duyguakar/CS210_TermProject_AnalyzingMyGirlsGroupChat/blob/main/preprocessedata.ipynb).

The [final preprocessed](https://github.com/duyguakar/CS210_TermProject_AnalyzingMyGirlsGroupChat/blob/main/final_chat_data.csv) data from the analysis of my girls' group chat includes several key elements that are cleaned, organized, and prepared for deeper insights. 

It consists of a structured dataset with message timestamps, sender names, and the content of messages, stripped of any unnecessary formatting or media links. Timestamps are converted into a consistent format to analyze activity patterns by hour, day, and week. The data also includes a breakdown of message lengths, the frequency of emojis, and word usage patterns to study conversational tone and engagement. I categorize messages into reply threads to identify how conversations flow and whether certain topics trigger prolonged discussions. 

Additionally, metadata like the total number of messages per sender, response times, and the overall volume of activity over time are included. This preprocessing ensures the data is ready for uncovering trends, group dynamics, and behavioral patterns. 

## **Data Visualizations and Analysis**

After my analysis, documented [here](https://github.com/duyguakar/CS210_TermProject_AnalyzingMyGirlsGroupChat/blob/main/Data_Analysis_and_Visualizations.ipynb), I uncovered some interesting insights about how we communicate. The results showed that the group is highly centralized, with a few members sending the majority of messages and acting as the core of the conversation. I noticed clear patterns in how active we are based on the time of day, with the most messages being sent in the evening, likely when we’re all winding down and catching up. I also found that certain topics triggered longer, more active discussions, while others were quickly acknowledged and moved on from. It was interesting to see how some members consistently initiated conversations, while others were more responsive. This analysis really gave me a deeper understanding of how we interact as a group and the dynamics of our chats—it’s not just random messages but a reflection of how close we are and how our daily routines influence when and how we talk.

## **Findings**

**Centrality Measures**
 The centrality analysis reveals the roles members play in the group dynamics. Metrics like in-degree, out-degree, and betweenness centrality highlight who is most active, influential, or critical in maintaining communication flow. For instance, out-degree centrality identifies members who initiate conversations, while in-degree centrality shows those who receive the most responses. Although some memebers such as Defne and Gülbin ve more active, in-degree values (number of incoming interactions) were consistent across all users, and no user has an unusually high or low in-degree compared to others.

**Monthly Activity Trends**
The line graph illustrates a declining trend in monthly activity. The highest activity occurs in October, with a consistent drop leading to December. This could indicate seasonal changes in communication patterns or shifting group dynamics over time.

**Top Words Used**
The frequency analysis of top words shows recurring themes and common conversational patterns. Words like "kanka," "abi," and "ya" dominate.

**Message Timing Patterns**
The heatmap demonstrates daily and hourly activity trends. Evening hours are the most active, especially on specific days like Thursday and Friday, suggesting these are prime times for group engagement.

**Response Time Distribution**
The scatter plots for response times show variability among members. Some members, such as Duru, tend to take longer to respond, while others are more prompt. This could reflect individual habits or levels of availability.

**Message Length Distribution**
The analysis of message lengths shows that most messages are concise, but some members occasionally send longer texts. This variability indicates differences in communication styles or the nature of shared content.

**Day vs. Night Activity**
The bar chart comparing day and night activity reveals that members are significantly more active at night. Defne, in particular, dominates nighttime messaging, reflecting her preference or availability during these hours.

**Outgoing-to-Incoming Ratios**
This analysis highlights how members balance sending and receiving messages. Some members, like I, Defne, and Gülbin are initiators with high outgoing-to-incoming ratios, while others are more responsive. 

Conclusions The analysis provides a detailed view of group communication dynamics. It uncovers trends in activity, individual behaviors, and overall group patterns, offering insights into how the group interacts and evolves over time. These findings could be useful for enhancing engagement or simply better understanding the group’s behavior.

## **Limitations**

One of the key limitations I faced during this analysis was maintaining privacy. To ensure anonymity, I had to modify the way I saved my friends' names on my phone, replacing them with pseudonyms or initials to prevent any sensitive information from being identifiable in the dataset. Still as I presnenetd my raw data, the group members names are visible althpugh with consent.

Additionally, analyzing personal conversations posed its own challenges,as I avoided drawing conclusions that might misrepresent the group's dynamics. While the analysis provided interesting insights, the personal nature of the data meant that certain nuances, such as sarcasm, and humor, which cannot be captured.

I also had to exclude media files, images, and voice notes due to their sensitive nature.

# **Future Work**

**Media Analysis**

I would like to expand this analysis to include media files, such as images, videos, and voice notes, as they are a significant part of how we communicate in the group. These media interactions often carry important context and emotions that are missed when focusing solely on text-based messages. To incorporate media files, I would need to find different methods, as privacy is an issue. For example, I could extract metadata like file type and timestamps without examining the actual content. 

I might also use sentiment analysis on captions or text embedded within images and videos to capture additional context.

**Emoji and Sticker Analysis**

Another area I would like to explore is integrating emoji analysis, as emojis are often used to enhance or change the tone of messages. By combining this with media analysis, I could create a more comprehensive picture of our communication style. Overall, expanding to include these aspects would make the analysis more insightful.
