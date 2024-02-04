# Number Thing
Your advertising campaign has a segment of users. Now a user request comes, how do you know if your campaign should be shown to this user or not? Moreover, you have thousands of campaigns.\
Number Thing is a novel system that allow you to register campaigns with segments of users, so you can quickly retrieve the list of campaigns associated with a user.\
In its core, Number Thing is a system that maps IDs to a list of numbers. It achieve low latency by leveraging the local file system of the worker instances and local caching to remove network calls in its read path. By doing so, it also reduce network congestion drastically, since writes are expected to be much more infrequent compared to reads.
