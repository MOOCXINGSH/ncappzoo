.PHONY: all
all: ilsvrc12 gendernet googlenet squeezenet alexnet

.PHONY: ilsvrc12
ilsvrc12:
	@echo "\making ilsvrc12"
	(cd ../../data/ilsvrc12; make;)

.PHONY: gendernet
gendernet: 
	@echo "\nmaking gendernet"
	(cd ../../caffe/GenderNet; make compile;)

.PHONY: googlenet
googlenet: 
	@echo "\nmaking googlenet"
	(cd ../../caffe/GoogLeNet; make compile;)

.PHONY: squeezenet
squeezenet:
	@echo "\nmaking squeezenet"
	(cd ../../caffe/SqueezeNet; make compile;)

.PHONY: alexnet
alexnet:
	@echo "\nmaking alexet"
	(cd ../../caffe/AlexNet; make compile;)


.PHONY: run
run: all
	@echo "\nRunning image-classifier.py";
	python3 image-classifier.py

.PHONY: help
help:
	@echo "possible make targets: ";
	@echo "  make help - shows this message";
	@echo "  make all - makes the following: run";
	@echo "  make run - runs the stream_infer program";
	@echo "  make clean - removes all created content and temporary files";

clean: clean
	@echo "\nmaking clean";
	(cd ../../data/ilsvrc12/; make clean;);
	(cd ../../caffe/GenderNet; make clean;);
	(cd ../../caffe/GoogLeNet; make clean;);
	(cd ../../caffe/SqueezeNet; make clean;);
	(cd ../../caffe/AlexNet; make clean;);
