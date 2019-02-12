# $FreeBSD$

PORTNAME?=	fbsdist
PORTVERSION=	0.5
CATEGORIES=	sysutils

MAINTAINER=	florian@wagner-flo.net

USE_GITHUB=	yes
GH_ACCOUNT=	wagnerflo
GH_PROJECT=	fbsdist
GH_TAGNAME=	77b20f8

RUN_DEPENDS+=	gpg:${PORTSDIR}/security/gnupg

USES=		uidfix
MAKE_ARGS=	SCRIPT=${PORTNAME}

.include <bsd.port.mk>
