# Basic Widgetastic

## Use of basic Widget:
- Imports requirnments

```
from widgetastic.widget import Browser, View, Text, TextInput
from selenium import webdriver

selenium = webdriver.Firefox()
selenium.get('file:///home/some_path/demo_widget.html')
```

- With `Browser` class form widgetastic create an object. This `browser` object will provide
the access to basic methods which are wrapped arround selenium. 

```
class MyBrowser(Browser):
    pass

browser = MyBrowser(selenium)
```

- With `View` class from Widgetastic create an object. This will help to hold the `widgets`.

```
class MyView(View):
    pass

view = MyView(browser)
```

- Lets, start with first widget access. `TextInput` from widgetastic can take three passible 
arguments. It can be initialize with `id`, `name` or `locator`. `TextInput` widget is assigned to `view` with a proper `id` as follows:

```
text_input = TextInput(view, id='textinput')
```

- Check `text_input` properly displayed on UI or not using method `is_displayed`
```
text_input.is_displayed
Out: True
```

- Read the initial data in `text_input`
```
text_input.read()
Out: ''
```

- Fill `text_input` with some data. lets, try `Python Pune` string

```
text_input.fill('Python Pune')
Out: True
```

- Initialize `Text` widget from widgetastic.
```
text_data = Text(view, locator='//*[@id="textarea"]')
```
- Check `Text` properly displyed on UI or not. 
```
text_data.is_displayed
Out: True
```
- Read the data form `Text`
```
text_data.read()
Out: 'Welcome to Python Pune Meetup. Have fun with Widgetastic'
```