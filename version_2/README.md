# Python Chatbox

This is a simple chat application created using [Python](https://www.python.org/) and [Curses](https://docs.python.org/3/howto/curses.html) along with [Socket Programming](https://docs.python.org/3/library/socket.html). This application allows for simultaneous, real-time chatting from the terminal. We don't have to run two different scripts to Send and Receive messages. We can `Send` and `Receive` messages asynchronously on the same screen.

It has three scripts

-   **[Server.py](./version_1/Server.py)**  
    This is a server-side of the application which handles the communications between multiple clients

-   **[HandleClient](./packages/HandleClient.py)**  
    This is a client-side of the application which handles incoming and outgoing messages for a specific client. This script acts as a mediator between `Server` and `Client`

-   **[Main.py](./Main.py)**  
    This is the entry point of the application. This script contains a gui-like screen for interacting. It provides `Text Area` and `Text View Area`, which can be used to send and display messages.

## Installation
Most of the packages used in the project are built-in packages. However, some packages need to be installed.  
Run the following command to install all the packages required. 

```powershell
pip install -r requirements.txt
```

## Usages
To get started, first, we need to make sure the Server is up and running. To do so, run the [Server.py](./version_1/Server.py).
```bash
python Server.py
```
After the server is started, you will see some information on the screen that is required to connect to the server from the client. 

Now, let the server run on its terminal (can run on a remote server too), and start a new terminal, which executes [Main.py](./Main.py) file.
```bash
python Main.py
```
This is the entry file for the client that provides a GUI-like interface. 

Fill in all the information asked by the interface.   
Now you can send messages and any other client connected to the server will be able to receive and send messages.   
You will see both Text Field and Message Area on the same terminal (Main.py's terminal).  

## Commands
`:exit`, Quit the program
`!!exit`, Shuts down the server
`ENTER`, Sends message(submit)
`L_CTRL + ENTER`, inserts line-break
`BACKSPACE`, clear the character in front of the cursor
`DELETE`, clear the character behind the cursor

## Others
**Potential Upgrades**:
_This includes both versions of chatbox(s)_

-   File sharing between Clients
-   Video Communication
-   Audio Communication
-   UI for sign-in and sign-up
-   Separate Chatroom
