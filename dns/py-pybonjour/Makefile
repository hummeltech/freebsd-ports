PORTNAME=	pybonjour
PORTVERSION=	1.1.1
PORTREVISION=	1
CATEGORIES=	dns python
PKGNAMEPREFIX=	${PYTHON_PKGNAMEPREFIX}

MAINTAINER=	jhixson@FreeBSD.org
COMMENT=	Pure-Python interface to Apple Bonjour
WWW=		https://github.com/depl0y/pybonjour-python3

LICENSE=	MIT

LIB_DEPENDS=	libdns_sd.so.1:net/mDNSResponder

USES=		python
USE_PYTHON=	autoplist distutils
USE_GITHUB=	yes
GH_ACCOUNT=	depl0y
GH_PROJECT=	pybonjour-python3
GH_TAGNAME=	2c8283f

NO_ARCH=	yes

.include <bsd.port.mk>
