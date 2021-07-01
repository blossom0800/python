# groupby로 추출해낸 series를 다시 df로 바꾸기
  - `df.groupby("Country")["id_null"].mean().to_frame()`
  - Series에서 `.to_frame()`을 붙여서 df로 변환해줌
