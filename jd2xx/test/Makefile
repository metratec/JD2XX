-include ../Makefile.conf

# JAVA_HOME is usually set on Java boxes
JDK ?= $(JAVA_HOME)

JSRC = $(wildcard *.java)
JOBJ = $(JSRC:%.java=%.class)

JAVAC = $(JDK)/bin/javac

JFLAGS = -O -cp "../jd2xx.jar"

.PRECIOUS: %.class

all:
	$(JAVAC) $(JFLAGS) *.java

%.class: %.java
	$(JAVAC) $(JFLAGS) $^

clean:
	$(RM) $(JOBJ)

distclean: clean
	$(RM) *.bak
