## 🔗 서브 모듈 생성 방법
✔️ 서브 모듈 사용이유 : 공통으로 사용하는 코드를 서브 모듈에 적용함 -> 본인 레포지토리에 서브 모듈이 있는 경우는 수정하면 안됨 pull만 해야함 but, 한번 잘못하면 삭제 하기 힘들어서 잘 안사용함

>1. 본인의 레포지토리에서 `git submodule add 서브모듈_주소 서브모듈_생성이름` ➡️  서브모듈 생성
>
>2. `git add .` ➡️ 변경 사항 커밋
>
>3. `git commit -m "커밋메세지"` ➡️ 커밋 메세지
>
>4. `git push origin 브랜치명` ➡️ git에 푸시

</br>

## 🔄 서브 모듈 업데이트 방법
>1. `git submodule update --remote` ➡️ 서브 모듈 업데이트
>
>2. `git push  origin 브랜치명` ➡️ git에 푸시

</br>

## ⛓️‍💥 서브 모듈 삭제 방법 
⭐️ 커밋 및 add 아직 안한 변경사항 복구는 `git restore .`

>1. `git config -f .gitmodules --remove-section submodule.modules` ➡️ `.gitmodules` 파일에서 서브모듈 정보 삭제
>
>2. `git config --remove-section submodule.modules` ➡️ `.git/config` 파일에서 서브모듈 정보 삭제
>
>3. `rm -rf .git/modules/modules` ➡️ `.git/modules`에서 서브모듈 내부 데이터 삭제
>
>4. `rm -rf modules` ➡️ 서브모듈 디렉터리 삭제
>
>5. `git add .gitmodules` ➡️ 변경 사항 커밋
>
>6. `git rm --cached modules` ➡️ modules를 git  추적 대상에서 제거하는 명령어
>
>7. `git commit -m "Remove submodule: modules` ➡️ 커밋 메세지
>
>8. `git push origin 브랜치명` ➡️ git에 푸시

