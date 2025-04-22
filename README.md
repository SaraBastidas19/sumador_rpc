# sumador_rpc

1. Instala dependencias (si no están)
sudo apt update
sudo apt install -y rpcbind libtirpc-dev

2. Crea tu carpeta y entra
mkdir sumador_rpc
cd sumador_rpc

3. rea los archivos (sumador.x, sumador_server.c)
nano sumador.x
nano sumador_server.c

4.Genera los archivos RPC automáticamente
rpcgen sumador.x

5. Compila con make
make

6. Inicia el servicio RPC y el servidor
sudo service rpcbind start
./sumador_server

7. En otra terminal, ejecuta el cliente
./sumador_client localhost

