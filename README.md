# ITIS-6177-Final-Project

Microsoft Azure Text to Speech API Documentation

##Text to Speech Requirements:

This is built by using Microsoft Azure Text to Speech API. For this initially we have to create an account in the Azure portal.
https://azure.microsoft.com/en-us/products/cognitive-services/text-to-speech/

##Setup:

Creating the speech resource in the azure microsoft account for getting the subscription key and endpoint.

Installation the code through git clone link 

cd ITIS---6177-Final-Project

Create .env file in this directory and include the following data:

API_AUTH_URL = https://eastus.api.cognitive.microsoft.com/sts/v1.0/issuetoken
API_URL = https://eastus.tts.speech.microsoft.com/cognitiveservices/v1
API_KEY = <your-api-key>
SERVICE_NAME_NEURAL = (en-US, JessaNeural)
VOICE_URL = https://eastus.tts.speech.microsoft.com/congnitiveservices/voices/list
VOICE_HOST = eastus.tts.speech.microsoft.com


###Installation dependencies:

npm install - nodejs package manager.
node app.js - JavaScript run engine.

###Applications:
Node js for running the js program.
Terminal for running the code.
Postman for testing purposes.

###Testing process:
We can test this the postman workspace api by giving this link: http://167.71.14.20:4004/

The main two endpoints for this API are: 
   /voices
   /create



###GET Method:  This is the link used for getting the list of voices to be viewed. 
 
http://167.71.14.20:4004/voices

<img width="696" alt="Screen Shot 2022-12-08 at 5 55 32 PM" src="https://user-images.githubusercontent.com/30731706/206827790-bd073fc8-d458-430a-8fe8-a97e4792fd39.png">


###POST Method: This is the link used for posting our request to convert text to speech in json format in Postman application. 

http://167.71.14.20:4004/create

POST > Body > raw > JSON

{
   “TEXT”: “Enter the text which you want to convert to speech? ”
}

<img width="696" alt="Screen Shot 2022-12-08 at 6 00 58 PM" src="https://user-images.githubusercontent.com/30731706/206827879-fe6d49a0-9e59-4b04-b486-296995f8a064.png">


Here Default given voices in app.js, 

Below I am attaching the video of this working model Text to Speech.
 


https://user-images.githubusercontent.com/30731706/206827857-2ebee395-f59e-4936-9deb-4e86c7c1d5be.mov



###PITCH:
In addition to this, there are a few features like Pitch to the voice. Where it takes the pitch value and converts it into accordingly.

 POST > Body > raw > JSON

{
   “TEXT”: “Enter the text which you want to convert to speech? ”,
   “PITCH”: 1
}

<img width="1022" alt="Screen Shot 2022-12-09 at 11 20 20 AM" src="https://user-images.githubusercontent.com/30731706/206827901-6fd9d845-d0cd-4a0e-b182-1324de0ace6c.png">


###SPEEKING_SPEED:
In addition to this, there are a few features like SPEEKING_SPEED to the voice. Where it takes the speaking speed value and converts the voice speed according to the given value.

 POST > Body > raw > JSON

{
   “TEXT”: “Enter the text which you want to convert to speech? ”,
   “PITCH”: 1,
   “SPEEKING_SPEED”: 1
}

<img width="1022" alt="Screen Shot 2022-12-09 at 11 18 49 AM" src="https://user-images.githubusercontent.com/30731706/206827910-cc8e6566-1eba-42c1-a494-c75dbd18b7fe.png">


###5.Swagger:

Follow the below link to access swagger application:

http://167.71.14.20:4080/docs/




###Response:
 
Code Description
200  Successful
400  Bad data
500  Internal Server Error


##References:
  

https://azure.microsoft.com/en-us/products/cognitive-services/text-to-speech/    

https://learn.microsoft.com/en-us/azure/cognitive-services/speech-service/index-text-to-speech

https://learn.microsoft.com/en-us/azure/cognitive-services/speech-service/get-started-text-to-speech

    
