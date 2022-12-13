## 왜 배포 자동화를 시도하였는가?

---

그룹 프로젝트를 하면서 배포 테스트해보기 위해 ncloud 서버를 이용하였다. 처음 세팅을 하는 과정은 어렵지 않았지만 개발이 진행되면서 main branch에 새로운 내용이 추가되었고 해당 내용을 반영하기위해 **매번 서버에 직접 접속하여 빌드와 재실행하는 과정이 번거롭다고 느껴졌다**. 이를 해결하기 위해 Github Actions를 도입하기로 했고 서버에서 일어나는 과정들을 자동화해보기로 하였다.

## 배포 자동화 - CI/CD는 무엇인가?

---

- CI(Continuous Integration)은 Build와 Test 과정을 지속적으로 제공함으로써 프로그램의 에러를 줄이고 품질을 유지하게 해준다.
- CD(Continuous Delivery & Continuous Deploy)는 Deploy 과정을 지속적으로 제공하는 것으로 개발자 단계의 산출물을 고객이 사용가능한 환경까지 자동으로 배포하는 과정이라고 할 수 있다.

이중 배포 자동화는 Continuous Deploy에 해당된다고 할 수 있다.

## 왜 Github Actions를 사용하게 되었는가?

---

> 빌드, 테스트 및 배포 파이프라인을 자동화할 수 있는 CI/CD(연속 통합 및 지속적인 업데이트) 플랫폼 - Github Docs
> 

[깃허브 문서](https://docs.github.com/ko)에 나와있는 것처럼 대표적인 CI/CD 도구이다. 

그 중에서 Github Actions는 Github와 연관성이 있어서 작업에 접근하기가 좋을 것이라고 생각했고 기타 프로그램이나 사전 작업 없이 YAML 파일 하나만으로 작성할 수 있어서 사용하게 되었다.

또한 추후에 다른 사용자들이 제공하는 유용한 기능들을 추가하여 사용할 수 있다는 점이 있었다.

[https://github.com/sdras/awesome-actions](https://github.com/sdras/awesome-actions)

(미완성..)

## Reference

- 트러블슈팅

[https://github.com/appleboy/ssh-action/issues/21](https://github.com/appleboy/ssh-action/issues/21)

[ssh 를 사용하여 배포시 서버측의 environment 를 불러오지 못하는 문제 (github action)](https://epicarts.tistory.com/160)

- 참고 자료

[[GitHub Action Learning] #1 GitHub Actions 소개](https://callmemaru.com/posts/github-actions-learning-1/)

- docs

[Understanding GitHub Actions - GitHub Docs](https://docs.github.com/ko/actions/learn-github-actions/understanding-github-actions)

- Github Actions 작동방식

[https://tech.kakao.com/2022/05/06/github-actions/](https://tech.kakao.com/2022/05/06/github-actions/)