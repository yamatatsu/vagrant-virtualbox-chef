# staging同等の仮想マシンをローカルにつくってくれる

## 使い方

### 1.各種インストール

```
brew cask install vagrant
brew cask install virtualbox
```

* vagrant: virtualboxとかchefとかを駆使してくれる人
* virtualbox: 仮想マシンを立ててくれる専門の人

```
vagrant up
```

初回はimageのインストールのためにめっちゃ時間かかるかも  
以下のエラーが出たらもっかい vagrant up すると治るかも

```
SSL read: error:00000000:lib(0):func(0):reason(0), errno 54
```

```
touch ~/.ssh/config
vagrant ssh-config --host local-development >> ~/.ssh/config
ssh local-development
```


```
gem install chef knife-solo berkshelf
```


以下仮置き opsworksで使ってるレシピたち
Setup
  opsworks_initial_setup
  ssh_host_keys
  ssh_users
  mysql::client
  dependencies
  ebs
  opsworks_ganglia::client
Configure
  opsworks_ganglia::configure-client
  ssh_users
  mysql::client
  agent_version
Deploy
  deploy::default
Undeploy
Shutdown
  opsworks_shutdown::default
