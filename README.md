# Verification of Lorentz Covariance: LT vs. LW Potential

로렌츠 변환(Lorentz Transformation)과 Liénard-Wiechert(LW) 포텐셜이라는 두 가지 독립적인 경로를 통해 계산한 Electromagnetic filed가 동일함을 보인 프로젝트입니다.

## 🚀 Key Implementation

*   **Dual Path Verification**: 정지계 필드의 로렌츠 변환 결과와 이동하는 전하의 LW 필드 계산 결과를 직접 비교
*   **Shooting Algorithm**: 지연 시간($t_r$)을 의 해를 찾기 위해 **Shooting Algorithm**을 이용한 수치 해석 알고리즘 설계
*   **Parallel Computing**: `multiprocessing.Pool`을 활용하여 수만 개의 격자점 연산을 최적화하고, Amdahl의 법칙을 기반으로 성능 벤치마크 수행

## 📊 Results & Analysis

*   **High Precision**: $v \ll c$ 영역에서 float64 부동소수점 오차 한계($10^{-15} \sim 10^{-16}$) 수준의 정밀도로 공변성 확인
*   **Edge Case Analysis**: $v$가 광속에 인접할 때 발생하는 수치적 오차 원인(Shooting window limit 등) 분석
*   **Visual Representation**: `Plotly`를 이용한 3차원 전자기장 벡터 시각화 및 인터랙티브 상호작용 구현

---

> **💡 상세한 물리적 유도 과정, 오차 분석 그래프 및 병렬화 벤치마크 결과는 첨부된 [Verification_of _Lorentz_covariance...ppt] 파일에서 확인하실 수 있습니다.**
