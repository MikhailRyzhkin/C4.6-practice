# C4.6-practice

Задание C4.6.1
Разверните на Server2 Elasticsearch+Kibana. Настройте визуализацию логов Kibana на ней самой. Log shipper используйте любой на ваш выбор.
Пришлите ментору для проверки скриншот интерфейса Kibana с ее логами и конфиг-файл log shipper.
![Screenshot_1](https://user-images.githubusercontent.com/69116076/233106718-4da6cbc4-6ad2-4fb2-a31a-2ec74a06587f.png)
![Screenshot_2](https://user-images.githubusercontent.com/69116076/233107011-24f6732d-f9de-4110-bcd7-9b16740eb40d.png)
![Screenshot_3](https://user-images.githubusercontent.com/69116076/233109249-8309de9d-164a-4357-af84-643d2234a490.png)
На сервере-2 со стеком ELK используется: локальные nginx logs-filebeats-logstash-elasticsearch-kibana


Задание C4.6.2
Настройте на Server1 с помощью RSyslog отправку логов любого приложения (nginx/Jenkins/что-то еще на ваш выбор) в Elasticsearch на Server2.
Проверьте через Kibana, что логи доставляются (в пункте Discover).
Для проверки пришлите ментору скриншот с логами вашего приложения из Kibana и конфиги самого приложения и RSyslog.
![Screenshot_4](https://user-images.githubusercontent.com/69116076/233109860-e61d5ad3-c08d-484c-b5b0-dd8992ae7f8d.png)
![Screenshot_5](https://user-images.githubusercontent.com/69116076/233110212-c8f8f70f-76b4-4aa2-8e6f-929352c740b5.png)
На сервере-1 с rsyslog используется: локальные nginx logs-logstash(сервер-2)-elasticsearch(сервер-2)-kibana(сервер-2)

Сервере ELK принимает одновременно логи nginx с обоих серверов из filebeats и rsyslog.
Схема такая:
![Архитектура ELK-1](https://user-images.githubusercontent.com/69116076/233112074-04bb34c2-3d23-4d65-8c1f-fb3e2c15067e.png)
