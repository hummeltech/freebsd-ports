PORTNAME=	commons-jelly
PORTVERSION=	1.0
PORTREVISION=	1
CATEGORIES=	lang devel java
MASTER_SITES=	APACHE_COMMONS_BINARIES
PKGNAMEPREFIX=	apache-

MAINTAINER=	ports@FreeBSD.org
COMMENT=	XML based scripting engine
WWW=		https://commons.apache.org/proper/commons-jelly/index.html

LICENSE=	APACHE20

USES=		java

NO_BUILD=	yes

DATADIR=	${JAVASHAREDIR}/${PORTNAME}
READMES=	LICENSE.txt NOTICE.txt README.txt RELEASE-NOTES.txt

SUB_FILES=	jelly.sh
PLIST_FILES=	bin/jelly
PLIST_DIRS=	%%DATADIR%%/custom
PORTDOCS=	*
PORTDATA=	*

OPTIONS_DEFINE=	DOCS

post-extract:
	${RM} ${WRKSRC}/bin/jelly.bat ${WRKSRC}/bin/jelly

do-install:
	(cd ${WRKSRC} && ${COPYTREE_SHARE} "custom lib bin" \
		${STAGEDIR}${DATADIR})
	${INSTALL_SCRIPT} ${WRKDIR}/jelly.sh ${STAGEDIR}${PREFIX}/bin/jelly
	(cd ${WRKSRC}/docs && ${COPYTREE_SHARE} . ${STAGEDIR}${DOCSDIR})
	${INSTALL_DATA} ${READMES:S|^|${WRKSRC}/|} ${STAGEDIR}${DOCSDIR}

.include <bsd.port.mk>
