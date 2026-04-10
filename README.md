# Repository for final project
Final Project

https://github.com/cristoverordonez1-creator/oaqjp-final-project-emb-ai.git

2a_emotion_detection

def emotion_detector(text_to_analyse): 
    
    url = 'https://sn-watson-emotion.labs.skills.network/v1/watson.runtime.nlp.v1/NlpService/EmotionPredict'
    
    myobj = { "raw_document": { "text": text_to_analyse } }
    
    header = {"grpc-metadata-mm-model-id": "emotion_aggregated-workflow_lang_en_stock"}
    
    response = requests.post(url, json=myobj, headers=header)


2b_application_creation

theia@theiadocker-cristoverord:/home/project/final_project$ python3.11

Python 3.11.14 (main, Oct 10 2025, 08:54:03) [GCC 11.4.0] on linux

Type "help", "copyright", "credits" or "license" for more information.

>>> import requests
>>> url = 'https://sn-watson-emotion.labs.skills.network/v1/watson.runtime.nlp.v1/NlpService/EmotionPredict'
>>> header = {"grpc-metadata-mm-model-id": "emotion_aggregated-workflow_lang_en_stock"}
>>> myobj = { "raw_document": { "text": "I love this new technology." } } 
>>> response = requests.post(url, json=myobj, headers=header)
>>> print(response.status_code)
200
>>> 
