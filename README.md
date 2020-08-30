# Pushon
A web app I wrote to push multiple Docker images simultaneously to a specified registry.
Saves a lot of time when pushing images to a registry:
* Without Pushon:
  * Upload images to a remote server with Docker installed.
  * Save each image using ```docker save```.
  * Tag each image with the registry name using ```docker tag```.
  * Push each image to the registry using ```docker push```.
* With Pushon:
  * Drag and drop the images to Pushon or select them manually.
  * Submit the images and wait for the process to complete.
  
<img src="https://i.imgur.com/mu2a05J.png" alt="pushon"/>

docker run -d --restart always -v /var/run/docker.sock:/var/run/docker.sock -p 8080:8080 --name pushon -it pushon:latest
