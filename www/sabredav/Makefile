# $FreeBSD$

PORTNAME=	sabredav
PORTVERSION=	3.0.5
CATEGORIES=	www
MASTER_SITES=	https://github.com/fruux/sabre-dav/releases/download/${PORTVERSION}/

MAINTAINER=	florian@wagner-flo.net
COMMENT=	WebDav, CalDav and Carddav Server/Framework written in PHP

LICENSE=	BSD3CLAUSE

USES=		cpe zip
CPE_VENDOR=	fruux
USE_PHP=	ctype dom iconv mbstring pcre spl xmlreader xmlwriter

WRKSRC=		${WRKDIR}/SabreDAV
NO_BUILD=	yes

do-install:
	  ${MKDIR} ${STAGEDIR}/${WWWDIR}
	  (cd ${WRKSRC} && ${COPYTREE_SHARE} . ${STAGEDIR}/${WWWDIR} )

.include <bsd.port.mk>
