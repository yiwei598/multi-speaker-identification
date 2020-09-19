# multi-speaker-identification
Understanding of essence area:
The signal processing includes two major methods: digital signal processing and analog signal processing. The main different between these two methods is digital signal processing using A/D converter to transfer analog signal to digital signal. Then the microprocessor analyses it and output the different type of result signal based on the request of project, however, the analog signal processing directly analyses analog signal.
Digital signal processing has more advantage rather than analog signal processing. So most of applications use digital signal processing to analyses signal. There are three main subfields. First one is audio signal processing, the second one is digital image processing and third one is speech processing. 
In this specific multi-speaker identification project, we will do further research about the speech processing. 
Understanding of use cases and application of multi-speaker identification:
1.	use case: 
As a phone user, I want to use multi-speaker identification to identify who are talking to my Siri when someone is talking around me at the same time.
As a meeting organizer, I want to use multi-speaker identification to identify who is talking right now
As a student study online, I want to use multi-speaker identification to figure out who said which sentence in the recording lecture.
As a film producer, I want to use multi-speaker identification to cut out the actor’s voice from filming site.
2.	Application:
Siri voice control 
Zoom recording meeting
video captioning

Review of different approaches:
For the Siri, what we need to do is speaker recognition. There are basically two kinds of recognition. One is text-dependent and the other one is text-independent method. The former requires the speaker to provide utterances of key words or sentences, the same text being used for both training and recognition, whereas the latter do not rely on a specific text being spoken. For activating the Siri, we could use basic text-dependent method, it is easier to set up and convenient for system to match up. However both two methods have big disadvantage, which is not applicable for recording the other speaker and only used to identify one speaker.

For the zoom recording meeting, we need to use speaker diarization. There are five basic subsystems: 
•	Speech Detection: Extract speech part in one audio recording using a Voice Activity Detector (VAD) module.
•	Speech Segmentation: Extract out small segments of your audio call in a continuous manner.
•	Embedding Extraction: This system creates a neural-network based embedding of your speech segments extracted in the previous step. An embedding is a vector representation of data which could be used by the deep learning framework.
•	Clustering: Cluster embeddings we created above and the system will training itself by using supervised learning method in order to identify which embeddings are belong to same speaker and assigned the label of that speaker as well.
•	Transcription: Segment out the audio into clips belonging to each speaker, and pass it to a Speech-to-Text model (or ASR) which produces the transcript of the speech segment.
The advantage of these method is obvious: it can identify multi-speaker at the same time and no need to collect voice sample in advance of the conversation because the embedding extraction step collect samples for analyzing at the same time, however the disadvantage comparing to system which collect voice sample in advance is less accuracy and more difficulty to do real-time job.

