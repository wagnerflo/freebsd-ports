PORTNAME=	prisma-engines${DISTVERSION:S|.||g}
DISTVERSION=	5.9.1
PORTREVISION=	1
CATEGORIES=	databases

MAINTAINER=	florian@wagner-flo.de
COMMENT=	Engine components of Prisma ORM
WWW=		https://github.com/prisma/prisma-engines

PLIST_SUB+=	PORTNAME=${PORTNAME}

LICENSE=	APACHE20
LICENSE_FILE=	${WRKSRC}/LICENSE

USES=		cargo ssl

CARGO_INSTALL=	no

USE_GITHUB=	yes
GH_ACCOUNT=	prisma
GH_PROJECT=	prisma-engines

LIB_DEPENDS=	libprotobuf.so:devel/protobuf
BUILD_DEPENDS=	git:devel/git

INSTALL_SRC_DIR=	${CARGO_TARGET_DIR}/${CARGO_BUILD_TARGET}/release
INSTALL_TGT_DIR=	${STAGEDIR}${PREFIX}/libexec/${PORTNAME}

do-install:
	@${MKDIR} ${INSTALL_TGT_DIR}
.for i in prisma-fmt query-engine schema-engine
	@${INSTALL_SCRIPT} ${INSTALL_SRC_DIR}/${i} ${INSTALL_TGT_DIR}
	@${STRIP_CMD} ${INSTALL_TGT_DIR}/${i}
.endfor
	@${INSTALL_DATA} ${INSTALL_SRC_DIR}/deps/libquery_engine.so ${INSTALL_TGT_DIR}
	@${MV} ${INSTALL_TGT_DIR}/libquery_engine.so ${INSTALL_TGT_DIR}/libquery_engine.so.node
	@${STRIP_CMD} ${INSTALL_TGT_DIR}/libquery_engine.so.node

.include <bsd.port.mk>
