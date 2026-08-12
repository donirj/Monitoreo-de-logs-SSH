<!-- 
-Analizar, filtrar e identificar archivo auth.log los mensajes con el siguiente formato:
-"Invalid user tong from 202.152.201.166 port 50052"
-No repetir mensajes
-Tecnologías: Linux, grep, awk
 -->

<!-- 
    
1. Para filtrar logs con "Invalid user": 

 grep "Invalid user" auth.log 

2. Para filtrar sin repeticiones "Invalid user: user, from IP: {IP}, port {port} "

 grep "Invalid user" auth.log | awk '{print "Invalid user: " $6 ", from IP: " $8 ", port " $10}' | uniq

 -->
