PORTNAME=	Net-Libdnet
PORTVERSION=	0.990
CATEGORIES=	net perl5
MASTER_SITES=	CPAN
PKGNAMEPREFIX=	p5-

MAINTAINER=	perl@FreeBSD.org
COMMENT=	Libdnet interface
WWW=		https://metacpan.org/release/Net-Libdnet

LICENSE=	BSD3CLAUSE

BUILD_DEPENDS=	${RUN_DEPENDS}
RUN_DEPENDS=	p5-Class-Gomor>=0:devel/p5-Class-Gomor
LIB_DEPENDS=	libdnet.so:net/libdnet

USES=		perl5
USE_PERL5=	configure

CONFIGURE_ARGS=	INC='-I${LOCALBASE}/include'

post-install:
	${STRIP_CMD} ${STAGEDIR}${PREFIX}/${SITE_ARCH_REL}/auto/Net/Libdnet/Libdnet.so

.include <bsd.port.mk>
