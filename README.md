## Assignment 3

test 브랜치에서  한개의 커밋을 취소하고 두 개의 커밋을 더한다. 
```
git reset HEAD^
git add .
git commit -m "seventh"
git add .
git commit -m "eighth"
git push origin test
``` 
다음과 같은 상태가 된다. 

![image](https://user-images.githubusercontent.com/68385605/136385567-3ee82519-0c95-4cdb-af50-0a2a2a93acdf.png)

cherry-pick 을 이용해 커밋을 test 브랜치에서 master 브랜치로 가져온다.  
가져올 커밋의 해시는 커밋메시지 seventh, eighth 에 대응하는 커밋의 해시를 가진다.
따라서

```
git checkout master
# 커밋메시지 seventh 에 대응하는 커밋의 해시
git cherry-pick 4e8bedb8
# 커밋메시지 eighth 에 대응하는 커밋의 해시
git cherry-pick d6732006
git push origin master
```

결과화면은 다음과 같다.

![image](https://user-images.githubusercontent.com/68385605/136387124-541d70fd-2115-4e31-9d9c-afffaab23a8b.png)


Assignment 3 완료. 


