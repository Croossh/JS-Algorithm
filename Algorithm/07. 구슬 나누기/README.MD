#회고

서로다른 구슬 n개 중 m개를 뽑는 경우의 수 공식<br>
👉 n! / (n - m)! \* m! <br>

<br>
자주 쓰는 팩토리얼을 함수화시켜 두었다.
```javascript
const factorial = (num) => {
        let res = 1;
        for(let i = num; i >= 2; i--){
            res *= i;
        }
        return res;
    }
```
<br>
마지막엔 Math.round로 반올림 처리해주었다.

## 추가

30! 경우 2.652528598121911e+32 로 자바스크립트가 표현할 수 있는 수를 넘어서 저렇게 표기가 되었다.<br>
다른 언어는 자료형을 먼저 선언하여 메모리 크기를 정하게 되는데, js는 메모리크기를 따로 정하지 않아 생긴 문제이다.<br>
<br>
이런 경우 BigInt를 통해 265252859812191104246398737973248 로 표현할 수 있는 방법을 알게되었다.<br>
※ 프로그래머스 문제 자체에서 BigInt를 적지 않아도 정답처리되어 이번 문제에서는 패스하였다.
