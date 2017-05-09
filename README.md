ansible-Proxy
=============

ansibleを使って、Ubuntuにプロキシの設定をします。  

ansible...サーバ構成管理ソフトウェア  

テスト環境
-----

Ubuntu 16.04.2 LTS

実行環境
-----

ansibleはpipで入手する．

```
$ ansible --version
ansible 2.3.0.0
  config file =
    configured module search path = Default w/o overrides
      python version = 2.7.12 (default, Nov 19 2016, 06:48:10) [GCC 5.4.0 20160609]
```

proxyの設定場所
------
roles/proxy/vars/main.yml  
```
https_proxy: "https://proxy.example.com:8080/"  
http_proxy: "http://proxy.example.com:8080/"  

```


proxyを設定するもの
------
+ bash
+ git
+ wget
+ curl
+ yum

実行手順
----
簡易版  
hosts内に対象サーバのIPアドレスを入力しておくこと。  

```
ansible-playbook setup.yml -i hosts -K
```

