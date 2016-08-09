# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure(2) do |config|

  config.vm.box = "ubuntu/xenial64"

  config.vm.provision "shell", inline: <<-SHELL
    sudo add-apt-repository ppa:hvr/ghc --yes
    sudo apt-get update
    sudo apt-get install ghc-7.0.1 ghc-7.2.1 cabal-install-1.16 --yes
    echo "export PATH=/opt/ghc/7.0.1/bin/:/opt/cabal/1.16/bin/:$PATH" > ghc-env-7.0.1.sh
    echo "export PATH=/opt/ghc/7.2.1/bin/:/opt/cabal/1.16/bin/:$PATH" > ghc-env-7.2.1.sh
    /opt/cabal/1.16/bin/cabal update
  SHELL

end
