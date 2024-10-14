# Lanit test task
 
git --help
git --version
sudo apt install git
sudo apt-get update
apt install git
git --version

# Add Docker's official GPG key:
sudo apt-get update
sudo apt-get install ca-certificates curl
sudo install -m 0755 -d /etc/apt/keyrings
sudo curl -fsSL https://download.docker.com/linux/ubuntu/gpg -o /etc/apt/keyrings/docker.asc
sudo chmod a+r /etc/apt/keyrings/docker.asc

# Add the repository to Apt sources:
echo \
  "deb [arch=$(dpkg --print-architecture) signed-by=/etc/apt/keyrings/docker.asc] https://download.docker.com/linux/ubuntu \
  $(. /etc/os-release && echo "$VERSION_CODENAME") stable" | \
  sudo tee /etc/apt/sources.list.d/docker.list > /dev/null
sudo apt-get update

sudo apt-get install docker-ce docker-ce-cli containerd.io docker-buildx-plugin docker-compose-plugin

docker ps

docker-compose --version

apt-cache policy docker-ce

mkdir -p ~/.docker/cli-plugins/
curl -SL https://github.com/docker/compose/releases/download/v2.29.7/docker-compose-linux-x86_64 -o ~/.docker/cli-plugins/docker-compose

chmod +x ~/.docker/cli-plugins/docker-compose

docker compose version

mkdir simple_website
cd simple_website/
git clone git@github.com:geshan/nginx-docker-compose.git
git config --global user.name "Excentricitet"
git clone https://github.com/geshan/nginx-docker-compose.git
cd ~
sudo apt install nodejs
node -v
npm --version
apt install npm
npm --version
cd simple_website/
cd nginx-docker-compose/
docker compose -f basic.yaml up

nano basic.yaml
# изменяем порт на 80

# В адресную строку браузера своей машины (не виртуальной) вбиваю http://185.128.106.67:80/

# Создаём новое подключение к серверу
curl http://localhost:80