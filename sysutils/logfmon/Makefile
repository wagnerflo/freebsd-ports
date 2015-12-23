# $FreeBSD: $

PORTNAME=	logfmon
PORTVERSION=	1.2
CATEGORIES=	sysutils
MASTER_SITES=	https://github.com/nicm/logfmon/releases/download/${PORTVERSION}/

MAINTAINER=	florian@wagner-flo.net
COMMENT=	Log file monitoring daemon

GNU_CONFIGURE=	yes
USE_RC_SUBR=	logfmon

post-install:
	@${MKDIR} ${STAGEDIR}${EXAMPLESDIR}
	@${INSTALL} ${COPY} -m 644 ${WRKSRC}/examples/* ${STAGEDIR}${EXAMPLESDIR}

.include <bsd.port.mk>
