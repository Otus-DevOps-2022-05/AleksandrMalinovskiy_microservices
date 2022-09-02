.DEFAULT_GOAL := help
help: ## Показать доступные команды для make
	@grep -E '^[a-zA-Z_-]+:.*?## .*$$' $(MAKEFILE_LIST) | sort | awk 'BEGIN {FS = ":.*?## "}; {printf "\033[36m%-30s\033[0m %s\n", $$1, $$2}'

ps: ## Cписок запущенных контейнеров
	      docker ps --size
bld-ui: ## Сборка ui
	      cd src/ui && bash docker_build.sh
bld-post: ## Сборка post
	      cd src/post-py && bash docker_build.sh
bld-coment: ## Сборка coment
	      cd src/comment && bash docker_build.sh
bld-prf: ## Сборка prometheus
	      docker build -t $(USER_NAME)/prometheus monitoring/prometheus/
bld-blbx: ## Сборка blackbox
	      docker build -t $(USER_NAME)/blackbox monitoring/blackbox/
push-ui: ## Пуш образа ui на DockerHub
	      docker push $(USER_NAME)/ui
push-comment: ## Пуш образа comment на DockerHub
	      docker push $(USER_NAME)/comment
push-post: ## Пуш образа post на DockerHub
	      docker push $(USER_NAME)/post
push-prometheus: ## Пуш образа prometheus на DockerHub
	      docker push $(USER_NAME)/prometheus
