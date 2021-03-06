## CREMA-D (Crowd-sourced Emotional Mutimodal Actors Dataset)

#### Access

If you access the GitHub repository, please fill out [this form](https://docs.google.com/forms/d/e/1FAIpQLSdvOR994_Hsx7OkBU3oCzluXcmxw2P1nr-zBxcPgVBNLdD9Eg/viewform?usp=sf_link). That way we can keep a record of the community of CREMA-D users.

#### Storage requirements

Note: This repository uses Git Large File Storage, [git-lfs](https://git-lfs.github.com). You will need to install it on top of your git installation in order to get the video and audio files.  If you just download the zip file (~24MB zipped, ~163MB unzipped) then all of the video and audio files will just be links to the git-lfs file. For more information [go here](https://git-lfs.github.com). 

- **zip download:** Downloading the repository as a zip will get you all of the R scripts and csv files as well as stubs for all of the audio and video files. The zipped size is ~24MB, and the unzipped size is ~163MB.
- **git clone:** ~7.55GB is required to clone the whole repository. In addition to the R scripts and csv files, there is audio and video from 7442 recordings as flash video, mp3, and wav files as described below.

#### This Directory holds files used in the paper: 

[Cao H, Cooper DG, Keutmann MK, Gur RC, Nenkova A, Verma R. CREMA-D: Crowd-sourced Emotional Multimodal Actors Dataset. IEEE transactions on affective computing. 2014;5(4):377-390. doi:10.1109/TAFFC.2014.2336244.](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC4313618/)

#### The collection of the videos is described in this paper:

[Keutmann, M. K., Moore, S. L., Savitt, A., & Gur, R. C. (2015). Generating an item pool for translational social cognition research: methodology and initial validation. Behavior research methods, 47(1), 228-234.](https://www.ncbi.nlm.nih.gov/pubmed/24719265)

#### License:
This Crowd-sourced Emotional Mutimodal Actors Dataset (CREMA-D) is made available under the Open Database License: http://opendatacommons.org/licenses/odbl/1.0/. Any rights in individual contents of the database are licensed under the Database Contents License: http://opendatacommons.org/licenses/dbcl/1.0/



#### Description

##### Text Data Files:

1. SentenceFilenames.csv - list of movie files used in study
2. finishedEmoResponses.csv - the first emotional response with timing.
3. finishedResponses.csv - the final emotional Responses with emotion levels with repeated and practice responses removed, used to tabulate the votes
4. finisedResponsesWithRepeatWithPractice.csv - the final emotional responses with emotion levels with repeated and practice responses in tact. Used to observe repeated responses and practice responses.
5. processedResults/tabulatedVotes.csv - the tabulated votes for each movie file.

##### R Scripts

1. processFinishedResponses.R - converts the finisedResponses.csv the tabulated
2. readTabulatedVotes.R - reads processedResults/tabulatedVotes.csv


  
##### Finished Responses Columns <br>(finishedResponses.csv and<br> finishedResponsesWithRepeatWithPractice.csv)
- "localid" - a participant identifier
- "pos" - the original log file order for the participant
- "ans" - the emotion character with level separated by an underscore
- "ttr" - the response time in milliseconds
- "queryType" - a numeric value specifying the type of stimulus: 1. - voice only, 2. face only, 3. audio-visual
- "numTries" - number of extra emotion clicks. 
- "clipNum" - the file order of the clip from SentenceFilenames.csv
- "questNum" - the order of questions for the query type
- "subType" - the type of response in the logs, all values are 4 for the final emotion response
- "clipName" - the name of the video file
- "sessionNums" - the distinct number for the session
- "respEmo" - the emotion response
- "respLevel" - the emotion level response
- "dispEmo" - the displayed emotion
- "dispVal" - the displayed value
- "dispLevel" - a numeric representation of the displayed value, 20 for low, 50 for med, 80 for hi.

##### Finished EmoResponses Columns <br> (finishedEmoResponses.csv)

- "localid" - a participant identifier
- "sessionNums" - the distinct number for the session
-  "queryType" - a numeric value specifying the type of stimulus: 1. - voice only, 2. face only, 3. audio-visual
-  "questNum" - the order of questions for the query type
-  "pos" - the original log file order for the participant
-  "ttr" - the response time in milliseconds
-  "numTries" - number of extra emotion clicks. 
-  "clipNum" - the file order of the clip from SentenceFilenames.csv
-  "clipName" - the name of the video file

##### Summary Table Columns <br> processedResults/summaryTable.csv
- "fileName" - name of the movie file rated           
- "VoiceVote" - the emotion (or emotions separated by a colon) with the majority vote for Voice ratings. (A, D, F, H, N, or S)      
- "VoiceLevel" - the numeric rating (or ratings separated by a colon) corresponding to the emotion(s) listed in "VoiceVote"       
- "FaceVote" - the emotion (or emotions separated by a colon) with the majority vote for Face ratings. (A, D, F, H, N, or S)      
- "FaceLevel" - the numeric rating (or ratings separated by a colon) corresponding to the emotion(s) listed in "FaceVote"       
- "MultiModalVote" - the emotion (or emotions separated by a colon) with the majority vote for MultiModal ratings. (A, D, F, H, N, or S)      
- "MultiModalLevel" - the numeric rating (or ratings separated by a colon) corresponding to the emotion(s) listed in "MultiModalVote"       



##### Tabulated Votes Columns <br> processedResults/tabulatedVotes.csv

- "A" - count of Anger Responses
- "D" - count of Disgust Responses
- "F" - count of Fear Responses
- "H" - count of Happy Responses
- "N" - count of Neutral Responses
- "S" - count of Sad Responses
- "fileName" - name of the movie file rated           
- "numResponses" - total number of responses
- "agreement" - proportion of agreement
- "emoVote" - the majority vote agreement
-  "meanEmoResp" - the mean of all emotion levels
-  "meanAngerResp" - the mean of the anger levels
-  "meanDisgustResp" - the mean of the disgust levels
-  "meanFearResp" - the mean of the fear levels     
-  "meanHappyResp" - the mean of the happy levels
-  "meanNeutralResp" - the mean of the neutral levels
-  "meanSadResp" - the mean of the sad levels
-  "medianEmoResp" - the median of all emotion levels
-  "meanEmoRespNorm" - the normalized mean of all emotion levels
- "meanAngerRespNorm" - the normalized mean of anger emotion levels
-  "meanDisgustRespNorm" - the normalized mean of disgust emotion levels
-  "meanFearRespNorm" - the normalized mean of fear emotion levels
-  "meanHappyRespNorm" - the normalized mean of happy emotion levels
-  "meanNeutralRespNorm" - the normalized mean of neutral emotion levels
-  "meanSadRespNorm" - the normalized mean of sad emotion levels
-  "medianEmoRespNorm"  - the normalized median of all emotion levels

##### Video Files
Flash Video Files used for presentation to the Raters are stored in the VideoFlash directory.

##### Audio Files

MP3 Audio files used for presentation to the Raters are stored in the AudioMP3 directory.


##### Processed Audio


WAV Audio files converted from the original video into a format appropriate for computational audio processing are stored in the AudioWAV directory.



##### Funding Sources
All data collection and method development was supported by the following funding sources:
- NIH R01 MH073174 (Computational quantification of emotion in faces and voice for neuropsychiatry) from National Institute of Mental Health (NIMH)
- NIH R34 MH105248 (Developing CBT-informed social enactment training curricula for CHR youths) from NIMH
- NIH R01 MH107235 (Multimodal brain maturation indices modulating psychopathology and neurocognition) from NIMH
