# gimbal camera parsing 코드에서 buffer에 넘겨진 데이터가 제대로 안받아지는 현상

###  <해결> buffer에 받을때는 무조건 데이터 하나씩 받아서 넘기기 때문에 
###    HAL_UART_Receive_IT(통신할 huart,buffer,1); 로 설정해야 함.
###    또한 데이터가 너무 많기 때문에 링버퍼를 이용해야 함. 이때 링버퍼는 원형 queue임.
    
###



