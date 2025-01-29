# Running-on-Android

Here is a short guide to run deepseek r1 model on android. The model used is the DeepSeek-R1-Distill-Qwen-1.5B.
<img src="img (2).jpg" alt="chat" width="500"/>

**1. Install some apps**

- install termux from [f-droid](https://f-droid.org/en/packages/com.termux/) or [playstore](https://play.google.com/store/apps/details?id=com.termux&hl=en).
- install [ollama app](https://github.com/JHubi1/ollama-app/releases)

**2. Termux setup**

    # open and update
    apt update
    
    #Install some packages
    pkg install golang cmake clang gzip git
    
**3. Installing Ollama**

    #clonning repo
    https://github.com/ollama/ollama.git
    cd ollama
    
    #go generate and build
    go generate ./...
    go build .
    
    #handling the permission issue
    chmod -R 700 ~/go & rm -r ~/go  

    #copy binary to termux path
    cp ollama/ollama /data/data/com.termux/files/usr/bin/

**4. Running the deepseek-r1 model**

    ollama run deepseek-r1:1.5b //download the model
    
**5. Open the ollama app and add the model**

if theres and error just try it again few more times.

<img src="img (1).jpg" alt="appsetting" width="500"/>
<img src="img (3).jpg" alt="model" width="500"/>
