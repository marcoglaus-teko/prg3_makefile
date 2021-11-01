#
# define compiler and compiler flag variables
#
JFLAGS = -d out
JC = javac

.SUFFIXES: .java .class

.java.class:
	$(JC) $(JFLAGS) $*.java

#
# CLASSES is a macro consisting of 4 words (one for each java source file)
#
CLASSES = \
    Main.java \
    Person.java

#
# the default make target entry
#
default: classes

#
# This target entry uses Suffix Replacement within a macro:
# $(name:string1=string2)
# 	In the words in the macro named 'name' replace 'string1' with 'string2'
# Below we are replacing the suffix .java of all words in the macro CLASSES
# with the .class suffix
#
classes: $(CLASSES:.java=.class)

#
# RM is a predefined macro in make (RM = rm -f)
#
clean:
	$(RM) out/*.class

#
# -cp classpath
#
run:
	java -cp out Main