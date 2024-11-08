# Microsoft-Learn-Location-Mention-Recognition-Challenge
Can you identify locations in a tweet?

## BACKGROUND
At disaster onset, microblogging posts with critical information such as medical assistance, food or shelter needs, reports of trapped people, and severely damaged infrastructure, are not useful for response authorities if they are not geotagged. While microblogging posts with exact GPS coordinates are usually scarce, often they contain toponyms (i.e. place/area/street names), which can be helpful for authorities to estimate the location. However, due to the high volume of microblogging posts, manual extraction of location cues cannot scale. An automated process is required for the recognition and geolocation of toponyms in microblogging posts.

Therefore, the objective of this challenge is to encourage the development of systems for Location Mention Recognition (LMR) from microblogging posts during emergencies. These automatic systems are anticipated to support the relief activities that are executed by the response authorities during disasters.

We use X (Twitter formerly) posts as our data source for microblogging posts.

## MORE INFORMATION
The LMR system is one component of a Location Mention Prediction (LMP) system that serves as a part of a larger ecosystem of disaster response as depicted in the following Figure:

![image](https://github.com/user-attachments/assets/bd6cf77a-1889-4eec-a452-1a8633fa5de5)

![image](https://github.com/user-attachments/assets/3a06bc78-0de0-4ab2-8282-99e8f6a3bea7)


The LMP systems consist of two main components i.e., LMR and LMD. The Location Mention Recognition (LMR) component is responsible for extracting toponyms, i.e., place or location names from microblogging posts and assigning location types (e.g., country, state, county, city) to them. Whereas, the Location Mention Disambiguation (LMD) component resolves the extracted location mentions to geographical areas using a geo-positioning database (i.e., gazetteer). In this particular challenge, we only focus on the Location Mention Recognition task.

The LMR task has aims at detecting location mentions and their spans regardless of their location types. Given a microblogging post, the task is to recognize all location mentions. For example, in the following microblogging post, “Paris” is the only location mentioned. Microblogging post: “Paris flooding shuts down train lines.”

The figure below illustrates further the LMR task.

![image](https://github.com/user-attachments/assets/f76989e1-fb7f-470a-bb58-f162865597c0)


The location mentions (LMs) are defined as specific geo-point (e.g., school), geo-lines (e.g., street), or geo-areas (e.g., city). Addresses (e.g., Rue de Rivoli, Paris, France) and location expressions (e.g., 10km away from Paris) are not location mentions.

The LMR system has to detect the address component as separate LMs with a space between LMs:

Rue de Rivoli Paris France

## EVALUATION
The evaluation metric for this challenge is Word Error Rate Metric.

You can read more about WER in this medium article. Here are some libraries to start off with.

For every row in the dataset, submission files should contain 2 columns: ID and Locations.

If there are more than one location in a text, separate them with a space and keep them in order.

## RESULTS 
##### https://zindi.africa/competitions/microsoft-learn-location-mention-recognition-challenge/leaderboard
* PUBLIC LB: 0.142822049
* PRIVATE LB: 0.1504467
