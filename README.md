# TIL-7
# concat과 merge의 차이
concat :
axis=0 행을 기준으로 위아래로 같은 컬럼끼리 값을 이어 붙여 새로운 행을 만듦
axis=1 컬럼을 기준으로 인덱스가 같은 값을 옆으로 붙여 새로운 컬럼을 만듦
merge :
index 혹은 특정 컬럼 값을 기준으로 두 개의 데이터프레임을 연결

df[df['Quantity'] < 0] : cancle 시킨 것 마이너스 값으로 
