## Contents

    

1 설명

    

1.1 특징

[[편집](http://rigvedawiki.net/r1/wiki.php/DownBooRu?action=edit&section=1)]

## 1 설명 ¶

  

국내 티스토리 블로거 빵집상인이 제작한 겔부루 계열 다운로드 프로그램.  
여타 외국 다운프로그램들과 달리 일일이 이미지를 선택하는 방식이 아닌, 태그에 묶여있는 모든 이미지들을 한꺼번에 다운로드하는 방식을 취하고
있다. 겔부루와 같은 엔진을 쓰는 사이트(safebooru 등)이여도 가능하다.

  

중복검색,제외 검색어 등을 지원하고 있으며`[1]` 2012년 8월 업데이트된 1.5.1 베타버젼에서는 동시 다운로드 개수(thread)도
지원하고 있다.`[2]`

  

프로그램에 있는 버그 대부분은 1.5.1 베타의 멀티스레딩 기능을 업데이트하면서 나온 버그이다. 릴레이 다운로딩 클래스 하나만 고치면 되는데
제작자가 멀티스레딩환경엔 익숙치 못하여서 계속 못고치고 있다고 한다.  
MFC의 유명한 AFX 멀티스레드 버그 중 하나가 새로 생성된 AfxThread에서 메인프레임에 접근하면 프로그램이 크래시되는 버그이다. 이
문제를 해결하기 위해서 소스코드는 [싱글톤](%EC%8B%B1%EA%B8%80%ED%86%A4.md) 등과 여러 가지 더러운 편법으로
도배되어 있다.

[[편집](http://rigvedawiki.net/r1/wiki.php/DownBooRu?action=edit&section=2)]

### 1.1 특징 ¶

  

  * **속도**(1.5.1 베타버젼)
제작자 본인도 속도로 승부한다라는 말을 했을 정도로 겔부루의 서버만 안정되어있다면 수백개의 이미지도 수분 이내로 받아지는 엄청난 속도를
자랑한다. 다만, 서버가 불안정하면 스레드를 높게 설정해도 속도가 잘 나오지 않는다.

  

  * 오류(...)
이미지의 수가 많을수록, 스레드가 높을 수록 속도와 비례해 파일 자체가 누락되거나 0kb의 정체불명의 빈 이미지 파일이 다운받아지기도 한다.
혹은 이미지가 깨진 채로 있는 파일도 있다.(...)

`\----`

  * `[1]` 이것은 겔부루 자체의 기능이다. (keyword1 keyword2)는 and 검색어이며, (keyword1 - keyword2)면 keyword1의 검색결과 중 keyword2를 제외한 결과를 표시한다.
  * `[2]` 다만 개수를 정할 때 주의를 해야하는 것이 태그에 묶여진 이미지가 10개 정도인데 16쓰레드를 지정할 경우 오류가 나서 끝없이 조각파일, 공파일을 다운로드하는 현상이 발생한다.
