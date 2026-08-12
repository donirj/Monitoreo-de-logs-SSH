<!-- 
-Script Bash para analizar /var/log/auth.log y detectar intentos fallidos de autenticación.
-Extracción de IP y usuario mediante grep, awk y tail.
-Notificaciones push mediante ntfy.sh.
-Automatización de ejecución cada 5 minutos mediante cron.
-Tecnologías: Linux, Bash, Cron, SSH, curl, grep, awk.kc
 -->

<!-- 
    
1. Para filtrar logs con "Invalid user": 

 grep "Invalid user" auth.log 

2. Para filtrar sin repeticiones "Invalid user: user, from IP: {IP}, port {port} "

 grep "Invalid user" auth.log | awk '{print "Invalid user: " $6 ", from IP: " $8 ", port " $10}' | uniq

 -->
