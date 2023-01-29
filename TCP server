import socket
serversocketobj = socket.socket(socket.AF_INET, socket.SOCK_STREAM) ##af_inet is ipv4 and sock stream will spevify we are using tcp connection less protocol
host = socket.gethostbyname()
port = 444
serversocketobj.bind((host, port)) ##binding host and port
serversocketobj.listen((3))  ##setup listener upto 3

while True:
    clientsocket, address = serversocketobj.accept()  ##Type of info that we are going to accepted from client 
    print("Received connection from " % str(address))  ##convert address into string
    message = "Hello thanks for connecting" + "\r\n"
    clientsocket.send(message) ##will be sent to client once connected
    clientsocket.close() ##close socket
