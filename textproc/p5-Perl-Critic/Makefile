PORTNAME=	Perl-Critic
PORTVERSION=	1.156
CATEGORIES=	textproc devel perl5
MASTER_SITES=	CPAN
PKGNAMEPREFIX=	p5-

MAINTAINER=	perl@FreeBSD.org
COMMENT=	Critique Perl source for style and standards
WWW=		https://metacpan.org/release/Perl-Critic

LICENSE=	ART10 GPLv1+
LICENSE_COMB=	dual
LICENSE_FILE=	${WRKSRC}/LICENSE

BUILD_DEPENDS=	${RUN_DEPENDS}
RUN_DEPENDS=	p5-B-Keywords>=1.23:devel/p5-B-Keywords \
		p5-Config-Tiny>=2:devel/p5-Config-Tiny \
		p5-Exception-Class>=1.23:devel/p5-Exception-Class \
		p5-File-Which>=0:sysutils/p5-File-Which \
		p5-List-SomeUtils>=0.55:devel/p5-List-SomeUtils \
		p5-Module-Pluggable>=3.1:devel/p5-Module-Pluggable \
		p5-PPI>=1.277:textproc/p5-PPI \
		p5-PPIx-QuoteLike>=0:textproc/p5-PPIx-QuoteLike \
		p5-PPIx-Regexp>=0.068:textproc/p5-PPIx-Regexp \
		p5-PPIx-Utils>=0.003:textproc/p5-PPIx-Utils \
		p5-Perl-Tidy>=0:devel/p5-Perl-Tidy \
		p5-Pod-Parser>=0:textproc/p5-Pod-Parser \
		p5-Pod-Spell>=1:textproc/p5-Pod-Spell \
		p5-Readonly>=2:devel/p5-Readonly \
		p5-String-Format>=1.18:textproc/p5-String-Format

USES=		perl5
USE_PERL5=	modbuild

NO_ARCH=	yes

.include <bsd.port.mk>
