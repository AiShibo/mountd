#	$OpenBSD: Makefile,v 1.5 2022/08/29 17:00:30 deraadt Exp $

PROG=	mountd
MAN=	exports.5 mountd.8

.PATH: ${.CURDIR}/../../lib/libutil
.PATH: ${.CURDIR}/../../lib/libc/rpc
SRCS+= mountd.c imsg.c imsg-buffer.c rpc_commondata.c svc.c

LDADD=	-lutil
DPADD=	${LIBUTIL}

CFLAGS+= -I${.CURDIR}/../../sys
CFLAGS+= -I${.CURDIR}/../../compat
CFLAGS+= -I${.CURDIR}/../../include
CFLAGS+= -I${.CURDIR}/../../lib/libutil


.include <bsd.prog.mk>

# Don't compile mountd as static binary by default
LDSTATIC=       
