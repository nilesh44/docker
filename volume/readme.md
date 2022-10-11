## why we required docker volume ?
* if we create an docker container without any volume  attached to it and if suppose container get crashed the whatever the sourceCode, logs or data which is created in that container will lost.
to make data persistence for docker container we have to create and attach an docker volume to container which will be generating persistence data .
* attaching volume to an container and storing any type of data in volume is best practice.
* volume are directories placed on host machine.
* volume of host machine always in sync with volume attached in container . 
