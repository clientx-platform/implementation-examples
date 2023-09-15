
# ClientX Agent Bot Demo using Rasa

> You should be running this demo on a local installation of ClientX and a non dockerd setup for the `localhost` and `ports` to be accessible for all the services involved. If you are intending to run in a remote server, ensure you change the localhost urls with appropriate IP addresses and make sure the ports should be accessible for all the services involved. 

This is a sample implementation of agent bot capabilities in clientx using [rasa](https://rasa.com/) . Rasa Open Source is a machine learning framework to automate text- and voice-based assistants.

You can refer the [rasa documentation](https://rasa.com/docs/rasa/user-guide/installation/) to get it up and running in your machine. 

This implementation isn't a recommended set up for production, but just to illustrate the capabilities of the platform. Please build on top of this ideas discussed to have in running in production.




## Get a rasa project up and running. 

Go to a new directory and create a rasa project. If you have rasa installed in your machine you can get it up and running by follow in commands.  Refer [docs](https://rasa.com/docs/rasa/user-guide/rasa-tutorial/) to get the installation up and running. 

```
mkdir rasa
cd rasa
rasa init --no-prompt
```

go to `credentials.yml` file in the directory and ensure the following value is set. This is to ensure we can communicate with rasa through rest api

```
rest:
  # you don't need to provide anything here - this channel doesn't
  # require any credentials
```

start the rasa server with following command

```
 rasa run -m models --enable-api --log-file out.log
```

