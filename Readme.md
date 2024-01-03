## Readme

### An simple introduction to download NASA datasets using Python

See Also: https://disc.gsfc.nasa.gov/information/howto?title=How%20to%20Generate%20Earthdata%20Prerequisite%20Files

### Create prerequisite files

1. Before creating files, ensure you have the access to NASA datasets: https://disc.gsfc.nasa.gov/earthdata-login
2. .netrc

```bash
cd ~
touch .netrc
echo "machine urs.earthdata.nasa.gov login <uid> password <password>" >> .netrc, where <uid> is your username and <password> is your Earthdata Login password without the brackets.
chmod 755 .netrc, every user can access it (since I am using my personal computer, I allow everyone to acces it.)
```

3. .urs_cookies

```bash
cd ~
touch .urs_cookies, create an empty file to store cookies
```

4. .dodsrc

```bat
cd ~
pwd, to get  <YourHomeDirectory> to paste below
touch .dodsrc
echo "HTTP.NETRC=<YourHomeDirectory>/.netrc" >> .dodsrc
echo "HTTP.COOKIEJAR=< YourHomeDirectory >/.urs_cookies" >> .dodsrc
```

### Initialize Python API

Run initialize.ipynb

### Choose datasets to download

1. Choose the dataset you try to download in NASA
2. download the files_list.txt 

### Download using Python 

Run download_rawdata.ipynb

