# K8S_API_PROJECT
Kubernetes management platform using that Kubernetes client library

## **Envirement**
||||
|--|--|--|
|명칭|Version|비고|
|JAVA|||
|Spring Boot|||
|Kubernetes|||
|Kafka|||
|zookeeper|||
|Kong API Gateway|||
|Grafana|||
|Prometheus|||
|Redis|||
|Cassandra|||
|PostgreSQL|||
|MySQL|||

## **Project RoadMap**
- Repository Map

||||||
|--|--|--|--|--|
|명칭|사용 언어|포트번호|경로|비고|
|Spring Cloud Gateway|Java Spring Boot|8080:8080|[SCG](./scg/)||
|API Client|Java Spring Boot|8001:8001|[api_client](./api_client/)||
|Kafka Cluster|vagrantfile , Shell script| - |[Kafka_Cluster](./Kafka_Cluster/)||
|Kubernetes Cluster|vagrantfile , Shell script| - |[Kubernetes_Cluster](./Kubernetes_Cluster/)||

### **GOAL INFO**
- 각 Project 별 GOAL Section 관리하여 프로젝트 목표치 달성 여부 판단

|||||
|--|--|--|--|
|명칭|GOAL Section Path|달성 여부|비고|
|Spring Cloud Gateway|[SCG_GOAL]()|-|GOAL 제작중|
|API Client|[api_client]()|-|GOAL 제작중|
|Kafka Cluster|[Kafka_Cluster_GOAL](./Kafka_Cluster/README.md/#goal)|X||
|Kubernetes Cluster|[Kubernetes_Cluster_GOAL](./Kubernetes_Cluster/README/#goal)|X||

## **Architecture**

![K8S_Mangement_Platform][K8S_Mangement_Platform]

[K8S_Mangement_Platform]:./images/K8S_Mangement_Platform.png