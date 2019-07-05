# mkpyenv

Small wrapper script over python/virtualenv and other utilities.

Purpose is to make life easier when using python virtualenvs.  

**Use it on your own risk. Please inspect the script before using and make sure it does what you intend.**     

 
Requirements:

- python 2/3
- virtualenv
- OPTIONAL: pipreqs
- OPTIONAL: direnv


How to install

```bash
 git clone https://github.com/stefan-kiss/mkpyenv
 cd mkpyenv
 cp mkpyenv /usr/local/bin/
```
( make sure /usr/local/bin is in ${PATH} )

## Usage
```
/usr/local/bin/mkpyenv [ OPTIONS ] < directory>
OPTIONS:
    -h show this help
    -v <version>    - python 2 or 3 as supported by virtualenv -p python ${version}
    -r <true|false> - create requierments file
    -m <method>     - create requierments option. currently supporting:
                        localpip        -> use pip in the EXISTING local venv (require existing
                        pipreqs         -> use pipreqs in the NEW local venv
    -F <true|false> - force overwrite an existing venv environment
    -R <true|false> - force overwrite an existing requirements.txt
    -B <true|false> - backup existing requirements.txt
    -d <true|false> - write .envrc
```
## default flags
-v 3
-r true
-m pipreqs
-F false
-R false
-B true
-d true 

