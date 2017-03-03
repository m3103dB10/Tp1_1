EL HAJOUI
Samy

# Tp1

##Compte rendu

##Programme Client :

from socket import 

serverName = "10.98.2.87"                      
serverPort = 12000                        
clientSocket = socket(AF_INET, SOCK_DGRAM)                      
message = raw_input('Input lowercase sentence:')                    
clientSocket.sendto(message,(serverName, serverPort))                
modifiedMessage, serverAddress = clientSocket.recvfrom(2048)
print modifiedMessage
                    
                    
##Programme Serveur :

from socket import 
serverPort = 12000
serverSocket = socket(AF_INET, SOCK_DGRAM)
serverSocket.bind(('', serverPort))
print "The server is ready to receive"
while 1:
	message, clientAddress = serverSocket.recvfrom(2048)
	print "rec"
	modifiedMessage = message.upper()
	serverSocket.sendto(modifiedMessage, clientAddress)
    
    
- De plus, on peut communiquer entre 2 machines distantes, en remplaçant le serverName par l'adresse IP de la machine en question    




    
    


    
