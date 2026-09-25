PORTNAME=	simulide
PORTVERSION=	1.1.0
CATEGORIES=	emulators

MAINTAINER=	simulide-freebsd@example.com
COMMENT=	Electronic circuit simulator and MCU IDE
WWW=		https://www.simulide.com/

USES=		qt:5 desktop-file-utils
USE_QT=		core gui widgets xml concurrent network svg multimedia serialport

NO_BUILD=	yes
DISTFILES=

SIMULIDE_SRC=	${.CURDIR}/../../..
DATADIR=	${PREFIX}/share/simulide

PLIST_FILES=	bin/simulide \
		share/icons/hicolor/scalable/apps/simulide.svg

PORTDATA=	*

DESKTOP_ENTRIES= \
	"SimulIDE" \
	"Real-time electronic circuit simulator and MCU IDE" \
	"simulide" \
	"simulide" \
	"Education;Development;Electronics;" \
	false

do-install:
	${MKDIR} ${STAGEDIR}${PREFIX}/bin
	${MKDIR} ${STAGEDIR}${DATADIR}
	${MKDIR} ${STAGEDIR}${PREFIX}/share/icons/hicolor/scalable/apps
	${INSTALL_PROGRAM} ${SIMULIDE_SRC}/build_XX/simulide \
		${STAGEDIR}${PREFIX}/bin/simulide
	${CP} -R ${SIMULIDE_SRC}/resources/data \
		${STAGEDIR}${DATADIR}/
	${CP} -R ${SIMULIDE_SRC}/resources/examples \
		${STAGEDIR}${DATADIR}/
	${INSTALL_DATA} ${FILESDIR}/simulide.svg \
		${STAGEDIR}${PREFIX}/share/icons/hicolor/scalable/apps/simulide.svg

.include <bsd.port.mk>
