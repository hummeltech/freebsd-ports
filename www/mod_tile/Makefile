PORTNAME=		mod_tile
DISTVERSIONPREFIX=	v
DISTVERSION=		0.7.0
CATEGORIES=		www

MAINTAINER=		david.hummel@gmail.com
COMMENT=		System for serving raster OpenStreetMap tiles via Apache
WWW=			https://github.com/openstreetmap/mod_tile

LICENSE=		GPLv2
LICENSE_FILE=		${WRKSRC}/COPYING

BUILD_DEPENDS=		bash:shells/bash
LIB_DEPENDS=		libcairo.so:graphics/cairo \
			libapr-1.so:devel/apr1 \
			libcurl.so:ftp/curl \
			libglib-2.0.so:devel/glib20 \
			libicuuc.so:devel/icu \
			libiniparser.so:devel/iniparser \
			libmapnik.so:graphics/mapnik \
			libsasl2.so:security/cyrus-sasl2

USES=			apache cmake:noninja,testing compiler:c++14-lang gettext-runtime llvm:15,build pkgconfig

USE_GITHUB=		yes
GH_ACCOUNT=		openstreetmap

CMAKE_ARGS=		-DCMAKE_BUILD_TYPE:STRING=Release \
			-DCMAKE_LIBRARY_PATH="${LOCALBASE}/lib" \
			-DENABLE_TESTS:BOOL=ON

OPTIONS_DEFINE=		MEMCACHED RADOS
MEMCACHED_DESC=		Enable Memcached storage backend
MEMCACHED_LIB_DEPENDS=	libmemcached.so:databases/libmemcached
RADOS_DESC=		Enable RADOS storage backend
RADOS_LIB_DEPENDS=	librados.so:net/ceph14

.include <bsd.port.mk>