# NDZ36-Playbook

Playbook для установки java elastic & kibana

К Сожалению проверка роли elastic падает с ошибками:

```
TASK [Check Elastic version] ***************************************************
fatal: [centos8]: FAILED! => {"changed": false, "cmd": "/opt/elastic/7.10.1/bin/elasticsearch --version", "delta": "0:00:02.561320", "end": "2021-02-02 09:34:27.361774", "msg": "non-zero return code", "rc": -9, "start": "2021-02-02 09:34:24.800454", "stderr": "", "stderr_lines": [], "stdout": "", "stdout_lines": []}
fatal: [ubuntu]: FAILED! => {"changed": false, "cmd": "/opt/elastic/7.10.1/bin/elasticsearch --version", "delta": "0:00:03.795555", "end": "2021-02-02 09:34:28.502314", "msg": "non-zero return code", "rc": 137, "start": "2021-02-02 09:34:24.706759", "stderr": "Killed", "stderr_lines": ["Killed"], "stdout": "", "stdout_lines": []}
ok: [centos7]
```

Каждый раз падает на разном контейнере, из-за чего падает не разобрался. Если запускать молекулу без удаления контейнеров, а потом войти в контейнер и выполнить команду вручную все проходит нормально