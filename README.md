# MobileBERT를 활용한 환자 리뷰의 긍,부정 예측

## 1. 개요

### 1.1 의료 서비스의 중요성

의료 기술이 발전함에 따라 환자들의 의료 만족도는 더이상 병원이 제공하는 의료
품질에만 국한되지 않고, 의료 서비스 방면으로 확장되어가고 있다.
[1.참고](https://ir.ymlib.yonsei.ac.kr/bitstream/22282913/137544/1/T005533.pdf)
 앞 참고의 내용을 보면 알다시피 환자가 느끼는
의료 서비스의 수준은 곧 환자의 재방문 의사로 이어짐을 알 수 있다.
이는 의료 수준의 차별성으로는 다른 병원과의 차이를 두드러지게 낼 수 없는 요즘,
점차 의료 서비스의 중요성이 대두되고 있음을 알려주는 지표로써 볼 수 있다?
### 1.2 프로젝트 목표
위에서 말했듯, 의료 서비스는 점점 대두되고 있다.
그래서 이 프로젝트는 의사에 대한 환자의 리뷰를 입력받고 긍, 부정데이터로 나눈
뒤 다른 환자의 리뷰를 입력했을 때
그 리뷰가 긍정일지 부정일지 예측해보는 코드를 짜 실행해보고자 한다.
## 2.원시 데이터

### 2.1 데이터 구성

- 데이터명

  
|index|rating| comment |
|-----|------|---------|
| 색인 | 평가 | 리뷰 |
- 데이터 예시

  
| index | rating | comment |
|--------|--------|---------|
| 0 | 2.0 |Ich bin franzose und bin seit ein paar Wochen inmuenchen. Ich hatte Zahn Schmerzen und mein Kollegu...|
| 1 | 6.0 |Dieser Arzt ist das unmöglichste was mir in meinem Lebenje begegnet ist,er ist unfreundlich ,sehr h...|
| .. |...|...|
| 439278 | 1.0 |Prof. Herbort hat mein vorderes KB sehr gut operiert.Gute Aufklärung (welche Sehne wird genommen), ...|
| 439279 | 1.0 |Beste Kompetenz. Vertrauensverhältnis von Beginn an sehrhoch. Erklärung 1a. &lt;br /&gt; 100% Zufriedenhe...|
