# 정사각형

평면에 다각형이 하나 주어진다. 주어지는 다각형은 꼭지점이 6개인 L자 모양의 다각형이다. 다각형은 항상 모든 변이 가로와 세로 방향으로만 있으며, 다음과 같은 형태로 주어진다. 4개의 변의 길이가 주어지는데, 우선 가장 왼쪽 위 꼭지점에서 오른쪽으로 나가는 변의 길이가 주어진다. 그 다음 시계 방향으로 가면서 연속으로 있는 3개의 변의 길이가 주어진다.

![그림 1](images/1508726001567_pic1.png)

이 문제에서 풀고 싶은 것은, 주어진 다각형 **안에** 그릴 수 있는, 변의 길이가 K이하인 정사각형의 개수이다. **정사각형들의 일부가 겹치는 것은 전혀 상관이 없다.** 여기서 다루는 정사각형은 변이 주어진 다각형과 평행해야 한다. 또, 정사각형의 모든 꼭지점과 주어진 다각형의 꼭지점과의 가로 방향 거리와 세로 방향 거리가 모두 정수라야 한다. 위의 예에서, 주어진 다각형 안에 그릴 수 있는 변의 길이가 1인 정사각형은 14개가 있음을 알 수 있다. 변의 길이가 2인 정사각형을 생각해 보면 모두 7개가 있음을 알 수 있다. 따라서, K=2라면 답은 21이 된다.

한가지 주의할 점은 입력으로 주어지는 변의 길이들 중 세번째 값은 0일 수 있다는 것이다. 이 경우 주어지는 다각형이 직사각형이라고 생각하면 된다. 첫번째, 두번째, 네번째 값은 항상 0보다 크다.

다각형의 변의 길이와 정사각형의 변의 길이의 제일 큰 값을 입력으로 받아서 그릴 수 있는 정사각형의 개수를 출력하는 프로그램을 작성하라.

## 입력 형식

첫째 줄에 정수 a, b, c, d, K가 주어진다. 정수 a, b, d, K는 모두 0보다 크다. 정수 c는 0 혹은 양수이다. 모든 값은 100 보다 작거나 같다.

## 출력 형식

한 줄에, 문제에서 설명한 대로 그릴 수 있는 정사각형의 개수를 출력한다.

## 입력 예제

```
3 2 1 2 2
```

## 출력 예제

```
21
```

## 채점 방식

입력 케이스들은 다음과 같은 종류로 구별되며, 한 종류의 케이스를 다 맞추어야 그 종류에 배정된 점수를 받을 수 있다.

* 종류1 (10점): c = 0, K = 1 이다.
* 종류2 (10점): K = 1 이다.
* 종류3 (10점): c = 0 이다.
* 종류4 (40점): 문제의 원래 제한조건 이외의 추가된 제한이 없음.

## 해설

<접기>포함과 배제의 원리를 이용하면 쉽게 해결할 수 있는 문제이다. for문으로 정사각형의 크기 s를 정한 뒤, 크기가 s인 정사각형을 놓을 수 있는 갯수를 간단한 수식으로 구할 수 있다.</접기>
