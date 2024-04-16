## シート名は「週数-YYYYMMDD」の形で入力すること  
例）1-20240401  
コピペして使ってください  

### シート名をとってくる関数  
=CONCATENATE("第",LEFT(RIGHT(CELL("filename"),LEN(CELL("filename"))-FIND("]",CELL("filename"))),1),"週")		

### シート名から日付をとってくる関数  
=DATE(MID(RIGHT(CELL("filename"),8),1,4),MID(RIGHT(CELL("filename"),8),5,2),RIGHT(CELL("filename"),2))  

### 
