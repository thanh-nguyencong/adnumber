# AdNumber
Your advertising campaign has a segment of users. Now a user request comes, how do you know if your campaign should be shown to this user or not? Moreover, you have thousands of campaigns.\
AdNumber is a novel system that allow you to register campaigns with segments of users, so you can quickly retrieve the list of campaigns associated with a user.\
It achieve low latency by leveraging the local file system of the CampaignProvider instances and local caching to remove network calls in its read path. By doing so, it also reduce network congestion drastically, since writes are expected to be much more infrequent compared to reads.\
The system comprises of a group of CampaignProviders that answer queries for campaigns given a user number. Segment Manager which provides the segments for CampaignProvider, and a group of CampaignProvider
