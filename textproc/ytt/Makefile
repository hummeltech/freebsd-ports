PORTNAME=	ytt
DISTVERSIONPREFIX=	v
DISTVERSION=	0.49.0
PORTREVISION=	7
CATEGORIES=	textproc

MAINTAINER=	yuri@FreeBSD.org
COMMENT=	YAML templating tool that works on YAML structure instead of text
WWW=		https://carvel.dev/ytt/

LICENSE=	APACHE20
LICENSE_FILE=	${WRKSRC}/LICENSE

USES=		go:1.22,modules

GO_MODULE=	github.com/carvel-dev/ytt
GO_TARGET=	./cmd/ytt/

PLIST_FILES=	bin/${PORTNAME}

.include <bsd.port.mk>
