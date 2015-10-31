# Created by: Florian Wagner <florian@wagner-flo.net>
# $FreeBSD$

PORTNAME?=	fbsdist
PORTVERSION=	0.2
CATEGORIES=	sysutils

USE_GITHUB=	yes
GH_ACCOUNT=	wagnerflo
GH_PROJECT=	fbsdist
GH_TAGNAME=	c75b4f0

RUN_DEPENDS+=	gpg:${PORTSDIR}/security/gnupg

MAKE_ARGS=	SCRIPT=${PORTNAME}

.include <bsd.port.mk>
