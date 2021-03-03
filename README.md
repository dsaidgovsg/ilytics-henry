<img src="logo.png" width="200">

## Backend

This repo contains the backend(gunicorn, flask, and darknet model) for ilytics.sg 


## Run Instruction


1. Clone this repository & checkout to the correct branch

 - `git clone https://github.com/dsaidgovsg/ilytics.git`

2. Navigate into the repository

 - `cd ilytics`
 - `git fetch -a`
 - `git checkout -t handover_sfa_gpu`

3. Ensure that the 4 files are in ./aimodel folder before running the following steps.

> 1. `.cfg`
> 2. `.data` 
> 3. `.names`
> 4. `.weights`

4. Build the docker image
 `docker build . --tag ilytics_backend_gpu`

5. Run the docker container
 `docker run --gpus=all --name ilytics_backend_gpu -itd -p 8888:8888 ilytics_backend_gpu`

6. Check if container is running
```
Run the following command and ensure 'ilytics_backend_gpu' is visible on the 'Name' column
```
- `docker ps`

7. Your Backend is up and running!


