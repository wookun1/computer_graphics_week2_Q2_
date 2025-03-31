
![image](https://github.com/user-attachments/assets/bc0210bd-e19b-4663-a55f-ded87746280c)


# 과제 2 - Q2: 감마 보정 (Gamma Correction)

 목표
렌더링된 장면에 감마 보정(Gamma Correction, γ = 2.2)을 적용하여  
화면상에 더 자연스럽고 사실적인 색상과 밝기를 표현합니다.

---

 구현 내용

- `Phong Shading` 결과에 대해 감마 보정 적용
- 감마 보정 공식:

  ```cpp
  vec3 applyGammaCorrection(const vec3& color) {
      return vec3(pow(color.r, 1.0 / 2.2),
                  pow(color.g, 1.0 / 2.2),
                  pow(color.b, 1.0 / 2.2));
  }
항목	감마 보정 전 (Q1)	감마 보정 후 (Q2)
색감	어둡고 탁함	밝고 자연스러움
명암	급격한 변화	부드러운 그라데이션
현실감	인공적 느낌	카메라로 촬영한 듯한 자연스러움
특히, 그림자나 반사광이 있는 부분에서 감마 보정 효과가 눈에 띕니다.
