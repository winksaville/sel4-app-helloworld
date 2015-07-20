#
# Copyright 2015, Wink Saville
#
# This software may be distributed and modified according to the terms of
# the BSD 2-Clause license. Note that NO WARRANTY is provided.
# See "LICENSE_BSD2.txt" for details.

apps-$(CONFIG_APP_HELLOWORLD) += helloworld

# Libraries needed
helloworld-y = libsel4 libsel4startstop libsel4putchar libsel4string libsel4printf libsel4assert

helloworld: kernel_elf $(helloworld-y)
