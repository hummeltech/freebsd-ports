PORTNAME=	ohmyzsh
PORTVERSION=	20241128
CATEGORIES=	shells

MAINTAINER=	skozlov@FreeBSD.org
COMMENT=	Community-driven framework for managing your zsh configuration
WWW=		https://ohmyz.sh/

LICENSE=	MIT
LICENSE_FILE=	${WRKSRC}/LICENSE.txt

RUN_DEPENDS=	zsh:shells/zsh

USE_GITHUB=	yes
GH_TAGNAME=	69a6359f7cf8978d464573fb7b023ee3cd00181a

NO_ARCH=	yes
NO_BUILD=	yes

SUB_FILES=	pkg-message

post-extract:
	${RM} -r ${WRKSRC}/log ${WRKSRC}/cache
.for f in install upgrade uninstall check_for_upgrade
	${RM} ${WRKSRC}/tools/${f}.sh
.endfor

post-patch:
	${REINPLACE_CMD} -e "s|%%DATADIR%%|${DATADIR}|g" ${WRKSRC}/templates/zshrc.zsh-template

do-install:
	${MKDIR} ${STAGEDIR}${DATADIR}
	cd ${WRKSRC} && ${COPYTREE_SHARE} . ${STAGEDIR}${DATADIR} "! -path \./\.* ! -name *\.bak ! -name *\.orig"

.include <bsd.port.mk>
