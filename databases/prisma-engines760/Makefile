PORTNAME=	prisma-engines${DISTVERSION:S|.||g}
DISTVERSION=	7.6.0
PORTREVISION=	1
CATEGORIES=	databases

MAINTAINER=	florian@wagner-flo.de
COMMENT=	Engine components of Prisma ORM
WWW=		https://github.com/prisma/prisma-engines

PLIST_SUB+=	PORTNAME=${PORTNAME}

LICENSE=	APACHE20
LICENSE_FILE=	${WRKSRC}/LICENSE

USES=		cargo pkgconfig ssl

CARGO_INSTALL=	no
CARGO_ENV+=	GIT_HASH=${DISTVERSION} \
		CARGO_PROFILE_RELEASE_LTO=thin \
		OPENSSL_INCLUDE_DIR=${OPENSSLINC} \
		OPENSSL_LIB_DIR=${OPENSSLLIB}

USE_GITHUB=	yes
GH_ACCOUNT=	prisma
GH_PROJECT=	prisma-engines

LIB_DEPENDS=	libprotobuf.so:devel/protobuf

INSTALL_TGT=	${STAGEDIR}${PREFIX}/libexec/${PORTNAME}

do-install:
	@${MKDIR} ${INSTALL_TGT}
	@${INSTALL_SCRIPT} \
	  ${CARGO_TARGET_DIR}/${CARGO_BUILD_TARGET}/release/schema-engine \
	  ${INSTALL_TGT}
	@${STRIP_CMD} ${INSTALL_TGT}/schema-engine

.include <bsd.port.mk>
