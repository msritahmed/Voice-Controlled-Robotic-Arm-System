# Voice-Controlled-Robotic-Arm-System Project
In our project, the voice-controlled robotic arm is designed to assist the medical sector by aiding doctors during operations through efficient object picking and placement.

Train
Connect your Voice Recognition V3 Module with Arduino, By Default:
connection

Download VoiceRecognitionV3 library.(download zip file or use git clone https://github.com/elechouse/VoiceRecognitionV3.git command)

When use zip format file, extract VoiceRecognitionV3.zip to Arduino Sketch\libraries folder, or if you use git clone command copy VoiceRecognitionV3 to Arduino Sketch\libraries .

Open vr_sample_train(File -> Examples -> VoiceRecognitionV3 -> vr_sample_train)

Choose right Arduino board(Tool -> Board, UNO recommended), Choose right serial port.

Click Upload button, wait until Arduino is uploaded.

Open Serial Monitor. Set baud rate 115200, set send with Newline or Both NL & CR.
![image](https://github.com/user-attachments/assets/ee580a56-0d82-4544-9423-216115937853)


Send command settings(case insensitive) to check Voice Recognition Module settings. Input settings, and hit Enter to send

![image](https://github.com/user-attachments/assets/f0ca0622-1900-4395-a8bb-e5bd24decb2a)

![image](https://github.com/user-attachments/assets/4195d1f2-ddd3-43c9-8513-b6d084f9d8cd)

Train Voice Recognition Module. Send sigtrain 0 On command to train record 0 with signature "On". When Serial Monitor prints "Speak now", you need speak your voice(can be any word, meaningful word recommended, may be 'On' here), and when Serial Monitor prints "Speak again", you need repeat your voice again. If these two voice are matched, Serial Monitor prints "Success", and "record 0" is trained, or if are not matched, repeat speaking until success.
When training, the two led on the Voice Recognition Module can benefit your training process. After send train command, the SYS_LED is blinking which remind you to be ready, then speak your voice as soon as the STATUS_LED lights on, the record finishes once when the STATUS_LED lights off. Then the SYS_LED is blinking again, these status repeated, when the training is successful, SYS_LED and STATUS_LED blink together, if training is failed SYS_LED and STATUS_LED blink together quickly.


![image](https://github.com/user-attachments/assets/b910da00-f383-4076-b7f8-b1cd519a8e23)

Train another record. Send sigtrain 1 Off command to train record 1 with signature "Off". Choose your favorite words to train (it can be any word, meaningful word recommended, may be 'Off' here).


![image](https://github.com/user-attachments/assets/c97f5e92-115b-4f39-92dd-a11220c6f4dd)















