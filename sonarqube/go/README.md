== Executa o código go
go run math.go

== Criando Branch
git checkout -b feature/ci 
git push origin feature/ci

== Commit
git add .
git commit -m "ci: add feature to push docker image to docker hub"
git push origin [NOME_BRANCH]

== Apagar o Branch feature/ci 
git checkout develop 
git pull origin develop 
git branch -d feature/ci


== Gerando imagem para teste
docker build -t teste .

== Testando a imagem
docker run --rm teste

== Gerando build da imagem via CI
[github.com/marketplace/actions/build-and-push-docker-images](https://github.com/marketplace/actions/build-and-push-docker-images)


== Dando push na imagem automaticamente

==============================================================
Sonarqube
==============================================================
1) Iniciando com Sonarqube
https://www.sonarsource.com/products/sonarqube/
2) Conceitos principais
3) Instalando primeiro projeto 

token criado
goproject: sqp_a13318f7e4d36d3770a1d6cf228436e8a4b7ec55

executando o sonar-scanner
sonar-scanner \
  -Dsonar.projectKey=go-project \
  -Dsonar.sources=. \
  -Dsonar.host.url=http://localhost:9000 \
  -Dsonar.token=sqp_a13318f7e4d36d3770a1d6cf228436e8a4b7ec55
  
4) Trabalhando com cobertura de código
5) Cobrindo código Javascript
6) Preparando ambiente para SonarCloud
[sonarcloud.io](https://www.sonarsource.com/products/sonarcloud/)

sonarqube/go > git init
sonarqube/go > git status

git add .
git commit -m "feat: add sum function"
