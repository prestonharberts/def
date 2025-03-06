# def (a CLI dictionary reference tool)

def is a CLI program that uses sdvc to quickly print StarDict dicitonary items to the Terminal.

## Setup

I recommend putting this script in your PATH so that it can be called from anywhere. I made a Bin folder in my user directory, moved bib to it, and added this line to my `.bashrc`:

```bash
export PATH=/home/$USER/Bin/:$PATH
```

Next, give execution privileges to bib:

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
rm ~/Downloads/stardict* -r
```

## Usage

This program is used `def <word>` but currently does not work with multiple-word dictionary entries like `personal computer`. See the example below for the definition of "how":


