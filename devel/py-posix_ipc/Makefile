PORTNAME=	posix_ipc
PORTVERSION=	1.1.1
PORTREVISION=	1
CATEGORIES=	devel python
MASTER_SITES=	PYPI
PKGNAMEPREFIX=	${PYTHON_PKGNAMEPREFIX}

MAINTAINER=	bofh@FreeBSD.org
COMMENT=	POSIX IPC primitives for Python
WWW=		https://semanchuk.com/philip/posix_ipc/

LICENSE=	BSD3CLAUSE
LICENSE_FILE=	${WRKSRC}/LICENSE

USES=		python
USE_PYTHON=	distutils autoplist

post-install:
	${STRIP_CMD} ${STAGEDIR}/${PYTHONPREFIX_SITELIBDIR}/posix_ipc*.so

# requires mqueuefs and sem kernel modules loaded

do-test:
	@cd ${WRKSRC} && ${PYTHON_CMD} ${PYDISTUTILS_SETUP} test

.include <bsd.port.mk>
