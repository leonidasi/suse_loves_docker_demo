all :: sles11sp3 sles12
	@echo 'DONE'

webapp ::
	cd webapp_demo; make

sles12 :: webapp
	@echo Building SLE12 demo image
	docker build -f Dockerfile-sles12 -t sles12_webapp .

sles11sp3 :: webapp
	@echo Building SLE11SP3 demo image
	docker build -f Dockerfile-sles11sp3 -t sles11sp3_webapp .

clean ::
	rm webapp_demo/webapp_demo
	docker rmi sles11sp3_webapp
	docker rmi sles12_webapp
