# Makefile for the Openswan in-tree test cases
# Copyright (C) 2014 Michael Richardson <mcr@xelerance.com>
#
# This program is free software; you can redistribute it and/or modify it
# under the terms of the GNU General Public License as published by the
# Free Software Foundation; either version 2 of the License, or (at your
# option) any later version.  See <http://www.fsf.org/copyleft/gpl.txt>.
#
# This program is distributed in the hope that it will be useful, but
# WITHOUT ANY WARRANTY; without even the implied warranty of MERCHANTABILITY
# or FITNESS FOR A PARTICULAR PURPOSE.  See the GNU General Public License
# for more details.

OPENSWANSRCDIR?=$(shell cd ../../..; pwd)
srcdir?=${OPENSWANSRCDIR}/tests/unit/libpluto

all: programs

include ${OPENSWANSRCDIR}/Makefile.inc

UNITTESTS_0+=lp03-whacksemantics
UNITTESTS_0+=lp04-nsscert
UNITTESTS_0+=lp05-sha256cert
UNITTESTS_0+=lp07-orient
UNITTESTS_0+=lp28-addrinfoserialize
UNITTESTS_0+=lp29-adns
UNITTESTS_0+=lp30-dnskick
UNITTESTS_0+=lp31-IDhostpair
UNITTESTS_0+=lp33-IDanypair
UNITTESTS_0+=lp33-dnsload2
UNITTESTS_0+=lp33-IDanypair
UNITTESTS_0+=lp34-orientafterlisten
UNITTESTS_0+=lp40-orientafterprivate
UNITTESTS_0+=lp41-orientmoon
UNITTESTS_0+=lp42-loadbobdefaultroute
UNITTESTS_0+=lp50-rekey-no-reply-rekey
UNITTESTS_0+=lp60-bestif
UNITTESTS_0+=lp70-invalid-init-msg

UNITTESTS_I1+=lp02-parentI1
UNITTESTS_R1+=lp06-parentR1notchosen
UNITTESTS_R1+=lp08-parentR1
UNITTESTS_I2+=lp10-parentI2
UNITTESTS_I2+=lp11-parentI2dup
UNITTESTS_R2+=lp12-parentR2
UNITTESTS_I3+=lp13-parentI3

UNITTESTS_I1+=lp14-initiateself
UNITTESTS_R1+=lp15-respondself
UNITTESTS_I2+=lp16-initiateselfI2
UNITTESTS_R2+=lp17-childselfpolicy

UNITTESTS_I1+=lp18-certificateselfI1
UNITTESTS_R1+=lp19-certreplyselfR1
UNITTESTS_I2+=lp20-certificateselfI2
UNITTESTS_R2+=lp21-certreplyselfR2
UNITTESTS_R2+=lp22-certreplymanyR2



UNITTESTS_I1+=lp23-davecertI1
UNITTESTS_R2+=lp24-certreplydaveR2
UNITTESTS_R2+=lp25-wrongcacert
UNITTESTS_I2+=lp26-davecertI2

UNITTESTS_I1+=lp27-dnsloadI1
UNITTESTS_R2+=lp32-parentR2anychoice
UNITTESTS_I1+=lp36-h2hI1
UNITTESTS_R1+=lp37-h2hR1
UNITTESTS_I2+=lp38-h2hI2
UNITTESTS_R2+=lp39-h2hR2

UNITTESTS_I1+=lp71-alg-h2hI1
UNITTESTS_R1+=lp72-alg-h2hR1
UNITTESTS_I2+=lp73-alg-h2hI2
UNITTESTS_R2+=lp74-alg-h2hR2
UNITTESTS_I3+=lp75-alg-h2hI3
UNITTESTS_I3+=lp76-s2s-while-h2h-I1

UNITTESTS_I3+=lp77-del-matching-st
UNITTESTS_R4+=lp80-h2h-rekeyikev2-R2-msgid0
UNITTESTS_I3+=lp81-h2h-rekeyikev2-I3-msgid0
UNITTESTS_R2+=lp82-h2h-deleteSA-R2
UNITTESTS_I3+=lp83-h2h-deleteSA-I3
UNITTESTS_R2+=lp84-h2h-deleteSA-R2-R
UNITTESTS_I3+=lp85-h2h-invalid-deleteSA-I3
UNITTESTS_R2+=lp86-h2h-invalid-deleteSA-R2-R
UNITTESTS_I1+=lp90-h2h-sareplace-I1
UNITTESTS_R1+=lp91-h2h-sareplace-R1

UNITTESTS_I1+=lp43-parentM1
UNITTESTS_I1+=lp210-1des-fails

UNITTESTS_R1+=lp44-h2hR1-deny-ikev1
UNITTESTS_R1+=lp45-h2hR1-noikev2
UNITTESTS_I1+=lp46-rekeyikev2-I1
UNITTESTS_R1+=lp47-rekeyikev2-R1
UNITTESTS_I4+=lp48-rekeyikev2-inCR1
UNITTESTS_I1+=lp52-davecert-gatewayID-I1
UNITTESTS_R1+=lp53-davecert-gatewayID-R1
UNITTESTS_I2+=lp54-davecert-gatewayID-I2
UNITTESTS_R2+=lp55-davecert-gatewayID-R2
UNITTESTS_I1+=lp56-rekeyv2nopfs-I1
UNITTESTS_R1+=lp57-rekeyv2nopfs-R1
UNITTESTS_I4+=lp58-rekeyv2nopfs-inCR1
UNITTESTS_I1+=lp61-nattI1
UNITTESTS_R1+=lp62-nattR1
UNITTESTS_I2+=lp63-nattI2
UNITTESTS_R2+=lp64-nattR2
UNITTESTS_I3+=lp65-nattI3
UNITTESTS_I4+=lp66-natt-replaceI
UNITTESTS_R4+=lp67-natt-replaceR

UNITTESTS_I1+=lp87-rekeyv2-inval-I1
UNITTESTS_R1+=lp88-rekeyv2-inval-R1
UNITTESTS_I4+=lp89-rekeyv2-inval-inCR1

UNITTESTS_I1+=lp201-ca-h2hI1
UNITTESTS_R1+=lp202-ca-h2hR1
UNITTESTS_I2+=lp203-ca-h2hI2
UNITTESTS_R2+=lp204-ca-h2hR2
UNITTESTS_I3+=lp205-ca-h2hI3

# first runs tests that have no interdependancies
UNITTESTS=${UNITTESTS_0}
# then run all the I1,R1,I2,R2,I3
UNITTESTS+=${UNITTESTS_I1}
UNITTESTS+=${UNITTESTS_R1}
UNITTESTS+=${UNITTESTS_I2}
UNITTESTS+=${UNITTESTS_R2}
UNITTESTS+=${UNITTESTS_I3}
UNITTESTS+=${UNITTESTS_I4}
UNITTESTS+=${UNITTESTS_R4}

# running 'make check KEEPGOING=1' will run through all tests w/o stopping
ERROR_CHECK=$(if ${KEEPGOING},,set -e;)
programs clean check pcapupdate:
	@${ERROR_CHECK} for unittest in ${UNITTESTS}; do ${MAKE} -C $$unittest $@; done

testlist:
	@echo ${UNITTESTS}
