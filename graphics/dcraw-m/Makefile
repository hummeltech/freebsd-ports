PORTNAME=	dcraw-m
PORTVERSION=	9.22
PORTREVISION=	10
CATEGORIES=	graphics

MAINTAINER=	waitman@waitman.net
COMMENT=	Modified Decoder for RAW files from digital cameras
WWW=		http://www.cybercom.net/~dcoffin/dcraw/

LICENSE=	GPLv2

LIB_DEPENDS=	libjasper.so:graphics/jasper \
		liblcms2.so:graphics/lcms2

USE_GITHUB=	yes
GH_ACCOUNT=	waitman
GH_TAGNAME=	1392579

USES=		jpeg magick:6 pkgconfig

CFLAGS+=	-Wall -I${LOCALBASE}/include \
		`pkg-config MagickWand --cflags` \
		-DMAGICKCORE_HDRI_ENABLE=0 \
		-DMAGICKCORE_QUANTUM_DEPTH=16
LDFLAGS+=	`pkg-config MagickWand --libs` -lm -llcms2 -ljpeg \
		-ljasper
LIBS+=		-L${LOCALBASE}/lib

PLIST_FILES=	bin/dcraw-m

do-build:
	( cd ${WRKSRC} ; \
	${CC} ${CFLAGS} ${LIBS} ${LDFLAGS} -o ${PORTNAME} ${PORTNAME}.c )

do-install:
	${INSTALL_PROGRAM} ${WRKSRC}/${PORTNAME} ${STAGEDIR}${PREFIX}/bin/

.include <bsd.port.mk>
