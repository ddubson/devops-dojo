##### COPY
COPY command copies a file or directory from the directory containing the Dockerfile to the container's image directory

e.g. `COPY <src> <dest>`

##### CMD
Default command to run when the container is launched. Alternative command is `ENTRYPOINT`

e.g. `CMD ['cmd','arg1','arg1-value', arg2', 'arg2-value', ...]`

##### WORKDIR
Sets the directory in which all commands should execute from in a container