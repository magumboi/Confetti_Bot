
# Confetti_Bot 🤖
![License: MIT][ico-license]

This is a forked version of HQ_bot, a bot to help answer questions on trivia games like Confetti, HQ and CashShow. This bot takes screenshot of the game on the phone and uses googles tesseract OCR to read the questions and options. It automates the process of googling of the answers and gives the most likely answer! It is 70%+ accurate!

* Multiprocessing methods were used to make google api calls 2x faster (from about 8.5s to 3.8s). 
* tesseract spanish package were used to read spanish words properly.

Since it is against the policy of HQ-trivia i do not encourage anyone to use this during a live game and this is purely for educational purposes.  

## Packages Used

Use python 3.7.2. In particular the packages/libraries used are...

* JSON - Data Storage 
* Pillow - Image manipulation
* Google-Search-API - Google searching
* wikipediaapi - Wikipedia searches
* pytesseract - Google's free/open source OCR (requires seperate installtion)
* beautifulsoup4 - Parse google searches/html
* lxml - Beautifulsoup parser
* opencv2 - Image maniplulation
* pyscreenshot - Take screenshot of the game
* wxPython - GUI interface

*To easily install these*
1. Install python 3.7.2
2. Install above packages
    * `$ pip3 install -r requirements.txt`
3. For tesseract 
	* On Mac
	     `$ brew install tesseract`
    * Windows
        * Go to [UB-Mannheim's Repository](https://github.com/UB-Mannheim/tesseract/wiki)
        * Then find the `tesseract 4.0` binary that corresponds with your system (32 or 64 bit)
         ![](https://i.imgur.com/N2hU0xE.png)
        * Don't forget to add tesseract installation folder to the PATH


## Usage

Make sure all packages above are installed. For Android screen mirroring you could use [scrcpy](https://github.com/Genymobile/scrcpy) and for iOS, quicktime player. **The code expects the phone to be on the left side of the screen.** If you want to change the screenshot co-ordinates change the values inside the ImageGrab in the `screen_grab()` function. To use the script : 

```bash
$ git clone https://github.com/magumboi/Confetti_Bot.git
$ cd Confetti_Bot
$ pip3 install -r requirements.txt
$ python answer_bot.py
Press s to screenshot live game, sampq to run against sample questions or q to quit:
s
...Question...
```
## Screenshots




## Contributing

All contributions are welcome.

## Credits

- [Sushant Rao][link-author]
- [All Contributors][link-contributors]

## Special shout out
[Jake Mor][jake-mor] was the person behind HQuack, the most viral popular bot to help solve HQ questions. His implementation inspired me to try my own. I recommend reading this [article][jake-more] to learn more about the whole story.

## Useful links

- [Wikipedia-API][link-wikiapi]
- [Google-Search-API][link-gapi]
- [Tesseract][link-tesseract]

## License

The MIT License (MIT)

[ico-license]: https://img.shields.io/badge/license-MIT-brightgreen.svg?style=flat-square
[link-vysor]: https://www.vysor.io/
[link-author]: https://github.com/sushant10
[link-contributors]: ../../contributors
[link-wikiapi]: https://pypi.python.org/pypi/wikipedia
[link-gapi]: https://github.com/abenassi/Google-Search-API
[link-mike]: https://github.com/mikealmond/hq-trivia-assistant
[link-tesseract]: https://github.com/tesseract-ocr/tesseract/wiki
[jake-mor]: http://jakemor.com/
[jake-more]: https://medium.com/@jakemor/hquack-my-public-hq-trivia-bot-is-shutting-down-5d9fcdbc9f6e
[sampq]: ()
