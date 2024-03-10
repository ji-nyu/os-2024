## CPU 가상화 마무리 대화

> **교수:** 자, 이제 CPU 가상화에 대해 얼마나 배웠는지 알아볼까?

**학생:** (교수의 의도를 간파하며) 교수님은 제가 "예"라고 대답하기를 원하시는 것 같네요.

> **교수:** (웃으며) 그건 사실이지만, 진심으로 궁금하기도 하다. 그럼, 나에게 쉴 틈을 좀 주지 않겠나?

**학생:** 네, 물론입니다. 제가 배운 내용을 말씀드릴게요. 우선 CPU 가상화 방법에 대해 알게 되었고, 트랩, 인터럽트, 프로세스 전환 등 중요한 기법들을 이해하게 되었어요.

> **교수:** 좋아, 잘 알았네!

**학생:** 하지만 이 모든 상호작용은 다소 복잡해 보이네요. 어떻게 더 자세히 알 수 있을까요?

> **교수:** 좋은 질문이야. 실제로 해보는 것만큼 좋은 방법은 없지. 단순히 책만 읽는 것보다 직접 프로젝트를 해보면 훨씬 더 많이 이해할 수 있을거야.

**학생:** 네, 그럴 것 같아요. 그런데 운영체제의 철학에 대해서는 어떻게 생각하시나요?

**학생:** 운영체제는 꽤 편집증적인 성향을 가지고 있는 것 같아요. 컴퓨터를 장악하고 싶어하는 의도가 느껴지고, 프로그램의 효율적인 실행을 원하면서도 악성 프로세스를 막고 싶어하는 모습이 보이죠. 마치 편집증 환자가 승리한 것 같아요. 그래서 우리는 운영체제를 자원 관리자라고 부르는 것 같습니다.

> **교수:** 그렇게 말할 수도 있겠군. 자네는 이제 정리를 시작하는 것 같아 보이는데, 매우 좋아!

**학생:** 감사합니다. 그럼 정책에 대해서는 어떻게 생각하시나요?

**학생:** 스케줄링 정책은 이해하기 쉬웠지만, 동시에 SJF와 RR처럼 동작하는 스케줄러를 구축하는 것은 어려울 것 같아요. MLFQ는 꽤 깔끔했지만, 실제로 구현하는 것은 쉽지 않을 것 같습니다.

> **교수:** 사실이야. 어떤 스케줄러를 사용해야 하는지에 대한 논란은 오늘날까지 이어지고 있다네. 예를 들어, Linux의 CFS, BFS와 O(1) 스케줄러 사이의 다툼을 한 번 보게.

**학생:** 정말 정답이 있는 건가요?

> **교수:** 아마 없을 것 같아. 결국, 평가 기준마다 결과가 달라질 수 있거든. 스케줄러가 반환 시간이 좋으면 응답 시간이 나쁘고, 그 반대도 참이지. Lampson이 말했듯이 아마도 목표는 최선의 해결책을 찾는 것이 아니라 사고를 피하는 것이지.

**학생:** 그건 조금 우울하네요.

> **교수:** 공학은 원래 그런거야. 하지만 실용적인 관점에서 생각하면 모든 문제가 깔끔하고 쉬운 해결책을 가지는 것은 아니지.

**학생:** 스케줄러를 의도대로 움직이게 하는 개념이 정말 맘에 들었어요. 다음에 제가 Amazon의 EC2에서 작업할 때 조사해 볼 무언가가 있을 것 같습니다.

> **교수:** (웃으며) 내가 괴물을 만들어 낸 것 같네!

**학생:** 하지만 원래 그런 의도 아니셨습니까? 우리가 흥미를 느껴서 스스로 조사하게 만드는 것?

> **교수:** 그렇게 생각하지만, 그게 효과가 있을 줄은 몰랐지!

**흥미진진한 대화는 끝났지만, 학생의 탐구는 계속된다. 과연 그는 CPU 가상화의 비밀을 완전히 밝혀낼 수 있을까?**

### 메모리 가상화

**학생:** 가상화에 대한 이야기는 이제 끝인가요?

> **교수:** 아니다! 아직 끝나지 않았네. 우리는 CPU 가상화에 대한 이야기를 마쳤을 뿐, 옷장 속에 숨어있는 진정한 괴물, 메모리 가상화는 아직 남아있지. 메모리 가상화는 CPU 가상화보다 훨씬 복잡하고, 하드웨어와 운영체제의 상호작용에 대한 더 깊은 이해를 필요로 하지.

**학생:** 왜 그렇게 어려운가요?

> **교수:** 메모리 가상화에는 많은 세부적인 내용들이 있고, 이를 이해하기 위해서는 체계적인 모델을 구축해야 하기 때문이지. 우리는 베이스-바운드와 같은 기본적인 기술부터 시작하여 TLB, 멀티 레벨 페이지 테이블 등의 복잡한 개념까지 다루게 될 거야. 그리고 궁극적으로는 현대 가상 메모리 관리자의 작동 방식을 완전히 이해할 수 있을 거야.

**학생:** 좋아요! 정보 홍수와 수면 부족으로 고생하는 불쌍한 학생들을 위해 팁을 좀 주세요.

> **교수:** 수면 부족은 간단하게 해결할 수 있지. 덜 놀고 더 자도록 하게. 메모리 가상화를 이해하기 위해서는 먼저 사용자 프로그램이 생성하는 모든 주소는 가상 주소라는 것을 명심해야 하네. 운영체제는 각 프로세스에게 자신만의 커다란 전용 메모리를 가지고 있다는 환상을 제공하고, 하드웨어의 도움을 받아 가상 주소를 실제 물리 주소로 변환하여 원하는 정보를 찾아내는 거야.

**학생:** 그렇군요. 외울 수 있을 것 같습니다... "사용자 프로그램의 모든 주소는 가상이다. 사용자 프로그램의 모든 주소는 가상이다..."

> **교수:** 중얼거리는 게 뭐야?

**학생:** 아, 아무것도... 어쨌든, 왜 운영체제는 이런 환상을 제공하고 싶어 하는 거죠?

> **교수:** 사용하기 쉬운 시스템을 제공하기 위해서야. 운영체제는 각 프로세스에게 코드와 데이터를 저장할 수 있는 대용량의 연속된 주소 공간을 제공하고, 프로그래머는 "이 변수를 어디에 저장해야 할까?"와 같은 걱정을 하지 않아도 된다는 거지. 프로그램의 가상 주소 공간이 크고 변수 등을 위한 많은 공간을 가지고 있기 때문이야.

**학생:** 다른 이유는 없나요?

> **교수:** 음... 고립(isolation)과 보호(protection)도 중요한 이유지. 우리는 잘못된 프로그램이 다른 프로그램의 메모리를 읽고, 더 안 좋게는 덮어 쓰도록 만들고 싶지 않지.

**학생:** 아마 싫어하겠죠. 싫어하는 사람이 작성한 프로그램이 아니라면 말이죠.

> **교수:** 음... 다음 학기 시간표에 도덕과 윤리 수업을 추가해야 할 것 같군. 운영체제 수업이 윤리를 가르치는 건 아니니까.

**학생:** 아마 그래야 할지도 모르겠어요. 하지만, 프로세스의 잘못된 행동에 대한 운영체제의 올바른 대응은 해당 프로세스를 죽이는 것이라고 제가 가르친 건 아니라는 것을 기억해 주세요.

**흥미진진한 대화 속에서 학생은 메모리 가상화에 대한 깊은 이해를 얻게 된다. 그는 과연 메모리 가상화의 비밀을 완전히 밝혀낼 수 있을까?**

```{note}
메모리 가상화 개념을 이해하기 위해서는 컴퓨터 아키텍처와 운영체제에 대한 기본적인 지식이 필요합니다.
```

## 메모리 가상화를 정리하는 대화

**학생:** (지쳐) 와, 정말 많은 내용이었네요.

> **교수:** 그렇구나. 그래서 이제 어떻게 할 생각이야? 시험 대비라고?

**학생:** 음, 그렇죠. 하지만 이렇게 많은 내용을 어떻게 다 기억하라는 거죠?

> **교수:** 세상에, 그저 시험을 위해 이 내용들을 기억하려는 것이 아니길 바라네.

**학생:** 그러면 왜 기억해야 하는 거죠?

> **교수:** 글쎄, 그보다 더 중요한 이유가 있지. 세상에 나갔을 때 시스템들이 실제로 어떻게 동작하는지 알기 위해서, 여기서 무언가를 배우는 것이 중요하지 않니?

**학생:** 흠... 예를 하나 들어주실 수 있나요?

> **교수:** 물론이지! 대학원 때 내 친구가 메모리 접근 속도를 측정하고 있었는데, 가끔씩 예상보다 훨씬 느린 속도가 나왔어. 모든 데이터가 레벨 2 캐시에 다 들어갔다고 생각했거든. 그래서 접근 속도가 엄청 빠를 것이라고 말이지.

**학생:** (고개를 끄덕이며)

> **교수:** 무슨 일인지 알 수 없었어. 그런 경우에는 어떻게 해야 할까? 쉬워, 교수님께 물어보는 거지! 우리 지도교수님 중 한 분께 찾아가서 질문했지. 그 교수님은 우리가 만든 그래프를 보시더니, 간단하게 "TLB"라고 말씀하셨어. 아하! 그렇지, TLB 미스들이 있었던 거야! 왜 그것을 생각하지 못했을까? 가상 메모리가 어떻게 동작하는지에 대한 모델을 잘 이해하고 있으면 여러 종류의 흥미로운 성능 관련 문제들을 진단하는 데 도움이 된단 말이지.

**학생:** 이해할 수 있을 것 같아요. 이런 것들이 어떻게 동작하는지 개념적 모델을 만들려고 노력하고 있거든요. 현장에 나가 혼자 일하면서, 시스템이 예상과 다르게 동작하더라도 놀라지 않도록 말이죠. 시스템이 어떻게 동작할지를 생각만으로도 예상을 할 수 있게 되겠네요.

> **교수:** 정확히 그렇지. 그래서 지금까지 무엇을 배웠니? 가상 메모리가 어떻게 동작하는지 이해하게 되었니?

**학생:** 음, 프로세스가 메모리를 참조할 때 어떤 일들이 일어나는지에 대한 개념은 이제 잘 잡은 것 같아요. 여러 번 언급하셨는데요, 프로세스가 각 명령어들을 반입하는 것과 또한 명시적으로 로드와 스토어를 수행할 때 어떻게 동작하는지를 이해했어요.

> **교수:** 좋아 보이는구나. 그럼 더 자세히 설명해 봐 줄 수 있니?

**학생:** 음, 이거 하나는 항상 기억할 건데요, 예를 들어 C 언어로 작성된 프로그램에서 볼 수 있는 주소들은 말이죠...

> **교수:** 다른 언어들도 어떤 것이 있니?

**학생:** (계속하면서) ... 네, 교수님이 C를 좋아하시는 것 알아요. 저도 그렇죠! 어쨌든, 제가 말하려고 했던 것은요, 이제는 프로그램 내에서 볼 수 있는 주소들은 가상 주소들이라는 것을 정확히 알겠어요. 데이터와 코드가 메모리에 있는 것처럼 보이도록 프로그래머에게 환상을 심어준다는 것도 알겠어요. 예전에는 포인터의 주소를 출력해 볼 수 있다는 것이 멋지다고 생각했죠. 그렇지만, 이제는 불만스럽습니다. 그저 가상 주소일 뿐이잖아요! 데이터가 존재하는 실제 물리 주소를 볼 수가 없단 말이죠.

> **교수:** 그래, 운영체제는 그러한 정보들을 볼 수 있도록 설계되었지. 하지만 일반적인 프로그래머에게는 필요하지 않은 정보야. 중요한 것은 프로그램이 올바르게 동작하는 것이고, 그러기 위해서는 가상 메모리 시스템이 투명하게 작동해야 한다는 거지.

**학생:** 그렇군요. 그래서 TLB가 중요하다는 것을 알게 되었어요. 주소 변환을 위한 작은 하드웨어 캐시가 말이죠. 페이지 테이블은 크고 느린 메모리에 존재하기 때문에 TLB가 정말 핵심적인 것 같아요. TLB가 없다면 프로그램 속도가 엄청 느려질 거예요. 가상 메모리를 실제로 가능하게 만드는 것은 TLB라고 생각합니다. TLB 없이 시스템을 만드는 것은 상상할 수가 없죠! 그리고 TLB가 다룰 수 있는 범위를 넘어서는 작업 세트를 갖는 프로그램을 생각하면 몸서리가 처지네요. 그 많은 TLB 미스들을 처리하는 것은 쉽지 않을 것 같아요.

> **교수:** 그렇지. TLB는 가상 메모리 시스템의 핵심적인 부품이라고 할 수 있지. TLB 외에 또 무엇을 배웠니?

**학생:** 페이지 테이블 또한 중요한 자료 구조라는 것을 알게 되었어요. 하지만 그저 자료 구조일 뿐이고, 어떤 자료 구조든 사용될 수 있다는 것을 알았습니다. 처음에는 배열과 같은 간단한 자료 구조(선형 페이지 테이블이라고도 불림)로 시작하고, 멀티레벨 테이블(트리처럼 보이는 것)로 발전했습니다. 그리고 커널의 가상 메모리 페이지 테이블에 페이지를 사용할 수 있는 좀 더 복잡한 방법도 배웠습니다.

> **교수:** 좋아.

**학생:** 그리고 주소 변환 자료 구조는 프로그래머가 자신의 주소 공간에서 원하는 작업을 수행할 수 있도록 충분히 유연해야 한다는 것을 알게 되었어요. 멀티레벨 테이블과 같은 자료 구조는 그런 면에서 완벽합니다. 사용자가 주소 공간의 일부만 필요할 때만 테이블에 공간을 생성하기 때문에 적은 양의 메모리만 낭비됩니다. 간단한 베이스와 바운드 레지스터를 사용하던 초기의 방법은 충분히 유연하지 못했습니다. 자료 구조는 사용자가 예상하는 수준에 부합해야 하고 가상 메모리 시스템에서 원하는 기능을 제공해야 합니다.

> **교수:** 훌륭한 관찰이야. 디스크로 스왑하는 것에 대해서는 어떻게 생각하니?

**학생:** 음, 분명히 공부하기 재미있었고, 페이지 교체 정책이 어떻게 작동하는지 알게 되어 좋았어요. 기본적인 정책들은 약간은 당연했지만(예를 들어 LRU와 같은), 실제 가상 메모리 시스템을 만드는 것은 좀 더 흥미로운 것 같아요. VMS 사례 연구에서 보았던 것처럼 말이죠. 하지만 왜 그런지, 기법들이 정책들보다 더 흥미로운 것 같아요.

> **교수:** 오, 왜 그렇게 생각했을까?

**학생:** 음, 말씀하셨듯이, 결국에는 정책에 대한 문제에 대한 최선의 해결책은 간단했습니다. 메모리를 더 많이 사라고 하셨죠. 하지만, 기법은 실제로 어떻게 동작하는지를 이해하고 있어야 한다는 말이죠. 말이 나온 김에 ...

> **교수:** 그래?

**학생:** 음, 제 기계가 요즘에 상당히 느려진 것 같아요... 메모리가 그렇게 비싸지도 않으니까...

> **교수:** 오 좋아, 괜찮아! 여기 얼마 줄게. 가서 DRAM 좀 사거라. 구두쇠 씨.

**학생:** 교수님, 감사합니다! 이제 디스크로 절대로 스왑하지 않으리라—또는 만약 한다고 해도, 최소한 어떤 일이 실제로 일어나는지는 알겠습니다!

## 메모리 가상화

**학생:** 가상화에 대한 이야기는 이제 끝인가요?

> **교수:** 아니다! 아직 끝나지 않았네. 우리는 CPU 가상화에 대한 이야기를 마쳤을 뿐, 옷장 속에 숨어있는 진정한 괴물, 메모리 가상화는 아직 남아있지. 메모리 가상화는 CPU 가상화보다 훨씬 복잡하고, 하드웨어와 운영체제의 상호작용에 대한 더 깊은 이해를 필요로 하지.

**학생:** 왜 그렇게 어려운가요?

> **교수:** 메모리 가상화에는 많은 세부적인 내용들이 있고, 이를 이해하기 위해서는 체계적인 모델을 구축해야 하기 때문이지. 우리는 베이스-바운드와 같은 기본적인 기술부터 시작하여 TLB, 멀티 레벨 페이지 테이블 등의 복잡한 개념까지 다루게 될 거야. 그리고 궁극적으로는 현대 가상 메모리 관리자의 작동 방식을 완전히 이해할 수 있을 거야.

**학생:** 좋아요! 정보 홍수와 수면 부족으로 고생하는 불쌍한 학생들을 위해 팁을 좀 주세요.

> **교수:** 수면 부족은 간단하게 해결할 수 있지. 덜 놀고 더 자도록 하게. 메모리 가상화를 이해하기 위해서는 먼저 사용자 프로그램이 생성하는 모든 주소는 가상 주소라는 것을 명심해야 하네. 운영체제는 각 프로세스에게 자신만의 커다란 전용 메모리를 가지고 있다는 환상을 제공하고, 하드웨어의 도움을 받아 가상 주소를 실제 물리 주소로 변환하여 원하는 정보를 찾아내는 거야.

**학생:** 그렇군요. 외울 수 있을 것 같습니다... "사용자 프로그램의 모든 주소는 가상이다. 사용자 프로그램의 모든 주소는 가상이다..."

> **교수:** 중얼거리는 게 뭐야?

**학생:** 아, 아무것도... 어쨌든, 왜 운영체제는 이런 환상을 제공하고 싶어 하는 거죠?

> **교수:** 사용하기 쉬운 시스템을 제공하기 위해서야. 운영체제는 각 프로세스에게 코드와 데이터를 저장할 수 있는 대용량의 연속된 주소 공간을 제공하고, 프로그래머는 "이 변수를 어디에 저장해야 할까?"와 같은 걱정을 하지 않아도 된다는 거지. 프로그램의 가상 주소 공간이 크고 변수 등을 위한 많은 공간을 가지고 있기 때문이야.

**학생:** 다른 이유는 없나요?

> **교수:** 음... 고립(isolation)과 보호(protection)도 중요한 이유지. 우리는 잘못된 프로그램이 다른 프로그램의 메모리를 읽고, 더 안 좋게는 덮어 쓰도록 만들고 싶지 않지.

**학생:** 아마 싫어하겠죠. 싫어하는 사람이 작성한 프로그램이 아니라면 말이죠.

> **교수:** 음... 다음 학기 시간표에 도덕과 윤리 수업을 추가해야 할 것 같군. 운영체제 수업이 윤리를 가르치는 건 아니니까.

**학생:** 아마 그래야 할지도 모르겠어요. 하지만, 프로세스의 잘못된 행동에 대한 운영체제의 올바른 대응은 해당 프로세스를 죽이는 것이라고 제가 가르친 건 아니라는 것을 기억해 주세요.

**흥미진진한 대화 속에서 학생은 메모리 가상화에 대한 깊은 이해를 얻게 된다. 그는 과연 메모리 가상화의 비밀을 완전히 밝혀낼 수 있을까?**

```{note}
메모리 가상화 개념을 이해하기 위해서는 컴퓨터 아키텍처와 운영체제에 대한 기본적인 지식이 필요합니다.
```

## 메모리 가상화를 정리하는 대화

**학생:** (지쳐) 와, 정말 많은 내용이었네요.

> **교수:** 그렇구나. 그래서 이제 어떻게 할 생각이야? 시험 대비라고?

**학생:** 음, 그렇죠. 하지만 이렇게 많은 내용을 어떻게 다 기억하라는 거죠?

> **교수:** 세상에, 그저 시험을 위해 이 내용들을 기억하려는 것이 아니길 바라네.

**학생:** 그러면 왜 기억해야 하는 거죠?

> **교수:** 글쎄, 그보다 더 중요한 이유가 있지. 세상에 나갔을 때 시스템들이 실제로 어떻게 동작하는지 알기 위해서, 여기서 무언가를 배우는 것이 중요하지 않니?

**학생:** 흠... 예를 하나 들어주실 수 있나요?

> **교수:** 물론이지! 대학원 때 내 친구가 메모리 접근 속도를 측정하고 있었는데, 가끔씩 예상보다 훨씬 느린 속도가 나왔어. 모든 데이터가 레벨 2 캐시에 다 들어갔다고 생각했거든. 그래서 접근 속도가 엄청 빠를 것이라고 말이지.

**학생:** (고개를 끄덕이며)

> **교수:** 무슨 일인지 알 수 없었어. 그런 경우에는 어떻게 해야 할까? 쉬워, 교수님께 물어보는 거지! 우리 지도교수님 중 한 분께 찾아가서 질문했지. 그 교수님은 우리가 만든 그래프를 보시더니, 간단하게 "TLB"라고 말씀하셨어. 아하! 그렇지, TLB 미스들이 있었던 거야! 왜 그것을 생각하지 못했을까? 가상 메모리가 어떻게 동작하는지에 대한 모델을 잘 이해하고 있으면 여러 종류의 흥미로운 성능 관련 문제들을 진단하는 데 도움이 된단 말이지.

**학생:** 이해할 수 있을 것 같아요. 이런 것들이 어떻게 동작하는지 개념적 모델을 만들려고 노력하고 있거든요. 현장에 나가 혼자 일하면서, 시스템이 예상과 다르게 동작하더라도 놀라지 않도록 말이죠. 시스템이 어떻게 동작할지를 생각만으로도 예상을 할 수 있게 되겠네요.

> **교수:** 정확히 그렇지. 그래서 지금까지 무엇을 배웠니? 가상 메모리가 어떻게 동작하는지 이해하게 되었니?

**학생:** 음, 프로세스가 메모리를 참조할 때 어떤 일들이 일어나는지에 대한 개념은 이제 잘 잡은 것 같아요. 여러 번 언급하셨는데요, 프로세스가 각 명령어들을 반입하는 것과 또한 명시적으로 로드와 스토어를 수행할 때 어떻게 동작하는지를 이해했어요.

> **교수:** 좋아 보이는구나. 그럼 더 자세히 설명해 봐 줄 수 있니?

**학생:** 음, 이거 하나는 항상 기억할 건데요, 예를 들어 C 언어로 작성된 프로그램에서 볼 수 있는 주소들은 말이죠...

> **교수:** 다른 언어들도 어떤 것이 있니?

**학생:** (계속하면서) ... 네, 교수님이 C를 좋아하시는 것 알아요. 저도 그렇죠! 어쨌든, 제가 말하려고 했던 것은요, 이제는 프로그램 내에서 볼 수 있는 주소들은 가상 주소들이라는 것을 정확히 알겠어요. 데이터와 코드가 메모리에 있는 것처럼 보이도록 프로그래머에게 환상을 심어준다는 것도 알겠어요. 예전에는 포인터의 주소를 출력해 볼 수 있다는 것이 멋지다고 생각했죠. 그렇지만, 이제는 불만스럽습니다. 그저 가상 주소일 뿐이잖아요! 데이터가 존재하는 실제 물리 주소를 볼 수가 없단 말이죠.

> **교수:** 그래, 운영체제는 그러한 정보들을 볼 수 있도록 설계되었지. 하지만 일반적인 프로그래머에게는 필요하지 않은 정보야. 중요한 것은 프로그램이 올바르게 동작하는 것이고, 그러기 위해서는 가상 메모리 시스템이 투명하게 작동해야 한다는 거지.

**학생:** 그렇군요. 그래서 TLB가 중요하다는 것을 알게 되었어요. 주소 변환을 위한 작은 하드웨어 캐시가 말이죠. 페이지 테이블은 크고 느린 메모리에 존재하기 때문에 TLB가 정말 핵심적인 것 같아요. TLB가 없다면 프로그램 속도가 엄청 느려질 거예요. 가상 메모리를 실제로 가능하게 만드는 것은 TLB라고 생각합니다. TLB 없이 시스템을 만드는 것은 상상할 수가 없죠! 그리고 TLB가 다룰 수 있는 범위를 넘어서는 작업 세트를 갖는 프로그램을 생각하면 몸서리가 처지네요. 그 많은 TLB 미스들을 처리하는 것은 쉽지 않을 것 같아요.

> **교수:** 그렇지. TLB는 가상 메모리 시스템의 핵심적인 부품이라고 할 수 있지. TLB 외에 또 무엇을 배웠니?

**학생:** 페이지 테이블 또한 중요한 자료 구조라는 것을 알게 되었어요. 하지만 그저 자료 구조일 뿐이고, 어떤 자료 구조든 사용될 수 있다는 것을 알았습니다. 처음에는 배열과 같은 간단한 자료 구조(선형 페이지 테이블이라고도 불림)로 시작하고, 멀티레벨 테이블(트리처럼 보이는 것)로 발전했습니다. 그리고 커널의 가상 메모리 페이지 테이블에 페이지를 사용할 수 있는 좀 더 복잡한 방법도 배웠습니다.

> **교수:** 좋아.

**학생:** 그리고 주소 변환 자료 구조는 프로그래머가 자신의 주소 공간에서 원하는 작업을 수행할 수 있도록 충분히 유연해야 한다는 것을 알게 되었어요. 멀티레벨 테이블과 같은 자료 구조는 그런 면에서 완벽합니다. 사용자가 주소 공간의 일부만 필요할 때만 테이블에 공간을 생성하기 때문에 적은 양의 메모리만 낭비됩니다. 간단한 베이스와 바운드 레지스터를 사용하던 초기의 방법은 충분히 유연하지 못했습니다. 자료 구조는 사용자가 예상하는 수준에 부합해야 하고 가상 메모리 시스템에서 원하는 기능을 제공해야 합니다.

> **교수:** 훌륭한 관찰이야. 디스크로 스왑하는 것에 대해서는 어떻게 생각하니?

**학생:** 음, 분명히 공부하기 재미있었고, 페이지 교체 정책이 어떻게 작동하는지 알게 되어 좋았어요. 기본적인 정책들은 약간은 당연했지만(예를 들어 LRU와 같은), 실제 가상 메모리 시스템을 만드는 것은 좀 더 흥미로운 것 같아요. VMS 사례 연구에서 보았던 것처럼 말이죠. 하지만 왜 그런지, 기법들이 정책들보다 더 흥미로운 것 같아요.

> **교수:** 오, 왜 그렇게 생각했을까?

**학생:** 음, 말씀하셨듯이, 결국에는 정책에 대한 문제에 대한 최선의 해결책은 간단했습니다. 메모리를 더 많이 사라고 하셨죠. 하지만, 기법은 실제로 어떻게 동작하는지를 이해하고 있어야 한다는 말이죠. 말이 나온 김에 ...

> **교수:** 그래?

**학생:** 음, 제 기계가 요즘에 상당히 느려진 것 같아요... 메모리가 그렇게 비싸지도 않으니까...

> **교수:** 오 좋아, 괜찮아! 여기 얼마 줄게. 가서 DRAM 좀 사거라. 구두쇠 씨.

**학생:** 교수님, 감사합니다! 이제 디스크로 절대로 스왑하지 않으리라—또는 만약 한다고 해도, 최소한 어떤 일이 실제로 일어나는지는 알겠습니다!