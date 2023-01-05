---
title: "[Algorithm] 백준 문제 풀이 (2798번 블랙잭)"
date: 2021-01-04
categories: [Public]
tags: [algorithm]
---

[문제 링크](https://www.acmicpc.net/problem/2798 "블랙잭")

---

#### 문제 풀이 과정

이 문제는 이전에 종만북에서 살짝 공부했던 완전탐색 알고리즘을 써서 푸는 문제다. (물론 다른 방법도 있겠지만 브루트포스 알고리즘 카테고리에 있었다.)<br>
완전탐색 문제인 만큼 재귀함수를 이용해 풀기로 했다.<br>
base case는 다음과 같이 설정했다.<br>
1. 카드 3장의 합이 M보다 클 때 -> 최대합을 업데이트하지 않고 그대로 반환한다.
2. 카드 3장의 합이 M보다 작거나 같을 때 -> 최대합과 비교하여 둘중 큰 값으로 최대합을 업데이트하고 반환한다.


완전탐색 알고리즘은 아주 기초적인 알고리즘이기에 어렵지 않게 풀 수 있었다. 재귀함수를 설계하는건 늘 어려워서 고민을 하긴 했지만 이전에 공부했던 구조대로 코드를 구성하니 나름 수월하게 풀 수 있었다.

<전체 코드>
~~~cpp
#include <iostream>
#include <vector>
using namespace std;

int calcMaxSum(int limit, vector<int>& cards, int toPick=3, int sum=0, int next=0, int maxSum=-1);

int main() {
	int cardCount, limit;
	cin >> cardCount >> limit;
	vector<int> cards;
	for (int i = 0; i < cardCount; i++) {
		int temp;
		cin >> temp;
		cards.push_back(temp);
	}
	cout << calcMaxSum(limit, cards);
}

int calcMaxSum(int limit, vector<int>& cards, int toPick, int sum, int next, int maxSum) {
	if (toPick == 0) {
		if (sum > limit) return maxSum;
		if (sum <= limit) {
			maxSum = maxSum < sum ? sum : maxSum;
			return maxSum;
		}
	}
	for (int i = next; i < cards.size(); i++) {
		sum += cards[i];
		maxSum = calcMaxSum(limit, cards, toPick - 1, sum, i + 1, maxSum);
		sum -= cards[i];
	}
	return maxSum;
}
~~~
