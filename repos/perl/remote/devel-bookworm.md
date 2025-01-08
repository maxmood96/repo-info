## `perl:devel-bookworm`

```console
$ docker pull perl@sha256:be4b26f0eae525ba403f272a1c13285dce2fbd2193c0a515497a0faad5aa4dda
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

### `perl:devel-bookworm` - linux; amd64

```console
$ docker pull perl@sha256:b00e02eee05daaf90cb7ba2739811fb48017e94f651e7d21a3270c16fd675d4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **363.9 MB (363935143 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da62d839b198b759fe8362854ef7aff7b5c783e40d05d6b6255d4ec2ea1dd252`
-	Default Command: `["perl5.41.6","-de0"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1734912000'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 21 Nov 2024 11:29:59 GMT
WORKDIR /usr/src/perl
# Thu, 21 Nov 2024 11:29:59 GMT
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/C/CO/CONTRA/perl-5.41.6.tar.gz -o perl-5.41.6.tar.gz     && echo 'efe7b25a353e2f370818bf6cf1545807c144acf2d9a48368a990827aa71db21d *perl-5.41.6.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.41.6.tar.gz -C /usr/src/perl     && rm perl-5.41.6.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.085.tar.gz'     && echo '95b2f7c0628a7e246a159665fbf0620d0d7835e3a940f22d3fdd47c3aa799c2e *IO-Socket-SSL-2.085.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.085.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.085* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Thu, 21 Nov 2024 11:29:59 GMT
WORKDIR /usr/src/app
# Thu, 21 Nov 2024 11:29:59 GMT
CMD ["perl5.41.6" "-de0"]
```

-	Layers:
	-	`sha256:0a96bdb8280554b560ffee0f2e5f9843dc7b625f28192021ee103ecbcc2d629b`  
		Last Modified: Tue, 24 Dec 2024 21:32:13 GMT  
		Size: 48.5 MB (48497066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54c7be425079efba0003054ee884bf72f1ffebca733bedd6f077d2809ee9aa6f`  
		Last Modified: Wed, 08 Jan 2025 03:47:00 GMT  
		Size: 23.9 MB (23865817 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7aa8176e6d893aff4b57b2c22574ec2afadff4673b8e0954e275244bfd3d7bc1`  
		Last Modified: Tue, 24 Dec 2024 23:16:06 GMT  
		Size: 64.4 MB (64391074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1523f4b3f5602bf41caf8d8e649536ac0b3e56984c81a9f518fb20c6516ca075`  
		Last Modified: Wed, 08 Jan 2025 03:48:53 GMT  
		Size: 211.3 MB (211306201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72d9ab8a9c359cf8ae7f84f67f1c9b3bd383491eb16cabe94dfba3347ac063bc`  
		Last Modified: Wed, 25 Dec 2024 01:24:25 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fef0480e2a844ec28f660521326bf556caa81b7b4603dbe21944ce1a2e70017f`  
		Last Modified: Wed, 25 Dec 2024 01:24:25 GMT  
		Size: 15.9 MB (15874721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63c78c7edfb3a244b200165c49f979f48ff57b861fa14f4df2fa0707acec404e`  
		Last Modified: Wed, 25 Dec 2024 01:24:24 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-bookworm` - unknown; unknown

```console
$ docker pull perl@sha256:779e1bc85e9e6c61d75ff29474b78686c50c41c0ad98c2b0e9d43da62d5701db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15491984 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d769f3cb1c7ed9980b5802c4a2153b7ad1342872b2d7432c347372a7e3f3b7c7`

```dockerfile
```

-	Layers:
	-	`sha256:55bf38a94fef2958db1d1e7b7aea079db56dd0c106e2374ebf464dd1fa1d6f45`  
		Last Modified: Wed, 08 Jan 2025 03:54:29 GMT  
		Size: 15.5 MB (15473481 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0a4945fbfadbc20cd0f585071c0e2300bccdab387553e462849bb7857397b1cf`  
		Last Modified: Wed, 25 Dec 2024 01:24:24 GMT  
		Size: 18.5 KB (18503 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-bookworm` - linux; arm variant v5

```console
$ docker pull perl@sha256:b037f5fc14a977f6207a88adaac74313fe54b658951a88fe64b9848282647516
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **330.3 MB (330322749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:627fc69eb2c756698e41bfe3d34e139d5530e7bc4c8b04868a0e9ea55e97176f`
-	Default Command: `["perl5.41.6","-de0"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1734912000'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 21 Nov 2024 11:29:59 GMT
WORKDIR /usr/src/perl
# Thu, 21 Nov 2024 11:29:59 GMT
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/C/CO/CONTRA/perl-5.41.6.tar.gz -o perl-5.41.6.tar.gz     && echo 'efe7b25a353e2f370818bf6cf1545807c144acf2d9a48368a990827aa71db21d *perl-5.41.6.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.41.6.tar.gz -C /usr/src/perl     && rm perl-5.41.6.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.085.tar.gz'     && echo '95b2f7c0628a7e246a159665fbf0620d0d7835e3a940f22d3fdd47c3aa799c2e *IO-Socket-SSL-2.085.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.085.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.085* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Thu, 21 Nov 2024 11:29:59 GMT
WORKDIR /usr/src/app
# Thu, 21 Nov 2024 11:29:59 GMT
CMD ["perl5.41.6" "-de0"]
```

-	Layers:
	-	`sha256:9bbb619898c2cd76f2f957a170378432dffd62e9bd50226234d805ff7ac0d544`  
		Last Modified: Tue, 24 Dec 2024 21:33:13 GMT  
		Size: 46.0 MB (46024242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0349a30657cc8a48dadcd47420d47a1614d83b85dca5ce8b1e26ac1c4a5a247`  
		Last Modified: Wed, 25 Dec 2024 01:30:39 GMT  
		Size: 22.5 MB (22540466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57e29fd2ce2ac1a28218c54bef4d2c9d159f2a524d7e4bb45b04701439ef9a71`  
		Last Modified: Wed, 25 Dec 2024 04:48:58 GMT  
		Size: 62.0 MB (61996736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4128ccded1bccf224a135daae0222962c43b3fc2ca161661c2056bcc60cde71`  
		Last Modified: Wed, 25 Dec 2024 06:19:27 GMT  
		Size: 184.6 MB (184601212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a81ace3f18941aa94775b037165ed58a4456b3d449ff091986a4ce2f6d6774d`  
		Last Modified: Wed, 25 Dec 2024 10:30:22 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f5d3f4665ead42b4c990e1dd9a45f2c50c6023e275b4a0dacc19c947197bd2c`  
		Size: 15.2 MB (15159827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d771af8e71c2f71ecf16526a47f0a4a258b37f719faeb2fcd84981840340551`  
		Last Modified: Wed, 25 Dec 2024 11:09:16 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-bookworm` - unknown; unknown

```console
$ docker pull perl@sha256:2385cbc35443ae2f37650b143936f073a2783f5cc0b829289c7c2fa1da139c1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15291018 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2718be8194806ed7702fc821cad3e1c9a22b7e44c5f68c79bc877f0ae6688437`

```dockerfile
```

-	Layers:
	-	`sha256:6458f7da2068ae80af7f73b4c6721b8d44953881bb6b1e4a31e5578d10bcf833`  
		Last Modified: Wed, 25 Dec 2024 11:09:17 GMT  
		Size: 15.3 MB (15272423 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4496e6d80232abb08b02566484f1fdf2927632d46e4046eb933d3aefd87dea37`  
		Last Modified: Wed, 25 Dec 2024 11:09:16 GMT  
		Size: 18.6 KB (18595 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-bookworm` - linux; arm variant v7

```console
$ docker pull perl@sha256:718963b23b28031aab2de1299bd49db140ec86e1e9f2b2450543a4389785928f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **315.8 MB (315805005 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:765436cebc46cc77a5ee0a199bf4c82314c318b76bf328a1c3105cc6d2c7231c`
-	Default Command: `["perl5.41.6","-de0"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1734912000'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 21 Nov 2024 11:29:59 GMT
WORKDIR /usr/src/perl
# Thu, 21 Nov 2024 11:29:59 GMT
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/C/CO/CONTRA/perl-5.41.6.tar.gz -o perl-5.41.6.tar.gz     && echo 'efe7b25a353e2f370818bf6cf1545807c144acf2d9a48368a990827aa71db21d *perl-5.41.6.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.41.6.tar.gz -C /usr/src/perl     && rm perl-5.41.6.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.085.tar.gz'     && echo '95b2f7c0628a7e246a159665fbf0620d0d7835e3a940f22d3fdd47c3aa799c2e *IO-Socket-SSL-2.085.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.085.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.085* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Thu, 21 Nov 2024 11:29:59 GMT
WORKDIR /usr/src/app
# Thu, 21 Nov 2024 11:29:59 GMT
CMD ["perl5.41.6" "-de0"]
```

-	Layers:
	-	`sha256:e5492f1033203c78872d1ddcc5f604ba35c18b30ac50e9f89180b9d7dfa33fb9`  
		Last Modified: Tue, 24 Dec 2024 21:33:33 GMT  
		Size: 44.2 MB (44199967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8edd0b2553b5f713f3599802646253e049500cbf687966d319c07d85faa64679`  
		Last Modified: Wed, 25 Dec 2024 03:43:44 GMT  
		Size: 21.8 MB (21767217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcaf98fafca7f2bb5e42aa0418e5ad79c885f1afd75a0c044855cb3f9f482cb6`  
		Last Modified: Wed, 25 Dec 2024 13:00:56 GMT  
		Size: 59.6 MB (59638987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e83d023041aaecc65d16b7b91769e4928cb4f4f650899a539fa07e3615ad9d8`  
		Last Modified: Wed, 25 Dec 2024 15:45:54 GMT  
		Size: 175.2 MB (175243028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a9f2296542b3ecc5510c45c5a389a1a6debd33325c33801dc2261ebecf2baad`  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42643099cef1c7e2009daef2e1c682cbf323047661d9ad719c9de6cc74fc9925`  
		Size: 15.0 MB (14955539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca8044417866c1308053edeb7fca627548f302b65f507ab8ef7a7bb77fd344ec`  
		Last Modified: Wed, 25 Dec 2024 21:30:43 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-bookworm` - unknown; unknown

```console
$ docker pull perl@sha256:2646514adc4a314297d89d7b45b3d994e90f582ed6c5b0d2d2a29cdaf736bdf3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15296489 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c29d7fb7fc5c630f0ec97c7f9210f4d9582c08e99541c5df01ed2990660605b1`

```dockerfile
```

-	Layers:
	-	`sha256:a178569c10196509b3258407348166e201e6d4bdfc7df2979d3b408383f61798`  
		Last Modified: Wed, 25 Dec 2024 21:30:43 GMT  
		Size: 15.3 MB (15277897 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ac2472b09141e50764d856ae724b076b6fb67a9131e430ba775a2bb0666c6126`  
		Last Modified: Wed, 25 Dec 2024 21:30:43 GMT  
		Size: 18.6 KB (18592 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-bookworm` - linux; arm64 variant v8

```console
$ docker pull perl@sha256:2bdb6a003a88dd2e18699e862f9decc7a2af3b2aac508c0b951519ec8538a499
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **354.6 MB (354597074 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8a251c50adda6ce0bc7c5882d2ec99f1e7646c380351e18112249edff556567`
-	Default Command: `["perl5.41.6","-de0"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1734912000'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 21 Nov 2024 11:29:59 GMT
WORKDIR /usr/src/perl
# Thu, 21 Nov 2024 11:29:59 GMT
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/C/CO/CONTRA/perl-5.41.6.tar.gz -o perl-5.41.6.tar.gz     && echo 'efe7b25a353e2f370818bf6cf1545807c144acf2d9a48368a990827aa71db21d *perl-5.41.6.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.41.6.tar.gz -C /usr/src/perl     && rm perl-5.41.6.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.085.tar.gz'     && echo '95b2f7c0628a7e246a159665fbf0620d0d7835e3a940f22d3fdd47c3aa799c2e *IO-Socket-SSL-2.085.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.085.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.085* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Thu, 21 Nov 2024 11:29:59 GMT
WORKDIR /usr/src/app
# Thu, 21 Nov 2024 11:29:59 GMT
CMD ["perl5.41.6" "-de0"]
```

-	Layers:
	-	`sha256:ba1dd0e85e0bf7e5cb632a24bbc3ec0060700bc5be9273b05d7e059950225037`  
		Last Modified: Tue, 24 Dec 2024 21:34:06 GMT  
		Size: 48.3 MB (48325484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92b12b0dccf212c795e61e16dcc85f0caa01c231281e3287400bd334ffedb5ff`  
		Last Modified: Wed, 25 Dec 2024 01:49:19 GMT  
		Size: 23.4 MB (23405768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd63102cac360c09802a29bab13f15de711e8bd1a730d419c66110513700983c`  
		Last Modified: Wed, 25 Dec 2024 08:11:51 GMT  
		Size: 64.3 MB (64347452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e5e0e9e68b5c9172e85869f2decfc76c39919ba6ae80d8e2b597d25e854f0d3`  
		Last Modified: Wed, 25 Dec 2024 11:19:12 GMT  
		Size: 202.7 MB (202686398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f3ef01457f9732b43a96688539e6b2cd31db73b8b099b90d426c5a2e6e5a394`  
		Last Modified: Wed, 25 Dec 2024 15:21:46 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9519802809fe970180252e4a7fd1c7338bb13e894839ceb24f32fa186d9d3510`  
		Last Modified: Wed, 25 Dec 2024 16:23:55 GMT  
		Size: 15.8 MB (15831706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8efc941fc51d2589c84464dd386c0673769833d18550c5dc397fa6535c850442`  
		Last Modified: Wed, 25 Dec 2024 16:23:54 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-bookworm` - unknown; unknown

```console
$ docker pull perl@sha256:164af91c028ed0f94dcdbfe652d8691f75a4438dd8cdd8de635dec5e1a978c47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15520661 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48a2ca8b9c3e6e2ba90b85a34f131248fcd8d09743b343880b342a77d78571d5`

```dockerfile
```

-	Layers:
	-	`sha256:6803f2fed829c2d0ba97e6a9a83b4dbf766224c7bfdf8a0a699ddf331c565f1d`  
		Last Modified: Wed, 25 Dec 2024 16:23:54 GMT  
		Size: 15.5 MB (15502030 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f3616f61884fb80e168693cc31debcdfb0cb26d2199b63b5b2bca16130531b6a`  
		Last Modified: Wed, 25 Dec 2024 16:23:54 GMT  
		Size: 18.6 KB (18631 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-bookworm` - linux; 386

```console
$ docker pull perl@sha256:f1ba01f1b54bc9e78991f2556a28f7a63dd065a55da288e79b17ea3a0a0a632e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **366.0 MB (365983843 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6827b07edc27245f1f918609b7d3c798e9f8743c0edc32378838d4037149b647`
-	Default Command: `["perl5.41.6","-de0"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1734912000'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 21 Nov 2024 11:29:59 GMT
WORKDIR /usr/src/perl
# Thu, 21 Nov 2024 11:29:59 GMT
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/C/CO/CONTRA/perl-5.41.6.tar.gz -o perl-5.41.6.tar.gz     && echo 'efe7b25a353e2f370818bf6cf1545807c144acf2d9a48368a990827aa71db21d *perl-5.41.6.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.41.6.tar.gz -C /usr/src/perl     && rm perl-5.41.6.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.085.tar.gz'     && echo '95b2f7c0628a7e246a159665fbf0620d0d7835e3a940f22d3fdd47c3aa799c2e *IO-Socket-SSL-2.085.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.085.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.085* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Thu, 21 Nov 2024 11:29:59 GMT
WORKDIR /usr/src/app
# Thu, 21 Nov 2024 11:29:59 GMT
CMD ["perl5.41.6" "-de0"]
```

-	Layers:
	-	`sha256:dd322311a74f01b8b9ba5bb8502c37125af9fcf12a3c2deee1502f4932057adb`  
		Size: 49.5 MB (49475925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3b9279710e4c4095d352a56880e4113f2fb4d9d31a4afa310d05a0399ef8f46`  
		Last Modified: Tue, 24 Dec 2024 22:14:43 GMT  
		Size: 24.7 MB (24706895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a30bb48ca6a662c9684d6f7de3d6b9c6909f6205b690c91406e06e0872d69aaa`  
		Last Modified: Tue, 24 Dec 2024 23:16:09 GMT  
		Size: 66.2 MB (66211662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e9f260c3ceedc14c6d40a97e604c5fafe4ae04fc97161d786230fedbc3a4488`  
		Size: 210.2 MB (210222920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21aa4186c07e0bb4132731e95f2c4305422836de8c32c770942ad7de2b48f75a`  
		Last Modified: Wed, 25 Dec 2024 01:24:18 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a22de7b6cb6f3079943ed05960205a39daf13c89290e9d93946c5d9b640e85ee`  
		Last Modified: Wed, 25 Dec 2024 01:24:18 GMT  
		Size: 15.4 MB (15366176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:710c4d3cba795caf2d67ac06d984cd8668bb22e68480e27ba1b08a1df255c326`  
		Last Modified: Wed, 25 Dec 2024 01:24:18 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-bookworm` - unknown; unknown

```console
$ docker pull perl@sha256:ab31be836755afffeaa50569d422fea40f8c3007403cccd7e11ead583ff6ae4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15470517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5448566afde81c4de0541616bb3508440645b61652d637bf8ec9bd3dec2a8386`

```dockerfile
```

-	Layers:
	-	`sha256:0d8a23201577d14aba421a916abdb123d7af256d259280852ae54ca7fa565ecb`  
		Last Modified: Wed, 25 Dec 2024 01:24:18 GMT  
		Size: 15.5 MB (15452056 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:311d50084be8ac8fa1cc0f098e8b897d066b7dcde61fa800e3edbeb068601658`  
		Last Modified: Wed, 25 Dec 2024 01:24:17 GMT  
		Size: 18.5 KB (18461 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-bookworm` - linux; mips64le

```console
$ docker pull perl@sha256:af98fbced867a1254795efce53d4a99c6c13d43bee70624b81825dc67f8c8957
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **340.5 MB (340472625 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6abea1cb002311f2b456fe20f7d39386a69969fe657a26e3ff3aad43022aa53b`
-	Default Command: `["perl5.41.6","-de0"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1734912000'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 21 Nov 2024 11:29:59 GMT
WORKDIR /usr/src/perl
# Thu, 21 Nov 2024 11:29:59 GMT
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/C/CO/CONTRA/perl-5.41.6.tar.gz -o perl-5.41.6.tar.gz     && echo 'efe7b25a353e2f370818bf6cf1545807c144acf2d9a48368a990827aa71db21d *perl-5.41.6.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.41.6.tar.gz -C /usr/src/perl     && rm perl-5.41.6.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.085.tar.gz'     && echo '95b2f7c0628a7e246a159665fbf0620d0d7835e3a940f22d3fdd47c3aa799c2e *IO-Socket-SSL-2.085.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.085.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.085* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Thu, 21 Nov 2024 11:29:59 GMT
WORKDIR /usr/src/app
# Thu, 21 Nov 2024 11:29:59 GMT
CMD ["perl5.41.6" "-de0"]
```

-	Layers:
	-	`sha256:fa42b2983a081afbe5b1653f1c107472f7b73564ae2a3f6a75d6b4702023cc0c`  
		Last Modified: Tue, 24 Dec 2024 21:33:19 GMT  
		Size: 48.8 MB (48771644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cb6e11ed066e836dca02164f5f47ac1b39b5177eecb98796a4c515c972272aa`  
		Last Modified: Wed, 25 Dec 2024 11:45:56 GMT  
		Size: 23.5 MB (23458082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:988cb190aa8a2556e06728d7eacbb8faf4d6ab4515c38db72b67645a5fa04f41`  
		Last Modified: Wed, 25 Dec 2024 19:15:14 GMT  
		Size: 63.3 MB (63283024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:995166b4afe0ef9d7f14aef9b7b6059c2b9e68f1f5510604c837908aff37c066`  
		Last Modified: Thu, 26 Dec 2024 00:44:50 GMT  
		Size: 189.9 MB (189876548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2dbd4f5d7e579913a21cffeffd492283fcf1e9e02077c9dbe881ccf18f1d0b5`  
		Last Modified: Thu, 26 Dec 2024 03:39:23 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:146b828192f2511a71bbcbaeafb60c465c3e779331fba10c58d70a932edc3cad`  
		Last Modified: Thu, 26 Dec 2024 06:14:13 GMT  
		Size: 15.1 MB (15083060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a5ad065df24263e35d7a88d14c67103faaf91246a44d6f9e9372b70b4c1f5a0`  
		Last Modified: Thu, 26 Dec 2024 06:14:11 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-bookworm` - unknown; unknown

```console
$ docker pull perl@sha256:fd0b0a43b22b779dc73bbbccd2bc0745b9bc93f63b2820482ce0daeb0dacdc6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.4 KB (18371 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40db2a56a0c51861ec3f4a7129a30766c7c1907044927968d73b8d1b718e8e43`

```dockerfile
```

-	Layers:
	-	`sha256:0d607e4dea2db5fea31e3d2964f0840c64105b112b7236c004ccf5b13762b350`  
		Last Modified: Thu, 26 Dec 2024 06:14:11 GMT  
		Size: 18.4 KB (18371 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-bookworm` - linux; ppc64le

```console
$ docker pull perl@sha256:4faf11ebe2660f36827fd935d405cf157ff10af3f7cc714d002a822855437caf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **377.9 MB (377872543 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a23d53563c57bdb75448426d3c46ace70b60c3ee679900369043558db94e6bf`
-	Default Command: `["perl5.41.6","-de0"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1734912000'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 21 Nov 2024 11:29:59 GMT
WORKDIR /usr/src/perl
# Thu, 21 Nov 2024 11:29:59 GMT
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/C/CO/CONTRA/perl-5.41.6.tar.gz -o perl-5.41.6.tar.gz     && echo 'efe7b25a353e2f370818bf6cf1545807c144acf2d9a48368a990827aa71db21d *perl-5.41.6.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.41.6.tar.gz -C /usr/src/perl     && rm perl-5.41.6.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.085.tar.gz'     && echo '95b2f7c0628a7e246a159665fbf0620d0d7835e3a940f22d3fdd47c3aa799c2e *IO-Socket-SSL-2.085.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.085.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.085* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Thu, 21 Nov 2024 11:29:59 GMT
WORKDIR /usr/src/app
# Thu, 21 Nov 2024 11:29:59 GMT
CMD ["perl5.41.6" "-de0"]
```

-	Layers:
	-	`sha256:308f39459045dc7bdf1e0f0796ba6cc67e14899ab5c36afc6c0692da37a1f331`  
		Last Modified: Wed, 25 Dec 2024 09:07:26 GMT  
		Size: 52.3 MB (52328075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5a609591090f1b2fe90289666414a8be62bd40b89ccbd53d2567ba14f37f52a`  
		Last Modified: Wed, 25 Dec 2024 12:51:22 GMT  
		Size: 25.5 MB (25523681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b44eb81eb15a16dd3be1309db287e3a3b8589c16f49f4938705cd78c20f9035c`  
		Last Modified: Wed, 25 Dec 2024 13:15:17 GMT  
		Size: 69.8 MB (69812237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc88116b337337204514f1443b661b30d7821092e93cc32e73d38803d573dc8e`  
		Last Modified: Wed, 25 Dec 2024 14:10:42 GMT  
		Size: 214.3 MB (214339172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e1dd5841c636113d18ae7c5f708dd630ef4b0d5e4d59bb988d56f61747f030e`  
		Last Modified: Wed, 25 Dec 2024 18:06:43 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfe344dac9f792ed85374d7d2708a47322f97685c608527306a49840a8852dec`  
		Last Modified: Wed, 25 Dec 2024 18:46:59 GMT  
		Size: 15.9 MB (15869111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7f292088d371757f4a1b4dfc06ffc68e85c014a1610ed5a20b39acc51416e2e`  
		Last Modified: Wed, 25 Dec 2024 18:46:58 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-bookworm` - unknown; unknown

```console
$ docker pull perl@sha256:1741cbb35919a3a6c2955bd740a6f2ba1f5132cccbe61b482a3f694341b38176
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15468437 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5994f1357fcba5b4d1da35f7a9ae949e651ec995dc14cb9afbf130bf4cc8997`

```dockerfile
```

-	Layers:
	-	`sha256:ff86d530080df70cd7efea8969781b9893f235365fd53dfcca1714d3c848d9dc`  
		Last Modified: Wed, 25 Dec 2024 18:46:58 GMT  
		Size: 15.4 MB (15449878 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7cae03647af126b36d704c21de8bb693b78b7bd507ca8799c476019b0faf7f26`  
		Last Modified: Wed, 25 Dec 2024 18:46:58 GMT  
		Size: 18.6 KB (18559 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-bookworm` - linux; s390x

```console
$ docker pull perl@sha256:91dc4b456ac46d8617f76053f8a7f4b57f215296e613aeab1f127c8c9d35f0d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **334.0 MB (334021316 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:107a84600751737419c336bbe9ef0ed33baf907c94314e27e12ec513f988d7fc`
-	Default Command: `["perl5.41.6","-de0"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1734912000'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 21 Nov 2024 11:29:59 GMT
WORKDIR /usr/src/perl
# Thu, 21 Nov 2024 11:29:59 GMT
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/C/CO/CONTRA/perl-5.41.6.tar.gz -o perl-5.41.6.tar.gz     && echo 'efe7b25a353e2f370818bf6cf1545807c144acf2d9a48368a990827aa71db21d *perl-5.41.6.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.41.6.tar.gz -C /usr/src/perl     && rm perl-5.41.6.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.085.tar.gz'     && echo '95b2f7c0628a7e246a159665fbf0620d0d7835e3a940f22d3fdd47c3aa799c2e *IO-Socket-SSL-2.085.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.085.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.085* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Thu, 21 Nov 2024 11:29:59 GMT
WORKDIR /usr/src/app
# Thu, 21 Nov 2024 11:29:59 GMT
CMD ["perl5.41.6" "-de0"]
```

-	Layers:
	-	`sha256:29bd91c5aff546f191fe0c6a3ff3058c52bb3850131ee98a2d3fe9b96198878c`  
		Last Modified: Tue, 24 Dec 2024 21:33:12 GMT  
		Size: 47.1 MB (47149625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65c625039a5998156fd2a92e83b33c35e10b4f91017063d54d2a949d78884a65`  
		Last Modified: Wed, 25 Dec 2024 00:16:25 GMT  
		Size: 23.9 MB (23864731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba2c4d6ca294087595fc1adf8f3d033945c38a166a01db670c00b336716a18a6`  
		Last Modified: Wed, 25 Dec 2024 03:29:07 GMT  
		Size: 63.5 MB (63473996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e88c95c11e135edcc3e50ddc764dd43154a7deb840aeab95b0811be73511f52`  
		Last Modified: Wed, 25 Dec 2024 05:10:29 GMT  
		Size: 183.3 MB (183324742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23d6dbb9224cb5e9b714541e04abe3d522ad9281cb2371f6a168a89f64e62e22`  
		Last Modified: Wed, 25 Dec 2024 08:54:12 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82e63cc523997ec99f307cb7f8c0ebfdbc1e8b2a46cd07678002ee646406bb99`  
		Last Modified: Wed, 25 Dec 2024 09:38:13 GMT  
		Size: 16.2 MB (16207956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb0e2d97da339338753e3bb84f6e44cfb6526305d1761e3169662105bf9d2016`  
		Last Modified: Wed, 25 Dec 2024 09:38:13 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-bookworm` - unknown; unknown

```console
$ docker pull perl@sha256:dca39ee5a8d26c3641bda4a0782c86639016f7fe47c84db4d7ad0c45cb92e4ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15304674 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf420f25bc5ebedb14b23fc953c3dc54218676273ca289e8de03c9348f0d2b79`

```dockerfile
```

-	Layers:
	-	`sha256:f3a5ff7adb3a9ca454a2fa1f3334744710eca61b711220f96c0db5c476e24154`  
		Last Modified: Wed, 25 Dec 2024 09:38:13 GMT  
		Size: 15.3 MB (15286171 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0ff1b292b9aa94578cec826d0fe54fd3ead052879aee807c679b0b2a9cf15812`  
		Size: 18.5 KB (18503 bytes)  
		MIME: application/vnd.in-toto+json
