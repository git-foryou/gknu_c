# gknu_c
## 9/28 1학년 2학기 퀴즈시험 코드

- 1번 : 두 수를 함수를 이용해서 더하시오.

#include <stdio.h>

int Add(int a, int b) { 
	return a + b;
}

int main() {
	printf("%d", Add(11, 22));
	return 0;
}

- 2번 : 숫자 읽고 (*)로 직각 삼각형 그리기.

#include <stdio.h>

int main() {
	int N; 
	scanf_s("%d", &N);

	for (int i = 1; i <= N; i++) {
		for (int j = 1; j <= i; j++)
			printf("*");
		printf("\n");
	}
	return 0;
}
