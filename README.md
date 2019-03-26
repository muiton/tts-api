# Text to Scheech Free API
![Logo](https://i.imgur.com/ZJ6o6r2.png)

## About
[Textto-Speech.Net](https://www.textto-speech.net) is provideing free API for converting text into speech or mp3 files. We use Google's TTS engine to make it happen.

So Full credit goes to [Google](https://www.google.com/) 😘

## API Endpoints

### Create MP3 File
__This Endpoint will only accept POST requests__
```
https://tts-api.org/make
```

#### Variables accepted by this Endpoint
Vairable | Description
--- | ---
__text__ | The text that is going to be converted to Audio File ( MP3 File )
__lang__ | The Language Key Code ( Curretly supports more than 60 languages )

### Get Languages
__This Endpoint will only accept GET requests__
```
https://tts-api.org/getlang
```

#### Variables accepted by this Endpoint
Vairable | Description
--- | ---
__none__ | __"/getlang"__ Endpopint does not require any variables

## Demos 

__Note :__ For all demos we have used __[unirest](http://unirest.io/)__ Library.

### Make Text to Speech

* #### cURL
```curl
curl -X POST --include 'https://tts-api.org/make' \
  -H 'Content-Type: application/x-www-form-urlencoded' \
  -d 'text=Hello, world!' \
  -d 'lang=en-us'
```

* #### PHP
```php
$response = Unirest\Request::post("https://tts-api.org/make",
  array(
    "Content-Type" => "application/x-www-form-urlencoded"
  ),
  array(
    "text" => "Hello, world!",
    "lang" => "en-us"
  )
);
```

* #### Python
```python
response = unirest.post("https://tts-api.org/make",
  headers={
    "Content-Type": "application/x-www-form-urlencoded"
  },
  params={
    "text": "Hello, world!",
    "lang": "en-us"
  }
)
```

### Get Supported Langauges

* #### cURL
```curl
curl --get --include 'https://tts-api.org/getlang'
```

* #### PHP
```php
$response = Unirest\Request::get("https://tts-api.org/getlang");
```

* #### Python
```python
response = unirest.get("https://tts-api.org/getlang")
```
## Support
For any kind of query or issues please use bellow methods.
* Mail at [madcode.git@gmail.com](mailto:madcode.git@gmail.com)
* Create an ticket or issue [here](https://github.com/madcode-git/tts-api/issues)

## Copyrigtht
* [Textto-Speech.Net](https://www.textto-speech.net)
* [Rayhan Sardar](https://github.com/madcode-git)
