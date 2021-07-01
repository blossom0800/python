# input
  `np.where(df["컬럼명"].isnull(), 1, 0)` -- 해당 컬럼에 결측치가 있는지 확인해서 True면 1로, False면 0으로 반환하기
# 결과
  `array([0, 0, 0, ..., 0, 0, 0])`
# Note
  sql의 decode랑 비슷한 것 같다
