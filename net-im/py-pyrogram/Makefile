PORTNAME=	pyrogram
PORTVERSION=	2.0.106
CATEGORIES=	net-im python
MASTER_SITES=	PYPI
PKGNAMEPREFIX=	${PYTHON_PKGNAMEPREFIX}
DISTNAME=	Pyrogram-${DISTVERSION}

MAINTAINER=	florian@wagner-flo.de
COMMENT=	Telegram MTProto API Framework for Python
WWW=		https://pyrogram.org/

LICENSE=	LGPL3

BUILD_DEPENDS=	${PYTHON_PKGNAMEPREFIX}setuptools>0:devel/py-setuptools@${PY_FLAVOR}
RUN_DEPENDS=	${PYTHON_PKGNAMEPREFIX}pyaes>=1.6.1:security/py-pyaes@${PY_FLAVOR} \
		${PYTHON_PKGNAMEPREFIX}pysocks>=1.7.1:net/py-pysocks@${PY_FLAVOR}

NO_ARCH=	yes
USES=		python
USE_PYTHON=	autoplist distutils

.include <bsd.port.mk>
