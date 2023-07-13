# SR-Speech-Recognizition-DataPipeline.github.io
This document focuses on the development of the data pipeline, specifically designed for the recognition and analysis of child speech patterns and disorders. 
Introduction: This document focuses on the development of the Ennis data pipeline, specifically designed for the recognition and analysis of child speech patterns and disorders. The primary goal of this pipeline is to enable efficient processing and evaluation of child speech data, ultimately aiding in the identification and diagnosis of speech-related conditions. The pipeline will be built using various Application Programming Interfaces (APIs) to facilitate seamless integration and analysis of the collected speech data.

Purpose and Objectives: The Ennis data pipeline serves as a comprehensive solution for recognizing child speech patterns and analyzing speech disorders. Its primary purpose is to streamline the processing and analysis of child speech data, enabling efficient identification and diagnosis of speech-related conditions. The pipeline consists of several components, each contributing to a specific aspect of the overall analysis process.

1.	Child speech Transcription Pipeline:
•	This component focuses on transcribing the recorded child speech data into text format.
•	It leverages advanced speech-to-text algorithms and techniques to accurately convert speech into written form.
•	The transcription output serves as the foundation for subsequent analysis and processing stages.
2.	Story Segment Calculator:
•	This component aims to identify and segment individual stories or speech samples within the transcribed data.
•	It employs algorithms to detect story boundaries, allowing for better organization and management of speech data.
3.	Story Calculator:
•	The story calculator component focuses on extracting key metrics and features from individual speech samples or stories.
•	It analyzes the linguistic characteristics, fluency, and structure of each story, providing valuable insights for further analysis.
4.	Story Metric Calculator:
•	This component calculates specific metrics related to speech quality, intelligibility, and linguistic complexity withing each story segment.
•	It helps quantify and assess various aspects of child speech, aiding in the identification of potential speech disorders.

5.	Language Speech Analysis Pipeline:
•	The language speech analysis pipeline combines the output from the previous components to perform a comprehensive analysis of child speech.
•	It applies advanced natural language processing (NLP) and machine learning techniques to extract meaningful insights and patterns from the transcribed speech data.
6.	MLCU (Mean Length of Child Utterance) and PGU (Proportion of Grammatical Utterances):
•	These components focus on calculating key metrics related to language development and grammatical proficiency in child speech.
•	MLCU quantifies the average length of child utterances, while PGU measures the proportion of grammatically correct utterances.
7.	Enni-Based Screener:
•	This component utilizes the output from the previous stages to implemt an Ennis-based screening algorithm.
•	It applies predefines criteria and thresholds to identify potential speech disorders or areas of concern in the child speech data.
Depending on the availability of annotations from the transcription stage, the downstream components of the Ennis data pipeline can be dynamically adjusted or modified. This flexibility ensures that the pipeline’s analysis processes align with the availability of annotated data, allowing for adaptability and scalability.


Preparing JSONS:

1.	Within this JSON, the variable “audio_file” represents the uploaded .wav audio file of a child. The “duration” indicates the total time length of the audio, while the “sample rate” specifies the rate at which the audio is sampled. The audio data is sourced from the Childes Talk Bank, specifically from the Ennis repository.  If there are multiple speakers in the audio, the “selected_speaker_name” field is used to specify the desired speaker, focusing solely on the child’s speech. The “child_id” corresponds to the unique identifier of the child, and the “stories” field represents the number of stories narrated by the child in the audio.
 

2.	Language Speech Analysis JSON contains information about an audio file and its associated child speech data. The audio file is name “audio.wav” and has a duration of 180.5 seconds. It has a sample rate and a channel. The “selected_speaker_name” field indicates that the speech from the child should be considered for analysis. The child is identifies by the “Child_id” with the value 1234. The “transcription” field is currently empty and can be used to store the transcription of the child’d speech if available. This JSON includes an array of “stories” narrated by the child. Each story has its own set of attributes “story_id” represents the unique identifier for each story, “start+time” and “end_time” indicate the timestamps of when each story was recorded, “story” contains the actual text of the story narrated by the child, “word_counts” denotes the number of words in the story,”pgu” stands for the proportion of grammatical utterances, which represents the ratio of grammatically correct utterances in the story.Independent_clauses and dependent clauses indicates the number of independent,dependent cluases in the story, Mean length of Child Utterance, which represents the average length of the child’s utterances in the story.


 

3.	Story segment calculator, the variable “audio_file” represents the uploaded .wav audio file of a child. The “duration” indicates the total time length of the audio, while the “sample rate” specifies the rate at which the audio is sampled. Sg1,sg2 …. Are the segments of sentences for each story in the audio.If there are multiple speakers in the audio, the “selected_speaker_name” field is used to specify the desired speaker, focusing solely on the child’s speech. The “child_id” corresponds to the unique identifier of the child, and the “stories” field represents the number of stories narrated by the child in the audio.
 


4.	Story selector, the variable “audio_file” represents the uploaded .wav audio file of a child. The “duration” indicates the total time length of the audio, while the “sample rate” specifies the rate at which the audio is sampled. Sg1,sg2 …. Are the segments of sentences for each story in the audio. Intially “story_selected” is assigned to NULL, it is to select a particular story of the child.If there are multiple speakers in the audio, the “selected_speaker_name” field is used to specify the desired speaker, focusing solely on the child’s speech. The “child_id” corresponds to the unique identifier of the child, and the “stories” field represents the number of stories narrated by the child in the audio.


 

5.	Story Metric, the variable “audio_file” represents the uploaded .wav audio file of a child. The “duration” indicates the total time length of the audio, while the “sample rate” specifies the rate at which the audio is sampled. Sg1,sg2 …. Are the segments of sentences for each story in the audio. Intially “story_selected” is assigned to NULL, it is to select a particular story of the child.If there are multiple speakers in the audio, the “selected_speaker_name” field is used to specify the desired speaker, focusing solely on the child’s speech. The “child_id” corresponds to the unique identifier of the child, and the “stories” field represents the number of stories narrated by the child in the audio.





