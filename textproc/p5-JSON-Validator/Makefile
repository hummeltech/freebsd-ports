PORTNAME=	JSON-Validator
PORTVERSION=	5.15
CATEGORIES=	textproc perl5
MASTER_SITES=	CPAN
PKGNAMEPREFIX=	p5-

MAINTAINER=	perl@FreeBSD.org
COMMENT=	Validate data against a JSON schema
WWW=		https://metacpan.org/dist/JSON-Validator

LICENSE=	ART20

BUILD_DEPENDS=	${RUN_DEPENDS}
RUN_DEPENDS=	p5-Mojolicious>=7.28:www/p5-Mojolicious \
		p5-YAML-LibYAML>=0.80:textproc/p5-YAML-LibYAML
TEST_DEPENDS=	p5-Data-Validate-Domain>0:dns/p5-Data-Validate-Domain \
		p5-Data-Validate-IP>0:net-mgmt/p5-Data-Validate-IP \
		p5-Net-IDN-Encode>0:textproc/p5-Net-IDN-Encode \
		p5-Test-Deep>0:devel/p5-Test-Deep

USES=		perl5
USE_PERL5=	configure

NO_ARCH=	yes

.include <bsd.port.mk>
