PORTNAME=	DBD-Sybase
PORTVERSION=	1.25
CATEGORIES=	databases perl5
MASTER_SITES=	CPAN
PKGNAMEPREFIX=	p5-

MAINTAINER=	perl@FreeBSD.org
COMMENT=	Sybase DBI driver for Perl 5
WWW=		https://metacpan.org/release/DBD-Sybase

LICENSE=	ART10 GPLv1+
LICENSE_COMB=	dual

BUILD_DEPENDS=	${RUN_DEPENDS}
BUILD_DEPENDS+=	freetds>=1.3.10:databases/freetds
LIB_DEPENDS=	libct.so:databases/freetds
RUN_DEPENDS=	p5-DBI>=0:databases/p5-DBI

USES=		gettext perl5
USE_PERL5=	configure

CONFIGURE_ENV=	SYBASE=${LOCALBASE}

.if defined(BATCH)
CONFIGURE_ARGS=	< /dev/null
.endif

post-install:
	${STRIP_CMD} ${STAGEDIR}${PREFIX}/${SITE_ARCH_REL}/auto/DBD/Sybase/Sybase.so

.include <bsd.port.mk>
