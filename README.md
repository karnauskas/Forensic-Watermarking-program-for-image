# Forensic-Watermarking-program-for-image

## Development contents
* **이미지 기반의 다양한 창작물들에 대하여 불법 복제와 유통이 성행하는 현재, 기존의 워터마크 활용 방식을 확장하여 이를 추적하는데 기여하는 포렌식 워터마킹 프로그램 제작을 목표로 한다.**   

* **압축 강인성**: 워터마크가 삽입된 이미지를 고의적으로 변형을 가하여 실효성을 제거하려 하는 공격들이 존재하는데, 해당 프로젝트는 삽입된 이미지에 압축 공격을 가하는 방식에 대한 강인성을 확보한다. 일반적으로 널리 사용되는 JPEG 압축 방식을 이용한 손실 압축에도 삽입된 워터마크가 유지되는 압축 강인성을 가지도록 구현한다.

* **비가시성**: 삽입된 워터마크가 원본 이미지에 그대로 나타나는 삽입 방식과 원본 이미지에 나타나지 않는 방식으로 삽입 알고리즘을 구현할 수 있다. 해당 프로젝트는 삽입된 워터마크가 원본 이미지에 표현되지 않도록 구현하여 비가시성을 확보한다. 또한, 워터마크가 삽입된 이미지에서 워터마크를 추출하는 과정에서 원본 이미지가 필요하지 않다. 따라서, 해당 프로젝트는 blind watermarking으로 구별되어진다.

* **QR 코드**: 해당 프로젝트에서 사용되는 워터마크는 입력 받은 정보를 버전1~3의 QR 코드로 변환하여 사용한다. 삽입하고자 입력받는 데이터의 길이에 따라 최대 32x32 크기의 QR 코드를 생성하며 352bit(숫자 101, 영숫자 61, binary 42, 한자 26의 길)를 표현할 수 있다. 또한, 오류복원 단계 M을 기준으로 15%의 손상 부분을 자체적으로 복원하는 기능을 가진다. 이러한 이유로 해당 프로젝트의 워터마크로 사용된다.

 해당 프로젝트는 삽입할 데이터를 입력받고 QR 코드로 변환한 후 선택 버튼을 통해 삽입하고자 하는 원본 이미지를 선택하고 삽입 버튼으로 삽입 과정을 진행한다. 추출 버튼을 통해 워터마크가 삽입된 이미지를 선택하여 추출을 진행하여 삽입된 QR 코드를 복원하여 QR 코드 스캐너로 삽입된 정보를 확인한다.

## Development enviroment
**개발 도구**: Visual studio 2017   
**개발 언어**: C++   
**사용 라이브러리**: MFC, OpenCV   
* 삽입하고자 하는 데이터 입력, 원본 이미지 선택, 삽입, 추출의 과정을 위한 GUI 프로그램 개발을 위해 MFC 기반으로 개발한다.
* 디지털 이미지에 대한 다양한 영상처리 기술을 이용하기 위해 오픈소스 라이브러리인 OpenCV를 이용한다.

## Implement

## Result

웹 데모 버전 링크

제한사항

발전사항
