### Setting up a secured way to store docker credentials in windows.

> https://github.com/docker/docker-credential-helpers

docker.exe and docker-credential-wincred.exe location

`C:\Program Files\Docker\Docker\resources\bin`

If its not found, download from the release section using above link.

To configure open config.json file from
C:\Users\<USERNAME>\.docker

add/update the field `"credsStore": "wincred"` if not already present inside the json.

Note: the value must match the file's ending word after '-' docker-credential-_wincred_

Then in terminal run `docker logout` if you want existing credentials to be stored this way.

Then do `docker login <URL>` URL defaults to docker hub "https://index.docker.io/v1/"

Will ask for the Username and Password, provide the same for the respective url.