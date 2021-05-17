# Created by: Florian Wagner <floran@wagner-flo.net>
# $FreeBSD: $

PORTNAME=	tgrey
CATEGORIES=	mail
PORTVERSION=	0.1.a.20160308
PORTREVISION=	1

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
CXXFLAGS+=	-Wno-error=deprecated-declarations

LIB_DEPENDS=	libtdb.so:databases/tdb

.include <bsd.port.mk>
