PORTNAME=	uchar
PORTVERSION=	0.0.2
DISTVERSIONPREFIX=	v
PORTREVISION=	4
CATEGORIES=	devel
PKGNAMEPREFIX=	ocaml-

MAINTAINER=	danfe@FreeBSD.org
COMMENT=	Compatibility library for OCaml's Uchar module
WWW=		https://ocaml.github.io/uchar/

LICENSE=	LGPL21 # (with linking exception)
LICENSE_FILE=	${WRKSRC}/LICENSE

BUILD_DEPENDS=	ocamlbuild:devel/ocaml-ocamlbuild \
		opam-installer:devel/ocaml-opam

USES=		ocaml
USE_GITHUB=	yes
GH_ACCOUNT=	ocaml

PLIST_FILES=	${OCAML_SITELIBDIR}/${PORTNAME}/META

do-build:
	cd ${BUILD_WRKSRC} && ocaml pkg/build.ml \
		native=true native-dynlink=true

do-install:
	cd ${INSTALL_WRKSRC} && opam-installer -i \
		--prefix=${STAGEDIR}${PREFIX} \
		--libdir=${OCAML_SITELIBDIR} ${PORTNAME}.install

.include <bsd.port.mk>
