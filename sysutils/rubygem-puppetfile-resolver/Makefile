PORTNAME=	puppetfile-resolver
DISTVERSION=	0.6.3
CATEGORIES=	sysutils rubygems
MASTER_SITES=	RG

MAINTAINER=	puppet@FreeBSD.org
COMMENT=	Dependency resolver for Puppetfiles as a gem
WWW=		https://rubygems.org/gems/puppetfile-resolver

LICENSE=	APACHE20
LICENSE_FILE=	${WRKSRC}/LICENSE

RUN_DEPENDS=	rubygem-molinillo>=0.6<1:devel/rubygem-molinillo \
		rubygem-semantic_puppet>=1.0<2:devel/rubygem-semantic_puppet

USES=		gem

NO_ARCH=	yes

.include <bsd.port.mk>
