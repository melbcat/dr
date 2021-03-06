#############################################################################
# Makefile for building dhexclock
#     Project: dhexclock
#    Template: app
#############################################################################

####### System-dependendant options

####### BEGIN
#
#   This section was automatically generated from
#      /usr/lib/qt-1.44/Makefile for building on
#       on Tue Jul 13 14:00:30 CDT 1999
#

QTDIR = /usr

# Compiling
SYSCONF_CXX		= g++

# Compiling with support libraries
SYSCONF_CXXFLAGS_X11	= -I/usr/X11R6/include
SYSCONF_CXXFLAGS_QT	= -I$(QTDIR)/include/qt3
SYSCONF_CXXFLAGS_OPENGL	= -I/usr/X11R6/include

# Compiline YACC output
SYSCONF_CXXFLAGS_YACC     = -Wno-unused -Wno-parentheses

# Linking with support libraries
# X11
SYSCONF_LFLAGS_X11	= -L/usr/X11R6/lib
SYSCONF_LIBS_X11	= -lX11 -lXext
# Qt, Qt+OpenGL
SYSCONF_LFLAGS_QT	= -L$(QTDIR)/lib
SYSCONF_LIBS_QT		= -lqt-mt
SYSCONF_LIBS_QT_OPENGL	= -lqgl
# OpenGL
SYSCONF_LFLAGS_OPENGL	= -L/usr/X11R6/lib
SYSCONF_LIBS_OPENGL	= -lMesaGL -lMesaGLU -lXmu -lXext -lm
# Yacc
SYSCONF_LIBS_YACC	= 

# Linking applications
SYSCONF_LINK		= g++
SYSCONF_LFLAGS		= -g
SYSCONF_LIBS		= 

# Link flags shared objects
SYSCONF_LFLAGS_SHOBJ	= -shared

# Meta-object compiler
SYSCONF_MOC		= $(QTDIR)/bin/moc

# Linking shared libraries
#   - Build the $(TARGET) library, eg. lib$(TARGET).so.0.0
#   - Place target in $(DESTDIR) - which has a trailing /
#   - Usually needs to incorporate $(VER_MAJ) and $(VER_MIN)
#
SYSCONF_LINK_SHLIB	= g++
SYSCONF_LINK_TARGET_SHARED	= lib$(TARGET).so.$(VER_MAJ).$(VER_MIN)
SYSCONF_LINK_LIB_SHARED	=  $(SYSCONF_LINK_SHLIB) -shared -Wl,-soname,lib$(TARGET).so.$(VER_MAJ) \
				     $(LFLAGS) -o $(SYSCONF_LINK_TARGET_SHARED) \
				     $(OBJECTS) $(OBJMOC) $(LIBS); \
				 mv $(SYSCONF_LINK_TARGET_SHARED) $(DESTDIR); \
				 cd $(DESTDIR); \
				 rm -f lib$(TARGET).so lib$(TARGET).so.$(VER_MAJ); \
				 ln -s $(SYSCONF_LINK_TARGET_SHARED) lib$(TARGET).so; \
				 ln -s $(SYSCONF_LINK_TARGET_SHARED) lib$(TARGET).so.$(VER_MAJ)

# Linking static libraries
#   - Build the $(TARGET) library, eg. lib$(TARGET).a
#   - Place target in $(DESTDIR) - which has a trailing /
#
SYSCONF_AR		= ar cqs
SYSCONF_LINK_TARGET_STATIC = lib$(TARGET).a
SYSCONF_LINK_LIB_STATIC	= rm -f $(DESTDIR)$(SYSCONF_LINK_TARGET_STATIC) ; \
				 $(SYSCONF_AR) $(DESTDIR)$(SYSCONF_LINK_TARGET_STATIC) $(OBJECTS) $(OBJMOC) 
# Compiling application source
SYSCONF_CXXFLAGS	= -g -pipe -O2 -fno-strength-reduce
# Compiling library source
SYSCONF_CXXFLAGS_LIB	= -g -O2 -fno-strength-reduce -fPIC
# Compiling shared-object source
SYSCONF_CXXFLAGS_SHOBJ	= -g -O2 -fno-strength-reduce -fPIC
# Default link type (stati linking is still be used where required)
SYSCONF_LINK_LIB	= $(SYSCONF_LINK_LIB_SHARED)
SYSCONF_LINK_TARGET	= $(SYSCONF_LINK_TARGET_SHARED)

####### End of automatically generated section
####### END

####### Compiler, tools and options

CXX	=	$(SYSCONF_CXX)
CXXFLAGS=	$(SYSCONF_CXXFLAGS_QT) $(SYSCONF_CXXFLAGS)
LFLAGS	=	$(SYSCONF_LFLAGS_QT) $(SYSCONF_LFLAGS_X11) $(SYSCONF_LFLAGS)
LIBS	=	$(SYSCONF_LIBS_QT) $(SYSCONF_LIBS_X11) $(SYSCONF_LIBS)
MOC	=	$(SYSCONF_MOC)

####### Target

TARGET	= dhexclock
DESTDIR = ./
VER_MAJ = 1
VER_MIN = 0

####### Files

#HEADERS =	digital_hexal_clock.h \
#		seven_segment_display.h \
#		hexal_segment_display.h \
#		daysec.h \
#		hexon.h
#SOURCES =	digital_hexal_clock.cpp \
#		seven_segment_display.cpp \
#		hexal_segment_display.cpp \
#		daysec.c \
#		hexon.c \
#		main.cpp
OBJECTS =	main.o \
		day_sec.o \
		digital_hexal_clock.o \
		hexal_segment_display.o \
		hexon.o \
		seven_segment_display.o
SRCMOC	=	moc_digital_hexal_clock.cpp \
		moc_seven_segment_display.cpp \
		moc_hexal_segment_display.cpp
OBJMOC	=	moc_digital_hexal_clock.o \
		moc_seven_segment_display.o \
		moc_hexal_segment_display.o

####### Implicit rules

.SUFFIXES: .cpp .cxx .cc .C .c

.cpp.o:
	$(CXX) -c $(CXXFLAGS) $(INCPATH) -o $@ $<

.cxx.o:
	$(CXX) -c $(CXXFLAGS) $(INCPATH) -o $@ $<

.cc.o:
	$(CXX) -c $(CXXFLAGS) $(INCPATH) -o $@ $<

.C.o:
	$(CXX) -c $(CXXFLAGS) $(INCPATH) -o $@ $<

.c.o:
	$(CXX) -c $(CXXFLAGS) $(INCPATH) -o $@ $<

####### Build rules

all: $(DESTDIR)$(TARGET)

$(DESTDIR)$(TARGET): $(OBJECTS) $(OBJMOC) 
	$(SYSCONF_LINK) $(LFLAGS) -o $(TARGET) $(OBJECTS) $(OBJMOC) $(LIBS)

moc: $(SRCMOC)

tmake:
	tmake digital_hexal_clock.pro

run:	all
	$(DESTDIR)$(TARGET)

clean:
	-rm -f $(OBJECTS) $(OBJMOC) $(SRCMOC)
	-rm -f *~ core

####### Compile

digital_hexal_clock.o: digital_hexal_clock.cpp \
		digital_hexal_clock.hpp

main.o: main.cpp \
		digital_hexal_clock.hpp

#moc_digital_hexal_clock.o: moc_digital_hexal_clock.cpp \
#		digital_hexal_clock.h

#moc_digital_hexal_clock.cpp: digital_hexal_clock.h
#	$(MOC) digital_hexal_clock.h -o moc_digital_hexal_clock.cpp

moc_%.o:	moc_%.cpp %.hpp

moc_%.cpp: %.hpp
	$(MOC) $< -o $@
