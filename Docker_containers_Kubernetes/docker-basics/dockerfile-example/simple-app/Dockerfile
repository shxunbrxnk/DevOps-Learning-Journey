FROM node    #this instruction pulls an image from docker hub which is used as a foundation)

WORKDIR /app #this instuction creates a directory of an application we are going to containarize)

COPY . /app  #this instruction copy's every file/script that is in the project folder into the app folder )

RUN  npm install #this instruction basically installs a dependencies to run this application in a container)

EXPOSE 80  #this instruction exposes a port through which the app will be accessible through)

CMD ["node", "server.js"] # this instruction basically pulls the image and then runs it against the server.js script which is our source code
