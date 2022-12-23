# speech-to-text

## About
It often happens that you cannot listen to a voice message, but the information in it is very important? This bot will help you. The bot turns a voice message in to a text message.

## How it works?
After sending a voice message, the bot downloads it in ```ogg``` format. The speech recognition library does not work with this format, so first the bot will convert the received file in to a ```wav``` format, using FFmpeg. After that, the speech recognition function is launched. Heard text is written to a variable and sent to the user. If in the message a silence or the words are illegible - the user will get an error. After the end of the work, the bot automatically delete all unnecessary files.

## Usage
First of all, you need to download the repository. And use this command to install the requirements:

```sh
pip install -r requirements.txt
```

For the correct work you also need a FFmpeg. You can install it as a plugin, use a library, or use a buildpack.

| FFmpeg | Link |
| ------ | ------ |
| Plugin | https://www.ffmpeg.org/ |
| Library | https://github.com/kkroening/ffmpeg-python |
| Buildpack | https://github.com/jonathanong/heroku-buildpack-ffmpeg-latest |
