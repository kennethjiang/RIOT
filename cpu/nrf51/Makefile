# define the module that is build
MODULE = cpu

# add a list of subdirectories, that should also be build
DIRS = periph $(RIOTCPU)/cortexm_common $(RIOTCPU)/nrf5x_common

# build one of the radio drivers, if enabled
ifneq (,$(filter radio_nrfmin,$(USEMODULE)))
    DIRS += radio/nrfmin
endif

# (file triggers compiler bug. see #5775)
SRC_NOLTO += vectors.c

include $(RIOTBASE)/Makefile.base
