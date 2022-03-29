version = 1.24.0
build: Dockerfile
	docker build -f Dockerfile  -t "mlflow:${version}" --build-arg version=${version} .

deploy:
	docker tag mlflow:${version} xiaofine/mlflow:${version} 
	docker tag mlflow:${version} xiaofine/mlflow:latest

	docker push  xiaofine/mlflow:${version} 
	docker push  xiaofine/mlflow:latest


all: build deploy
	