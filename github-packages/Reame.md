export GH_USERNAME='Sharma10x'
export GH_TOKEN=''
export GH_IMAGE_NAME='hello-world'
export GH_VER='1.0.0'
export TAG_NAME='ghcr.io/sharma10x/hello-world:1.0.0'
echo $GH_TOKEN | docker login ghcr.io -u $GH_USERNAME --password-stdin

docker tag hello-world:latest $TAG_NAME

docker push $TAG_NAME
LABEL org.opencontainers.image.source https://github.com/OWNER/REPO