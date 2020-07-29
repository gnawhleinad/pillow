define make-target
$(basename $(1)).pdf: $(1)
	pdflatex $$< $$@
endef

TARGETS := $(wildcard *.tex)
$(foreach t,$(TARGETS),$(eval $(call make-target,$(t))))

.PHONY: all
.DEFAULT_GOAL := all
all: $(foreach t,$(TARGETS),$(basename $(t)).pdf)
