+ I am using `Docker Image` to install postgres and run the container. The reason for it is quite simple. It is light weight and runs in an isolated enviroment.

### Follow the following commands

+ `docker pull postgres` -> pulls the postgres image into the local machine.
+ `docker run --name keshavDB -e POSTGRES_PASSWORD=myPassword -d -p 8000:5432 postgres` -> runs the server in the local machine at port 8000. The `-d` flag is for the detached mode, while `-p` is to expose our isolated port to the local port on the machine. However all the data will be lost once the container is stopped.
+ `docker run --name keshavDB -e POSTGRES_PASSWORD=myPassword -d -p 8000:5432 -v /path/to/local/directory:/var/lib/postgresql/data postgres` -> This command runs the container with a volume mounted for the container.
+ `docker run -it --rm --link keshavDB:postgres postgres psql -h postgres -U postgres` -> This command is used to access the server by the client.
