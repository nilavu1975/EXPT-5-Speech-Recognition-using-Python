# EXPT-5-Speech-Recognition-using-Python

# AIM: 

# To perform and verify speech recognition using SCILAB.

# APPARATUS REQUIRED: 
PC installed with SCILAB. 

# PROGRAM: 
```
!pip install SpeechRecognition pydub
import speech_recognition as sr
from pydub import AudioSegment
from pydub.silence import split_on_silence

# Path to your audio file
audio_file_path = '/content/sakthi.wav' # Change this to your file name and format
r = sr.Recognizer()

# Load the audio file
with sr.AudioFile(audio_file_path) as source:
    print("Reading audio file...")
    audio = r.record(source) # read the entire audio file

    print("Attempting to recognize speech...")
    try:
        text = r.recognize_google(audio)
        print("Recognized Text:")
        print(text)
    except sr.UnknownValueError:
        print("Google Speech Recognition could not understand audio")
    except sr.RequestError as e:
        print(f"Could not request results from Google Speech Recognition service; {e}")
```

# OUTPUT: 
<img width="847" height="526" alt="Screenshot 2026-09-03 100620" src="https://github.com/user-attachments/assets/a4af4e27-5fc4-4444-957f-b43a94f204a0" />



# RESULT: 
Thus the speech recognition using SCILAB was performed and verified.
