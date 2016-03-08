# Created by: Florian Wagner <floran@wagner-flo.net>
# $FreeBSD: $

PORTNAME=	tgrey
CATEGORIES=	mail
PORTVERSION=	0.1.a.20160308

USE_GITHUB=	yes
GH_ACCOUNT=	wagnerflo
GH_TAGNAME=	5241feb

MAINTAINER=	florian@wagner-flo.net
COMMENT=	Greylisting for Postfix using tdb as backend
LICENSE=	BSD2CLAUSE

USES=		pkgconfig autoreconf libtool
AUTOMAKE_ARGS=	--add-missing

GNU_CONFIGURE=	yes
CONFIGURE_ARGS=	--with-db-path=/var/db/tgrey.tdb

BUILD_DEPENDS+=	tdb>=1.2.11:${PORTSDIR}/databases/tdb
RUN_DEPENDS:=	${BUILD_DEPENDS}

.include <bsd.port.mk>
