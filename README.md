# quoteNf
Simple python quote email notifier.

The sole purpose of this project was to try out Phython...

At first config file is loaded afterwards previous settings are restored (restart).
If you want a fresh start, simply remove the recovery.json file

Notify at a set margin or percentage
| :exclamation:  Note that a too low interval, might exceed the daily free quota!   |
|-------------------------------------------------------------------------------------|
## Rapid API
<a href="https://rapidapi.com/">API for Yahoo Finance</a>
## Yagmail
<a href="https://github.com/kootenpv/yagmail">Git Repo</a>
Installation:
```python
pip3 install yagmail[all]
```
Setup with Google app :
```python
import yagmail
yagmail.register('mygmailusername', 'mygmailpassword') # keyring registration
```
Usage:
```python
yag = yagmail.SMTP("user@gmail.com")
yag.send(subject="Great!")
```
## config.json example
It is possible to list one symbol multiple times and it's also possible to exclude attributes.
```json
{
  "host": "yahoo-finance-low-latency.p.rapidapi.com",
  "api_key": "1234oiu1345oi123aslrktj2340958lkj234sdflkjdfklj999",
  "interval": 60,
  "email_sender": "sender@example.com",
  "email_recipients": ["ra@example.com", "rb@example.com"],
  "notifications": [
    { "symbol": "USDEUR=X", "price": 100, "percentage": 10 },
    { "symbol": "JNJ", "price": 100, "percentage": 10, "spread": 50 }
  ]
}```
