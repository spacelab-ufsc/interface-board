SRC=main
TARGET=IIP_doc

ifndef BUILD_DIR
	BUILD_DIR=build
endif

all:
	mkdir -p $(BUILD_DIR)
	latexmk -pdf -jobname=$(BUILD_DIR)/$(TARGET) $(SRC).tex

index:
	makeindex $(BUILD_DIR)/$(TARGET).nlo -s nomencl.ist -o $(BUILD_DIR)/$(TARGET).nls

view:
	evince $(BUILD_DIR)/$(TARGET).pdf &

clean:
	rm $(BUILD_DIR)/* figures/*.eps header/*.aux chapters/*.aux references/*.aux
