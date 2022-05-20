# RabbitMQ Tutorial

### Execute in container application docker
```bash
docker-compose up -d 
docker exec -it application bash
```

### Exercise 1
```bash
shell 1: php receive.php
shell 2: php send.php
```

### Exercise 2
```bash
shell 1: php worker.php
shell 2: php new_task.php "A very hard task which takes two seconds.."
```

### Exercise 3
```bash
shell 1: php receive_log.php > logs_from_rabbit.log
shell 2: php receive_log.php
shell 3: php emit_log.php
```

### Exercise 4
```bash
shell 1: php receive_logs_direct.php warning error > logs_from_rabbit.log
shell 2: php receive_logs_direct.php info warning error
shell 3: php emit_log_direct.php error "Run. Run. Or it will explode."
```

### Exercise 5
```bash
shell 1: php receive_logs_topic.php "#"
shell 2: php emit_log_topic.php "kern.critical" "A critical kernel error"
```

### Exercise 6
```bash
shell 1: php rpc_server.php
shell 2: php rpc_client.php
```
