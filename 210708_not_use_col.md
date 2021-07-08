# 결측치를 확인한 후 쓰지 않는 컬럼을 담을 때
  - `not_use = df.isnull().sum().sort_values(ascending = False).head(안담을 컬럼 수)`
  - `not_use_col = not_use.index` # 컬럼에 담아줄 것이므로 `.index` 처리를 해야 함
