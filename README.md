# InstagramDownloader

[![standard-readme compliant](https://img.shields.io/badge/readme%20style-standard-brightgreen.svg?style=flat-square)](https://github.com/RichardLitt/standard-readme)

An IG downloader for single or multiple profiles. In the second case, it assumes a file with a profile name per row and sequentially downloads every new picture, based on a file keeping the last timestamp of the update, in its relative directory.

No access token is needed but optionally you can insert your login name and password and download as yourself. Not recommended for huge downloads as Instagram doesn't like that and can identify your account if you are logged in. A couple of tens of accounts to download should be fine.

## Install

Make sure to install first [Instaloader](https://github.com/instaloader/instaloader) as the script uses its API.

Then download the script and run as

```python
./instagram_downloader.py [run|update|profilename]
```

## Usage

There are 3 main operations, `run`, `update` and a profile name. Each can be given a date to start download the images or you can change the hardcoded date in the script's file. `run` doesn't check the previous time a profile images were downloaded and it is thus meant for a first run, when no previously attemtps were done. Otherwise, `update` is what you need, as a file with the last downloaded timestamp will be present in each profile's directory and only the new images will be downloaded.

The start date can be given as an argument, as in

```python
./instagram_downloader.py -s 2018 01 02 update
```

## Contribute

PRs accepted.

## License

MIT © Gianluca Fiore

[![ko-fi](https://www.ko-fi.com/img/donate_sm.png)](https://ko-fi.com/W7W7KA0Z)

