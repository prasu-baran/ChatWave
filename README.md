# ChatWave

## OverView
ChatWave in C with Socket Programming using threads and using select system call. Both Threads and Select system call allows to handle multiple clients in socket programming simultaneosly. Private messages, group chats and file tranfer are supported. Messages and files transfer are client side encrypted. No one outside of the chat, during transmission, can read or listen to them. Check the [Features](#features) section for more.

## Using Threads
serverThread.c and clientThread.c uses threads to achieve Client Server Architecture.

Command to start serverThread.c

  ```bash
  gcc serverThread.c -o serverThread
  ./serverThread <port_no>
  ```
<br>
Command to start clientThread.c

  ```bash
  gcc clientThread.c -o clientThread
  ./clientThread <IP_Address> <port_no> <username>
  ```
 - A new file named **username.txt** will be created
 - All the messages received from clients and server will be shown in the file  

## Using Select
server.c and client.c uses select() system call to achieve Client Server Architecture.

Command to start server.c

  ```bash
  gcc server.c -o server
  ./server <port_no>
  ```
<br>
Command to start client.c

  ```bash
  gcc client.c -o client
  ./client <IP_Address> <port_no> <username>
  ```
 - A new file named **username.txt** will be created
 - All the messages received from clients and server will be shown in the file  

## Features

-Handles multiple clients concurrently
-Enforces unique usernames
-Private messaging between two clients
-Broadcasting messages to all active clients
-File transfer between clients
-Client reporting system
-Server-controlled client removal
-Client-side encrypted message and file transmission
-Configurable idle timeout
-Group chat functionality:
 -Create a group
 -Join a group
 -Leave a group
 -Groups with no members are automatically deleted

## Still in Process
