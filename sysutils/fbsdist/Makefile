# $FreeBSD$

PORTNAME?=	fbsdist
PORTVERSION=	0.6
CATEGORIES=	sysutils

MAINTAINER=	florian@wagner-flo.net

USE_GITHUB=	yes
GH_ACCOUNT=	wagnerflo
GH_PROJECT=	fbsdist
GH_TAGNAME=	f0103a1

RUN_DEPENDS+=	gpg:security/gnupg

USES=		uidfix
MAKE_ARGS=	SCRIPT=${PORTNAME}

.include <bsd.port.mk>
