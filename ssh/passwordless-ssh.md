# Passwordless SSH to server

Useful when you trust a server and don't want to enter the password everytime.

1. Generate a public/private key pair

	`ssh-keygen -t rsa`

2. Copy the public key to the server.

	2.1. Linux

		ssh-copy-id <user>@<host>

	2.2. Windows

		type <path_to_home>\.ssh\id_rsa.pub | ssh <user>@<host> "cat >> .ssh/authorized_keys"
	
	Note: While copying the public key, you will have to enter the password.

3. Test

	`ssh <user>@<host>`
	should not ask for the password now and directly provide the prompt window of the host.

