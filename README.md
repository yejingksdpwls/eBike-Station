> # eBike-Station
2024.07.03 ~ 2024.08.25  
천안시 전기자전거 충전소 및 대여소 최적의 설치 위치 선정 프로젝트  
> ## 🖥 프로젝트 요약
- 천안시 내 전기자전거 충전소 및 대여소의 최적 설치 위치 선정 프로젝트
- 천안시 데이터를 활용한 현황 시각화 및 분석 진행
- MCLP 모델을 사용한 최적 위치 선정

> ## 🛠️ Tools
> <img src="https://img.shields.io/badge/Python-3776AB?logo=Python&logoColor=white"> <img src="https://img.shields.io/badge/QGIS-3A6A3A?logo=QGIS&logoColor=white">

<br/>

> ## 🧱 MCLP
![image](https://github.com/user-attachments/assets/a4104cd7-6dfc-4222-8fb0-342f502bfd12)
## **📌 모델 정의**
### **🔹 목적 함수**
$$
\text{Maximize} \sum_{i \in I} w_i y_i
$$
- **목표:** 배치된 시설로 커버되는 **수요 포인트의 가중치 합을 최대화**하는 것  
- \( w_i \) : 수요 포인트 \( i \) 의 서비스 수요량  
- \( y_i \) : 수요 포인트 \( i \) 가 최소 한 개의 시설에 의해 커버되면 1, 그렇지 않으면 0  

---

### **🔹 제약 조건**
#### **1️⃣ 제약조건 1: 시설 설치 개수 제한**  
$$
\sum_{j \in J} x_j = K
$$
- 총 **\( K \)개의 시설만 설치 가능**하도록 제한  

#### **2️⃣ 제약조건 2: 이진 변수 조건 (시설 설치 여부)**  
$$
x_j \in \{0,1\}, \forall j \in J
$$
- \( x_j = 1 \)이면 배치포인트 \( j \)에 시설을 설치  
- \( x_j = 0 \)이면 시설을 설치하지 않음  

#### **3️⃣ 제약조건 3: 수요 포인트 커버 여부**  
$$
y_i \in \{0,1\}, \forall i \in I
$$
- \( y_i = 1 \)이면 수요점 \( i \)가 최소 한 개의 시설로부터 서비스 받음  
- \( y_i = 0 \)이면 서비스 받지 않음  
<br/>

> ## 📊Dashboard
![Dashboard](Dashboard/Dashboard.jpg)
