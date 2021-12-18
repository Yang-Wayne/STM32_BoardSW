# STM32_BoardSW
base Board : B-L4S5I-IOT01A  
Base SW : STM32CubeExpansion_Cloud_AWS_V2.0.0
Develop IDE : STM Cube IDE V1.5.0
we develop this project based on Base SW. the base sw can be downloaded from https://www.st.com/en/evaluation-tools/b-l4s5i-iot01a.html#tools-software

#0
Projects\B-L4S5I-IOT01A\Applications\Cloud\aws_demos\config_files 경로에 있는
aws_demo_config.h 파일에서 CONFIG_XXX_DEMO_ENABLED 라는 형태의 10개의 #define 문을 사용해서 해당 프로젝트의 동작 모드를 결정할 수 있다.(한번에 1개 모드만 Enable해야함)
이 프로젝트는 10개의 데모 동작 중에서 CONFIG_MQTT_DEMO_ENABLED 모드를 Base로 하여 개발하기 시작함

#1
Middlewares/Third_Party/amazon-freetos/demos/include 경로에 있는
aws_clientcredential.h  파일에서 
wifi ssid, password, security type , aws-core REST API , Thing name 정의해서 사용한다.
실제 코드에서 사용하는 Define 문의 이름은 아래와 같음
clientcredentialWIFI_SSID , clientcredentialWIFI_PASSWORD, clientcredentialWIFI_SECURITY, clientcredentialMQTT_BROKER_ENDPOINT , clientcredentialIOT_THING_NAME

wifi ssid, password를 공유하지 않기 위해 gitignore 에서 해당 헤더파일은 버전관리에서 제외하고 사용할 것임
