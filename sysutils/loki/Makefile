PORTNAME=	loki
DISTVERSIONPREFIX=	v
DISTVERSION=	3.5.3
CATEGORIES=	sysutils
PKGNAMEPREFIX=	grafana-

MAINTAINER=	freebsd@funzi.org
COMMENT=	Scalable, highly-available, multi-tenant log aggregation system
WWW=		https://github.com/grafana/loki
MASTER_SITES+=	https://raw.githubusercontent.com/${GH_ACCOUNT}/${GH_PROJECT}/${DISTVERSIONFULL}/:gomod
DISTFILES+=	pkg/push/go.mod

LICENSE=	AGPLv3
LICENSE_FILE=	${WRKSRC}/LICENSE

USES=		go:modules

USE_GITHUB=	yes
GH_ACCOUNT=	grafana
GH_PROJECT=	loki

GO_MOD_DIST=	github
GO_MODULE=	github.com/${GH_ACCOUNT}/${GH_PROJECT}
GO_PKGNAME=	github.com/${GH_ACCOUNT}/${GH_PROJECT}
GO_TARGET=	./cmd/loki ./cmd/loki-canary ./cmd/logcli
GO_BUILDFLAGS=	-v -ldflags "${LD_FLAG_STRING}"

USE_RC_SUBR=	loki

LD_FLAG_STRING=	-s \
		${LD_FLAG_X_PREFIX}.Version=${PORTVERSION} \
		${LD_FLAG_X_PREFIX}.Revision=${PORTREVISION} \
		${LD_FLAG_X_PREFIX}.Branch=HEAD \
		${LD_FLAG_X_PREFIX}.BuildUser=${BUILD_USER} \
		${LD_FLAG_X_PREFIX}.BuildDate=$$(date -u +"%Y-%m-%dT%H:%M:%SZ")
LD_FLAG_X_PREFIX=	-X github.com/grafana/loki/pkg/util/build
BUILD_USER?=	${USER}

LOKI_USER?=	loki
LOKI_GROUP?=	loki
LOKI_DATADIR?=	/var/db/${PORTNAME}

SUB_LIST=	LOKI_USER=${LOKI_USER} \
		LOKI_GROUP=${LOKI_GROUP} \
		LOKI_DATADIR=${LOKI_DATADIR}

USERS=		${LOKI_USER}
GROUPS=		${LOKI_GROUP}

PLIST_SUB=	${SUB_LIST}

post-install:
	@${CP} ${WRKSRC}/cmd/loki/loki-local-config.yaml ${STAGEDIR}${PREFIX}/etc/loki.yaml.sample
	@${MKDIR} ${STAGEDIR}${LOKI_DATADIR}
	@${MKDIR} ${STAGEDIR}${LOKI_DATADIR}/rules-temp

.include <bsd.port.mk>
