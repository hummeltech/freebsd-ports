PORTNAME=	mapnik
DISTVERSIONPREFIX=	v
DISTVERSION=	3.1.0
PORTREVISION=	3
CATEGORIES=	graphics geography
MASTER_SITES=	https://github.com/mapnik/mapnik/releases/download/${DISTVERSIONFULL}/

PATCH_SITES=	https://github.com/mapnik/mapnik/commit/
PATCHFILES=	8944e81367d2b3b91a41e24116e1813c01491e5d.patch \
		83779b7b6bdd229740b1b5e12a4a8fe27114cb7d.patch \
		7f0daee8b37d8cf6eff32529b1762ffd5104f3f3.patch
PATCH_DIST_STRIP=	-p1 -F3

MAINTAINER=	david.hummel@gmail.com
COMMENT=	Free Toolkit For Developing Mapping Applications
WWW=		http://www.mapnik.org/

LICENSE=	LGPL21+
LICENSE_FILE=	${WRKSRC}/COPYING

BUILD_DEPENDS=	${LOCALBASE}/share/fonts/dejavu/DejaVuSans.ttf:x11-fonts/dejavu
LIB_DEPENDS=	libboost_filesystem.so:devel/boost-libs \
		libboost_program_options.so:devel/boost-libs \
		libboost_regex.so:devel/boost-libs \
		libboost_system.so:devel/boost-libs \
		libfreetype.so:print/freetype2 \
		libharfbuzz.so:print/harfbuzz \
		libicuuc.so:devel/icu
RUN_DEPENDS=	dejavu>0:x11-fonts/dejavu

USES=		compiler:c++14-lang gmake gnome pkgconfig python tar:bzip2
USE_GNOME=	libxml2
USE_LDCONFIG=	yes
MAKE_ARGS=	PYTHON="${PYTHON_CMD}"
MAKE_ENV=	JOBS=${MAKE_JOBS_NUMBER}
HAS_CONFIGURE=	yes
CONFIGURE_ARGS=	CUSTOM_CFLAGS="${CFLAGS}" \
		CUSTOM_CXXFLAGS="${CXXFLAGS}" \
		CUSTOM_LDFLAGS="${LDFLAGS}" \
		DESTDIR="${STAGEDIR}" \
		INPUT_PLUGINS="`${ECHO} ${INPUT_PLUGINS} | ${TR} ' ' ,`" \
		SYSTEM_FONTS=${LOCALBASE}/share/fonts/dejavu \
		XMLPARSER=libxml2
CONFIGURE_ENV=	PYTHON="${PYTHON_CMD}"

PORTDOCS=	AUTHORS.md CHANGELOG.md CODE_OF_CONDUCT.md INSTALL.md README.md docs/*

INPUT_PLUGINS=	csv raster shape geojson topojson

OPTIONS_DEFINE=		CAIRO DOCS JPEG PNG PROJ TIFF WEBP
OPTIONS_DEFAULT=	CAIRO GDAL JPEG OGR PGRASTER PNG POSTGIS PROJ SQLITE3 \
			TIFF WEBP MAPNIK_INDEX MAPNIK_RENDER PGSQL2SQLITE SHAPEINDEX SVG2PNG
OPTIONS_GROUP=		INPUT APPS OTHER
OPTIONS_GROUP_INPUT=	GDAL OGR PGRASTER POSTGIS SQLITE3
OPTIONS_GROUP_APPS=	MAPNIK_INDEX MAPNIK_RENDER PGSQL2SQLITE SHAPEINDEX SVG2PNG
OPTIONS_GROUP_OTHER=	BENCHMARK CPP_TESTS DEMO
OPTIONS_SUB=		yes

INPUT_DESC=	Input plugins
GDAL_DESC=	GDAL input plugin
OGR_DESC=	OGR input plugin
POSTGIS_DESC=	PostGIS input plugin
PGRASTER_DESC=	PGraster input plugin
SQLITE3_DESC=	SQLite input plugin

APPS_DESC=		Additional applications
MAPNIK_INDEX_DESC=	Compile mapnik-index application
MAPNIK_RENDER_DESC=	Compile mapnik-render application
PGSQL2SQLITE_DESC=	Compile pgsql2sqlite application
SHAPEINDEX_DESC=	Compile shapeindex application
SVG2PNG_DESC=		Compile svg2png application

OTHER_DESC=	Other
BENCHMARK_DESC=	Compile C++ benchmark scripts
CPP_TESTS_DESC=	Compile C++ tests
DEMO_DESC=	Compile C++ demo application

PROJ_DESC=	PROJ support

CAIRO_DESC=	Enable cairo rendering

GDAL_VARS=		INPUT_PLUGINS+=gdal
GDAL_LIB_DEPENDS=	libgdal.so:graphics/gdal
OGR_VARS=		INPUT_PLUGINS+=ogr
OGR_LIB_DEPENDS=	libgdal.so:graphics/gdal
POSTGIS_VARS=		INPUT_PLUGINS+=postgis
POSTGIS_USES=		pgsql
PGRASTER_VARS=		INPUT_PLUGINS+=pgraster
PGRASTER_USES=		pgsql
SQLITE3_VARS=		INPUT_PLUGINS+=sqlite
SQLITE3_USES=		sqlite:3

MAPNIK_INDEX_VARS=	CONFIGURE_ARGS+=MAPNIK_INDEX=True
MAPNIK_INDEX_VARS_OFF=	CONFIGURE_ARGS+=MAPNIK_INDEX=False
MAPNIK_RENDER_VARS=	CONFIGURE_ARGS+=MAPNIK_RENDER=True
MAPNIK_RENDER_VARS_OFF=	CONFIGURE_ARGS+=MAPNIK_RENDER=False
PGSQL2SQLITE_VARS=	CONFIGURE_ARGS+=PGSQL2SQLITE=True
PGSQL2SQLITE_VARS_OFF=	CONFIGURE_ARGS+=PGSQL2SQLITE=False
SHAPEINDEX_VARS=	CONFIGURE_ARGS+=SHAPEINDEX=True
SHAPEINDEX_VARS_OFF=	CONFIGURE_ARGS+=SHAPEINDEX=False
SVG2PNG_VARS=		CONFIGURE_ARGS+=SVG2PNG=True
SVG2PNG_VARS_OFF=	CONFIGURE_ARGS+=SVG2PNG=False

DEMO_VARS=		CONFIGURE_ARGS+=DEMO=True
DEMO_VARS_OFF=		CONFIGURE_ARGS+=DEMO=False
BENCHMARK_VARS=		CONFIGURE_ARGS+=BENCHMARK=True
BENCHMARK_VARS_OFF=	CONFIGURE_ARGS+=BENCHMARK=False
CPP_TESTS_VARS=		CONFIGURE_ARGS+=CPP_TESTS=True
CPP_TESTS_VARS_OFF=	CONFIGURE_ARGS+=CPP_TESTS=False

PNG_LIB_DEPENDS=	libpng.so:graphics/png
PNG_MAKE_ARGS_OFF=	PNG=False
JPEG_USES=		jpeg
JPEG_MAKE_ARGS_OFF=	JPEG=False
TIFF_LIB_DEPENDS=	libtiff.so:graphics/tiff
TIFF_MAKE_ARGS_OFF=	TIFF=False
WEBP_LIB_DEPENDS=	libwebp.so:graphics/webp
WEBP_MAKE_ARGS_OFF=	WEBP=False

PROJ_LIB_DEPENDS=	libproj.so:graphics/proj
PROJ_MAKE_ARGS_OFF=	PROJ=False

CAIRO_LIB_DEPENDS=	libcairo.so:graphics/cairo
CAIRO_BUILD_DEPENDS=	${PYTHON_PKGNAMEPREFIX}cairo>=1.8.2:graphics/py-cairo@${PY_FLAVOR}
CAIRO_MAKE_ARGS_OFF=	CAIRO=False

pre-configure-SQLITE3-on:
	@if ! ${LOCALBASE}/bin/sqlite3 :memory: 'create virtual table foo using rtree(pkid, xmin, xmax, ymin, ymax)' > /dev/null 2>&1; then \
		${ECHO_MSG} "" ; \
		${ECHO_MSG} "The SQLite plugin requires libsqlite3 built with RTREE support"; \
		${ECHO_MSG} "Please, reinstall 'databases/sqlite3' port with R*Tree module enabled"; \
		${ECHO_MSG} "" ; \
		${FALSE} ; \
	fi

post-patch:
	@${REINPLACE_CMD} -e 's#/usr/local#${LOCALBASE}#g' \
		-e 's#/usr/include#${LOCALBASE}/include#g' \
		-e "s#'/usr/' + LIBDIR_SCHEMA_DEFAULT#'${LOCALBASE}/' + LIBDIR_SCHEMA_DEFAULT#g" \
		${WRKSRC}/SConstruct
# Resolve warning: 'SyntaxWarning: "is not" with a literal. Did you mean "!="?'
	@${REINPLACE_CMD} -e 's#if len(operation_list) is not 2#if len(operation_list) != 2#g' \
		${WRKSRC}/scons/scons-local-3.0.1/SCons/Defaults.py

post-install:
	@${STRIP_CMD} ${STAGEDIR}${PREFIX}/bin/mapnik-index \
		${STAGEDIR}${PREFIX}/bin/mapnik-render \
		${STAGEDIR}${PREFIX}/bin/pgsql2sqlite \
		${STAGEDIR}${PREFIX}/bin/shapeindex \
		${STAGEDIR}${PREFIX}/bin/svg2png
	@${STRIP_CMD} ${STAGEDIR}${PREFIX}/lib/*.so
	@${STRIP_CMD} ${STAGEDIR}${PREFIX}/lib/mapnik/input/*.input

post-install-DOCS-on:
	@${MKDIR} ${STAGEDIR}${DOCSDIR}
	@cd ${WRKSRC} && ${INSTALL_DATA} AUTHORS.md CHANGELOG.md CODE_OF_CONDUCT.md INSTALL.md README.md ${STAGEDIR}${DOCSDIR}
	@${MKDIR} ${STAGEDIR}${DOCSDIR}/docs
	@cd ${WRKSRC} && ${INSTALL_DATA} docs/* ${STAGEDIR}${DOCSDIR}/docs

.include <bsd.port.mk>
