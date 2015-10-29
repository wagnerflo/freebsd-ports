# Created by: Florian Wagner <floran@wagner-flo.net>
# $FreeBSD: $

PORTNAME=	tgrey
PORTVERSION=	0.1.20150921
PORTREVISION=	1
CATEGORIES=	mail
MASTER_SITES=	https://bitbucket.org/wagnerflo/tgrey/get/
DISTNAME=	12c940f60c7f
DIST_SUBDIR=	${PORTNAME}

MAINTAINER=	florian@wagner-flo.net
COMMENT=	Greylisting for Postfix using tdb as backend

LICENSE=	BSD2CLAUSE
WRKSRC=		${WRKDIR}/wagnerflo-${PORTNAME}-${DISTNAME}

USES=		pkgconfig autoreconf libtool
AUTOMAKE_ARGS=	--add-missing

GNU_CONFIGURE=	yes
CONFIGURE_ARGS=	--with-db-path=/var/db/tgrey.tdb

BUILD_DEPENDS+=	tdb>=1.2.11:${PORTSDIR}/databases/tdb
RUN_DEPENDS:=	${BUILD_DEPENDS}

.include <bsd.port.mk>
