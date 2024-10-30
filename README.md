
# umbrella-helm-chart

- #DIKKAT
```
Subchart helmleriniz icerisindeki deployment yml larda deploy edilecek service isimlerini zorunlu sabitlemek gerekiryor. 
#Ornek  : fullnameOverride: "a-service"
```

- Versiyon Yönetimi
```
  Chart.yaml iniz icerisinde yer alan 
  " version: 0.0.1 " alanini her bir Helm Umbrella Chart uretimi oncesi artirmaniz gerekmektedir.
```


- for helmUmbrellaChart
```
Bu komut ile  "helm repo add helm_repo https://artifactory.example.com.tr/artifactory/local-helm-prod/" komutu ile repo helm repolara eklenebilir,
iki kullanim ornegi asagidadir.

dependencies:
- name: a-service
  version: "0.0.2"
  repository: "https://artifactory.turkcell.com.tr/artifactory/local-helm-prod/"
- name: api-gateway
  version: "2024-02-06.16.35"
  repository: "@helm_repo"
```


 