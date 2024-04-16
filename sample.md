## シート名は「週数-YYYYMMDD」の形で入力すること  
例）1-20240401  
コピペして使ってください  

### シート名をとってくる関数  
=CONCATENATE("第",LEFT(RIGHT(CELL("filename"),LEN(CELL("filename"))-FIND("]",CELL("filename"))),1),"週")		

### シート名から日付をとってくる関数  
=DATE(MID(RIGHT(CELL("filename"),8),1,4),MID(RIGHT(CELL("filename"),8),5,2),RIGHT(CELL("filename"),2))  

### 表から該当データの参照（※キャプチャ参照）
=IFERROR(IFS($B4=$I$3,VLOOKUP(C$3,$H:$M,2,),$B4=$J$3,VLOOKUP(C$3,$H:$M,3,),$B4=$K$3,VLOOKUP(C$3,$H:$M,4,),$B4=$L$3,VLOOKUP(C$3,$H:$M,5,),$B4=$M$3,VLOOKUP(C$3,$H:$M,6,),OR($B4="土",$B4="日"),""),"")
