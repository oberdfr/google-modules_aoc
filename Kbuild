# SPDX-License-Identifier: GPL-2.0

ccflags-y	+= -I$(srctree)/../private/google-modules/aoc_ipc
ccflags-y	+= -I$(srctree)/../private/google-modules/soc/gs/drivers/dma-buf/heaps
ccflags-y	+= -I$(srctree)/../private/google-modules/trusty/include
ccflags-y	+= -I$(srctree)/drivers/dma-buf

obj-$(CONFIG_WC_MBOX)			+= mailbox-wc.o

obj-$(CONFIG_AOC_DRIVER)		+= aoc_core.o
aoc_core-objs	:= aoc.o ../aoc_ipc/aoc_ipc_core.o aoc_firmware.o ion_physical_heap.o

obj-$(CONFIG_AOC_CHAR_DRIVER)		+= aoc_char_dev.o
obj-$(CONFIG_AOC_CONTROL_DRIVER)	+= aoc_control_dev.o
obj-$(CONFIG_AOC_CHAN_DRIVER)		+= aoc_channel_dev.o
obj-$(CONFIG_AOC_UWB_DRIVER)		+= aoc_uwb_platform_drv.o aoc_uwb_service_dev.o
obj-$(CONFIG_AOC_TBN_DRIVER)		+= aoc_tbn_service_dev.o

headers-y	:= uapi/aoc.h
