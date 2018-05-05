# TelegramApps-login-api
A simple class written in python to login or create telegram api_id and api_hash automatically.

The class has theese parameters:
- **phone_number** : The phone_number with prefix code
- callback : a function that get code received from telegram and return it
- app_name : The app name if it's not registered yet
- short_name: The app short name if it's not registered yet

**Note** - As default if app_name and short_name are not defined the class will create them automatically with random strings.

Here's to you a simple example without callback.
```python
from Apps import Apps 
phone_number = "+390000000000"
api_id, api_hash = Apps(phone_number).auto()
```

with callback...
```python
from Apps import Apps 

phone_number = "+390000000000"
def callback():
    # Do some stuff to get code received with telegram
    example_code = E7qh0bCgw2M
    return example_code

api_id, api_hash = Apps(phone_number, callback=callback).auto()
```

