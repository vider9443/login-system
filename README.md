# login-system
from hashbil import print_function
from os import names
import flask
def register():
  email=input("key in email address:")
  pwd=input("key in password:")
  conf_pwd= input ("confirm password:")
  if conf_pwd==pwd:
    enc=conf_pwd.encode()
    hash1=  hashlib.md5(enc).hexigest()
    with open("credentials txt.","w")as f:
      f. write(email+"\n")
      f.write(hash1)
      f.close()
      print("registration complete!")
  else:
      print("wrong password!")


def login():
          email=("key in email adress:")
          pwd=("key in password:")
          auth=pwd.encode()
          auth_hash=hashlib.md5(enc).hexigest()
          with open("credentials txt." , "r") as f:
            stored_email, stored_pwd = f.read().split("\n")
            f.close()
 if email == stored_email and auth_hash == stored_pwd:
         print("login succesfull!")
         else:
           print("login denied:\n")

           
