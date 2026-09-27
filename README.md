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

- 3번 : 홀수를 입력하고, * 표로 모래시계를 만드시오.

#include <stdio.h>

	int main() {
		int N;
		scanf_s("%d", &N);
	
		for (int i = 0; i <= N / 2; i++) {
			for (int j = 0; j < i; j++)
				printf(" ");
			for (int j = 0; j < N - 2 * i; j++)
				printf("*");
			printf("\n");
		}
	
		for (int i = N / 2 - 1; i >= 0; i--) {
			for (int j = 0; j < i; j++)
				printf(" ");
			for (int j = 0; j < N - 2 * i; j++)
				printf("*");
			printf("\n");
		}
		return 0;
	}

- 4번 : 주사위를 6000번 던질때 1부터6이 나올 확률을 구하시오.

		#include <stdio.h>
		#include <stdlib.h>
		#include <time.h>
		
		int main() {
			int count[7] = { 0 };
			srand(time(NULL));
		
			for (int i = 0; i < 6000; i++)
				count[(rand() % 6) + 1]++;
			
			for (int i = 1; i <= 6; i++) 
				printf("%d가 나올 확률은 = %.2f%%\n", i, count[i] / 6000.0 * 100);
			return 0;
		}


