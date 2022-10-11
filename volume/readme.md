## why we required docker volume ?
* if we create an docker container without any volume  attached to it and if suppose container get crashed the whatever the sourceCode, logs or data which is created in that container will lost.
to make data persistence for docker container we have to create and attach an docker volume to container which will be generating persistence data
