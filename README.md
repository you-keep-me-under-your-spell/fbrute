# fbrute
Tool for bruteforcing content on file-sharing websites, with support for multiple proxies.

# Usage
```
python fbrute --url https://i.imgur.com/ --ext .png --length 7 --threads 500 --proxyfile proxies.txt --outputfile links.txt --download files --ignore 302 404 --head
```

```
usage: fbrute [-h] [-u URL] [-e EXT [EXT ...]] [-c [CHARSET [CHARSET ...]]] [-l LENGTH] [-p PROXYFILE] [-o OUTPUTFILE]
              [-t THREADS] [--head] [-s SKIP] [--debug] [-d DOWNLOAD] [-x [SUCCESS [SUCCESS ...]]]
              [-i [IGNORE [IGNORE ...]]] [--shuffle]

optional arguments:
  -h, --help            show this help message and exit
  -u URL, --url URL     Base url
  -e EXT [EXT ...], --ext EXT [EXT ...]
                        File extensions (including dot at start)
  -c [CHARSET [CHARSET ...]], --charset [CHARSET [CHARSET ...]]
                        Characters to be used within filenames
  -l LENGTH, --length LENGTH
                        Length of filenames
  -p PROXYFILE, --proxyfile PROXYFILE
                        Proxy file
  -o OUTPUTFILE, --outputfile OUTPUTFILE
                        Output file for links
  -t THREADS, --threads THREADS
                        Number of threads to be used
  --head                Use HEAD method for requests
  -s SKIP, --skip SKIP  Skip ahead (amount or filename)
  --debug               Debug mode
  -d DOWNLOAD, --download DOWNLOAD
                        Enables download mode & sets directory
  -x [SUCCESS [SUCCESS ...]], --success [SUCCESS [SUCCESS ...]]
                        Success status codes
  -i [IGNORE [IGNORE ...]], --ignore [IGNORE [IGNORE ...]]
                        Ignored status codes
  --shuffle             Shuffle order of charset
  ```

# Proxies
Threads will automatically switch over to the next proxy in the list when an unrecognized status code is detected (e.g: 429).
