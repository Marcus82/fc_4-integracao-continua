-- Executa o código go
go run math.go

-- Criando Branch
git checkout -b feature/ 
git push origin feature/ci

--Apagar o Branch feature/ci 
git checkout develop 
git pull origin develop 
git branch -d feature/ci


git checkout -b feature/github-matrix
git add .
git commit -m "ci: add different versions to test with go"
git push origin feature/github-matrix

git branch -d feature/github-matrix

-- Gerando imagem para teste
docker build -t teste .

-- Testando a imagem
docker run --rm teste

== Gerando build da imagem via CI
git add .
git commit -m "build: add dockerfile to build docker build"
[github.com/marketplace/actions/build-and-push-docker-images](https://github.com/marketplace/actions/build-and-push-docker-images)