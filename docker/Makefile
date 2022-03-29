version = 1.24.0
build: Dockerfile
	docker build -f Dockerfile  -t "mlflow:${version}" --build-arg version=${version} .

deploy:
	docker tag mlflow:${version} registry.cn-hangzhou.aliyuncs.com/meetwhale/mlflow:${version} 
	docker tag mlflow:${version} registry.cn-hangzhou.aliyuncs.com/meetwhale/mlflow:latest

	docker push  registry.cn-hangzhou.aliyuncs.com/meetwhale/mlflow:${version} 
	docker push  registry.cn-hangzhou.aliyuncs.com/meetwhale/mlflow:latest


all: build deploy
	