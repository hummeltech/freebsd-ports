PORTNAME=	pyvmomi
DISTVERSIONPREFIX=	v
DISTVERSION=	7.0.3
PORTREVISION=	1
CATEGORIES=	net python

MAINTAINER=	robak@FreeBSD.org
COMMENT=	Python SDK for the VMware vSphere API of ESX, ESXi, and vCenter
WWW=		https://github.com/vmware/pyvmomi

USE_GITHUB=     yes
GH_ACCOUNT=     vmware
GH_PROJECT=	${PORTNAME}

LICENSE=	APACHE20

RUN_DEPENDS=	${PYTHON_PKGNAMEPREFIX}requests>=2.3.0:www/py-requests@${PY_FLAVOR} \
		${PYTHON_PKGNAMEPREFIX}six>=1.7.3:devel/py-six@${PY_FLAVOR}

USES=		python
USE_PYTHON=	autoplist distutils concurrent optsuffix

post-patch:
	${REINPLACE_CMD} -E "/data_files/s|\[\(''|\[\('${DOCSDIR}'|"  ${WRKSRC}/setup.py

.include <bsd.port.mk>
