---

layout: post 
title: "So, How Do You Make Agile Successful?" 
date: 2016-09-10 10:25:00 +0900
categories: agile
tags:
- agile
- scrum
- 토요타

---

<hr/>

얼마전 부터 코드리뷰를 시작하게 되었다. 또 다른 부서에서는 아침마다 간이 화이트보드에 포스트잇을 붙여가면서 scrum 미팅을 하고 있다. 
그리고 과제를 진행하면서 sprint 니 phase 하는 용어를 쓰고 있다.

모두 Agile 하게 일하고 싶은 것이다.

하지만, 여전히 관심이 없는 사람이 많으며 이들을 도입하기 전과 다른 점을 찾기 힘든 것도 사실로 보인다.

무엇이 문제일까? 이와 관련된 듯한 기사가 있어 포스팅 한다.

<hr/>

-	원문 : [So, How Dow You make Agile Successful?](https://www.infoq.com/articles/how-make-agile-successful?utm_source=infoq&utm_medium=popular_widget&utm_campaign=popular_content_list&utm_content=homepage)

```
Key takeaways

 -   Agile 의 본질
 -   Scrum 의 함정
 -   Agile 은 product, delivery 레벨에 각기 다른 skill 과 mindset 을 필요로 함
 -   CICD 를 사용해 Scrum 의 함정에서 비켜가자
 -   thinking skill 시스템 개발
```

[Why Agile Didn't Work](https://www.infoq.com/articles/agile-didnt-work) 를 쓴 이후 많은 논의가 있었다. 
Agile을 통해 좋은 경험을 한 사람도 있었지만, 아주 나쁜 기억을 가지게된 사람도 있다. 
하지만 양쪽 모두 일반적으로 하나의 결론을 내고 있다.`process 에 대한 얘기가 아니고 사람에 대한 얘기` 라는 것이다.
소프트웨어는 더이상 엘리트 산업이 아니다. 일반적으로 한 팀에서 뛰어난 사람이 몇명 있고 그외에는 평범한 수준의 엔지니어와 관리자가 있다. 
Agile 팀은 `먼저 협동하라. 그러면 Agile 의 마법을 보여줄 것` 이라고 얘기한다. 
바로 이 점이 Agile 에서 마음에 안드는 부분이다. Agile 이 효과를 내는 것은 `Agile 의 이론들이 뛰어나기 때문` 이고, 
효과를 내지 않는 경우는 `당신이 그것을 방해하고 잘못 실행하기 때문` 이라는 것이다. 
이것은 책임회피에 불과하다. 이보다 좀 더 건설적인 대응이 필요하다.

먼저 Agile 의 본질을 집어보자.

The essence of Agile
-------------------

scrum , lean, lean startup 모두 빠르게 delivery 하고 빠르게 feedback 받는 공통 점이 있다.
왜냐하면, feedback 으로부터 배울 필요가 있기 때문이다.
뭔가를 시작할 때, 그리 많이 알고 있지 않기 때문에 `요구사항을 명확하게 하고 risk 를 발견하기 위해 빠른 feedback 이 필요`하다.
개발단계의 bug 에 대한 신속한 feedback 은  `product 의 질을 향상`시킨다.

몇몇 관리자는 `'당신에게 일하라고 돈을 주는 것이지 배우라고 주는 것이 아니다'` 라고 한다.
이런 관리자들에게 조금 거칠게 얘기 하자면,
소프트웨어 엔지니어링은 지식 산업이다. 
공장의 조립 생산라인처럼 소프트웨어 엔지니어를 `아무렇게나 그룹으로 만들어놓고 높은 품질의 소프트웨어를 요구할 수 없다`.

Agile 은 사용자, 고객에게 배울 수 있는 기회 (혹은 도전할 수 있는 기회) 를 제공한다.
Agile 사용 통계에서 보자면 오직 20% 만이 정기적으로 사용되고 64%는 거의 사용되지 않거나 아예 사용되지 않는다.
Agile 과 함께, 이 20% 를 식별하고 64% 는 시간을 낭비하지 않기를 희망한다.
Agile 은 그들의 변덕스러운 mind 를 바꿀수 있다는 의미가 아니다. 
오히려 그들이 `작업의 양을 최대화 하기 위해  개발 과정에 참여하는` 것과 같은 시도를 하는 것에 대해 주의 깊게 생각해야 할 필요가 있다.

![alt breakdown](https://cdn.infoq.com/statics_s1_20160823-0357/resource/articles/how-make-agile-successful/en/resources/21.jpg)

그러나 `배우는게 쉽다는 것은 끝났다`. 
우리가 이해하지 못하는 것들에 대해 먼저 `겸손하고 오픈 마인드`가 되어야 한다.
그리고 나서야 실수나 반대의견을 집어내는 기술이 필요하다. 
또한 시스템적으로 생각할 수 있는 기술, 근본적인 원인까지 파내는 것 그리고 솔루션을 도출해 내는 것 또한 필요하다.
마지막으로, 솔루션을 시도해서 뭔가 바꿔볼 수 있는 용기와 인내가 필요하다.

관리자는 이런 방식에 많은 부담을 가지고 있다. 
왜냐면 Agile 은 빠른 feedback 을 하지기 때문에, 더 많은 issue를 더 빠르게 보게 된고, 이러한 부분은 관리적인 부분에 좀 더 관련이 있다.
관리적인 부분을 Scrum 마스터에게 위임한다는 것은 생각하지도 말아야 한다.
실제 회사에서는, `self-organizing(자체 조직화)` 팀들을 세우기 힘들기도 하다.
그리고 변화를 위해 `회사의 관료적인 부분을 통과 하기 위해 헌신하는 Scrum 마스터`를 기대하는 것도 비현실적이다.
Agile 전환이 단지 `관리자의 이슈에 대한 행위를 관찰하는 방법`에 성공적이라고 생각해보자.
만약 관리자의 행위가 미팅을 늘리고 컨트롤을 늘리는 것이라면, Agile 이 성공할 가능성은 낮아질 것이다.

 * 토요타에서 정의한 리더쉽에 대한 얘기들
 
 1. 행동하라. 그리고 조직의 일에 대해 마음을 열고 주시하라.
 2. 사람들이 정말 무슨 말을하는지 들어라.
 3. 시스템적 사고 (Systems thinking)
 4. 문제들을 명확히 정의하고 근본 원인을 밝혀라.
 5. 창조적 식별이 진짜 근본 원인에 대한 수단이다. 
 6. 계획하라. (Planning)
 7. 계획은 명확한 책임이 있는 행동을 포함한다.
 8. 미래의 기회를 확인하는 것에 대해 시간을 갖고 심사숙고 하라.
 9. 개개인의 실제 강점과 약점을 이해하라.
 10. 동기를 부여하고 조직 전체 사람들(권한이 없는)를 공통의 목표에 대해 영향을 미쳐라.
 11. 위의 모든 것을 가르칠 수 있도록 하라.
 
이 리더쉽 기술을은 issue 를 해결하는 것에 대해 최적화 되어 있다. 1-7 은 문제를 올바르게 풀기 위한 접근방법에 대한 것이다.
 8 은 문제가 반복되는 것을 방지하고 개선하기 위한 것이다. 9,10,11 은 인력 관리에 대한 것으로, 궁극적으로 올바른 문제 해결을 가르치는 것이 목표이다.
 

Scrum traps
-----------

표면적으로, Scrum 은 Agile 이론과 완벽히 매치되는 듯 보인다.
Timebox 로 delivery 한다는 얘기는 사용자의 feedback 이 빠르다는 의미이다.
user story 에서는 그들이 보는 비지니스 관점에서 우선순위를 알 수 있다.
반복적으로 나타나는 user story 는 우리가 사용자 feedback 에 맞춰가고 있다는 의미이다.
회고 모임은 우리가 지속적으로 배우고 개선함을 의미한다.

Scrum 이 보통 처음이거나, 때로는 어떤 팀이 받아들인 유일한 Agile 프로세스이기도 하다.
왜냐하면 Agile 원리와는 다르게, 짧은 시간안에 개선될 수 있는 프로세스가 명백하기 때문이다.
조잡한 형태로 말하자면 조금 미팅을 추가하고 작업을 분리하고, 작업을 잘게 쪼개는 것이다.
조잡한 형태에 최적화된 팀은 아마 길고 지루한 미팅에 불평을 하고 있을 것이다.
지속가능한 페이스 대신, 리뷰를 준비하는 과정에서 뭔가 얻기 위해 질주하고 있는 것을 발견할 것이다.

이것은 Scrum 자체의 잘못이 아니다. 그러나 많은 Agile 컨설턴트가 Scrum 을 사실상 Agile 프로세스로 선전하였기 때문에, 결과적으로 팀이 조잡한 형태를 띄게 되었다.
그리고 우리는 Scrum 은 이미 끝났고 좋은 것 보다 나쁜 것이 많다는 사실에 직면하게 되고 그 이유를 이해하게 된다.
이것이 진정한 Scrum 이냐 여부를 따진다면, 단지 나쁜 Agile 컨설턴트가 Scrum 을 그렇게 말한 것뿐이다.

Scrum 의 성공은 자기조직화된 팀(self-organizing teams) 에 달려있다. 
나는 자기조직화된 팀은 전제가 아닌 결과라고 하고 싶다.
몇몇 Scrum 사례들(user stories, velocity measurement, meetings)은 남용되기 쉽고, 근시안적인 기술적 결정과 밀착감시에 끌리기 쉽다는 점에서 다루기 까다롭다.

Self-organizing team
--------------------

Scrum 은 사람들을 교차기능팀(cross-functional teams : 조직내 서로 다른 부서에서 온 소수의 사람으로 구성된 팀) 으로 그룹 짓는다.
만약 팀이 필요한 모든 부분에 전문적이라면, 동기 이론에 따라 행복하게 Self-organizing 되어야 한다. 하지만, 이론과 실제는 다르다.

만약 팀이 관리시스템이나 특정 소프트웨어 로부터 지시를 받는 것에 익숙하다면, 뜻밖의 자유에 어쩔 줄 모를 수 있다.
스파이더맨에서 말하듯이 '큰 힘에는 큰 책임' 이 따른다. 
문제가 있는 팀의 사람들은 스스로 결정하고 싶어하지 않는다.
왜냐햐면 책임을 지고 싶지 않기 때문이다.

Scrum 을 통한 관리가 Self-organizing 를 보장하진 않는다. 이것이 실현되기 위해 사람들 사이에 많은 신뢰를 쌓는 과정이 필요하다.
이것이 바로 좋은 Agile의 결과이지 전제가 아니다.

관리를 통해 팀에게 힘을 실어 줄 수 있게 하고자 한다고 가정하자. 사실대로 말하자면 이건 때때로 립서비스에 불과할 수 있다.
파렴치한 매니저들이 뒤에서 Agile 의 변화를 수용하기 위해 더 일하라고 선동하는 반면, 관리 상태인 팀들은꾸준한 페이스로 일 할 수 있는 힘이 있다.
결과적으로 팀은 일이 마무리 될 때까지 매번 "sprint" 해야한다. 마지막에만 "sprint" 하는 과거 "waterfall" 방식으로 돌아가고 싶어하는 것이 이상할 것도 없다.


User story
----------

User Story 의 목적은 사용자와 팀 사이의 대화를 촉진 시키는 것이다. 
사용자에게 "무엇을 원하는가?" 라는 요구사항을 이끌어 내는 것은 어렵다. 
"이 부분의 처음부터 끝까지 어떻게 수행할지 말해주세요" 라는 이야기 형식을 사용하는 것이 요소들과 의견에 대해 듣기 더 쉬운 방법이다.

 > 1. 모든 것은 사용자 관점에서 봐야 한다. 사용자가 소프트웨어에 대한 기술을 항상 알고 있는 것이 아니라는 것은 인정하자. 그들은 좋아보이거나 나빠보이는 것은 얘기 하지만, 하나하나 자세한 기술적 요소까지 정의내릴 수 없다.
당신이 이 이야기에 2점을 준다면, 사용자는 13점을 준다. 왜냐면 당신은 좀 더 모듈화 하고 테스트하기 쉽게 하기 위해 코드를 손볼 필요가 있지만, 사용자는 이해하지 못할 것이기 때문이다.

몇몇 팀들은 코드의 품질을 개선하거나 기술적으로 의심이 가는 부분을 줄이기 위해 "technical stories"에 호소한다. "technical stories"를 만들어내는 것은 여전히 비즈니스와 IT 사이에 거리가 있다는 것을 의미한다.
"technical stories" 와 "user stories" 나란히 만드는 것은 "technical stories" 이 "user stories" 보다 나중에 쓰인다거나 희생될 수 있다는 환상을 만들어낸다.

 > 2. 비지니스가 장기적인 가치보다 단기적인 가치를 편애 하는 한, 사이의 간극은 쉽게 줄어들지 않을 것이다.

Scrum 에서, user stories 는 반복의 처음에 다듬어진다. 이것이 user stories 의 다음 단계에 집중 한다는 것을 의미하진 않는다. 현재 iteration 에서 중요한 needs 를 찾아내는 것이 실패하는 것은 나중에 큰 혼란이 초래될 수 있다.


Meetings
--------

미팅 - 아마도 Scrum 에서 가장 불만인 부분일 것이다.
매일 아침에 하는 미팅, 백로그 정리 회의, 계획 미팅, 리뷰 미팅, 회고 모임 - 끝나긴 하려나?

내 경험으로는, 작은 팀안에서 사람들은 누가 나에게 도움이 될 것인지 다른 사람이 무엇을 할 것인지 안다.
그들은 서로 알게될 기회가 많이 있다.
매일 스탠드업 미팅을 할 필요가 없다.
심지어 스탠드업 미팅은 15분임에도 불구하고, 15분이 넘기도 한다. 
엔지니어들은 "flow" 안에서 몰입이 이루어져 가장 효과적이다. 이 상태에서 문제를 푸는데 모든 것을 바친다.
매일 아침 계획된 스탠드업이 마치 방햬를 위해 계획 된 것 같고, 이것은 엔지니어들이 "flow" 상태로 빠지기 힘들게 한다. 

미팅이 성공적으로 개최되었다고 말하긴 쉽다.
단지 사람들이 참여하고 있고 그들의 의견을 내는 것에 두려워하지 않는 지 관찰하라.
만일 사람들이 폰을 가지고 놀고 있거나 졸린 눈을 하고 있다면, 미팅으로 그들을 고문시키기 보다 그들을 참여시킬 방법을 생각하라.


Velocity
--------

A consistent velocity is the Holy Grail for project managers, but unfortunately, it is not always achievable. 
If a team has done a similar project before and has advanced technical skills, the velocity diagram might be consistent. 
But in reality, a velocity chart might look like the following:

![alt StoryPoint](https://cdn.infoq.com/statics_s1_20160831-0533u1/resource/articles/how-make-agile-successful/en/resources/72.jpg)

The team starts to discover user stories as it goes along, so the burn down line (the blue one) at first looks like a burn up line! 
I guess there should be a point where the burn down line should start burning down, but the location of the point would be based on the nature of the project.

The trouble with velocity charts is that it can be so easily abused. 
Project managers will push teams to generate such charts so they can make “reliable” predictions. 
But you know software engineers are smart enough to game any metrics when push comes to shove (see The Original Sin of Software Metrics).


Micromanagement
---------------

“What have you done yesterday?”

“What do you plan to do today?”

“Why haven’t you done what you said you were going to do yesterday?”

“Why is this story 13 points? Someone has done something like this with 5 points?”

You see, with daily standup, story point size, and a velocity chart, it is so easy to turn the whole Scrum process into micromanagement. 
It is worse than it was in Waterfall days, because now you have to justify your work every day! 
Morale and innovation are killed in this day-after-day grinding process.

This kind of micromanagement hurts senior engineers most. 
Senior engineers know from experience 
how to approach a technical issue, 
how to break things down into chunks of work, 
how to plan their work based on those chunks, and at what moment they should stop writing feature code and start refactoring. 
I would like them to share their thinking process so that junior engineers can learn from them, 
but I would not, for the purpose of a neat and pretty burn down chart, 
ask them to break small things down into even smaller tasks or to make up “technical stories” to be approved 
before they start working on them (unless of course the “technical stories” are of high impact; 
but if so, senior as they are, they must know when to bring them up and involve others in the discussion).


Invest on skills, not on processes
----------------------------------

Strapping a process, a strict one like Scrum, on the same people having the same mindset and skillset, 
and expecting a miraculous result (capable of embracing changes) is not realistic. 
There are two layers of Agile, each calling for different mindset and skills.

> 1. Product level. One of the common misconceptions I heard is “we have a fixed scope, so we can’t be agile”. 
To this, my question is “Is this fixed scope guaranteed to deliver the value that it promises, or does it contain assumptions?” 
If a product manager clings to his/her list of features, it is more likely that he/she doesn’t know which feature will strike gold, 
and so he/she wants to deliver them all. Even if you have a feature list directly from end users, 
chances are that they will change their minds upon seeing or using these features.
 In Agile, product development calls for an experimental mindset, treating features as assumptions to be validated. 
 It will be very discomforting for someone who is accustomed to a feeling of certainty (even if it is just an illusion) to transition to this sort of trial-and-error style. 
 Besides the mindset change, the product team and the delivery team also need to practice and master the skills required to validate assumptions quickly.
 Just like a scientific experiment, they need to first have a hopeful hypothesis, design an experiment, and gather data to prove or disprove the hypothesis.
 This structured approach of “trial-and-error” will ease the fear of chaos.
> 2. Delivery level. Since Scrum is so easily misused despite its good intensions, if one is brave enough to try Scrum, 
I suggest trying CICD (continuous integration and continuous delivery) at the same time. 
If your business model doesn’t allow you to continuously deliver your product to end users,
 continuously delivering the product to a demo environment or staging environment is still useful. 
CICD counteracts Scrum traps in the following ways:
>> 1. It balances the “user centric” bias. User stories encourage users’ participation and make sure software is focused on maximizing that elusive 20% of features, 
but it doesn’t mean users know how to or even have the right to direct development work. 
To make CICD successful, code has to be maintained healthy. 
Accumulated technical debt will throw a wrench into the CICD chain. If technical debt is ignored and piled on, the CICD chain will quickly break.
>> 2. CICD really challenges teams’ capabilities. 
It requires advanced technical skills to oil the chain and make it run smoothly.
It requires the product to be well-designed and written for testability. 
What emerges from the CICD chain is working software, which is what really should be measured, not story points or velocity charts.

One good thing about CICD is that it contains a lot of information which is naturally captured from teams’ actions, for example:

> 1. From the source control system, you can perform code static analysis and understand if technical debt is accumulating over time; 
you can also get information as to how actively team members are participating in code reviews. For example, 
if you are using Git, you can analyze how quickly pull requests are merged and how many comments are posted. 
This can give you a clue as to whether teams are following good practices and working together closely.
> 2. From the build system, you can see how many builds fail each day and how quickly a failed build is fixed. 
This will give you a clue as to code quality and teams’ discipline.
> 3. From the defect system, you can analyze how many defects are captured by automation and how many by manual tests. 
You can further categorize defects into groups such as usability defects, security defects, performance defects, and functional defects. 
Each group might point to areas that teams need to strengthen.

One good way to hone your systems thinking skills is to gather information from multiple areas and analyze their relationship, 
instead of just focusing on one set of information (such as velocity) and optimizing one single part.

A common problem that affects CICD is lack of automation or lack of stable automation. 
A manager without systems-thinking skills will simply push for teams to write more automation tests. 
What is wrong with this approach? It violates the 11 laws of systems-thinking (Senge):

> 1. Today's problems come from yesterday's solutions.
> 2. The harder you push, the harder the system pushes back.
> 3. Behavior grows better before it grows worse.
> 4. The easy way out leads back in.
> 5. The cure can be worse than the disease.
> 6. Faster is slower.
> 7. Cause and effect are not always closely related in time and space.
> 8. Small changes can produce big results – but the areas of highest leverage are often the least obvious.
> 9. You can have your cake and eat it too – but not all at once.
> 10. Dividing an elephant in half does not produce two small elephants.
> 11. There is no blame.

Every software manager will probably have witnessed several corpses on the journey to accumulated technical debt; 
they should in theory understand the damage resulting from technical debt. 
So why is it so hard for them to resist the temptation of a symptomatic fix – in this example, pushing teams to write more automation? 
Part of the reason lies in the above laws, in particular, law 3 (behavior grows better before it grows worse) and law 7 (cause and effect are not always closely related in time and space). 
Having more automation tests, even if they are badly written, can be useful in the short term, until the burden of maintenance outweighs the benefits. 
Hopefully with CICD, the feedback delay will be shortened and the accumulating technical debt will be revealed quickly.

Part of the reason is in law 4 (the easy way out leads back in). The more experienced a manager is, the more entrenched his mental mode might be. 
"Mental models" are deeply ingrained assumptions, generalizations, or even pictures or images that influence how we understand the world and how we take action. 
Very often, we are not consciously aware of our mental models or the effects they have on our behavior (Senge).
In this example, what is the underlying mental model for the manager?

![alt ](https://cdn.infoq.com/statics_s1_20160831-0533u1/resource/articles/how-make-agile-successful/en/resources/53.jpg)

As pointed out by Peter Senge, the manager probably won’t even be aware of his mental model, 
he certainly won’t admit that he thinks testers are lazy or stupid or that it is the testers’ job to perform “quality assurance”. 
Scrum’s practice of having a cross-functional team is useful, because it brings together people with widely different perspectives. 
It is the manager’s job to build a trusting environment, so that different mental models can surface and get challenged, including, probably most importantly, 
his own mental model.

While discovering and probing into deeply-held mental models, the team might ask:

> 1. Is the system written for testability? A system written without testability in mind is hard to perform unit and API tests on, 
and testing is therefore done more on the UI level, which is fragile.
> 2. Should developers have a testing mindset? Most developers know how to use XUnit, 
but knowing how to write testMyMethod is not enough. They need to think like a tester: 
where might this method fail, what if this parameter is null, and what will happen if this method fails.
> 3. Should testers have good programing skills? Technical debt is a well-known concept these days, but test technical debt doesn’t get enough attention.
Automation test is code, and requires good programing skills as well. 
The automation framework needs to be written in a way that testers with less programming skills can easily write automation tests. 
Like production code, automation tests need to be stable and perform well. 
And since automation test cases serve as documentation for the system, they must be readable. 
Badly-written automation test cases are not assets but debts.
> 4. Do developers and testers know how to work with each other? While discussing user stories, are testers pointing out vulnerable areas for developers? 
Are developers considering testability? 
Or are developers handling user stories over to testers, and testers subsequently checking whether developers have done what they said they did?
> 5. Is testing just an activity for verifying software implementation against specifications? 
Or can testing be used to flesh out specifications and drive system design? 
This is probably a mental model leap for both developers and testers, a new skill for both to master.

Agile is hard, it will expose more issues more quickly, it is a challenge for both the team and management.
I’ve witnessed teams that have been paralyzed by issues cropping up constantly, 
they tried to use the same solutions or mental models to solve them, failed, and felt helpless. 
As Albert Einstein said, “We cannot solve our problems with the same thinking we used when we created them.” It is a learning journey; 
teams that look at issues holistically, understand the short-term and long-term consequences, pick up new skills, and update their mental models will be successful.

About the Author
----------------
![alt](https://cdn.infoq.com/statics_s1_20160831-0533u1/resource/articles/how-make-agile-successful/en/resources/Chen-Ping.jpg)

Chen Ping lives in Shanghai, China and graduated with a Masters Degree in Computer Science in 2005. 
Since then she has worked for Lucent and Morgan Stanley. 
Currently she is working for HP as a Development manager. 
Outside of work, she likes to study Chinese medicine. 
She blogs [here](http://perfspy.blogspot.kr/).