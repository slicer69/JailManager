PORTNAME=	jailmanager
PORTVERSION=	0.1
CATEGORIES=	sysutils

MAINTAINER=	jsmith@resonatingmedia.com
COMMENT=	Simple shell script for managing FreeBSD jails
WWW=		https://github.com/slicer69/jailmanager

LICENSE=	BSD3CLAUSE 
LICENSE_FILE_BSD3CLAUSE=	${WRKSRC}/LICENSE

RUN_DEPENDS=	${LOCALBASE}/bin/bash:shells/bash
USE_GITHUB=	yes
GH_ACCOUNT=	slicer69

PLIST_FILES=	bin/jm

do-build:

do-install:
	${INSTALL_SCRIPT} ${WRKDIR}/JailManager-${PORTVERSION}/jm ${STAGEDIR}${PREFIX}/bin/jm

.include <bsd.port.mk>
