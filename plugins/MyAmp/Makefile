#!/usr/bin/make -f
# Makefile for DISTRHO Plugins #
# ---------------------------- #
# Created by falkTX
#
# Modified by REIS0

VST2 ?= true
LV2 ?= true

# --------------------------------------------------------------
# Project name, used for binaries

NAME = MyAmp

# --------------------------------------------------------------
# Files to build

FILES_DSP = MyAmp.cpp

# --------------------------------------------------------------
# Do some magic

include ../../dpf/Makefile.plugins.mk

# --------------------------------------------------------------
# VST2 and LV2 targets

ifeq ($(VST2), true)
TARGETS += vst
endif

ifeq ($(LV2), true)
ifeq ($(HAVE_DGL),true)
TARGETS += lv2_sep
else
TARGETS += lv2_dsp
endif
endif

all: $(TARGETS)

# --------------------------------------------------------------
