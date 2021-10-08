# Remove Older Docker Installation
sudo apt-get remove docker docker-engine docker.io

# Install Docker
sudo apt-get update
sudo apt-get install docker.io

# Allow User to Run Docker
sudo usermod -aG docker $(whoami)

# Exit to Save Changes 

# Pull Postgres
docker pull postgres

# Run Postgres
docker run --name some-postgres -e POSTGRES_PASSWORD=mysecretpassword -d postgres

# Check Images
docker images

# Commit
docker commit -m "Docker Installation" -a "Username" Container-ID postgres

# Upload
docker login -u <Docker_Username>
docker tag local-imageid docker-username/docker-imagename
docker push docker-username/docker-imagename

# Create Dockerfile
vi Dockerfile

