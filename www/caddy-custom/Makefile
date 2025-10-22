# READ pkg-descr FOR INSTRUCTIONS!
# This port will NOT build in poudriere without (simple) manual
# intervention.

CADDY_DISTVERSION=	2.10.2
CADDY_PORTREVISION=	1
XCADDY_DISTVERSION=	0.4.5
XCADDY_PORTREVISION=	2

PORTNAME=	caddy-custom
PORTVERSION=	${CADDY_DISTVERSION}.${CADDY_PORTREVISION}.${XCADDY_DISTVERSION}.${XCADDY_PORTREVISION}
PORTREVISION=	8
CATEGORIES=	www
DISTFILES=	# none

MAINTAINER=	adamw@FreeBSD.org
COMMENT=	Caddy (www/caddy) with customized plugins
WWW=		https://caddyserver.com

LICENSE=	APACHE20

BUILD_DEPENDS=	xcaddy:www/xcaddy

USES=		go:no_targets

NO_PACKAGE=	Requires network access (see pkg-descr)

CONFLICTS_INSTALL=	caddy

USE_RC_SUBR=	caddy
SUB_FILES=	caddy

PLIST_FILES=	bin/caddy

.for plugin in ${CADDY_CUSTOM_PLUGINS}
PLUGINS+=	--with ${plugin}
.endfor

XCADDY_GO_BUILD_FLAGS?=	${GO_BUILDFLAGS}

XCADDY_ENV+=	XCADDY_WHICH_GO="${GO_CMD}" \
		XCADDY_GO_BUILD_FLAGS="${XCADDY_GO_BUILD_FLAGS}"

do-build:
	${MKDIR} ${WRKSRC}
	cd ${WRKSRC} && \
	${GO_ENV} GO111MODULE=on GOCACHE=${GO_GOPATH}/cache ${XCADDY_ENV} \
	  ${LOCALBASE}/bin/xcaddy build v${CADDY_DISTVERSION} ${PLUGINS}

do-install:
	${INSTALL_PROGRAM} ${WRKSRC}/caddy ${STAGEDIR}${PREFIX}/bin

.include <bsd.port.mk>
