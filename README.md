# def (a CLI dictionary reference tool)

def is a CLI program that uses sdvc to quickly print StarDict dicitonary entries to the Terminal.

- [Usage](#usage)
- [Setup](#setup)
- [Dependencies](#dependencies)

## Usage

This program is used `def <word>` but currently does not work with multiple-word dictionary entries like `cd player`. See the example below for the definition of "how":

<p align=center><img src="https://github.com/user-attachments/assets/519b507b-6736-4aec-b496-1adc21c30c8f" width="512"></p>

## Setup

I recommend putting this script in your PATH so that it can be called from anywhere. I made a Bin folder in my user directory, moved def to it, and added this line to my `.bashrc`:

```bash
export PATH=/home/$USER/Bin/:$PATH
```

Next, give execution privileges to def:

```bash
chmod u+x ~/Bin/def
```

## Dependencies

Run the following to install sdvc (changing the package manager to match your distribution's manager):

```
sudo dnf install sdcv -y
```

Run the following to install a dictionary:

```
cd ~/Downloads/
wget https://web.archive.org/web/20140917131745/http://abloz.com/huzheng/stardict-dic/dict.org/stardict-dictd_www.dict.org_gcide-2.4.2.tar.bz2
sudo mkdir -p /usr/share/stardict/dic
sudo tar -xvjf stardict-dictd_www.dict.org_gcide-2.4.2.tar.bz2 -C /usr/share/stardict/dic
rm ~/Downloads/stardict-dictd_www.dict.org_gcide-2.4.2.tar.bz2
```
