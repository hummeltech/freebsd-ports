PORTNAME=	read-edid
PORTVERSION=	3.0.2
CATEGORIES=	sysutils
MASTER_SITES=	http://www.polypux.org/projects/${PORTNAME}/

MAINTAINER=	danfe@FreeBSD.org
COMMENT=	Tools for reading the EDID from a monitor
WWW=		http://www.polypux.org/projects/read-edid/

LIB_DEPENDS=	libx86.so:devel/libx86

USES=		cmake localbase

PLIST_FILES=	bin/get-edid bin/parse-edid share/man/man1/get-edid.1.gz
PORTDOCS=	AUTHORS ChangeLog LICENSE README

OPTIONS_DEFINE=	DOCS

.include <bsd.port.mk>
