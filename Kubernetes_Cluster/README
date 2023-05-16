# Kubernetes Cluster
- vagrant를 통해 Kubernetes Cluster with develop env provisioning

## GOAL
|||||
|--|--|--|--|
|**No.**|**목표**|**구현 여부**|**비고**| 
|**1**|vagrant up 시 K8S provisioning|O|| 
|**2**|vagrant up 시 개발 환경에 맞춘 Kong API Gateway 구성|X||
|**3**|vagrant up 시 개발 환경에 맞춘 Prometheus 구성|X||
|**4**|vagrant up 시 개발 환경에 맞춘 Grafana 구성|X||

## running environment
- vagrant 
- virtual box 
- host os : window
    - host os가 linux일 경우 , 아래처럼 Vagrantfile의 synced_folder 경로 수정 필요
```Vagrantfile
...
#host_경로 , vm내부 경로 순서
master.vm.synced_folder "./join", "/home/vagrant/join"
...
worker.vm.synced_folder "./join", "/home/vagrant/join"
...
```

|name | version| 
|--|--|
|kubeadm |latest |
|container runtime |containerd://1.6.18 |

### 0.1 minimum requirements
|name |requirements | 
|--|--|
|cpu |16Core |
|memory |16GB |

최소 요구사항이 안된다면 , Vagrantfile의 cpu , memory값 수정하여 반영

### 0.2 port-forward option
Default로 local : 80 -> vm 8080 으로 설정
- Kong 설치 후 변경 예정

```Vagrantfile
...
Vagrant.configure("2") do |config|
  config.vm.network "forwarded_port", guest: 80, host: 8080
end
...
```
- [vagrant port-forward 공식문서](https://developer.hashicorp.com/vagrant/docs/networking/forwarded_ports)

## 1. usecase
worker join 명령어가 떨어지는 join directory 로컬에 생성 
- 꼭 Vagrantfile이 위치한 공간이어야 함
```bash
mkdir ./join
```

cluster up
```bash
vagrant up
```

cluster down
- vagrant vm 종료
```bash
vagrant halt
```

cluster exit
- vagrant vm 제거
```bash
vagrant destroy
```

Vagrantfile 변경 시 반영 명령어
- network 정책 및 특정 명령어는 반영 안되는경우 있음 .
```bash
vagrant reload
```

vagrant vm ssh 접근 명령어
```bash
#usecase
vagrant ssh 'hostname'

#실 사용 예
vagrant ssh master
vagrant ssh worker-1
vagrant ssh worker-2
```

vagrant ssh pem key 위치
```bash
/.vagrant/machines/master/virtualbox/private_key

# ssh usecase
ssh -P 2222 -i .vagrant/machines/master/virtualbox/private_key master@192.168.50.10
```