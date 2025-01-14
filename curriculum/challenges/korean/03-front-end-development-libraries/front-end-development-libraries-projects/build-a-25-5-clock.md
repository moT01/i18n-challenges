---
id: bd7158d8c442eddfaeb5bd0f
title: 25 + 5 시계 만들기
challengeType: 3
forumTopicId: 301373
dashedName: build-a-25--5-clock
---

# --description--

**Note:** **React 18 has known incompatibilities with the tests for this project (see [issue](https://github.com/freeCodeCamp/freeCodeCamp/issues/45922))**

** 목표:**이 앱을 만들어서 이와 유사한 기능을 제공하세요. <a href="https://25--5-clock.freecodecamp.rocks" target="_blank" rel="noopener noreferrer nofollow">https://25--5-clock.freecodecamp.rocks</a>.

아래 사용자 스토리를 만족시키고 모든 테스트를 통과하시오. 필요한 라이브러리나 API를 사용하시오. 자신만의 개성을 담아 디자인을 꾸며보세요.

이 프로젝트를 완료하기 위해 HTML, JavaScript, CSS, Bootstrap, SASS, React, Redux 및 jQuery를 혼합하여 사용할 수 있습니다. 이 섹션은 프론트엔드 프레임워크를 학습하는 것이 목적이기 때문에 (React 같은) 프론트엔드 프레임워크를 사용해야 합니다. 위에 나열된 기술만 사용하여 이 프로젝트를 완료하는 것이 권장되고 이외의 기술을 사용할 경우 문제가 있을 수 있습니다. Angular 및 Vue와 같은 다른 프론트엔드 프레임워크를 지원할 예정이지만 현재는 지원되지 않습니다. 이 프로젝트에 제안된 기술 스택을 사용하는 모든 이슈 보고서를 수용하고 문제를 해결하겠습니다. 즐거운 코딩하세요!

**유저 스토리 #1:** 문자열을 포함하는 `id="break-label"` 요소를 볼 수 있습니다(예: "휴식 시간").

**유저 스토리 #2:** 문자열을 포함하는 `id="session-label"` 요소를 볼 수 있습니다(예: "세션 길이").

**유저 스토리 #3:** 두 개의 클릭 가능한 요소를 볼 수 있습니다. 해당 ID는 `id="break-decrement"` 및 `id="session-decrement"`입니다.

**유저 스토리 #4:** 두 개의 클릭 가능한 요소를 볼 수 있습니다. 이 요소들의 ID는 `id="break-increment"` 및 `id="session-increment"`입니다.

**유저 스토리 #5:** 기본적으로(로드될 때) 값이 5로 표시되는 `id="break-length"`를 가진 요소를 볼 수 있습니다.

**유저 스토리 #6:** 기본적으로 값이 25로 표시되는 `id="session-length"`를 가진 요소를 볼 수 있습니다.

**유저 스토리 #7:** 세션이 초기화되었음을 나타내는 문자열을 포함하는 `id="timer-label"`를 가진 요소를 볼 수 있습니다(예: "세션").

**유저 스토리 #8:** `id="time-left"`를 가진 요소를 볼 수 있습니다. 주의: 일시 중지되었든 실행 중이든, 이 항목의 값은 항상 `mm:ss` 형식(예: 25:00)으로 표시되어야 합니다.

**유저 스토리 #9:** `id="start_stop"`를 가진 클릭 가능한 요소를 볼 수 있습니다.

**유저 스토리 #10:** `id="reset"`을 가진 클릭 가능한 요소를 볼 수 있습니다.

**유저 스토리 #11:** `reset`의 ID를 가진 요소를 클릭할 때 실행 중인 타이머가 있다면 정지되어야 하고, `id="break-length"` 내의 값은 `5`로 되돌아가야 하며, `id="session-length"` 내의 값은 25로 되돌아가야 하고, `id="time-left"` 내의 요소는 기본 상태로 재설정되어야 합니다.

**유저 스토리 #12:** `break-decrement`의 ID를 가진 요소를 클릭할 때 `id="break-length"` 내의 값이 1 만큼 감소하고 업데이트된 값을 볼 수 있어야 합니다.

**유저 스토리 #13:** `break-increment`의 ID를 가진 요소를 클릭할 때 `id="break-length"` 내의 값이 1 만큼 증가하고 업데이트된 값을 볼 수 있어야 합니다.

**유저 스토리 #14:** `session-decrement`의 ID를 가진 요소를 클릭할 때 `id="session-length"` 내의 값이 1 만큼 감소하고 업데이트된 값을 볼 수 있어야 합니다.

**유저 스토리 #15:** `session-increment`의 ID를 가진 요소를 클릭할 때 `id="session-length"` 내의 값이 1 만큼 증가하고 업데이트된 값을 볼 수 있어야 합니다.

**유저 스토리 #16:** 세션 또는 휴식 길이를 &lt;= 0으로 설정할 수 없어야 합니다.

**유저 스토리 #17:** 세션 또는 휴식 길이를 60 > 로 설정할 수 없어야 합니다.

**유저 스토리 #18:** 처음으로 `id="start_stop"`을 가진 요소를 클릭하면 타이머는 현재 `id="session-length"`에 표시된 값에서 시작되어야 합니다. 값이 원래 값 25에서 증가하거나 감소한 경우에도 해당합니다.

**유저 스토리 #19:** 타이머가 실행 중인 경우 `time-left`의 ID를 가진 요소는 `mm:ss` 형식으로 남은 시간을 표시해야 합니다(1 감소하고 1000ms마다 표시를 업데이트합니다).

**유저 스토리 #20:** 타이머가 실행 중인 상태에서 `id="start_stop"`을 가진 요소를 클릭하면 카운트다운이 일시 중지되어야 합니다.

**유저 스토리 #21:** 타이머가 일시 중지된 상태에서 `id="start_stop"`을 가진 요소를 클릭하면 카운트다운이 일시 중지된 지점에서부터 다시 실행되어야 합니다.

**유저 스토리 #22:** 세션 카운트다운이 0에 도달하고 (참고: 타이머는 반드시 00:00에 도달해야 함) 새로운 카운트다운이 시작되면 `timer-label`의 ID를 가진 요소는 휴식 시간이 시작되었음을 나타내는 문자열을 표시해야 합니다.

**유저 스토리 #23:** 세션 카운트다운이 0에 도달하면 (참고: 타이머는 반드시 00:00에 도달해야 함) 새로운 휴식 카운트다운이 `id="break-length"` 요소에 표시된 값에서 시작되어야 합니다.

**유저 스토리 #24:** 휴식 카운트다운이 0에 도달하고 (참고: 타이머는 반드시 00:00에 도달해야 함) 새로운 카운트다운이 시작되면 `timer-label`의 ID를 가진 요소는 세션이 시작되었음을 나타내는 문자열을 표시해야 합니다.

**유저 스토리 #25:** 휴식 카운트다운이 0에 도달하면 (참고: 타이머는 반드시 00:00에 도달해야 함) `id="session-length"`요소에 표시된 값에서 카운트다운이 시작되어야 합니다.

**유저 스토리 #26:** 카운트다운이 0에 도달하면 (참고: 타이머는 반드시 00:00에 도달해야 함) 시간이 다 되었다는 것을 나타내는 소리가 재생되어야 합니다. 이는 HTML5 `audio` 태그를 활용하고 해당 `id="beep"`가 있어야 합니다.

**유저 스토리 #27:** `id="beep"`를 가진 오디오 요소는 1초 이상이어야 합니다.

**유저 스토리 #28:** `reset`의 ID를 가진 요소를 클릭하면 `beep`의 ID를 가진 오디오 요소가 재생을 중지하고 처음으로 되감아져야 합니다.

이 프로젝트를 <a href='https://codepen.io/pen?template=MJjpwO' target='_blank' rel="noopener noreferrer nofollow">이 CodePen 템플릿</a>을 사용하여 빌드하고 `Save`를 클릭하여 자체 펜을 만들 수 있습니다. If you prefer to use another environment, then put this `<script>` tag into the body of your `index.html` file: `<script src="https://cdn.freecodecamp.org/testable-projects-fcc/v1/bundle.js"></script>`

완료되면 모든 테스트가 통과되는 작동 프로젝트의 URL을 제출하십시오.

# --solutions--

```js
// solution required
```
