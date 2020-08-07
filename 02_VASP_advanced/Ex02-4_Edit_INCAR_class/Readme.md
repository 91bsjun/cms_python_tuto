# 예제 2-4
- class 를 만들어 INCAR를 수정하는 예제
- 예제 2-2 에서 만든 def 활용

#### 작성 예시
<pre>
class Incar:
    def __init__(self, filename="INCAR"):
        INCAR 파일을 읽어서 dictionary 타입으로 전환
        
    def update(self, input_dict):
        수정할 옵션을 dictionary 타입으로 받아서 업데이트
        
    def write_incar(self):
        dictionary 타입을 INCAR 파일로 쓰게 하는 def
</pre>

#### 실행 예시 1. 파일 직접 실행

<pre>
class Incar:
    def ..
    def ..
    def ..

input_dict = {"ENCUT": 1E-05, "ISIF": 2, "ISYM=0"}
incar_file = "INCAR"

my_incar = Incar(incar_file)
my_incar.update(input_dict)
my_incar.write_incar()
</pre>

#### 실행 예시 2. 외부에서 import 하여 실행
<pre>
import 경로.Incar

input_dict = {"ENCUT": 1E-05, "ISIF": 2, "ISYM=0"}
incar_file = "INCAR"

my_incar = Incar(incar_file)
my_incar.update(input_dict)
my_incar.write_incar()
</pre>
