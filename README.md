This section provides a tutorial example on how to make a self-signed certificate trusted during a SSL socket communication.

© 2016 by Dr. Herong Yang. All rights reserved.

            

One way to resolve the self-signed certificate problem shown in the previous section, is to pre-install the server's public key on the client machine and define it as a trusted certificate:

On the server side, export my public key out as a certificate.
One the client side, import the server's public key into a key store file.
Run the SSL client program with the key store file as trusted. This can be done by using "-Djavax.net.ssl.trustStore=public.jks" as java option.