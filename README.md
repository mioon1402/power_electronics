# 🔌 Power Electronics Simulators
전력전자 도구들의 시뮬레이터

## 📦 포함된 시뮬레이터

### 1. **MOSFET 시뮬레이터 (Full Version)**
- **파일**: `mosfet_simulator.html`
- **특징**:
  - 📊 실시간 I-V 특성 곡선
  - 🎚️ Vgs, Vds 슬라이더 조절
  - 📈 여러 Vgs 값에 대한 곡선 동시 표시
  - 🎯 현재 작동점 표시
  - ⚙️ 계산된 파라미터 (Id, P, Ron, gm)
  - 🟢 작동 영역 자동 표시 (차단/선형/포화)
  - 💾 데이터 내보내기
- **용도**: 교육, 학습, 상세 분석
- **파일 크기**: ~50KB

### 2. **MOSFET 시뮬레이터 (Simple Version)**
- **파일**: `mosfet_simulator_simple.html`
- **특징**:
  - 경량 디자인 (그래프 없음)
  - 빠른 로딩
  - 블로그 사이드바 or 작은 영역에 최적
  - 기본 기능만 제공 (Vgs, Vds, Id, P, 작동 영역)
- **용도**: 빠른 확인, 제한된 공간에서의 사용
- **파일 크기**: ~5KB

## 🚀 티스토리 블로그 사용법

### 방법 1: 전체 버전 (권장)
1. `mosfet_simulator.html` 파일 다운로드
2. 티스토리 글 쓰기 → HTML/JavaScript 편집기
3. 파일의 전체 코드 복사
4. 편집기에 붙여넣기
5. 미리보기 확인 후 발행

### 방법 2: 경량 버전
1. `mosfet_simulator_simple.html` 파일 다운로드
2. 동일한 과정 반복

## 📖 상세 가이드
[MOSFET_SIMULATOR_GUIDE.md](MOSFET_SIMULATOR_GUIDE.md) 참고

## 🔧 MOSFET 모델 파라미터

기본 설정:
```
Vth (임계전압): 1.5V
Kn (트랜스컨덕턴스): 0.05
Lambda (채널 길이 변조): 0.02
```

HTML 파일 내 `mosfetParams` 객체에서 수정 가능

## 💻 기술 스택

- **HTML5**: 구조
- **CSS3**: 스타일 (그라디언트, 플렉스박스, 그리드)
- **JavaScript (Vanilla)**: 계산 및 상호작용
- **Chart.js 3.9.1** (Full 버전): 그래프 렌더링

## ✨ 주요 기능

- ✅ 실시간 MOSFET 특성 시뮬레이션
- ✅ 대화형 슬라이더 조절
- ✅ 자동 계산 (Id, P, Ron, gm)
- ✅ 작동 영역 판정 (차단/선형/포화)
- ✅ 반응형 디자인 (모바일 지원)
- ✅ 외부 라이브러리 의존성 최소화 (Chart.js만 CDN 사용)

## 📋 MOSFET 방정식

### 공식

**차단 영역 (Cutoff)**: $V_{gs} \leq V_{th}$
$$I_d = 0$$

**선형 영역 (Linear)**: $V_{gs} > V_{th}$, $V_{ds} \leq V_{gs} - V_{th}$
$$I_d = K_n \left[(V_{gs} - V_{th})V_{ds} - \frac{V_{ds}^2}{2}\right](1 + \lambda V_{ds})$$

**포화 영역 (Saturation)**: $V_{gs} > V_{th}$, $V_{ds} > V_{gs} - V_{th}$
$$I_d = \frac{K_n}{2}(V_{gs} - V_{th})^2(1 + \lambda V_{ds})$$

## 🎓 교육 활용

이 시뮬레이터는 다음 학습에 유용합니다:
- MOSFET의 I-V 특성 이해
- 에이온(On-resistance) 개념
- 트랜스컨덕턴스(gm) 학습
- 작동 영역(Region) 구분
- 전력 소비 분석

## 📱 호환성

- ✅ Chrome, Firefox, Safari, Edge
- ✅ 데스크톱, 태블릿, 모바일
- ✅ 모든 HTML 블로그 플랫폼 (Tistory, GitHub Pages, Notion 등)
- ⚠️ 온라인 연결 필요 (Chart.js CDN)

## 🔄 업데이트 계획

- [ ] PMOS 모델 추가
- [ ] 온라인/오프라인 버전
- [ ] 추가 MOSFET 모델 시뮬레이션
- [ ] 다크 모드
- [ ] 다국어 지원

## 📝 라이선스

자유롭게 수정하고 배포할 수 있습니다.

## 🐛 문제 보고

버그나 개선 사항이 있으면 이슈로 등록해주세요.

---

**버전**: 1.0  
**마지막 업데이트**: 2024년 4월 6일
