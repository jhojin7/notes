# Tecnical Writing One
https://developers.google.com/tech-writing/one

## Words
- 새롭거나 불확실한 워딩은 새로 정의해주기 (이미 다른데서 정의한거면 거기로 링크)
	- 새로 정의할게 많으면 Glossary를 만들어라
- A라고 하기로 한 단어를 뒤에 Aa라고 쓰지 말자. 독자가 compile하기 힘들다.
	- 단어를 줄여쓸거면 처음 언급할 때 줄임말도 같이 언급한다
	- ex) "Protocol Buffers (or protobufs for short) ..."
- 대명사: 명사가 나온 이후에 대명사를 사용 할 것.
- 대명사와 명사는 최대한 가까이 사용하기. (보통 5단어)
- this나 that 같은게 지칭하는게 모호할 경우, 문장을 여러개로 나눠서 explicitly 설명할것.

## Active Voive vs. Passive Voice
- 능동태 vs수동태
- 선결론: 능동태 써라.
- "Code ~is interpreted~ by python, but code ~is compiled~ by cpp" 
	- -> "Python interprets code, but cpp compiles code" 이렇게.
-  active voice를 써야하는 이유
	-  passive하게 쓰면 읽는 사람이 머릿속에서 한번 굴려서 해석해야함. 
	-  내용전달이 흐려짐.
	-  어떤 경우엔 목적어가 사라져서 해석하기 힘들어짐.
	-  active가 대부분 짧음.
-  리서치 같은 글에서도 수동태를 쓰면 정보가 불분명해짐. 
	-  누가 누구한테 무얼 했는지? 어떤 정보인지? -> 직관적으로 알기 힘들어짐.
	-  