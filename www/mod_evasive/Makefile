PORTNAME=	mod_evasive
PORTVERSION=	1.10.1
PORTREVISION=	2
CATEGORIES=	www security
DIST_SUBDIR=	apache2

MAINTAINER=	kiwi@FreeBSD.org
COMMENT=	Apache module to try to protect the HTTP Server from DoS/DDoS attacks
WWW=		https://github.com/jzdziarski/mod_evasive

LICENSE=	GPLv2
LICENSE_FILE=	${WRKSRC}/LICENSE

USES=		apache

USE_GITHUB=	yes
GH_ACCOUNT=	jzdziarski
GH_TAGNAME=	ad6e89f6c7d835945a7d329cc0f04adaefc3d114

AP_FAST_BUILD=	yes
AP_GENPLIST=	yes
MODULENAME=	${PORTNAME}20

PORTDOCS=	README test.pl

OPTIONS_DEFINE=	DOCS

.include <bsd.port.pre.mk>

post-patch:
	@${REINPLACE_CMD} -e "s|/bin/mail|/usr/bin/mail|g" \
		${WRKSRC}/mod_evasive.c ${WRKSRC}/mod_evasive20.c \
		${WRKSRC}/mod_evasiveNSAPI.c
.if ${APACHE_VERSION:M2.4}
	@${REINPLACE_CMD} -e 's/remote_ip/client_ip/g' ${WRKSRC}/mod_evasive20.c
.endif

post-install:
	@${MKDIR} ${STAGEDIR}${DOCSDIR}
	${INSTALL_DATA} ${PORTDOCS:S|^|${WRKSRC}/|} ${STAGEDIR}${DOCSDIR}

.include <bsd.port.post.mk>
