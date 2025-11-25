# face-cam-detection
# Build the image
docker build -t face-cam-app .

# Run with webcam access (Linux)
docker run --rm -it --device=/dev/video0 -e DISPLAY=$DISPLAY -v /tmp/.X11-unix:/tmp/.X11-unix face-cam-app

# Run with webcam access (macOS/Windows may need different configurations)
//Build the image
docker build -t face-cam-app .

//Run the container
docker run --rm -it \
  --device=/dev/video0 \
  -p 5000:5000 \
  face-cam-app
