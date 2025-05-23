PORTNAME=	oidn
DISTVERSIONPREFIX=	v
DISTVERSION=	2.3.2
CATEGORIES=	graphics
MASTER_SITES=	http://freebsd.org/:weights # bogus URL to make the framework happy, the fetch uses Git URL below
DISTFILES=	${PORTNAME}-weights-${WEIGHTS_GIT_HASH}${EXTRACT_SUFX}:weights

#PATCH_SITES=	https://github.com/${GH_ACCOUNT}/${GH_PROJECT}/commit/
#PATCHFILES=	e5e52d335c58365b6cbd91f9a8a6f9ee9a085bf5.patch:-p1 # fix compile error when using old libc++

MAINTAINER=	yuri@FreeBSD.org
COMMENT=	Intel(R) Open Image Denoise library
WWW=		https://www.openimagedenoise.org/ \
		https://github.com/RenderKit/oidn

LICENSE=	APACHE20
LICENSE_FILE=	${WRKSRC}/LICENSE.txt

ONLY_FOR_ARCHS=		amd64
ONLY_FOR_ARCHS_REASON=	Intel(R) MKL-DNN supports x86 64 bit platforms only (oidn contains a custom version of mkl-dnn, see math/mkl-dnn), and ISPC has a limited availability

FETCH_DEPENDS=	ca_root_nss>0:security/ca_root_nss \
		git:devel/git \
		git-lfs:devel/git-lfs
BUILD_DEPENDS=	ispc>=1.14.1:devel/ispc
LIB_DEPENDS=	libtbb.so:devel/onetbb

USES=		cmake:noninja compiler:c++14-lang python:build
USE_LDCONFIG=	yes

USE_GITHUB=	yes
GH_ACCOUNT=	RenderKit
GH_TUPLE=	OpenImageDenoise:mkl-dnn:9bea36e:m/external/mkl-dnn \
		ROCmSoftwarePlatform:composable_kernel:e85178b:composable_kernel/external/composable_kernel \
		NVIDIA:cutlass:66d9cdd:cutlass/external/cutlass

CMAKE_ARGS=	-DTBB_ROOT:STRING=${LOCALBASE} -DTBB_INCLUDE_DIR:STRING=${LOCALBASE}/include -DPYTHON_EXECUTABLE:STRING=${PYTHON_CMD}

PLIST_SUB=	VER="${PORTVERSION}"

OPTIONS_DEFINE=			APPS DOCS OPENIMAGEIO
OPTIONS_DEFAULT=		APPS OPENIMAGEIO
OPTIONS_SUB=			yes

APPS_DESC=			Build example and test apps
APPS_CMAKE_BOOL=		OIDN_APPS

DOCSDIR=			share/doc/OpenImageDenoise

OPENIMAGEIO_DESC=		Build with OpenImageIO for image formats support
OPENIMAGEIO_CMAKE_BOOL=		OIDN_APPS_OPENIMAGEIO
OPENIMAGEIO_LIB_DEPENDS=	libOpenImageIO.so:graphics/openimageio
OPENIMAGEIO_IMPLIES=		APPS # OpenImageIO is only used by apps and examples

WEIGHTS_GIT_URL=	https://github.com/RenderKit/oidn-weights.git
WEIGHTS_GIT_HASH=	28883d1769d5930e13cf7f1676dd852bd81ed9e7

pre-fetch:
	@if [ "${FORCE_FETCH_ALL}" = "true" ] || ! [ -f "${DISTDIR}/${DIST_SUBDIR}/${PORTNAME}-weights-${WEIGHTS_GIT_HASH}${EXTRACT_SUFX}" ]; then \
		${MKDIR} ${DISTDIR}/${DIST_SUBDIR} && \
		cd ${DISTDIR}/${DIST_SUBDIR} && \
		${ECHO} "==> Fetching the oidn/weights subproject with large LFS files" && \
		( \
			${MKDIR} ${WRKDIR}; \
			HOME=${WRKDIR}; \
			git config --global filter.lfs.smudge "git-lfs smudge -- %f" && \
			GIT_CLONE_PROTECTION_ACTIVE=false git clone -nq ${WEIGHTS_GIT_URL} ${PORTNAME}-weights-${WEIGHTS_GIT_HASH} && \
			(cd ${PORTNAME}-weights-${WEIGHTS_GIT_HASH} && git reset -q --hard ${WEIGHTS_GIT_HASH} && ${RM} -r .git) && \
			${RM} -r ${WRKDIR} \
		) && \
		${FIND} ${PORTNAME}-weights-${WEIGHTS_GIT_HASH} -and -exec ${TOUCH} -h -d 1970-01-01T00:00:00Z {} \; && \
		${FIND} ${PORTNAME}-weights-${WEIGHTS_GIT_HASH} -print0 | LC_ALL=C ${SORT} -z | \
		${TAR} czf ${PORTNAME}-weights-${WEIGHTS_GIT_HASH}${EXTRACT_SUFX} --format=ustar --gid 0 --uid 0 --options gzip:!timestamp --no-recursion --null -T - && \
		${RM} -r ${PORTNAME}-weights-${WEIGHTS_GIT_HASH}; \
	fi

post-extract:
	@cd ${WRKSRC} && ${RMDIR} weights && ${LN} -s ${WRKDIR}/${PORTNAME}-weights-${WEIGHTS_GIT_HASH} weights

.include <bsd.port.mk>
