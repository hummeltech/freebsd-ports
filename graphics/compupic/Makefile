PORTNAME=	compupic
PORTVERSION=	5.1.1063
PORTREVISION=	1
CATEGORIES=	graphics
MASTER_SITES=	http://files.photodex.com/archive/unix/
DISTNAME=	${PORTNAME}-${PORTVERSION}-i386-freebsd
EXTRACT_ONLY=	# extracted directly in install target

MAINTAINER=	ports@FreeBSD.org
COMMENT=	Digital content manager
WWW=		http://www.photodex.com/downloads/platforms/freebsd.html

NO_WRKSUBDIR=	yes
NO_BUILD=	yes
ONLY_FOR_ARCHS=	i386

do-install:
	${EXTRACT_CMD} ${EXTRACT_BEFORE_ARGS} ${DISTDIR}/${DISTNAME}.tar.gz \
		${EXTRACT_AFTER_ARGS} -C ${STAGEDIR}${PREFIX}
	${RM} ${STAGEDIR}${PREFIX}/bin/compupic
	${LN} -sf ${PREFIX}/compupic/compupic ${STAGEDIR}${PREFIX}/bin/compupic
	${INSTALL_MAN} ${STAGEDIR}${PREFIX}/compupic/compupic.1 \
		${STAGEDIR}${PREFIX}/share/man/man1

.include <bsd.port.mk>
