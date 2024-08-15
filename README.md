# setup-Python3.10

# Prerequisite

```
sudo apt update
sudo apt install software-properties-common -y
```

# Add custom APT repository

```
sudo add-apt-repository ppa:deadsnakes/ppa
sudo apt update
```

Press `ENTER` to confirm adding repository.

# Install Python 3.10

```
sudo apt install python3.10 python3.10-venv python3.10-dev
python3 --version
```

You will see previous of Python. At the writing time `Python 3.8.10`

## Make symbolic link (Optional)

> [!CAUTION]
> This may cause problem with terminal not open on Ubuntu
> 
> https://askubuntu.com/questions/1397938/terminal-not-opening-after-changing-python-version

```
ls -la /usr/bin/python3
sudo rm /usr/bin/python3
sudo ln -s python3.10 /usr/bin/python3
python3 --version
```

Now you will see `Python 3.10.x`

# Install PIP for Python 3.10

```
curl -sS https://bootstrap.pypa.io/get-pip.py | python3.10
python3.10 -m pip --version
```

# Test with system ENV

```
python3.10 -m pip install ipython
```

# Test with Virtual ENV

```
python3.10 -m venv venv
pip install ipython
```

# References

https://computingforgeeks.com/how-to-install-python-on-ubuntu-linux-system/
