<!-- glitch

json-server 배포
1) 바탕화면에서 터미널을 실행시키고 json-server 배포를 위한 폴더를 생성해 주세요.
mkdir [폴더명]
​
2) 폴더안으로 이동 합니다.
cd [폴더명]
​
3) nodejs 프로젝트 시작합니다. (package.json 파일 생성)
npm init -y
​
4) vscode 로 프로젝트 열기
code .
​
5) server.js 파일 만들기
// server.js
const jsonServer = require("json-server");
const server = jsonServer.create();
const router = jsonServer.router("db.json");
const middlewares = jsonServer.defaults();

server.use(middlewares);
server.use(router);
server.listen(3000, () => {
  console.log("JSON Server is running");
});
​
6) db.json 파일 만들기
{
  "pharmacies": []
}
​
7) package.json 파일에 scripts 설정
{
	"scripts": {
    "start": "node server.js"
  },
	"devDependencies": {
    "json-server": "^0.17.4"
  }
}
-->
# outsourcing-json-server
