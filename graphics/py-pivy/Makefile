PORTNAME=	pivy
PORTVERSION=	0.6.10
CATEGORIES=	graphics python
PKGNAMEPREFIX=	${PYTHON_PKGNAMEPREFIX}

MAINTAINER=	cmt@FreeBSD.org
COMMENT=	Python binding for Coin
WWW=		https://github.com/coin3d/pivy

LICENSE=	MIT

BUILD_DEPENDS=	swig:devel/swig
LIB_DEPENDS=	libCoin.so:graphics/Coin \
		libSoQt.so:x11-toolkits/soqt

USES=		cmake:indirect compiler:c11 python qt:6
USE_GITHUB=	yes
GH_ACCOUNT=	coin3d
USE_PYTHON=	distutils
USE_QT=		base

CMAKE_ARGS=	-DPIVY_USE_QT6="ON"

PLIST_SUB+=	DISTVERSION=${DISTVERSION}

INSTALL_TARGET=	install-strip

.include <bsd.port.mk>
