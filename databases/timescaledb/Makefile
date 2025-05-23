PORTNAME=	timescaledb
PORTVERSION=	2.19.0
CATEGORIES=	databases

MAINTAINER=	kbowling@FreeBSD.org
COMMENT=	Time-series database built on PostgreSQL
WWW=		https://www.timescale.com/

LICENSE=		APACHE20 TSL
LICENSE_COMB=		multi
LICENSE_NAME_TSL=	Timescale License Agreement
LICENSE_FILE_APACHE20=	${WRKSRC}/LICENSE-APACHE
LICENSE_FILE_TSL=	${WRKSRC}/tsl/LICENSE-TIMESCALE
LICENSE_PERMS_TSL=	dist-mirror pkg-mirror auto-accept

BROKEN_i386=	compilation fails: undeclared type '__uint128_t'

USES=		compiler:c11 cmake gettext-runtime cpe pgsql:14-17

USE_GITHUB=	YES
GH_ACCOUNT=	timescale

CPE_VENDOR=	timescale

PLIST_SUB=	PORTVERSION=${PORTVERSION}
SUB_FILES=	pkg-message
SUB_LIST=	PORTVERSION=${PORTVERSION}

OPTIONS_DEFINE=		SSL TSL
OPTIONS_DEFAULT=	SSL TSL
OPTIONS_SUB=		yes

SSL_DESC=		Build with OpenSSL support
TSL_DESC=		Enables TSL licensed code in additon to Apache license code

SSL_CMAKE_BOOL=		USE_OPENSSL
SSL_USES=		ssl
TSL_CMAKE_BOOL_OFF=	APACHE_ONLY

CMAKE_OFF=	REGRESS_CHECKS TAP_CHECKS WARNINGS_AS_ERRORS
WANT_PGSQL=	lib server

.include <bsd.port.mk>
