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
![image](https://github.com/sumanaradham3/SR-Speech-Recognizition-DataPipeline.github.io/assets/113401577/9c94a1df-eff9-4bac-b8f7-c1bc6ae0bbdb)

