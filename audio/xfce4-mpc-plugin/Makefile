PORTNAME=	xfce4-mpc-plugin
PORTVERSION=	0.5.5
CATEGORIES=	audio xfce
MASTER_SITES=	XFCE/panel-plugins
DIST_SUBDIR=	xfce4

MAINTAINER=	xfce@FreeBSD.org
COMMENT=	Musicpd client plugin for the Xfce panel
WWW=		https://docs.xfce.org/panel-plugins/xfce4-mpc-plugin/start

LICENSE=	ISCL

LIB_DEPENDS=	libharfbuzz.so:print/harfbuzz \
		libmpd.so:audio/libmpd
RUN_DEPENDS=	musicpd:audio/musicpd

USES=		compiler:c11 gettext-tools gmake gnome libtool pkgconfig \
		tar:bzip2 xfce
USE_GNOME=	cairo gdkpixbuf gtk30
USE_XFCE=	libmenu panel

GNU_CONFIGURE=		yes
INSTALL_TARGET=		install-strip
CONFIGURE_ARGS+=	--with-libmpd=${LOCALBASE}

OPTIONS_DEFINE=		NLS
OPTIONS_SUB=		yes

NLS_CONFIGURE_ENABLE=	nls
NLS_USES=		gettext-runtime

.include <bsd.port.mk>
