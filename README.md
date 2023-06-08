# PX4_Parameters_Doc
PX4 Open Source 기반 멀티콥터 개발 과정에서 확인되는 Parameter 특징 및 사용법 등을 서술한다.

## 초기 설정 단계

### MAV_0_CONFIG, MAV_1_CONFIG, MAV_2CONFIG
*Mavlink 프로토콜을 전송할 포트를 결정한다. Default PX4 Firmware에서는 MAV_0_CONFIG만 TELEM1에 할당되어 있으므로,
*Companion PC나 Telemetry 추가 장착을 통해 MAVLink를 여러군데서 사영하기 위해서는 MAV_1_CONFIG 또는 MAV_2_CONFIG 를 활성화 해주어야
*해당 포트의 다른 파라미터들이 활성화된다.
*PX4 Firmware rev 1.11.* 버전에서 MAV_0_CONFIG 만 보이는 증상 발생

### SYS_CTRL_ALLOC
*QGroundControl에서 Airframe 할당 후 Motor설정 시에 이 파라미터를 Enabled로 설정한다.  
*Motor탭 -> Actuators탭으로 변경되며 상세 설정을 할 수 있음.  
*<Motor탭>*  
![SYS_CTRL_ALLOC_disabled](https://user-images.githubusercontent.com/48579140/204711812-4da3a039-712d-4347-b043-616e334d4d84.png)  
*<Actuators탭>*   
![SYS_CTRL_ALLOC_enabled](https://user-images.githubusercontent.com/48579140/204712062-300a1ac0-c867-49c8-b95f-d55c8f2fd533.png)  
*Flight Controller SD카드의 /etc/config.txt를 통한 Parameter 변경 적용에 영향 미침. (22.11.30 기준)  
*PX4 Firmware rev 1.13.0beta 기준 해당 파라미터 보이지 않는 버그 존재.  
