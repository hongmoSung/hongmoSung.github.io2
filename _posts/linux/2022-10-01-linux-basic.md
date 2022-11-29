---
title: "linux 디렉토리와 파일"
categories:
  - linux
tags:
  - directory
  - file
toc: true
---
리눅스 시스템에서 파일과 디렉터리 관리에 사용되는 명령어  
리눅스 시스템은 계층적으로 구성된 디렉터리 구조에 파일을 보관한다.  
계층적 디렉터리(폴더) 구조란 트리 형태 안에 다수의 디렉터리가 존재한다는 의미이다.  
여기서 각 디렉터리는 다수의 파일과 서브 디렉터리를 포함할 수 있다.  

다른 운영체제와 다른 점은 전체적으로 하나의 파일 시스템으로 관리되고 다루어진다는 점이다.  
이러한 계층 구조에서 가장 사위의 디렉터리를 루트(/) 디렉터리라고 한다.  

### 파일 시스템 탐색
- #### ls (list segments) : 디렉터리의 내용 출력
    ```shell
    > ls [opstions] [names]
    ```
    
    | 짧은 옵션 | 긴 옵션              | 설정                                                              |
    |:------|:------------------|:----------------------------------------------------------------|
    | -a    | --all             | 모든 파일을 리스트 한다. (.도트)로 시작하는 숨김 파일도 보여 준다.                        |
    | -d    | --directory       | 디렉터리 자체에 대한 정보를 보여 준다.                                          |
    | -F    | --classify        | 우측에 파일의 종류를 알려 주는 문자를 붙여 보여준다. ex) 실행 파일은 +, 디렉터리는 /, 심벌릭 링크는 @ |
    | -h    | --human--readable | 파일 크기 포멧을 변경해 보여 준다.                                            |
    | -i    | --inode           | 왼쪽에 inode 번호를 보여 준다.                                            |
    | -l    | --format=long     | 긴 포멧으로 결과를 보여 준다.                                               |
    | -r    | --reverse         | 역순으로 결과를 보여준다. (ls는 기본적으로 알파벳순)                                 |
    | -R    | --recursive       | 재귀적으로 수행하여 서브 디렉터리 내용도 나열한다.                                    |
    | -S    | --sort=size       | 파일의 크기 순서로 결과를 보여 준다.                                           |
    | -t    | --sort=time       | 최종 수정 시간 순으로 보여 준다.                                             |

- #### cd (change directory) : 현재 작업 디렉터리의 이동
    ```shell
    > cd [directory]
    ```
  
    | 기호/환경 변수 | 설명                                          |
    |:--------------------------------------------|:--------------------------------------------|
    | $HOME    | 홈 디렉터리의 이름을 저장하는 환경 변수이다.                   |
    | ~        | 셀 명령에서 사용할 때 홈 디렉터리를 의미하는 기호이다. ex) ~사용자 계정 |
    | .        | 현재 작업 디렉터리를 의미                              |
    | ..       | 현재 작업 디렉터리의 부모 디렉터리를 의미하는 기호                |
    | $PWD     | 현재 작업 디렉터리를 저장한 환경 변수이다.                    |
    | $OLDPWD  | 현재 작업 디렉터리의 이전 작업 디렉터리를 저장한 환경 변수이다.        |  
- file
- pwd

### 파일 디렉터리 관리
- mkdir
- rmdir
- cp
- mv
- rm

### 파일 내용 확인
- more
- less
- head
- tail
- cat

## 참조
- [UNIX 시스템](http://www.yes24.com/Product/Goods/86687341)
- [생활코딩 리눅스 강좌](https://www.inflearn.com/course/생활코딩-리눅스-강좌)