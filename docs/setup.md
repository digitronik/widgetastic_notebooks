# Setup Environment

## Create project directory
```
mkdir widgetastic
cd widgetastic
```

## Pull tutorials
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
2. [Widgetastic Patternfly](https://github.com/RedHatQE/widgetastic.patternfly)
3. [Selenium](https://github.com/SeleniumHQ/selenium/)
4. [Ipython](https://ipython.org/)

```
cd tutorial_widgetastic
pip install -r requirements.txt
```

## Test Environment

### Open Ipython
In your user `shell` just type
```
ipython
```

### Import selenium
Import `webdriver` from `selenium` in `ipython`. Assign browser as `Firefox`. It should open `Firefox` browser and `get` command of `selenium` should open `url` which you pointout. 

```
from selenium import webdriver
selenium = webdriver.Firefox()
selenium.get('http://github.com')
```

Geat you done it.....

### Common Errors
- `WebDriverException`: Message: `'geckodriver'` executable needs to be in PATH.
    You need to download and set path for `greckdriver`
    - Download [greckdirver](https://github.com/mozilla/geckodriver/releases)
    - Extract and copy geckodriver in `/usr/local/bin`. You can export path as well.


