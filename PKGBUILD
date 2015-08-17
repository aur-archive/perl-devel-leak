# Contributor: John D Jones III <jnbek1972 -_AT_- g m a i l -_Dot_- com>
# Generator  : CPANPLUS::Dist::Arch 1.29

pkgname='perl-devel-leak'
pkgver='0.03'
pkgrel='1'
pkgdesc="Utility for looking for perl objects that are not reclaimed."
arch=('i686' 'x86_64')
license=('PerlArtistic' 'GPL')
options=('!emptydirs')
depends=('perl')
makedepends=()
url='http://search.mcpan.org/dist/Devel-Leak'
source=('http://search.mcpan.org/CPAN/authors/id/N/NI/NI-S/Devel-Leak-0.03.tar.gz')
md5sums=('9ee2cf88bd1dbc6091e38ef4597b54bb')
sha512sums=('177f64b87fa6ab08b93f7c5bfcbaf4421e8431bf795976a0a7efa0120828984fed29a2bc12918e5bea9ea3edccf6316ba8daf704f349aece84b45bdd11f57707')
_distdir="Devel-Leak-0.03"

build() {
  ( export PERL_MM_USE_DEFAULT=1 PERL5LIB=""                 \
      PERL_AUTOINSTALL=--skipdeps                            \
      PERL_MM_OPT="INSTALLDIRS=vendor DESTDIR='$pkgdir'"     \
      PERL_MB_OPT="--installdirs vendor --destdir '$pkgdir'" \
      MODULEBUILDRC=/dev/null

    cd "$srcdir/$_distdir"
    /usr/bin/perl Makefile.PL
    make
  )
}

check() {
  cd "$srcdir/$_distdir"
  ( export PERL_MM_USE_DEFAULT=1 PERL5LIB=""
    make test
  )
}

package() {
  cd "$srcdir/$_distdir"
  make install

  find "$pkgdir" -name .packlist -o -name perllocal.pod -delete
}

# Local Variables:
# mode: shell-script
# sh-basic-offset: 2
# End:
# vim:set ts=2 sw=2 et:
