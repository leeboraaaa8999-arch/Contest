# 핸드오프: 《숨》 V6 영상 리뷰

해양공모전 영상 《숨》(120초)의 V6 컷 "성게·해녀 (0:55–1:05)" 생성 결과물을 리뷰하고, 기획안 문서를 실제 사용 값으로 갱신한 세션입니다.

## 참고 자료

- 기획안 (Claude Docs): https://claude.ai/code/artifact/118f15c4-a9c2-4eac-a260-4121bc069193
  - 제목: 《숨》 해양공모전 영상 기획안
  - 작품 개요, 최종 타임라인 콘티, 내레이션 대본, 장면별 AI 프롬프트, 제작 체크리스트, AI 사용 내역서가 들어 있음
- 영상·이미지 파일은 이 레포에 없음 (사용자 기기에 있음)
  - 1차 V6: `Haenyeo_diver_searching_barren_r__20261018102815.mp4`
  - 2차 V6: `Haenyeo_diver_floating_underwater_1080p_20261018123332.mp4`
  - 2차 V6 시작 프레임: 모래시계 안쪽 시점의 바다 사막 이미지 (양쪽 유리 테두리, 강한 빛기둥)

## 기획안상 V6 사양

- 구간: 0:55–1:05 (약 10초), "현실: 바다 사막화" 파트, N3 내레이션(0:45–1:08) 위에 깔림
- 오디오 설계: 음악 중단 → 심해 저음 → 정적
- 화면: 하얗게 굳은 바닥 + 검은 성게 떼, 작은 물고기 한 마리, 빈 망사리를 쥐고 움직이지 않는 해녀(뒷모습, 얼굴 안 보임), 차갑고 황량한 회청색 빛

## 한 일

1. **1차 V6 리뷰** (4초, 1080p, 24fps, 오디오 포함)
   - 좋음: 백화된 바닥과 성게 표현
   - 문제: 해녀가 헤엄치다 수면으로 상승해 V11 클라이맥스와 충돌, 망사리 없음, 큰 핀, 빛기둥이 화사함, 4초로 짧음, 생성 사운드 포함
   - 처음엔 기획안 없이 일반 기준으로 봐서 "태왁 없음"을 지적했으나, V6 기준에서는 태왁이 아니라 망사리가 핵심이라 정정함
2. **재생성 프롬프트 제안**: 정지 자세, 빈 망사리, 핀 없음, 빛기둥 없음, 정적 카메라를 명시한 프롬프트 작성
3. **Google Flow "비정상적인 활동이 감지되었습니다" 오류 대응**
   - 원인: 프롬프트 문제가 아니라 계정·IP 단위 차단으로 추정
   - 대응책 안내: 재시도 중단 후 대기, 네트워크 변경, 탭 완전 종료, 재로그인, 프로필의 경고 표시 확인, 다른 기기
   - 결과: 사용자가 원래 쓰던 계정으로 바꿔서 해결
   - 두 번째 업로드는 1차와 같은 파일(MD5 동일)이었음을 확인
4. **2차 V6 리뷰** (4초, 1080p, 24fps, 오디오 포함)
   - 충족: 바닥과 성게, 물고기 한 마리, 해녀 정지, 뒷모습, 핀 없음, 차가운 빛
   - 문제: 첫 0.4~0.5초에 유리 테두리와 빛기둥이 남아 있다가 급히 사라짐, 망사리 바닥에 둥근 물체가 들어 있음(비어 있지 않음), 맨발이 눈에 띔, 여전히 4초, 생성 사운드 포함
   - 0.5초 문제의 원인: 시작 프레임(빛기둥·유리 테두리)과 프롬프트(`no light rays`)가 충돌해서 생김
5. **기획안 문서 수정** (AI 사용 내역서 › 영상 › V6 행)
   - 프롬프트 원문: 실제 사용한 프롬프트로 교체 (공통 스타일 문구는 내역서 규칙대로 제외)
   - 한국어 요약: "성게만 남은 바닥, 망사리를 쥐고 멈춰 떠 있는 해녀, 멀리 물고기 한 마리"
   - 비고: "시작 프레임: 모래시계 안쪽 시점의 바다 사막 이미지(유리 테두리, 업로드). 편집에서 앞 0.5초 컷, 생성 사운드 음소거"

## 결정 사항

- 2차 V6를 채택 후보로 봄. 앞 0.5초를 자르고 음소거하면 사용 가능
- 생성 사운드는 쓰지 않음 (V11과 같은 원칙, 저작권 체크리스트 항목)
- Flow는 원래 쓰던 계정 하나로만 사용 (계정 전환이 잦으면 차단 위험)

## 실제 사용한 V6 프롬프트

```
Barren chalky white seabed covered with black sea urchins, a single small fish drifting far away, a haenyeo diver seen from behind, completely still, floating in place with head slightly lowered, holding an empty mesh net bag, no fins, face not visible, static camera, no light rays, flat cold desolate grey-blue light, cinematic, photorealistic, muted teal and green palette, soft volumetric light, subtle 35mm film grain, 16:9
```

## 남은 할 일

- [ ] 편집: 2차 V6의 앞 0.5초 자르기, 오디오 음소거
- [ ] 길이 확보 (10초 슬롯): 3.5초를 60~70% 속도로 슬로모션 + Flow 연장으로 채우기
  - 연장 프롬프트 예시: `she remains completely still, the small fish slowly swims away, static camera`
- [ ] (선택) 재생성 시 보완 문구: `completely empty mesh net bag, nothing inside`, `black neoprene diving socks`
- [ ] (선택) 재생성 시 시작 프레임 처리 중 하나 선택
  1. 시작 프레임 없이 생성
  2. 유리 테두리를 자르고 빛기둥을 어둡게 한 이미지 사용
  3. 유리를 유지하려면 `seen through the curved glass of the hourglass, glass rim visible at the edges throughout`을 추가하고 `no light rays`는 빼기
- [ ] 내역서 이미지 표에 2차 시작 프레임 이미지를 I7로 추가 (사용자에게 도구와 프롬프트 확인 필요). 이 이미지는 기획안의 I5와 다름
- [ ] 다른 계정에서 만든 I1~I6을 현재 Flow 계정에 업로드 (V5→V6→V7 키프레임 연결용)
- [ ] 재생성하면 내역서 V6 행을 최종 프롬프트로 다시 갱신
