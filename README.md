# adobeConnectDownloader

a way to download your class recorded meeting that set up in adobe connect platform

# installation

Requirements:

* python 3

Just windows Users Go to https://www.python.org/downloads/ 

and below python library should be install by : sudo pip3 install PYTHONLIBRARY

* requests

Install requirements with pip install -r requirements.txt


and below requirement should be install by (for linux): sudo apt install PACKAGENAME 

* ffmpeg

Installing ffmpeg:
Compilation instruction: https://trac.ffmpeg.org/wiki/CompilationGuide

before any this the 0.01 version and just work fine under below conditions :

  for classes that:
  
    1- the Host(Professor) share their own screen not slides
    
    2- no passwords set for the class
    
# How to run 

clone the prject and in project directory run below command :

```python
python3 adobeConnectDownloader.py --url='LINK_TO_SESSION' --dirName='COURSE_NAME' --fileName='SESSION'
```

for example :

```python
python3 adobeConnectDownloader.py --url='http://*/p5u78g9re5i' --dirName='math' --fileName='session7'
```

the final video is SESSION.avi(session7.avi) and you can detele other files in the folder .

# advance 

1.this code merge all chat voice of Participants to file and this process could take times if you dont want this voices just use --options='noVoiceChat' and the end of the command. so the whole command is :

```python
python3 adobeConnectDownloader.py --url='http://*/p5u78g9re5i' --dirName='math' --fileName='session7' --options='noChatVoice'
```

the video output is session70.avi

2.if you are sure that zip file downloaded by code is not currepted and you dont want to downlaod it again use --fileExist at the end of command like :

```python
python3 adobeConnectDownloader.py --url='http://*/p5u78g9re5i' --dirName='math' --fileName='session7' --options='noChatVoice' --fileExist
```

# TODOS

- [ ] Deleting out file in each step in "adding all chat voice to .avi file"

- [ ] use below idea to merge all voice in one go(https://stackoverflow.com/questions/48169031/how-to-add-audio-to-existing-video-using-ffmpeg-at-specific-time)

- [ ] normilizing the output volume(https://superuser.com/questions/323119/how-can-i-normalize-audio-using-ffmpeg)

# contribute :heart:

help to imporve this code and also report any issue that you face with .

email : mohamad.shadfar54@gmail.com

have fun .
