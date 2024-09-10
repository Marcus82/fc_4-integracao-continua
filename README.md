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
