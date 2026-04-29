PORTNAME=	notifuse-server
DISTVERSIONPREFIX=	v
DISTVERSION=	30.1
PORTREVISION=	1
CATEGORIES=	www

MAINTAINER=	florian@wagner-flo.de
COMMENT=	An open-source & modern emailing platform
WWW=		https://www.notifuse.com/

LICENSE=	AGPLv3
LICENSE_FILE=	${WRKSRC}/LICENCE.md

USES=	go:modules

USE_GITHUB=	yes
GH_ACCOUNT=	Notifuse
GH_PROJECT=	notifuse

GO_MODULE=	github.com/Notifuse/notifuse
GO_MOD_DIST=	github

GO_BUILDFLAGS+=	-ldflags='-s -w'
GO_TARGET=	./cmd/api:notifuse-server
CGO_ENABLED=	0

.include <bsd.port.mk>
