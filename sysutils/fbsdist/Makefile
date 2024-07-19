# $FreeBSD$

PORTNAME?=	fbsdist
PORTVERSION=	0.8
CATEGORIES=	sysutils

MAINTAINER=	florian@wagner-flo.net

USE_GITHUB=	yes
GH_ACCOUNT=	wagnerflo
GH_PROJECT=	fbsdist
GH_TAGNAME=	68de522

RUN_DEPENDS+=	gpg:security/gnupg

USES=		uidfix
MAKE_ARGS=	SCRIPT=${PORTNAME}

.include <bsd.port.mk>
