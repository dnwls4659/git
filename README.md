# Git 관리 방법

1. master(development)
2. docs/git-flow 

* master 브랜치를 기준으로 docs/git-flow 브랜치를 딴다.

```shell
$ git checkout -b docs/git-flow
```

* 브랜치를 따고 아래와 같이 문서화를 한다.(작업 예시)
> 다음과 같은 요구사항을 반드시 지켜야 한다.
> 
> * 본인이 작업한 내용들이 담긴 브랜치의 커밋 내역을 하나로 합친 후 force push를 한다.
> * force push가 되었으면 master 브랜치로 Github에서 PR을 생성한다.

```text
(1). 커밋 스쿼시하기
1-1. Git Kraken에서 docs/git-flow 브랜치에서 스쿼시할 여러 커밋들을 선택한다.
1-2. 가장 오래된 커밋을 우클릭한 후, "Squash N commits"를 선택한다.
1-3. 브랜치 성격을 딴 커밋 메시지를 입력하여 스쿼시된 커밋을 대표할 메시지를 작성한다.

(2). master(development) 브랜치 기준으로 리베이스하기
2-1. master(development) 브랜치를 우클릭한다.
2.2. "Rebase 'docs/git-flow' onto 'master(development)'"를 선택한다.
2-3. 충돌이 감지되었다면 해결 후 "Continue rebase"를 선택한다.

(3). force push하기
3-1. Git Kraken에서 Push 버튼을 클릭한다.
3-2. Force push 옵션을 활성화한다.
3-3. Force push 버튼을 클릭 후 docs/git-flow 브랜치를 원격 저장소에 강제 푸시한다.

(4). Github에서 PR 병합하기
4-1. Github에서 PR을 생성한다.
4-2. PR이 생성되면 Merge 드롭다운에서 "Rebase and merge"를 선택한다.
4-3. 4-2와 같이 진행하는 이유는 커밋 히스토리를 리니어하게 가져가야 하기 때문이다.
```

# 참고사항

* 모르면 모른다고 달려가서 바로 질문하지말자.
* 모르면 모르는 것을 인정해야한다. 질문하기 앞서 내가 어디가 부족하고 어디까지 이해했는지를 구구절절 설명하지 않고 깔끔하게 정리해서 전달하고 다른 분들의 생각을 여쭤본다.
* 질문을 할 때는 내가 이해한 내용을 바탕으로 질문을 한다. 질문을 통해 내가 이해하지 못한 부분을 명확히 하고, 다른 사람의 의견을 듣는다.
* 인간은 망각의 동물이다. 실수는 반복되면 실력이 된다. 그런 실수를 반복하지 않기 위해서 위와 같이 겪었던 실수들을 다시 재발하지않게끔 해야 한다.