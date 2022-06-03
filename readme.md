## Takeaways

```markdown
# -rm removes the container after it has been stopped
# 4000 is host port, 5000 is container's exposed port
# _c are container names and _images are images
sudo docker run --name myapp_c -p 4000:5000 -rm myapp_image
```

### Volumes Intro
```markdown
# -v first path is absolute path; you can copy from vscode lhs sidebar
# e.g : /home/dev/Desktop/pro/self tut/docker-tut/api
# -v takes 2 args separated by colon 
# abs_path:app_path_inside_container
sudo docker run --name myapp_c -p 4000:5000 -rm -v /home/dev/Desktop/pro/self tut/docker-tut/api:/app myapp_image
```


```markdown
# need to add exception volume for node_modules
# -v /app/node_modules
sudo docker run --name myapp_c -p 4000:5000 -rm -v /home/dev/Desktop/pro/self tut/docker-tut/api:/app **-v /app/node_modules** myapp_image
```


![docker cheat sheet](dockercheatsheet8.png)


