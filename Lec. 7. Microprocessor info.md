
## Embedded computer
- IC - integrated circuit
	- 집적 회로는 특정 기능을 수행하는 전기 회로와 반도체 소자(주로 트랜지스터)들을 하나의 칩(Chip)으로 구현한 것이다. - single piece of silicon
	- 극소형화(miniaturization), 대량생산(mass production), 비용 절감(cost reduction)
- MCU - Microcontroller unit
	- CPU, 각종 주변장치, 메모리 등이 합쳐진 IC 회로 + 메모리 버스 등등
	- 추후에 소프트웨어적으로 개발을 진행할 수 있다.
- CPU - Cental processing unit
	- Program instruction을 실행하는 하드웨어 회로
	- instruction - 명령어 조합, 하나 또는 다수의 연산자(operand)로 이루어진다.
- PCB - printed circuit board
	- 전자 소자를 붙잡아주는 판
	- 전선이 보드에 그려져 있어서 소자의 양 전극을 연결 해줌.

## Typical embedded system software operations
- Closed-loop control
	- 계속 센서 체크 피드백 받음 -> 조절
- Sequencing
	- 처음부터 끝까지 과정(step)이 모두 설계되어 있음.
- Signal conditioning and processing
	- 다수의 센서를 통해 신호 제대로 가는지 체크 -> 올바른 신호 보내주기 위해 노이즈 걸러냄.
- Communications and networking
	- 다른 subsystems 또는 other system 이랑 소통함. 패킷 전송, 디코딩 과정 등등 (ex. 드론 무선 조종) 

## Interfaces of embeded systems
- Peripheral
	- CPU 외 주변기기 전부
- analog
	- 무한한 수
- digital
	- 유한한 수
- ADC(analog-to-digital converter)
	- 아날로그를 디지털 값으로 변환
- DAC(digital-to-analog converter)
	- 디지털을 아날로그 값으로 변환

## Concurrency - 동시 발생성
- MCU가 동시에 여러 신호를 처리해 줄 수 있다.
- 특정 기능이 추가될 수록 복잡성이 증가함
	- 하나가 추가되면 여러개가 추가되기 때문
- MCU는 concurrency를 제공한다. 
	- 한번에 여러 작업 수행 가능
	- interrupt handler - 시스템 작업에 문제가 발생했을 경우 suspend시킴
	- 