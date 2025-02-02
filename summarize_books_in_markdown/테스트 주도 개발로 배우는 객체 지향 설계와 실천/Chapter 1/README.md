# 🌈 Chapter 1: 테스트 주도 개발의 핵심은 무엇인가?

## 📚 학습 과정으로서의 소프트웨어 개발
- 프로젝트가 성공을 거두려면 거기에 관련된 사람들이 달성해야 할 바가 무엇인지를 이해하고 그 과정에서 잘못 이해하고 있는 바를 식별하고 해결하고자 협업해야 한다.
- 불확실한 변화를 예측하려면 경험이 늘어남에 따라 불확실성을 해결하는 데 도움이 될 프로세스가 필요하다.

## 📚 피드백은 가장 기본적인 도구다
- 팀에는 반복적인 활동 주기가 필요하다. 각 주기마다 새로운 기능을 추가하고 이미 완료한 작업의 양과 질에 관한 피드백을 받은다.
- 팀원들은 작업을 타임 박스로 나누고, 이 안에서 되도록 많은 기능을 분석, 설계, 구현, 배포한다.
- 완료된 작업을 각 주기마다 특정 종류의 환경에 배포하는 일은 아주 중요하다. 그들은 실제 진행 사황을 측정하고, 오류를 탐지하고 수정하며, 지금까지 배운 바에 따라 현재 계획을 조정할 수 있다. **배포하지 않고는 피드백이 완전해지지 않는다.**
- 각 피드백 고리는 시스템과 개발 프로세스의 다양한 측면을 다룬다. 안쪽 고리는 기술적 세부 사항에 좀 더 집중한다. 바깥쪽 고리는 조직과 팀에 좀 더 집중한다.
- 프로젝트의 어떠한 측면에 대해서도 피드백을 일찍 받을수록 좋다.

## 📚 변화를 돕는 실천법
- 시스템 규모를 믿을 수 있는 방식으로 키우고, 늘 일어나는 예상치 못한 변하에 대처하고 싶다면 두 가지 기술적인 토대가 필요하다.
  1. 회귀 오류를 잡아줄 꾸준한 테스트가 필요하다. 수동 테스트를 자주 하는 것은 비실용적이므로 구축과 배포, 시스템 버전 변경에 드는 비용을 줄이려면 되도록 테스트를 자동화해야 한다.
  2. 다음으로 코드를 가능한 한 단순하게 유지해야 하는데, 그렇게 하면 코드를 이해하고 수정하기가 더 쉽다. 코드의 설계를 개선하고 단순화하고, 중복을 제거하며, 코드가 명확하게 자신의 역할을 표현하게끔 코드를 사용할 때마다 꾸준히 코드를 리팩터링해야 한다.
- 테스트 주도 개발은 코드를 작성하기 전에 테스트를 작성한다. 작업을 완료한 후 작업 결과를 검증하려고 테스트를 사용하는 것이 아니라 TDD에서는 테스트를 설계 활동으로 바꾼다. 테스트를 사용해 코드에서 하고 싶은 바에 관한 생ㅇ각을 명확하게 한다.
- 개발 과정 내내 테스트를 작성한다면 변경에 대한 자신감을 주는 자동화된 회귀 테스트라는 안전망을 구축할 수 있다.

## 📚 테스트 주도 개발 간단 정리
- TDD의 핵심 주기는 테스트를 작성하고 해당 테스트가 동작하게 만들 코드를 작성한다. 코드를 가급적 테스트한 기능의 단순한 구현으로 리팩터링한다. 이러한 과정을 반복한다.
- 다음은 테스트를 작성했을 때의 장점이다.
  - 다음 작업에 대한 인수 조건이 명확해진다.
  - 느슨하게 결합된 구성 요소를 작성할 수 있게 되어 격리된 상태에서, 더 높은 수준으로, 모두 결합된 상태로 구성 요소를 손쉽게 테스트할 수 있다.
  - 코드가 하는 일에 대한 실행 가능한 설명이 더해진다.
  - 완전한 회구 스위트가 늘어난다.
- 다음은 테스트를 실행했을 때의 장점이다.
  - 콘텍스트를 선명하게 인지하는 동안 오류를 탐지한다.
  - 언제 작업이 충분히 완료됐는지 알게 되어 과도한 최적화를 하거나 불필요한 기능을 더하지 않게 된다.

> 실패하는 테스트 없이는 새 기능을 작성하지 말라.

## 📚 좀 더 큰 그림
- 어떤 기능을 구현할 때 인수 테스트를 작성하는 것으로 시작한다. 인수 테스트는 그것이 실패하는 동안 시스템이 아직까지 그 기능을 구현하지 않는다는 사실을 보여준다. 인수 테스트가 통과하면 작업이 끝난다.
- 인수 테스트는 보통 현재 작업 중인 인수 테스트와 작업을 마친 기능에 대한 인수 테스트를 구분한다.
- 단윈 테스트는 코드 품질을 유지하는 데 도움이 되고 작성한 후에는 바로 통화해야 한다. 실패하는 단위 테스트는 소스 저장소에 절대 커밋해서는 안 된다.

## 📚 전 구간 테스트
- 전 구간 테스트는 외부에서 유입되는 시스템하고만 상호 작용한다.
- 이미 안정적인 전 구간 테스트를 확보했고 개발 속도 향상이 정말 필요하지 않다면 시스템 내부 객체를 시험하기만 하는 인수 테스트를 피하려고 노력한다.
- 전 구간 테스트에서 시스템과 해당 시스템을 구축하고 배포하는 프로세스를 모두 시험하는 방식을 선호한다.
- 시스템은 인수 테스트가 모두 통과할 때 배포할 수 있는데, 인수 테스트가 모든 것이 동작하고 있다는 충분한 자신감을 불어넣어주기 때문이다.

## 📚 테스트의 수준
- 인수 테스트: 전체 시스템이 동작하는가?
- 통합 테스트: 변경할 수 없는 코드를 대상으로 코드가 동작하는가?
- 단위 테스트: 객체가 제대로 동작하는가? 객체를 이용하기가 편리한가?
- 인수 테스트의 *역할* 구현은 전 구간 테스트를 작성하는 것으로, 알다시피 전 구간 테스트는 가능한 한 전 구간에 걸쳐 이뤄져야 한다.
- 일부 코드가 변경할 수 없는 팀 바깥의 코드를 어떻게 이용할지 검사하는 테스트를 가리킬 때 통합 테스트라는 용어를 사용한다. 이러한 코드는 공용 프레임워크나 조직 내 다른 팀에서 개발한 라이브러리일지도 모른다. 통합 테스트가 탁월한 부분은 서드 파티 코드를 대상으로 만든 추상화가 기대한 대로 동작하는지 확인하는 데 있다.
- 단위 테스트 기법은 프로그래밍 스타일에 따라 달라지며, 따라서 그러한 접근법을 취하는 모든 시스템에 공통으로 적용된다.

## 📚 외부 품질과 내부 품질
- 외부 품질은 시스템이 고객과 사용자의 요구를 얼마나 잘 충족하는가이며(기능, 가용성, 신뢰성 등), 내부 품질은 시스템이 개발자와 관리자의 요구를 얼마나 잘 충족하는가이다.(이해하기 쉬운가, 변경하기 쉬운가 등)
- 외부 품질은 보통 계약의 일부다.
- 내부 품질은 달성하기가 더 어려울 떄가 있다. 내부 품질은ㅇ 거듭되고 예상할 수 없는 변경에 대처하게 하는 것이다. 예상 가능한 상태로 바꿀 수 있게 만드는 것이다.
- 전 구간 테스트를 실행해보면 시스템의 외부 품질을 알 수 있으며, 전 구간 테스트를 작성하면 도메인을 얼마나 잘 이해하는지 알 수 있다.
- 단위 테스트를 작성하면 코드 품질에 관한 피드백을 상당히 많이 얻을 수 있으며, 단위 테스트를 수행하면 깨진 클래스가 없는지 파악할 수 있다.
- 철저한 단위 테스트는 내부 품질을 개선하는 데 도움이 되는데, 단위를 테스트하려면 테스트 픽스처에서 해당 단위를 시스템 바깥에서 실행할 수 있게 구조하해야 하기 때문이다.
- 클래스를 단위 테스트하려면 클래스가 대체할 수 있는 명시적인 의존성과 호출하고 검증할 수 있는 명확한 책임을 지녀야 한다. 즉, 반드시 느슨하게 결합돼야 하고 응집력이 높아야 한다. 다른 말로는 잘 설계돼 있어야 한다.
- 설계를 잘못하면 단위 테스트를 작성하거나 이해하기 어렵다는 사실을 알게 됐다. 따라서 테스트를 먼저 작성하면 설계에 관한 귀중하고 즉각적인 피드백을 얻을 수 있다.
