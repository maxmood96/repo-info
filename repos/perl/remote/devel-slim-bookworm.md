## `perl:devel-slim-bookworm`

```console
$ docker pull perl@sha256:0a8295839c836129d3db761e8b929f38e59faad2db92799865844b992472963b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 16
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v5
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; mips64le
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `perl:devel-slim-bookworm` - linux; amd64

```console
$ docker pull perl@sha256:5ab925a91b14504236d3836f830f9ceccd1e346d59eeb833f8e8639392411ec1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.6 MB (58646097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c60ec484182bc18b1d87c6cf92f1ccd24c1954074f8706fdd2700cc4e7993ef`
-	Default Command: `["perl5.43.7","-de0"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 02:56:23 GMT
WORKDIR /usr/src/perl
# Tue, 03 Feb 2026 03:00:44 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/C/CO/CORION/perl-5.43.7.tar.gz -o perl-5.43.7.tar.gz     && echo 'd8aa3057fab477b779f6658e42471836cc05f6bcbfd8416959e2f8d177a47d0b *perl-5.43.7.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.43.7.tar.gz -C /usr/src/perl     && rm perl-5.43.7.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.091.tar.gz'     && echo 'c5996e7335912a5c99e06bdb47ff39df309a857cbd8fd2627a021cefdb53cf54 *IO-Socket-SSL-2.091.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.091.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.091* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Tue, 03 Feb 2026 03:00:44 GMT
WORKDIR /usr/src/app
# Tue, 03 Feb 2026 03:00:44 GMT
CMD ["perl5.43.7" "-de0"]
```

-	Layers:
	-	`sha256:4831516dd0cb86845f5f902cb9b9d25b5c853152c337eb57e4737a9b7e2a2eb9`  
		Last Modified: Tue, 03 Feb 2026 01:13:33 GMT  
		Size: 28.2 MB (28228487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec4eb07a1c0961c8c82b5f056ed8571dfe693500460923d98bae031c6190135a`  
		Last Modified: Tue, 03 Feb 2026 03:00:55 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42addadb3a14a875484266c3615d6d06569bd2ec9bf19d7a3abe473a9834fe7c`  
		Last Modified: Tue, 03 Feb 2026 03:00:56 GMT  
		Size: 30.4 MB (30417341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d601240c3a7b192baed4a584dcabb2ee2fff53df79ecb9a3119798d2cc916ce1`  
		Last Modified: Tue, 03 Feb 2026 03:00:55 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim-bookworm` - unknown; unknown

```console
$ docker pull perl@sha256:c2153dcdafaa8da13f766c29e65f15108b438fd3aab26762edb3e8609acda3d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3957584 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6f0fe505a31527502c2e0ee338e08dd246ac06c871b5d9c4dff597b4bf9a6f8`

```dockerfile
```

-	Layers:
	-	`sha256:bd499644eb9e3db3400af3e6074410aa674306042fc76e80a08402561e41f055`  
		Last Modified: Tue, 03 Feb 2026 03:00:56 GMT  
		Size: 3.9 MB (3939340 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2a62d5c40485ee23b4768d0fbda3ce0b2a5d63fc9ba657f956ef186a6282ad32`  
		Last Modified: Tue, 03 Feb 2026 03:00:55 GMT  
		Size: 18.2 KB (18244 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-slim-bookworm` - linux; arm variant v5

```console
$ docker pull perl@sha256:e1ea0223f9deb6e85b9b93db594d720095b6e8b84b3b634821d305f369c115ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.3 MB (53251429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6be40818d5b3b412f626fbefbbb50a5f8143e7567fb170c73f175849feaf7ca`
-	Default Command: `["perl5.43.7","-de0"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 03:36:01 GMT
WORKDIR /usr/src/perl
# Tue, 03 Feb 2026 03:41:52 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/C/CO/CORION/perl-5.43.7.tar.gz -o perl-5.43.7.tar.gz     && echo 'd8aa3057fab477b779f6658e42471836cc05f6bcbfd8416959e2f8d177a47d0b *perl-5.43.7.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.43.7.tar.gz -C /usr/src/perl     && rm perl-5.43.7.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.091.tar.gz'     && echo 'c5996e7335912a5c99e06bdb47ff39df309a857cbd8fd2627a021cefdb53cf54 *IO-Socket-SSL-2.091.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.091.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.091* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Tue, 03 Feb 2026 03:41:52 GMT
WORKDIR /usr/src/app
# Tue, 03 Feb 2026 03:41:52 GMT
CMD ["perl5.43.7" "-de0"]
```

-	Layers:
	-	`sha256:6036aff531a372e1e9da48952322760c8c052f6735e66afd3251a32e5baace8d`  
		Last Modified: Tue, 03 Feb 2026 01:13:33 GMT  
		Size: 25.8 MB (25757618 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:083d685b3afd0553c5de437e988aea2f248648013403610712c522e45a6c730a`  
		Last Modified: Tue, 03 Feb 2026 03:42:03 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:251169e978a55f6124dab37339bfda6e3173a23fe4b4c90a1ce9fe5f97a6d819`  
		Last Modified: Tue, 03 Feb 2026 03:42:03 GMT  
		Size: 27.5 MB (27493542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df2e3350499d1187b34f91da442b3be9256936cfeef06fb0ab92c9ad8c609b12`  
		Last Modified: Tue, 03 Feb 2026 03:42:03 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim-bookworm` - unknown; unknown

```console
$ docker pull perl@sha256:a35cc7afdb658615c887317d0f7ca5214177e1caaf0906609fdb79345e0e4ef2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3928507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf390bbfc032ddac0a9986951a9968a9eaf798ca41334ced539d222ee1f1f4a2`

```dockerfile
```

-	Layers:
	-	`sha256:0d922fef6dfb276cc5be4165db677a43886122b0fa90e16353392a2a0f673e4d`  
		Last Modified: Tue, 03 Feb 2026 03:42:03 GMT  
		Size: 3.9 MB (3910191 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9f250d577eccce2cf174d96d8568a08fc93e15cdd7804b393db4ea3976a2c82c`  
		Last Modified: Tue, 03 Feb 2026 03:42:03 GMT  
		Size: 18.3 KB (18316 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-slim-bookworm` - linux; arm variant v7

```console
$ docker pull perl@sha256:7ed764ca4628d682f962cb11e62173140f603d3e2e36a1262f30ac7b165b0aff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.5 MB (50504447 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b82efefacfaa3a144bb25c28e2812e18c517dc8b31d285fba70d79f34a0cc1b8`
-	Default Command: `["perl5.43.7","-de0"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1768176000'
# Mon, 26 Jan 2026 21:52:50 GMT
WORKDIR /usr/src/perl
# Mon, 26 Jan 2026 21:58:24 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/C/CO/CORION/perl-5.43.7.tar.gz -o perl-5.43.7.tar.gz     && echo 'd8aa3057fab477b779f6658e42471836cc05f6bcbfd8416959e2f8d177a47d0b *perl-5.43.7.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.43.7.tar.gz -C /usr/src/perl     && rm perl-5.43.7.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.091.tar.gz'     && echo 'c5996e7335912a5c99e06bdb47ff39df309a857cbd8fd2627a021cefdb53cf54 *IO-Socket-SSL-2.091.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.091.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.091* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Mon, 26 Jan 2026 21:58:24 GMT
WORKDIR /usr/src/app
# Mon, 26 Jan 2026 21:58:24 GMT
CMD ["perl5.43.7" "-de0"]
```

-	Layers:
	-	`sha256:ce9b9afe4e779d4b89f92e338fcd7dde1b11be3e68cd4c559a53dc9328ce4b5e`  
		Last Modified: Tue, 13 Jan 2026 00:42:03 GMT  
		Size: 23.9 MB (23934118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79edbb3a4a4232eff2357530dbad429069537fcac75332bfe53f1a0ae73a30bd`  
		Last Modified: Mon, 26 Jan 2026 21:58:35 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08f14def24c3c2250654922c1605f9fd777026deedbf40d8befaaf186ef079f1`  
		Last Modified: Mon, 26 Jan 2026 21:58:35 GMT  
		Size: 26.6 MB (26570066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b709c6b354b50e03ecd4264191d98c9d5e45c2b37d858309e8ffd32c2707f8a`  
		Last Modified: Mon, 26 Jan 2026 21:58:35 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim-bookworm` - unknown; unknown

```console
$ docker pull perl@sha256:6c8db59aa3a605f1de87e586738292b1dd501f76d2e966bd0b7470a359996ebc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3927731 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db731e9639415623ce155e04992c18c70b83c28569de680cd6efd8e7e724b27c`

```dockerfile
```

-	Layers:
	-	`sha256:a02a42100dec7d83201e1e94dc953e3620e0d07afeb3aad652db7da7e5042e14`  
		Last Modified: Mon, 26 Jan 2026 21:58:35 GMT  
		Size: 3.9 MB (3909416 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4a9137669cbe046afe63d5596aa6f1a46fd6012c4c286c458d7cb5edcf54feb8`  
		Last Modified: Mon, 26 Jan 2026 21:58:35 GMT  
		Size: 18.3 KB (18315 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-slim-bookworm` - linux; arm64 variant v8

```console
$ docker pull perl@sha256:86285656d55cd33ffaed5b4f0b8526f50282084daad78cd4683c91067eea915a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.4 MB (57379141 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aef701f046baba5b8e6fa3156bff509236ab90cd94885f7fe2c45a7f156724f8`
-	Default Command: `["perl5.43.7","-de0"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1768176000'
# Mon, 26 Jan 2026 21:54:44 GMT
WORKDIR /usr/src/perl
# Mon, 26 Jan 2026 21:59:31 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/C/CO/CORION/perl-5.43.7.tar.gz -o perl-5.43.7.tar.gz     && echo 'd8aa3057fab477b779f6658e42471836cc05f6bcbfd8416959e2f8d177a47d0b *perl-5.43.7.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.43.7.tar.gz -C /usr/src/perl     && rm perl-5.43.7.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.091.tar.gz'     && echo 'c5996e7335912a5c99e06bdb47ff39df309a857cbd8fd2627a021cefdb53cf54 *IO-Socket-SSL-2.091.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.091.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.091* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Mon, 26 Jan 2026 21:59:31 GMT
WORKDIR /usr/src/app
# Mon, 26 Jan 2026 21:59:31 GMT
CMD ["perl5.43.7" "-de0"]
```

-	Layers:
	-	`sha256:33bdc9671af8942d96d2f78f67aeec06580065dde1272decac3732689ec7c0e8`  
		Last Modified: Tue, 13 Jan 2026 00:42:00 GMT  
		Size: 28.1 MB (28107889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50891d2fc2f446edf225d539ccf0ca93d8a4bd8370cd6f7debb5cfc7961c8b5b`  
		Last Modified: Mon, 26 Jan 2026 21:59:42 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:938862b02c18683538361f36925ca012349f715668281c1a2099fcc26c7e67c1`  
		Last Modified: Mon, 26 Jan 2026 21:59:43 GMT  
		Size: 29.3 MB (29270984 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee8f0448a9527a3101ee34f12b52372f9f26ec06c5675c1caed9b7616782eb3c`  
		Last Modified: Mon, 26 Jan 2026 21:59:42 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim-bookworm` - unknown; unknown

```console
$ docker pull perl@sha256:ef174fb9dd957f18a3c8fa03e7fef8fab556c5a6c30f59754303022fa79db032
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3928913 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68cc18c1dc5c98fdb433e1a3baa04a05bf9dbc0a6d919283220513f15f039f73`

```dockerfile
```

-	Layers:
	-	`sha256:7775640aa261b45ddc813950fe934b6bfea01cb6266deebd670ff4022981d7b1`  
		Last Modified: Mon, 26 Jan 2026 21:59:42 GMT  
		Size: 3.9 MB (3910577 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f433489bdc8eb9bfff99dae88156486f3b7ecc4da4ef3fffb6838fb18fda505e`  
		Last Modified: Mon, 26 Jan 2026 21:59:42 GMT  
		Size: 18.3 KB (18336 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-slim-bookworm` - linux; 386

```console
$ docker pull perl@sha256:d1998e1ed5c03cfacdf91d135bbfc2b851a5130c775f4506549069493a4f8366
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.7 MB (58749697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71a689d28f4071c005a3bf067185550e2f633125bc21db6e2563781c63301b2c`
-	Default Command: `["perl5.43.7","-de0"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1768176000'
# Mon, 26 Jan 2026 21:56:33 GMT
WORKDIR /usr/src/perl
# Mon, 26 Jan 2026 22:01:42 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/C/CO/CORION/perl-5.43.7.tar.gz -o perl-5.43.7.tar.gz     && echo 'd8aa3057fab477b779f6658e42471836cc05f6bcbfd8416959e2f8d177a47d0b *perl-5.43.7.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.43.7.tar.gz -C /usr/src/perl     && rm perl-5.43.7.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.091.tar.gz'     && echo 'c5996e7335912a5c99e06bdb47ff39df309a857cbd8fd2627a021cefdb53cf54 *IO-Socket-SSL-2.091.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.091.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.091* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Mon, 26 Jan 2026 22:01:42 GMT
WORKDIR /usr/src/app
# Mon, 26 Jan 2026 22:01:42 GMT
CMD ["perl5.43.7" "-de0"]
```

-	Layers:
	-	`sha256:2a0cffcee0205fc7f72267552713e68aa945359253bcab303f4dd69e7491c38d`  
		Last Modified: Tue, 13 Jan 2026 00:42:37 GMT  
		Size: 29.2 MB (29210067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68ee3c57b970e9e5b06ebee95fc7199af48cfbcf6c7105b53770a97060ceccdb`  
		Last Modified: Mon, 26 Jan 2026 22:01:52 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fc93dd95bb01e0f749dab75a4384fb9aff69df653de67495442b5df492dc44e`  
		Last Modified: Mon, 26 Jan 2026 22:01:53 GMT  
		Size: 29.5 MB (29539363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0853ca1e405d7693dc661bb098222ee4218daba614a121ac776192f0c772e77`  
		Last Modified: Mon, 26 Jan 2026 22:01:52 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim-bookworm` - unknown; unknown

```console
$ docker pull perl@sha256:585600094e99e906b8229e98ac3f794e82276059cc96d39cf1dfcb351b15dab5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3951499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de77df72f028b65e40a3ee68cbba3b1939eb717e8c40a4d76e8dc0010bbab721`

```dockerfile
```

-	Layers:
	-	`sha256:823712d717717b691616ac899fc3efa9903c3e3b3d64ede54aef61e4b1cd5292`  
		Last Modified: Mon, 26 Jan 2026 22:01:53 GMT  
		Size: 3.9 MB (3933282 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c1e8b1fadc3e254192af85026a717d3fe6bbc7309442dd7fc9d9002701179e45`  
		Last Modified: Mon, 26 Jan 2026 22:01:52 GMT  
		Size: 18.2 KB (18217 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-slim-bookworm` - linux; mips64le

```console
$ docker pull perl@sha256:9ffc79562c7f65a03c3438a82db1e155d36365807b6a34672232829f911673d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.1 MB (57092046 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cf511719732253e96d18a1e7e42cd5e2c436f3f0b70a14f98a6c175a9478e6d`
-	Default Command: `["perl5.43.7","-de0"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 16:56:47 GMT
WORKDIR /usr/src/perl
# Mon, 26 Jan 2026 22:42:49 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/C/CO/CORION/perl-5.43.7.tar.gz -o perl-5.43.7.tar.gz     && echo 'd8aa3057fab477b779f6658e42471836cc05f6bcbfd8416959e2f8d177a47d0b *perl-5.43.7.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.43.7.tar.gz -C /usr/src/perl     && rm perl-5.43.7.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.091.tar.gz'     && echo 'c5996e7335912a5c99e06bdb47ff39df309a857cbd8fd2627a021cefdb53cf54 *IO-Socket-SSL-2.091.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.091.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.091* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Mon, 26 Jan 2026 22:42:50 GMT
WORKDIR /usr/src/app
# Mon, 26 Jan 2026 22:42:50 GMT
CMD ["perl5.43.7" "-de0"]
```

-	Layers:
	-	`sha256:c063a3c188d3088513ac303ee5a03a6c0ddff0d68a1e46804a822134a25bf8e8`  
		Last Modified: Tue, 13 Jan 2026 00:40:54 GMT  
		Size: 28.5 MB (28513755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35c538ce4879599b5ff715e79d55c510bcbc55404be84947cc500ebf09345570`  
		Last Modified: Tue, 13 Jan 2026 17:22:43 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53e6f48ec247c597bbc996bbed7ed79fe6d0f467269bee9f46e8ce0e4f94bb6e`  
		Last Modified: Mon, 26 Jan 2026 22:43:40 GMT  
		Size: 28.6 MB (28578023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebafe3499447c510e672ab4186283c0f97c1899591cbccc360a5a9c732cbc401`  
		Last Modified: Mon, 26 Jan 2026 22:43:36 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim-bookworm` - unknown; unknown

```console
$ docker pull perl@sha256:79d5c4ec386c9c0857e72020982588e6dc16b90bd6d0f3dd92006d99f0a95bf0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.1 KB (18086 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e422258a3a2bab2b0a0ccd4cbea06733ad4c9ec88c91a92f5bdb76fd1cc3fba`

```dockerfile
```

-	Layers:
	-	`sha256:0eff73ceae3d36a1e6efe54d862068adde7235a43323b3338a698cf5c97cf024`  
		Last Modified: Mon, 26 Jan 2026 22:43:36 GMT  
		Size: 18.1 KB (18086 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-slim-bookworm` - linux; ppc64le

```console
$ docker pull perl@sha256:d92f34a25453e7eb72111b09bce1491de26e05928e27b91475068be275dde60c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.3 MB (63279204 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b342f2badb8110bb4956764a7a558e8d097d6031c59d93bc104366a2034616d`
-	Default Command: `["perl5.43.7","-de0"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1768176000'
# Mon, 26 Jan 2026 22:01:40 GMT
WORKDIR /usr/src/perl
# Mon, 26 Jan 2026 22:09:40 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/C/CO/CORION/perl-5.43.7.tar.gz -o perl-5.43.7.tar.gz     && echo 'd8aa3057fab477b779f6658e42471836cc05f6bcbfd8416959e2f8d177a47d0b *perl-5.43.7.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.43.7.tar.gz -C /usr/src/perl     && rm perl-5.43.7.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.091.tar.gz'     && echo 'c5996e7335912a5c99e06bdb47ff39df309a857cbd8fd2627a021cefdb53cf54 *IO-Socket-SSL-2.091.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.091.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.091* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Mon, 26 Jan 2026 22:09:40 GMT
WORKDIR /usr/src/app
# Mon, 26 Jan 2026 22:09:40 GMT
CMD ["perl5.43.7" "-de0"]
```

-	Layers:
	-	`sha256:cf92d3bf0add4f20720c3232cd336a7f7f50627989684b748675db0b2f2ce746`  
		Last Modified: Tue, 13 Jan 2026 23:17:03 GMT  
		Size: 32.1 MB (32068709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4892f68912311db4d8a6f760096ce92822b53c261e1013ca20369a6ba601ebeb`  
		Last Modified: Mon, 26 Jan 2026 22:09:49 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91720c8a328ad74aabc55604a65a3ac3ab43f24d8e76da150e6cc5f4ba362e8f`  
		Last Modified: Mon, 26 Jan 2026 22:10:10 GMT  
		Size: 31.2 MB (31210227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:205ee06060e1cf2f9567107d7ee93b84833ebe4e21e820fc9f33f2597fae04bd`  
		Last Modified: Mon, 26 Jan 2026 22:10:09 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim-bookworm` - unknown; unknown

```console
$ docker pull perl@sha256:dc10e079f8005bcdcfd2fede8a73d91d629d69a78972bf51fdf21b5f4cc99210
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3943550 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0087ac82808de2537e1e6dbf287dd98b4f8eb595e84d594c40a684fd7402d143`

```dockerfile
```

-	Layers:
	-	`sha256:ad2cfcae727f3c3337e28f4c5def8d609f24bf312c55fdbdf5f56ce8396f8186`  
		Last Modified: Mon, 26 Jan 2026 22:10:09 GMT  
		Size: 3.9 MB (3925268 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3723e05d6351a64d2b443b11e27e8b5d1ec96945dc1b336fa6b7e747a9cafe2d`  
		Last Modified: Mon, 26 Jan 2026 22:10:08 GMT  
		Size: 18.3 KB (18282 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-slim-bookworm` - linux; s390x

```console
$ docker pull perl@sha256:a8a99662f236d8d8c322746ca07631f0249af359bcd745314f65216d529cae1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.9 MB (55856608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc230e17d0b6c64d7a64bb5ccc7ef59cc97e0ab380cfa98e9a7795be05e4ff22`
-	Default Command: `["perl5.43.7","-de0"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 03:52:45 GMT
WORKDIR /usr/src/perl
# Tue, 03 Feb 2026 04:18:13 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        zlib1g-dev        xz-utils        libssl-dev     && curl -fL https://cpan.metacpan.org/authors/id/C/CO/CORION/perl-5.43.7.tar.gz -o perl-5.43.7.tar.gz     && echo 'd8aa3057fab477b779f6658e42471836cc05f6bcbfd8416959e2f8d177a47d0b *perl-5.43.7.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.43.7.tar.gz -C /usr/src/perl     && rm perl-5.43.7.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.091.tar.gz'     && echo 'c5996e7335912a5c99e06bdb47ff39df309a857cbd8fd2627a021cefdb53cf54 *IO-Socket-SSL-2.091.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.091.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && savedPackages="ca-certificates curl make netbase zlib1g-dev libssl-dev"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.091* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Tue, 03 Feb 2026 04:18:13 GMT
WORKDIR /usr/src/app
# Tue, 03 Feb 2026 04:18:13 GMT
CMD ["perl5.43.7" "-de0"]
```

-	Layers:
	-	`sha256:ecc55ea5c88be14e2088142b1ea9ace24ffd6e3f4d54fd2ead5df425a13dd658`  
		Last Modified: Tue, 03 Feb 2026 01:12:48 GMT  
		Size: 26.9 MB (26884382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:171de2d1e78adca4746e26fff7c46d6469b06be791fd5484760b02b26a3e6854`  
		Last Modified: Tue, 03 Feb 2026 03:59:26 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:541f914d510b47b2cc5a50bb04d78709cc76411acbf310b85588ba71ba16c9fa`  
		Last Modified: Tue, 03 Feb 2026 04:18:29 GMT  
		Size: 29.0 MB (28971958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9f99ff9d334b73d5693f8bd2fc1e99edeeee16f3f06e91ded6134aa53110e3e`  
		Last Modified: Tue, 03 Feb 2026 04:18:28 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-slim-bookworm` - unknown; unknown

```console
$ docker pull perl@sha256:676f9278db3387dbf4fedf71e1e964754fbcfc645cb11c19aff856d2a695dee1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3942857 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2643671cc55b478f574b33952d37f71ebd3fdb3969a53c86a766381e820d64b7`

```dockerfile
```

-	Layers:
	-	`sha256:14423beb8d9cac61b4c74d13acffffd898c364af2623265a40c1534cf8bdabf2`  
		Last Modified: Tue, 03 Feb 2026 04:18:28 GMT  
		Size: 3.9 MB (3924613 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7e1a5a3893f253ed5af0efe044a80d3e56b269544432d9a1754c69b3e39d563b`  
		Last Modified: Tue, 03 Feb 2026 04:18:28 GMT  
		Size: 18.2 KB (18244 bytes)  
		MIME: application/vnd.in-toto+json
