SRC=main
TARGET=slb-iip-doc-v1.0

ifndef BUILD_DIR
	BUILD_DIR=build
endif

PDF_READER=evince

all:
	mkdir -p $(BUILD_DIR)
	latexmk -pdf -jobname=$(BUILD_DIR)/$(TARGET) $(SRC).tex
	cp -f $(BUILD_DIR)/$(TARGET).pdf .

index:
	makeindex $(BUILD_DIR)/$(TARGET).nlo -s nomencl.ist -o $(BUILD_DIR)/$(TARGET).nls

view:
	$(PDF_READER) $(BUILD_DIR)/$(TARGET).pdf &

clean:
	rm $(BUILD_DIR)/* figures/*.eps header/*.aux chapters/*.aux references/*.aux
