CGLAGS=-Wall -Wextra

all: tcpclient tcpserver udpclient udpserver

tcpclient: tcpclient.c
	gcc $(CGLAGS) -D BUFSIZE=2 -D SADDR='struct sockaddr' -D SIZE='sizeof(struct sockaddr_in)' tcpclient.c -o tcp_clent.out
tcpserver: tcpserver.c
	gcc $(CGLAGS) -D SERV_PORT=10050 -D BUFSIZE=100  -D SADDR='struct sockaddr' tcpserver.c -o tcp_serv.out
udpclient: udpclient.c
	gcc $(CGLAGS) -D SERV_PORT=20001 -D BUFSIZE=3 -D SADDR='struct sockaddr' -D SLEN='sizeof(struct sockaddr_in)' udpclient.c -o udp_client.out
udpserver: udpserver.c
	gcc $(CGLAGS) -D SERV_PORT=20001 -D BUFSIZE=3 -D SADDR='struct sockaddr' -D SLEN='sizeof(struct sockaddr_in)' udpserver.c -o udp_serv.out
