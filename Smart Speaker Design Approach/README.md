## Smart Speaker

![Smart Speaker](https://assets.pandaily.com/uploads/2019/08/amazon-and-google-home-smart-speaker.jpg)

Popular smart speakers: -
1. Alexa
2. Siri
3. Google Home etc.

The basic approach almost each smart speaker folows can be divided into 4 major categories: -

__:ear: Trigger/ Wakeword Detection:__ The moment one says, "Alexa" or "Hey, Siri", the smart speaker device starts to respond. So here "Alexa" or "Hey, Siri" is a trigger/wakeword. As soon as the devide hear this word, it'll respond.
The technical design would be to train a ML classification model on several sounds, all saying "Alexa".
- __Input:__ Sound clip with "Alexa" as the wakeword.
- __Output:__ ML model outputs 1 if the sound clip is "Alexa" and otherwise 0.

__Tech stack:__ TinyML wakeword detection

__:speaking_head: Speech Recognition:__ After the wake word detection, whatever follows is the command that Alexa has to execute. Eg., Alexa, Tell a joke.
So, basically "Tell a joke" should be extracted from the sentence. The ML model should be able to recognize each and every word in the sentence.
- __Input:__ Full instruction sentence with wakeword
- __Output:__ ML model outputs all the words after the wakeword

__:bulb: Intent Recognition:__ After the speech recognition, basic intents like "joke", "whether", "time", "units conversion", "simple question" are targets of ML model. And the input is the sentences where telling a joke/asking weather/simple question/unit conversion is the intent.
Say for example for "joke" intent, sentences could be "tell a joke", "a joke please", "could u tell a joke", "tell something funny" etc. The intent recognition should be robust enough to recognise the intent and output the target intent.
- __Input:__ The output of Speech recognition goes into intent recognition
- __Output:__ ML model outputs the intent of the instruction.

__:man_technologist: Specialized Program to Execute Command:__ After the intent of the user is recognised, write a software program to execute the command, like telling the time, joke or executing the instruction based on the intent.
- __Action:__ Execute the specialised program for the instruction.

______________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________







