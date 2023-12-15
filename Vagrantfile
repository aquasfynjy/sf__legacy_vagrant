Vagrant.configure("2") do |config|
  config.vm.box = "bento/ubuntu-20.04"
  config.vm.define "psql-8.4"
  config.vm.hostname = "psql-8.4"
  config.vm.provision "shell", inline: <<-SHELL
  echo "deb [arch=amd64] http://apt.postgresql.org/pub/repos/apt $(lsb_release -cs)-pgdg main" > /etc/apt/sources.list.d/postgresql.list
  wget --quiet -O - https://www.postgresql.org/media/keys/ACCC4CF8.asc | sudo apt-key add -
  apt-get update
  DEBIAN_FRONTEND=noninteractive apt install  -y postgresql-8.4
 SHELL
end
