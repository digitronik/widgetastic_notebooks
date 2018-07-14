# Setup Environment

## Create the project directory
```
mkdir widgetastic
cd widgetastic
```

## Pull tutorials from the [tutorial Github repo(https://github.com/digitronik/tutorial_widgetastic)
```
git clone https://github.com/digitronik/tutorial_widgetastic.git
```

## Create Python Virtual Environment:
- If you don't have `virtualenv`. Install virtualenv.
```
python -m pip install --user virtualenv
```
- Create virtual environment
```
python -m virtualenv env
```
- Activate Virtual Environment
```
source env/bin/activate
```
- Deactivate Virtual Environment
```
deactivate
```

## Install dependacies
1. [Widgetastic Core](https://github.com/RedHatQE/widgetastic.core)
	It includes widgetastic `main classes` and some basic `widgets`
2. [Widgetastic Patternfly](https://github.com/RedHatQE/widgetastic.patternfly)
	It includes `patternfly` and `bootstrap` widgets
3. [Selenium](https://github.com/SeleniumHQ/selenium/)
	For selenium `webdriver` to interact with Web-UI.
4. [Ipython](https://ipython.org/)
	A powerful `python` interactive shell to access things

```
cd tutorial_widgetastic
pip install -r requirements.txt
```

## Test  Your Environment

### Open Ipython shell
In your user `shell` just type
```
ipython
```

### Import `selenium` `webdriver`
Import `webdriver` from `selenium` in `ipython`. Assign a browser as `Firefox`. It should open `Firefox` browser and `get` command of `selenium` should open `url` which you point out. 

```
from selenium import webdriver
selenium = webdriver.Firefox()
selenium.get('http://github.com')
```

Geat you have done it.....

### Common Errors
- `WebDriverException`: Message: `'geckodriver'` executable needs to be in PATH.
    You need to download and set the path for `greckdriver`
    - Download [greckdirver](https://github.com/mozilla/geckodriver/releases)
    - Extract and copy geckodriver in `/usr/local/bin`. You can export path as well.
