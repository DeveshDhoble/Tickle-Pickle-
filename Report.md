# Tickle-Pickle-

Pickle in Python is primarily used in serializing and deserializing a Python object structure. In other words, it's the process of converting a Python object into a byte stream to store it in a file/database, maintain program state across sessions, or transport data over the network.

#server.py

import os
import pickle
def reverse_fun():
      with open("users.json","rb") as f:
          data = f.read()
      
      d = pickle.loads(data)
      return d

if __name__ == '__main__':
      print(reverse_fun())
      
      #Client.py
      
      import os
import pickle
def fun(name,password):
    s = {"username":name,"password":password}
    safecode = pickle.dumps(s)
    with open("users.json","wb") as f:
        f.write(safecode)
    return safecode

if __name__ == '__main__':
    u = input("Username : ")
    p = input("Password : ")
    yo_fun = fun(u,p)


#Before Executing this code, we have to  install module

>pip install pickle5

>pip install os-sys
