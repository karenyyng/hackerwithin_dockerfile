
# Usage by building the Dockerfile 
```
$ git clone https://github.com/karenyyng/hackerwithin_dockerfile.git
$ cd HackerWithinDavis_dockerfile
$ docker build -t <WHAT YOU NAME THIS DOCKER IMAGE> .
```					


# Usage by pulling from DockerHub:
There is a hook from the GitHub repo such that any changes 
from in GitHub will trigger a new build of the Docker image on DockerHub.
To pull from the built image and run it:
```
$ docker run -it \
-p 4000:4000 \ 
-v $(pwd):/root \
karenyng/hackerwithin_dockerfile \
ruby -S jekyll serve \
--host=0.0.0.0 --watch --force_polling
```

# Other info 
For more details of how to use Docker, see my Docker tutorial
[(link)](http://karenyyng.github.io/MySlideDeck/dockerTutorial.html).
