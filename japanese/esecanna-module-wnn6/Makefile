PORTNAME=	esecanna-module-wnn6
PORTVERSION=	1.0.0
PORTREVISION=	4
CATEGORIES=	japanese
MASTER_SITES=	http://esecanna.netfort.gr.jp/ \
		LOCAL/knu
DISTNAME=	${PORTNAME}_${PORTVERSION}
DIST_SUBDIR=	esecanna

MAINTAINER=	ports@FreeBSD.org
COMMENT=	Esecanna module for Wnn6
WWW=		http://esecanna.netfort.gr.jp/

DEPRECATED=	Upstream disapeared and distfile is no more available
EXPIRATION_DATE=2025-03-31

LIB_DEPENDS=	libwnn6.so:japanese/Wnn6-lib
RUN_DEPENDS=	${LOCALBASE}/sbin/esecannaserver:japanese/esecanna

GNU_CONFIGURE=	yes
USES=		gmake
LDFLAGS+=	-L${PREFIX}/lib
CFLAGS+=	-I${PREFIX}/include/wnn6

OPTIONS_DEFINE=	DOCS

post-install:
	@${MKDIR} ${STAGEDIR}${PREFIX}/share/doc/esecanna
.for i in README CHANGES
	${INSTALL_DATA} ${WRKSRC}/${i}.jp \
		${STAGEDIR}${PREFIX}/share/doc/esecanna/${i}.wnn6.jp
.endfor

.include <bsd.port.mk>
