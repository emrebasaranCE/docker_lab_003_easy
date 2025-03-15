"# docker_lab_003_easy" 

# 
With this example, i learned that we don't need a specific programming language, we can create images of everthing we want.  

# 

We can create what we want, but there is a catch. The catch is we can do whatever we want but still need to consider resource usage. For this reason, we shouldn't be impetuous...

#

As my course mentiones the command `cp`, i would like to explain in here too.

Container itself is a instance of a image we specified. And i thought that we couldnt access files of the container, turns out its not the case. We can access it by using the command `docker cp [source_path] [destination_path]`. As we can see, copying can be either way: from host to container or container to host. But we have be carefull while using this commands. To access docker's files, we need to specify dockers name or id like this: `docker cp ./test/test.txt [container_name/id]:/test`. In this use, if there isn't a folder named `test`, docker will create the file and then copy the `test.txt` to that path.   

# Naming & Tagging Containers and Images

### Tagging and Naming an Image
`docker build -t [image_name]:[image_tag] .`

### Naming
`docker run -p 3000:80 -d --rm --name [container_name]:[specific_image_tag] [image_id]`
With --name attribute, we can specify name of the container that has been created. Also with --rm, the container will deleted if this container is stopped.




