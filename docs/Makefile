# Makefile for docs building
.include "../Makefile.inc"

SGMLDIR=reference/sgml

# Coming in from the root, just build the manpage
all build: libcidr.3

# Write path into manpage
man: libcidr.3

libcidr.3: libcidr.3.in Makefile
	@${SED} -e 's|%%DOCDIR%%|${CIDR_DOCDIR}|' < libcidr.3.in > libcidr.3

# SGML docs
sgml ref reference:
	(cd ${SGMLDIR} && ${MAKE})

# Cleanup
clean:
	${RM} libcidr.3
	(cd ${SGMLDIR} && ${MAKE} clean)

allclean:
	${RM} libcidr.3
	(cd ${SGMLDIR} && ${MAKE} allclean)
