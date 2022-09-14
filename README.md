# Mindbox_test
Задача

Deployment для веб-приложения в kubernetes в виде yaml-манифеста. Есть следующие вводные:

- у нас мультизональный кластер (три зоны), в котором пять нод
- приложение требует около 5-10 секунд для инициализации
- по результатам нагрузочного теста известно, что 4 пода справляются с пиковой нагрузкой
- на первые запросы приложению требуется значительно больше ресурсов CPU, в дальнейшем потребление ровное в районе 0.1 CPU. По памяти всегда “ровно” в районе 128M memory
- приложение имеет дневной цикл по нагрузке – ночью запросов на порядки меньше, пик – днём
- максимально отказоустойчивый deployment
- минимального потребления ресурсов от этого deployment’а
