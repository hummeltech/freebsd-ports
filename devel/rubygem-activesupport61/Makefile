PORTNAME=	activesupport
PORTVERSION=	6.1.7.10
CATEGORIES=	devel rubygems
MASTER_SITES=	RG
PKGNAMESUFFIX=	61

MAINTAINER=	sunpoet@FreeBSD.org
COMMENT=	Utility classes and extension that are required by Rails MVC Framework
WWW=		https://github.com/rails/rails/tree/main/activesupport \
		https://rubyonrails.org/

LICENSE=	MIT
LICENSE_FILE=	${WRKSRC}/MIT-LICENSE

RUN_DEPENDS=	rubygem-concurrent-ruby>=1.0.2<2:devel/rubygem-concurrent-ruby \
		rubygem-i18n>=1.6,2<2,2:devel/rubygem-i18n \
		rubygem-minitest>=5.1:devel/rubygem-minitest \
		rubygem-tzinfo>=2.0<3:devel/rubygem-tzinfo \
		rubygem-zeitwerk>=2.3<3:devel/rubygem-zeitwerk

USES=		cpe gem

NO_ARCH=	yes

CPE_VENDOR=	activesupport_project

PORTSCOUT=	limit:^6\.1\.

.include <bsd.port.mk>
