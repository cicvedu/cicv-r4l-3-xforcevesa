KDIR ?= ../../../linux/

# Build Rust for Linux Module
LLVM?= 1

ifeq ($(LLVM), 1)
    RUSTC_FLAGS := $(RUSTC_FLAGS) -C opt-level=2 -C lto
endif

# Build the Rust kernel module
$(KDIR)/build:
	@echo Building Rust kernel module...
	$(MAKE) LLVM=$(LLVM) -C $(KDIR) M=$$PWD	
