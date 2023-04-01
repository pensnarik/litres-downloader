# Litres books downloader

Script allows you to download books that normally acessible only online or in Android/iOS LitRes application using Python and Selenium. It's assumed that the book has already been purchased and exists in your personal account.

## Usage

The only script arguments are `--url`, `--login` and `--password`. Script won't work if your account requires third-party authorization like Google. `--url` is a book URL, should look like `https://www.litres.ru/book/<author>/<name>-<id>/`.

Here is the common usage scenario (virtualenv is recommended):

```bash
$ virtualenv .venv
$ pip3 install -r requirements.txt
$ ./litres-downloader.py --url https://www.litres.ru/book/dru-neyl/prakticheskoe-ispolzovanie-vim-10014985/ --login <login> --password <password>
```

The book will be saved into final_book.pdf file.

## Requirements

The tool requires Selenium, img2pdf and Pillow libraries which are listed in [requirements.txt](requirements.txt).
