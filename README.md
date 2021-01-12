# 2021_Q1_PS_Training

각 문제 설명은 코드 아래 주석에 써져있습니다. 아마 블로그에 작성할 예정..? 일주일 1500점이 소목표, 하루 3문제가 목표.

<h2> ABC 162 D</h2>

문제의 내용은 길이 N 배열에서 RGB 한개씩 고르는데, R,G,B사이의 거리가 똑같으면 안된다. 
예를들어 RRGGBB의 경우 2번째 4번째 6번째 글자를 선택할 경우 각 글자 사이의 거리가 2로 똑같기에 이런건 선택하면 안된다. 
R의 갯수, G의 갯수, B의 갯수들을 세주고 각 갯수들을 곱하면 RGB의갯수를 구할수 있으며, 이것들 중에서 같은거를 제외하면된다. 
N이 4000이므로 N^2으로 쉽게 풀 수 있다. 시작점, 글자 사이의 간격을 정하고 단순 조건문으로 풀었다. 

<h2> ABC 163 D</h2>

문제의 내용은 문제를 읽으면 알 수 있다. 영어가 힘들수도 있지만, 사진을 보면 바로 이해할 수 있다. 
K개를 선택하는경우부터 N개를 선택하는 경우들에서 각 경우마다, 몇개의 정수들을 만들 수 있는지 더해주면 된다. 
각 경우에서 몇개의 정수를 만들 수 있는지 알아내는 방법은, 가장 크게 만든수에서 가장 작게 만든수를 빼주면된다. 그 사이에 있는 숫자들은 모두 만들 수 있으므로 이렇게 해주면된다. 
i라는 숫자에서 가장 작게 만들수 있는 수는 0부터 i-1까지를 선택하는 i*(i-1)/2이고, 가장 크게 만들 수 있는 수는 N+1부터 N-i까지를 선택하는 (N*2-i+1)*i/2이다. 

<h2> ABC 164 D</h2>

문제 내용은 i~j번째 수들을 십진수로 해서 2019의 배수들의 갯수를 구하는 문제다. 
S[a](mod m)=S[b](mod m) 이면 S[a]-S[b]는 m의 배수라는걸 이용하면 쉽게 풀린다. 구현 자체에서의 어려움은 없으나 문제를 보고 직관적으로 풀어야해서 어려웠다. 

<h2> ABC 165 D</h2>

문제 내용은 식만 보면 이해할 수 있다. floor(x/B)가 0이면서 x가 가장 큰수는 B-1이다. 만약 X가 B보다 크다면 X=B-1로, X가 B보다 작다면 X로 계산하면 된다. 

<h2> ABC 166 D</h2>

a^5-b^5=X를 만족하는 a,b를 구하면된다. X가 10^9이라는 점을 이용해서 a^5=2*10^9를 구해서 범위를 구해서 단순 반복문으로 계산하면된다. 

2*10^9=2*(2^10)^3=2*2^30=2*(2^6)^6 이므로 -2^7~2^7를 범위로 해서 했더니 맞았다. 
