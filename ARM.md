# What is ARM(Association Rule Model)? 
  :하나의 거래나 사건에 포함되어 있는 항목들의 경향을 파악해서 상호 연관성을 발견하는 것.
  
## Apriori node
  : 모든 항목집합에 대한 지지도를 계산하지 않고 원하는 빈발항목집합을 찾아내는 데 이용되는 선험적 규칙.
    if 한 항목집합이 빈발, 이 항목집합의 모든 부분집합 역시 빈발항목집합.

- support 지지도
    : 전체 거래 중 항목 X와 항목 Y를 동시에 포함하는 거래가 어느 정도 인가
      S = P(XnY)
- confidence 신뢰도
    : 항목 X를 포함하는 거래 중에서 항목 Y가 포함될 확률은 어느 정도 인가
      C = P(Y|X) = P(XnY)/P(X)
- Lift 향상도
    : 항목 X를 구매한 경우 그 거래가 항목 Y를 포함하는 경우와 항목 Y가 X와 무관하게 임의로 구매되는 경우의 비율
      L = P(Y|X)/P(Y) = P(XnY)/P(X)P(Y)
      if L > 1, positive correlation
         L < 1, negative correlation
         L = 1, independent correlation (coincedence)
         
- Field of Products need to be types of flag(이분) or set(범주)
