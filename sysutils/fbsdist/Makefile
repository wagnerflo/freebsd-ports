# $FreeBSD$

PORTNAME?=	fbsdist
PORTVERSION=	0.3
CATEGORIES=	sysutils

MAINTAINER=	florian@wagner-flo.net

USE_GITHUB=	yes
GH_ACCOUNT=	wagnerflo
GH_PROJECT=	fbsdist
GH_TAGNAME=	86c7815

RUN_DEPENDS+=	gpg:${PORTSDIR}/security/gnupg

USES=		uidfix
MAKE_ARGS=	SCRIPT=${PORTNAME}

.include <bsd.port.mk>
