# build image
$ docker build -t test-env .

# run with default command, it will display value of $MY_HOME
docker run test-env

# run with "/bin/sh", it will override echo command 
docker run test-env /bin/sh
   -> check value MY_HOME 
  

# run with supplied -e option, it will displya new value of MY_HOME which are "Chonburi"
docker run -it -e "MY_HOME=Chonburi" test-env


# run with supplied -e option & add /bin/sh3, it will override echo command and you can see new variable inside container
docker run -it -e "MY_HOME=Chonburi" test-env /bin/sh
   -> check value MY_HOME 
   
