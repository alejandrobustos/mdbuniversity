# docker for the course: Mongodb for DBA, in mongodb University.

This docker provides the necessary mongodb installation for the course mentioned in the title. This is valid for the course started on January 2016

You should do:
  - Run the build.sh in order to make the image from the Dockerfile.
  - Run the run.sh in order to run/create the container. It will use the net host configuration, so mongodb server will be listening on default port. If you want to remap the port into another (let's say 27117) just comment the first line and uncomment the second.

Now you will be prompted to a console inside the container with root permission. Type mongod to start mongo (first time will take a while).

Then you should be able to connect from the host by typing "mongo" on the terminal. If you remapped the port use "mongo --port 27117"

Just in case, root password is set to "toor".
