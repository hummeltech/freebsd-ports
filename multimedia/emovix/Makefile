PORTNAME=	emovix
PORTVERSION=	0.9.0
PORTREVISION=	2
CATEGORIES=	multimedia
MASTER_SITES=	SF/movix/eMoviX/0.9

MAINTAINER=	ports@FreeBSD.org
COMMENT=	Mini Linux distro to create bootable video CDs
WWW=		https://movix.sourceforge.net/

LICENSE=	GPLv2
LICENSE_FILE=	${WRKSRC}/COPYING

BROKEN=		Fails to generate ISO image
DEPRECATED=	Abandonware, uses over a decade year old software and no support for anything recent
EXPIRATION_DATE=2025-03-31

GNU_CONFIGURE=	yes
USES=		gmake perl5 shebangfix
SHEBANG_FILES=	mplayer-fonts/centralEU-cp1250/runme \
		mplayer-fonts/centralEU-iso-8859-2/runme \
		scripts/mkmovixiso scripts/movix-conf.in
NO_ARCH=	yes

.include <bsd.port.mk>
