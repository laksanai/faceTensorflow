-----------------------------------------run jupyter---------------------------------


sudo docker run -it --name bank --rm --gpus all -p 8888:8888 -e DISPLAY:$DISPLAY -v /tmp/.X11-unix:/tmp/.X11-unix:ro -v /home/thanakrit/python/laksanai/docker/FaceRecognition/:/home/laksanai/:rw laksanai/face:0.5


----------------------------------in docker container ---------------------------------------

jupyter notebook --ip 0.0.0.0 --port 8888 --no-browser --allow-root




--------------------- if upu not work on docker --------------------------------------

$ distribution=$(. /etc/os-release;echo $ID$VERSION_ID)       && curl -s -L https://nvidia.github.io/libnvidia-container/gpgkey | sudo apt-key add -       && curl -s -L https://nvidia.github.io/libnvidia-container/$distribution/libnvidia-container.list | sudo tee /etc/apt/sources.list.d/nvidia-container-toolkit.list

$ sudo apt-get update

$ sudo apt-get install -y nvidia-docker2

$ sudo systemctl restart docker



-------------------------tf can't open show gui------------------------------------------



----------------------------unlock file------------------------------------
sudo chown thanakrit:thanakrit bface.tar



--------------------------save docker image ------------------------

docker save -o <path for generated tar file> <image name>
