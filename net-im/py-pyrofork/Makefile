PORTNAME=	pyrofork
PORTVERSION=	2.3.61
CATEGORIES=	net-im python
MASTER_SITES=	PYPI
PKGNAMEPREFIX=	${PYTHON_PKGNAMEPREFIX}

MAINTAINER=	florian@wagner-flo.de
COMMENT=	Fork of Pyrogram. Telegram MTProto API Framework for Python
WWW=		https://github.com/Mayuri-Chan/pyrofork

LICENSE=	LGPL3

BUILD_DEPENDS=	${PYTHON_PKGNAMEPREFIX}hatchling>=0:devel/py-hatchling@${PY_FLAVOR}
RUN_DEPENDS=	${PYTHON_PKGNAMEPREFIX}pyaes>=1.6.1:security/py-pyaes@${PY_FLAVOR} \
		${PYTHON_PKGNAMEPREFIX}pysocks>=1.7.1:net/py-pysocks@${PY_FLAVOR} \
		${PYTHON_PKGNAMEPREFIX}pymediainfo>=6.0.1<=7.0.0:multimedia/py-pymediainfo@${PY_FLAVOR}

NO_ARCH=	yes
USES=		python
USE_PYTHON=	autoplist pep517

.include <bsd.port.mk>
