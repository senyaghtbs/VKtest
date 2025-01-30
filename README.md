# VKtest
Создал вм, на которую накатил K3s, после чего написал 2 манифеста для tarantool, Deployment и service c nodeport(для доступа из вне).
Применил манифесты, проверил, что под и сервис появились. 
Проверил доступность с помощью telnet по порту 30001 и получил такой ответ:
```
Ξ ~ → telnet 192.168.105.4 30001
Trying 192.168.105.4...
Connected to 192.168.105.4.
Escape character is '^]'.
Tarantool 3.3.1 (Binary) e5cfaab7-adb4-406f-a7e5-d3849f28e7e7
X7predNA3bc8/XnhafS3A8hp/nnsb418cr4N9foBk88=
````



Запуск Helm
cd VKtarantool-chart
helm install VKtarantool-release ./
