# COVID-19 Vaccination Slot Booking Script

### Important: 
- This is a proof of concept project. I do NOT endorse or condone, in any shape or form, automating any monitoring/booking tasks. **Use at your own risk.**
- This CANNOT book slots automatically. It doesn't skip any of the steps that a normal user would have to take on the official portal. You will still have to enter the OTP and Captcha.
- Do NOT use unless all the beneficiaries selected are supposed to get the same vaccine and dose. 
- There is no option to register new mobile or add beneficiaries. This can be used only after beneficiary has been added through the official app/site.
- API Details (read the first paragraph at least): https://apisetu.gov.in/public/marketplace/api/cowin/cowin-public-v2
- And finally, I know code quality isn't great. Suggestions are welcome.


### Usage:

EXE file that was being built via ```pyinstaller``` on GitHub Actions does not work anymore but the **Python 3.7** code still does. If you don't already have Python and do not know how to set it up, instructions are at the bottom. It's not complicated at all and takes literally 5 minutes. Please do that and come back here.

Download this code as zip, and extract it to some folder like ```C:\temp\covid-vaccine-booking```. Going by this structure, the py files should be in ```C:\temp\covid-vaccine-booking\src```. 

Open command prompt and run ```cd C:\temp\covid-vaccine-booking```

Install all the dependencies with the below. This is a one-time activity (for anyone not familiar with Python)
```
pip install -r requirements.txt
```

If you're on Linux or MacOS, install the SoX ([Sound eXchange](http://sox.sourceforge.net/ "Sound eXchange")) before running the Python script. To install, run:

Ubuntu:
```
sudo apt install sox
```
MacOS:
```
brew install sox
```

Finally, run the script file as shown below:
```
python src\covid-vaccine-slot-booking.py
```

If you already have a bearer token, you can also use:
```
python src\covid-vaccine-slot-booking.py --token=YOUR-TOKEN-HERE
```

### Python 3.7.3 Installation in Windows
- Check if Python is already installed by opening command prompt and running ```python --version```.
- If the above command returns ```Python <some-version-number>``` you're probably good - provided version number is above 3.6
- If Python's not installed, command would say something like: ```'python' is not recognized as an internal or external command, operable program or batch file.```
- If so, download the installer from: https://www.python.org/ftp/python/3.7.3/python-3.7.3-amd64.exe
- Run that. In the first screen of installer, there will be an option at the bottom to "Add Python 3.7 to Path". Make sure to select it.
- Open command prompt and run ```python --version```. If everything went well it should say ```Python 3.7.3```
- You're all set! 

