-- Executa o código go
go run math.go

-- Criando Branch
git checkout -b feature/ci 
git push origin feature/ci

--Apagar o Branch feature/ci 
git checkout develop 
git pull origin develop 
git branch -d feature/ci