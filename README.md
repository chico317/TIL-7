# TIL-7
# concat과 merge의 차이
concat :
axis=0 행을 기준으로 위아래로 같은 컬럼끼리 값을 이어 붙여 새로운 행을 만듦
axis=1 컬럼을 기준으로 인덱스가 같은 값을 옆으로 붙여 새로운 컬럼을 만듦
merge :
index 혹은 특정 컬럼 값을 기준으로 두 개의 데이터프레임을 연결

df[df['Quantity'] < 0] : cancle 시킨 것 마이너스 값으로 

*아주 긴 url의 경우 f-string으로 연결시켜줄수 있다.
page_no : 입력값으로 페이지 번호를 입력하면 해당 번호의 데이터를 가져옴
start_no : 입력받은 page_no로
예시)
def get_seoul_covid_100(page_no):
    start_no = (page_no-1)*100
    url = url = 'https://news.seoul.go.kr/api/27/getCorona19Status/get_status_ajax.php?draw=2'
    url=f'{url}&columns%5B0%5D%5Bdata%5D=0&columns%5B0%5D%5Bname%5D=&columns~~
    url=f'{url}&order%5B0%5D%5Bdir%5D=desc&start=100&length=100&search%5Bvalue%5D=&search%5Bregex%5D=true~~
    response = requests.get(url)
    data_json = response.json()
    return data_json
    
* time.sleep 시차를 두기 위해 / tqdm : 진행상태를 표시하기 위해
* num = re.sub('[^0-9]',"",num_string): 0~9에 해당되지않는것은 공백으로 치환
