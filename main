"""
Simple script to download and write files in Python
written for IBM Python & Data Science course
Rodrigo feb 27, 2021
"""

import requests
import os
import sys

class Pget(object):
    #constructor
    def __init__(self, url):
        self.url = url
        try:
            r = requests.get(url)
            file=r.url.split('/')[-1]
            path=os.path.join(os.getcwd(),file)
            with open(path, 'wb') as f:
                f.write(r.content)
                print(file,"was successfully downloaded.")
        except:
            print("Unable to reach the download the file!")

if len(sys.argv) == 2:
    link=sys.argv[1]
    Pget(link)
else:
    print("pget.py by Solaris\nSyntax: python pget.py URL")

