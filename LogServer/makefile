# ----------------------------------------------------------------------
#
# This makefile has been automatically generated by WinGDB 2.2, build 1191
# Do not edit.
#
# Project: LogServer
#
# ----------------------------------------------------------------------

PLATFORM=unix

ifneq ("$(windir)","")
PLATFORM=windows
endif

ifneq ("$(WinDir)","")
PLATFORM=windows
endif

ifneq ("$(WINDIR)","")
PLATFORM=windows
endif

UNAME=$(shell uname -o)

ifeq ("$(UNAME)","Cygwin")
PLATFORM=cygwin
endif

ifeq ("$(BUILD_CONFIGURATION)","")
	BUILD_CONFIGURATION=Debug
endif

ifeq ("$(BUILD_CONFIGURATION)","DebugLinux")
CC= gcc
CXX= g++
AR= ar
CFLAGS= -g -I ../../Medusa/
CXXFLAGS= -g -I ../../Medusa/
ARFLAGS= cru
LDFLAGS= -L ../Bin/ -L ../../Medusa/Bin/ -lMedusaD -lNetworkD -lGCQD -lpthread -ldl
RESULT=LogServerD
INTERMEDIATE_DIR=DebugLinux/obj
DESTINATION_DIR=../Bin
ifeq ("$(PLATFORM)","cygwin")
	RM=rm -f
	MKDIR=mkdir -p
	INTERMEDIATE_DIR_MK=$(INTERMEDIATE_DIR)
	DESTINATION_DIR_MK=$(DESTINATION_DIR)
else
	RM= rm -f
	MKDIR= mkdir -p
	INTERMEDIATE_DIR_MK=DebugLinux/obj
	DESTINATION_DIR_MK=../Bin
endif

endif

ifeq ("$(BUILD_CONFIGURATION)","ReleaseLinux")
CC= gcc
CXX= g++
AR= ar
CFLAGS= -g -O2 -I ../../Medusa/
CXXFLAGS= -g -O2 -I ../../Medusa/
ARFLAGS= cru
LDFLAGS= -L ../Bin/ -L ../../Medusa/Bin/ -lMedusa -lNetwork -lGCQ -lpthread -ldl
RESULT=LogServer
INTERMEDIATE_DIR=ReleaseLinux/obj
DESTINATION_DIR=../Bin
ifeq ("$(PLATFORM)","cygwin")
	RM=rm -f
	MKDIR=mkdir -p
	INTERMEDIATE_DIR_MK=$(INTERMEDIATE_DIR)
	DESTINATION_DIR_MK=$(DESTINATION_DIR)
else
	RM= rm -f
	MKDIR= mkdir -p
	INTERMEDIATE_DIR_MK=ReleaseLinux/obj
	DESTINATION_DIR_MK=../Bin
endif

endif

SOURCES= LogServer.cpp

SOURCEPATHS= LogServer.cpp

HEADERS=

VPATH= $(INTERMEDIATE_DIR)

OBJECTNAMES=$(patsubst %.c,%.o,$(patsubst %.cpp,%.o,$(SOURCES)))
OBJECTPATHS=$(addprefix $(INTERMEDIATE_DIR)/,$(OBJECTNAMES))

$(DESTINATION_DIR)/$(RESULT): $(OBJECTNAMES)
ifeq ("$(wildcard $(DESTINATION_DIR) )","")
	-$(MKDIR) $(DESTINATION_DIR_MK)
endif
	$(CXX) $(CXXFLAGS) $(SYSROOTFLAGS) $(OBJECTPATHS) -o $@ $(LDFLAGS)

$(INTERMEDIATE_DIR)/LogServer.d: $(SOURCES) $(HEADERS)
ifeq ("$(wildcard $(DESTINATION_DIR) )","")
	-$(MKDIR) $(DESTINATION_DIR_MK)
endif
ifeq ("$(wildcard $(INTERMEDIATE_DIR) )","")
	-$(MKDIR) $(INTERMEDIATE_DIR_MK)
endif
	$(CXX) $(CXXFLAGS) -MM $(SOURCEPATHS) > $@

-include $(INTERMEDIATE_DIR)/LogServer.d

clean:
	$(RM) $(DESTINATION_DIR)/$(RESULT)
	$(RM) $(INTERMEDIATE_DIR)/LogServer.d
	$(RM) $(OBJECTPATHS)

%.o: %.cpp
	$(CXX) $(CXXFLAGS) -c -o $(INTERMEDIATE_DIR)/$@ $<

%.o: %.c
	$(CC) $(CFLAGS) -c -o $(INTERMEDIATE_DIR)/$@ $<
