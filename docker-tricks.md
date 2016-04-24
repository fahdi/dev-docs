# Delete all images

In the bash, run the following command

  docker rmi $(docker images -q)
