# 결측치인 컬럼 제거하기
  - `df = df.dropna(subset=['컬럼명'])`
  - 제거 후 확인 : `df.isna().sum()` >> 결측치가 없어졌음을 확인
