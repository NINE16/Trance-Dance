run:

	@docker compose -f docker-compose.yml up -d --build

down:
	@docker compose -f docker-compose.yml down


fclean:
	docker system prune -af

clean:
	@docker stop $$(docker ps -qa);\
	docker rm $$(docker ps -qa);\
	docker rmi -f $$(docker images -qa);\
	docker volume rm $$(docker volume ls -q);\


.PHONY: all re down clean fclean