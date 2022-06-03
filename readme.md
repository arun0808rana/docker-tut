# Docker Tutorial

[Inspiration : Net Ninja](https://www.youtube.com/playlist?list=PL4cUxeGkcC9hxjeEtdHFNYMtCpjNBm3h7)

[Shaun's source code](https://github.com/iamshaunjp/docker-crash-course)

## Takeaways

### Deletion
```bash
# remove every image, container, volume
sudo docker system prune -a
```

### Listing
```bash
# list all containers, exclude -a to show only running containers
sudo docker ps -a
```

```bash
# -rm removes the container after it has been stopped
# 4000 is host port, 5000 is container's exposed port
# _c are container names and _images are images
sudo docker run --name myapp_c -p 4000:5000 -rm myapp_image
```

### Volumes Intro
```bash
# -v first path is absolute path; you can copy from vscode lhs sidebar
# e.g : /home/dev/Desktop/pro/self tut/docker-tut/api
# -v takes 2 args separated by colon 
# abs_path:app_path_inside_container
sudo docker run --name myapp_c -p 4000:5000 -rm -v /home/dev/Desktop/pro/self tut/docker-tut/api:/app myapp_image
```

### Volume for node_modules backup
```bash
# need to add exception volume for node_modules
# -v /app/node_modules
sudo docker run --name myapp_c -p 4000:5000 -rm -v /home/dev/Desktop/pro/self tut/docker-tut/api:/app -v /app/node_modules myapp_image
```

### Compose
```bash
# just run the damn thing in a single command
# although requires a config file called docker-compose.yaml or docker-compose.yml
docker compose up
```

### Official Dockerfile screenshot for reference
![screenshot of docker file in official docs](/assets/Screenshot%20from%202022-06-03%2014-22-08.png)

### Docker cheatsheet
![docker cheat sheet](/assets/dockercheatsheet8.png)
