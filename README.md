# ⚡ 전력량계량기 OCR프로젝트 Android

## 현 Repository는 Android 구현부에 해당됩니다. 

## 프로젝트 전체 README는 Server Repository에 작성되어 있으므로 아래 링크를 클릭해주세요.

## [👉Server Repository 로 이동👈](https://github.com/yujapie/ElectricityOCRServer)

- **⚡ 전력량계량기 OCR프로젝트**
  - 📁Repository 구조
  - 📌프로젝트 개요
  - 🕑개발 기간
  - 🛠프로젝트 구조
  - ✅분석 환경 및 도구
- **⚙ Server 구현**
  - 전처리 및 OCR 모델
  - DB 구축
  - Server 구현(Flask)
- **📱 Android 구현**
- **✨ 애플리케이션 실행영상**


## 📁Repository 구조

```
ElectricityMeterOCR
├── 📁java/com/lfin/electricitymeterocr
|	├── 📁DTO
|	|	├── 📃ElectricityMeterDTO.java					# 전력량계량기 DTO
|	|	├── 📃ElectricityPreprocessingDTO.java                          # 전력량계량기 이미지전처리 DTO
|	|	└── 📃ModemDTO.java						# 모뎀 DTO
|	|
|	├── 📃BarcodeDetectorActivity.java					# 바코드인식처리
|	├── 📃CameraActivity.java						# 카메라 촬영 전력량계량기 등록
|	├── 📃Common.java							# 자주사용되는 공통변수 저장 클래스
|	├── 📃GalleryActivity.java						# 갤러리 이미지선택을 이용한 전력량계량기 등록
|	├── 📃ListAdapter.java							# 조회화면의 ListAdapter
|	├── 📃MainActivity.java							# 메인화면 Activity
|	├── 📃MeterInfoActivity.java						# 조회화면 Activity
|	├── 📃MeterInfoDetailActivity.java					# 상세화면 Activity
|	└── 📃ViewPagerAdapter.java						# 상세화면의 이미지슬라이드 설정Adapter
|
└── 📁res
	├── 📃activity_barcode_detector.xml					# 모뎀 바코드 화면
	├── 📃activity_gallery.xml						# 갤러리 이미지 텍스트인식화면
	├── 📃activity_main.xml							# 메인화면
	├── 📃activity_meter_camera.xml						# 촬영 이미지 텍스트인식화면
	├── 📃activity_meter_info.xml						# 조회화면
	├── 📃activity_meter_info_detail.xml					# 상세화면
	├── 📃item_cell.xml							# 조회화면의 item
	└── 📃item_viewpager.xml						# 상세화면의 이미지슬라이드
```



## 추가된 라이브러리
- 이미지 슬라이드를 위한 라이브러리설정
```implementation "androidx.viewpager2:viewpager2:1.0.0"```

- 바코드인식 라이브러리
```implementation 'com.google.android.gms:play-services-vision:11.0.2'```
