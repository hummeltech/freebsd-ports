PORTNAME=	Net-BitTorrent-File
PORTVERSION=	1.02
DISTVERSIONSUFFIX=	-fix
PORTREVISION=	1
CATEGORIES=	net-p2p perl5
MASTER_SITES=	CPAN
PKGNAMEPREFIX=	p5-

MAINTAINER=	perl@FreeBSD.org
COMMENT=	Perl5 module for handles loading and saving of .torrent file
WWW=		https://metacpan.org/release/Net-BitTorrent-File

LICENSE=	ART10 GPLv1+
LICENSE_COMB=	dual

DEPRECATED=	Deprecated, no active development in more than a decade so any "new" functionality is missing and interoperability with recent software is very limited if not completely broken
EXPIRATION_DATE=2025-04-30

BUILD_DEPENDS=	${RUN_DEPENDS}
RUN_DEPENDS=	p5-Convert-Bencode>=0:converters/p5-Convert-Bencode \
		p5-Digest-SHA1>=0:security/p5-Digest-SHA1

NO_ARCH=	yes
USE_PERL5=	configure
USES=		perl5
WRKSRC=		${WRKDIR}/${PORTNAME}-${PORTVERSION}

.include <bsd.port.mk>
