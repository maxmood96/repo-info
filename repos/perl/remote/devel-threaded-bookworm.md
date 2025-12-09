## `perl:devel-threaded-bookworm`

```console
$ docker pull perl@sha256:9c252187abd1a57939d8fab2d3d6e62fa76144dfebc042834111214f5351034c
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

### `perl:devel-threaded-bookworm` - linux; amd64

```console
$ docker pull perl@sha256:b6ed0def12c1e50ec574712adc114e47c73676e2d420cae27780b8614dd3ca09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **364.5 MB (364461289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b56495ca2d270ec24dbe9619e75abb2fb6d4f0fac88e740e787b7f9aa01af822`
-	Default Command: `["perl5.43.5","-de0"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1765152000'
# Mon, 08 Dec 2025 23:06:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 00:05:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 00:43:10 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 01:34:42 GMT
WORKDIR /usr/src/perl
# Tue, 09 Dec 2025 01:54:43 GMT
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/C/CO/CONTRA/perl-5.43.5.tar.gz -o perl-5.43.5.tar.gz     && echo '4232e7a164873e687df929152ee7bbbf075c1d547bccba3d50353f81a897c259 *perl-5.43.5.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.43.5.tar.gz -C /usr/src/perl     && rm perl-5.43.5.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.091.tar.gz'     && echo 'c5996e7335912a5c99e06bdb47ff39df309a857cbd8fd2627a021cefdb53cf54 *IO-Socket-SSL-2.091.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.091.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.091* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Tue, 09 Dec 2025 01:54:43 GMT
WORKDIR /usr/src/app
# Tue, 09 Dec 2025 01:54:43 GMT
CMD ["perl5.43.5" "-de0"]
```

-	Layers:
	-	`sha256:c8443a297fa42e27cb10653777dd5a53f82a65fbc8b2d33f82b8722199f941d3`  
		Last Modified: Mon, 08 Dec 2025 22:16:25 GMT  
		Size: 48.5 MB (48480736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ae8659f7a8d357662281a0f87eb293725bb75ffa6c7356c38567f557d8a1f11`  
		Last Modified: Mon, 08 Dec 2025 23:07:04 GMT  
		Size: 24.0 MB (24029335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c237534654fe7a5c118fcee78652af952e57a4a07cc322c0ae3c367839bb0ccc`  
		Last Modified: Tue, 09 Dec 2025 00:06:16 GMT  
		Size: 64.4 MB (64396522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8d2a98f6bdfdbb1ba3c937c5e47cfa2cd11e74487543d277ca84f21f12ba393`  
		Last Modified: Tue, 09 Dec 2025 00:44:16 GMT  
		Size: 211.5 MB (211460710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab4d3c1b4553577f1021975fbc4ae894b579936ccb7604377280df5913649447`  
		Last Modified: Tue, 09 Dec 2025 01:39:43 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd3f7c231043ab35de03e5c301edeb4c1dab2185c43eeeb7fea7682d8267fbdb`  
		Last Modified: Tue, 09 Dec 2025 01:55:09 GMT  
		Size: 16.1 MB (16093720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab766151f02657e68576bf986c7aa8a29a91845b8c5516f41fec5a5a5bc6f3ab`  
		Last Modified: Tue, 09 Dec 2025 01:55:07 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-threaded-bookworm` - unknown; unknown

```console
$ docker pull perl@sha256:a59b49250dfde7ecf3061a1597043cb3ce59f602820597aa5f87aca283ddcdfc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.9 MB (15886311 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81e18986ba892b125de9b2b5b8ed07fdde509d7a2623085085b99c895878ce19`

```dockerfile
```

-	Layers:
	-	`sha256:c7c9d0ecd690bc3a1b679942894882d79ef4d5459af944b5dea03c58f2896cf7`  
		Last Modified: Tue, 09 Dec 2025 02:50:00 GMT  
		Size: 15.9 MB (15868605 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f1319433109affbde43cf47fc4bc27ae7af6a79e2a8d53b078643cac97ba30cb`  
		Last Modified: Tue, 09 Dec 2025 02:50:01 GMT  
		Size: 17.7 KB (17706 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-threaded-bookworm` - linux; arm variant v5

```console
$ docker pull perl@sha256:4b247342f3d688fb66b821480b5fe24dc5ee78f803056e4d4c94ec9036faae7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **330.8 MB (330817155 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75dd57ed3f7acb1ad07a0f336ea3af828f5fa41a6b143773fbd6c82a0c7998d4`
-	Default Command: `["perl5.43.5","-de0"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1765152000'
# Mon, 08 Dec 2025 23:53:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 01:18:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 02:13:30 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 03:50:15 GMT
WORKDIR /usr/src/perl
# Tue, 09 Dec 2025 04:01:56 GMT
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/C/CO/CONTRA/perl-5.43.5.tar.gz -o perl-5.43.5.tar.gz     && echo '4232e7a164873e687df929152ee7bbbf075c1d547bccba3d50353f81a897c259 *perl-5.43.5.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.43.5.tar.gz -C /usr/src/perl     && rm perl-5.43.5.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.091.tar.gz'     && echo 'c5996e7335912a5c99e06bdb47ff39df309a857cbd8fd2627a021cefdb53cf54 *IO-Socket-SSL-2.091.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.091.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.091* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Tue, 09 Dec 2025 04:01:56 GMT
WORKDIR /usr/src/app
# Tue, 09 Dec 2025 04:01:56 GMT
CMD ["perl5.43.5" "-de0"]
```

-	Layers:
	-	`sha256:a635f54eaf3a9fce0549b1b49b875e73326ccbc501c3133d86c2ac8fd7828fb8`  
		Last Modified: Mon, 08 Dec 2025 22:16:16 GMT  
		Size: 46.0 MB (46015801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f70892cf40cf00afad948163124cb46c26422ae7a58c48384378f9afd91c3e5`  
		Last Modified: Mon, 08 Dec 2025 23:53:57 GMT  
		Size: 22.7 MB (22705745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8089c2b20fedea36afc932499843f6245377677804c10ff2c0e867c4b27513c`  
		Last Modified: Tue, 09 Dec 2025 01:18:41 GMT  
		Size: 62.0 MB (62010644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bf65146386f6d1636f8e6d20118575504aa19edbffdf36f5cafe418ddd2909b`  
		Last Modified: Tue, 09 Dec 2025 02:14:32 GMT  
		Size: 184.7 MB (184720504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e93689d5eafc32c7476955bd38ec773d4682614c9bddb3c35bf63ad60e567073`  
		Last Modified: Tue, 09 Dec 2025 03:56:05 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5c7a9261cb7c152a55ab6a06c7592f005fdbdc0c13a1a3dc5568e1b02e4e620`  
		Last Modified: Tue, 09 Dec 2025 04:02:20 GMT  
		Size: 15.4 MB (15364195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25f7f37d25dce3a090f81555549365f39896053d453be1f000881c0e9513d505`  
		Last Modified: Tue, 09 Dec 2025 04:02:19 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-threaded-bookworm` - unknown; unknown

```console
$ docker pull perl@sha256:d5ab4fe0bc812f01bcc4e54cf95e798a357904f8b726e8e2e7c18f4dda114ea3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.7 MB (15683375 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6583bfc7ab1adcd57df7efe03d0c56f91e110ea387f5b455a751b4d4913a86e3`

```dockerfile
```

-	Layers:
	-	`sha256:2bde7fdd866aea72eb7885dad4adb3b2af8e4ac6cb12e63e81917b1479f36d9f`  
		Last Modified: Tue, 09 Dec 2025 05:48:13 GMT  
		Size: 15.7 MB (15665597 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:854b59c8877a2592df2728eee9b592f27814151540e0994e04ee3260f05e978e`  
		Last Modified: Tue, 09 Dec 2025 05:48:14 GMT  
		Size: 17.8 KB (17778 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-threaded-bookworm` - linux; arm variant v7

```console
$ docker pull perl@sha256:661f257d8edfe512f90818edb338b40f5388d54fdc1966772d8244e9adec9e6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **316.3 MB (316297960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8475757a256acdd845ea42583ab68139c8ef6d96890873d4ed9e66baeb1938d0`
-	Default Command: `["perl5.43.5","-de0"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1765152000'
# Tue, 09 Dec 2025 00:04:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 01:32:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 02:13:22 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 04:38:41 GMT
WORKDIR /usr/src/perl
# Tue, 09 Dec 2025 04:44:24 GMT
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/C/CO/CONTRA/perl-5.43.5.tar.gz -o perl-5.43.5.tar.gz     && echo '4232e7a164873e687df929152ee7bbbf075c1d547bccba3d50353f81a897c259 *perl-5.43.5.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.43.5.tar.gz -C /usr/src/perl     && rm perl-5.43.5.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.091.tar.gz'     && echo 'c5996e7335912a5c99e06bdb47ff39df309a857cbd8fd2627a021cefdb53cf54 *IO-Socket-SSL-2.091.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.091.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.091* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Tue, 09 Dec 2025 04:44:24 GMT
WORKDIR /usr/src/app
# Tue, 09 Dec 2025 04:44:24 GMT
CMD ["perl5.43.5" "-de0"]
```

-	Layers:
	-	`sha256:c3d6a83e736aa77820543663b2d6579ddd98b0f465c0fcad8aa9bd98a5b72a9c`  
		Last Modified: Mon, 08 Dec 2025 22:16:46 GMT  
		Size: 44.2 MB (44196066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af0a258ea9a718fb1bf2331996816ba335715a3c786bd79934d265fd78fb7f5a`  
		Last Modified: Tue, 09 Dec 2025 00:05:11 GMT  
		Size: 21.9 MB (21934635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a66aa6761aa99c557c882b6cb71cf839a06b4634c5e4d98e4a93d946b4554c6f`  
		Last Modified: Tue, 09 Dec 2025 01:33:23 GMT  
		Size: 59.7 MB (59652900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a62e3be8a0aae51e2187a228a8a625ff3ecff288e28ff8b1628284f0a4494705`  
		Last Modified: Tue, 09 Dec 2025 02:14:25 GMT  
		Size: 175.4 MB (175369883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d5ef77f66bb7b28e43226f2043249dc87b0a5f3fb6929bf8ba9ada6d1359807`  
		Last Modified: Tue, 09 Dec 2025 04:44:50 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:403f256bc46ce45cf051f84a165ce3e7cf608a0dbd63fa882cf65921fdf0db0b`  
		Last Modified: Tue, 09 Dec 2025 04:44:50 GMT  
		Size: 15.1 MB (15144212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88a87081643e7b36508d10de57035858e92a78b06322a6cece935dc8e0494ac3`  
		Last Modified: Tue, 09 Dec 2025 04:44:49 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-threaded-bookworm` - unknown; unknown

```console
$ docker pull perl@sha256:2c26c53cf29d138f45203eb1a65b5f2b818a9b1be82e2a16f275cfaf81400329
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.7 MB (15688851 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d595de46aa6b49c71686021d67908e5f11bd0b7212d04cf8d4f2939c9877eeab`

```dockerfile
```

-	Layers:
	-	`sha256:61c1a9840e3510d8200250e90285a694aabc792f3e4d9bee048b1304d6c065c1`  
		Last Modified: Tue, 09 Dec 2025 05:48:26 GMT  
		Size: 15.7 MB (15671073 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:941bcbf132737bf857b9f9fa04ceefd1c433ff561dde4db70a175d6c3f3a1733`  
		Last Modified: Tue, 09 Dec 2025 05:48:27 GMT  
		Size: 17.8 KB (17778 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-threaded-bookworm` - linux; arm64 variant v8

```console
$ docker pull perl@sha256:e59ae5a0ea2bc24d1e3b69b195009254470edc930cbed8d9114f810123e3718e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **355.4 MB (355359006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5781db75e96b9faea3a90c60571e9e396ad9697e9e706a776e74465ee26266a1`
-	Default Command: `["perl5.43.5","-de0"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1765152000'
# Mon, 08 Dec 2025 23:10:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 00:10:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 01:14:19 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 02:39:48 GMT
WORKDIR /usr/src/perl
# Tue, 09 Dec 2025 02:44:36 GMT
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/C/CO/CONTRA/perl-5.43.5.tar.gz -o perl-5.43.5.tar.gz     && echo '4232e7a164873e687df929152ee7bbbf075c1d547bccba3d50353f81a897c259 *perl-5.43.5.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.43.5.tar.gz -C /usr/src/perl     && rm perl-5.43.5.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.091.tar.gz'     && echo 'c5996e7335912a5c99e06bdb47ff39df309a857cbd8fd2627a021cefdb53cf54 *IO-Socket-SSL-2.091.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.091.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.091* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Tue, 09 Dec 2025 02:44:36 GMT
WORKDIR /usr/src/app
# Tue, 09 Dec 2025 02:44:36 GMT
CMD ["perl5.43.5" "-de0"]
```

-	Layers:
	-	`sha256:7f2b9668af76f73927725e2d1fb5d7224604d8c4c42cb8cdecb502257d9101c4`  
		Last Modified: Mon, 08 Dec 2025 22:16:59 GMT  
		Size: 48.4 MB (48359071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0da1fc24a51c3ab23b5143a2c67b43348114c11a8029b3483be57ab9fe54eb6`  
		Last Modified: Mon, 08 Dec 2025 23:10:26 GMT  
		Size: 23.6 MB (23598247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62a266a3916e0f2e8ff6996b219222479419b3dca87b3e3dfc3bd0108f509071`  
		Last Modified: Tue, 09 Dec 2025 00:11:40 GMT  
		Size: 64.4 MB (64371489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79bcc4522f03676e0bd8955225a4929c2246c10b35dabf07c8ea7a4aaea3efaf`  
		Last Modified: Tue, 09 Dec 2025 01:15:40 GMT  
		Size: 203.0 MB (202980996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:947f43b50997f2be858988b2820e9bfba97e8a28d07e0099cd2b3d3f904a7aa1`  
		Last Modified: Tue, 09 Dec 2025 02:45:05 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d584cf1b79baac653d12f08eebc2ea30ebfa941ae33328ac5b2967d4c3194026`  
		Last Modified: Tue, 09 Dec 2025 02:45:08 GMT  
		Size: 16.0 MB (16048938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90393226c851757df3e07d41e570e07ebe72351d847e50d049b6f6ab043225e5`  
		Last Modified: Tue, 09 Dec 2025 02:45:05 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-threaded-bookworm` - unknown; unknown

```console
$ docker pull perl@sha256:fb10c2f906f2e689b359102ce4da5746908be9928bd3d976733deb840d2efac8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.9 MB (15914917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41c9d38d5b25ebfb0261e25e9417422f05ac63f4146e2d6c3db595c2548659af`

```dockerfile
```

-	Layers:
	-	`sha256:e2fafd329635fa61df404ae147cea3f5ac9c9cc77826eb05d2c8c88cd0216be0`  
		Last Modified: Tue, 09 Dec 2025 05:48:39 GMT  
		Size: 15.9 MB (15897119 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:373be73ae2b3055c05f7776bf5cdfb23da2ef3f7ff63e867539fe613a67b56eb`  
		Last Modified: Tue, 09 Dec 2025 05:48:40 GMT  
		Size: 17.8 KB (17798 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-threaded-bookworm` - linux; 386

```console
$ docker pull perl@sha256:d0232c4d64dab5953c8d71a84c40fda3a8bd20431b645fd58843836c08e298a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **366.6 MB (366603260 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e81d954e7d9e71756eb6d45c59ed9742893e8c3aa663c423a15b643c0afd10a`
-	Default Command: `["perl5.43.5","-de0"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1765152000'
# Mon, 08 Dec 2025 23:14:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 00:23:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 01:15:45 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 02:24:32 GMT
WORKDIR /usr/src/perl
# Tue, 09 Dec 2025 02:29:57 GMT
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/C/CO/CONTRA/perl-5.43.5.tar.gz -o perl-5.43.5.tar.gz     && echo '4232e7a164873e687df929152ee7bbbf075c1d547bccba3d50353f81a897c259 *perl-5.43.5.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.43.5.tar.gz -C /usr/src/perl     && rm perl-5.43.5.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.091.tar.gz'     && echo 'c5996e7335912a5c99e06bdb47ff39df309a857cbd8fd2627a021cefdb53cf54 *IO-Socket-SSL-2.091.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.091.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.091* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Tue, 09 Dec 2025 02:29:57 GMT
WORKDIR /usr/src/app
# Tue, 09 Dec 2025 02:29:57 GMT
CMD ["perl5.43.5" "-de0"]
```

-	Layers:
	-	`sha256:5a0767b6533dfa923197197a2adf3860bde889326cc3199fec46ced873deb7e1`  
		Last Modified: Mon, 08 Dec 2025 22:16:44 GMT  
		Size: 49.5 MB (49466819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e8c9cca3d9f455dde3fab1917d275b029f5f2978fcd1f8f1b757098b58abc9d`  
		Last Modified: Mon, 08 Dec 2025 23:14:28 GMT  
		Size: 24.9 MB (24864339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd442778352104a3bf918f8351b8ac2573f9aa7b0d9136092884f7f79017f9a2`  
		Last Modified: Tue, 09 Dec 2025 00:24:01 GMT  
		Size: 66.2 MB (66233858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c11f912d8d8b79ebf66ce409372e2a04912e563acde172414a5a004db00cf18`  
		Last Modified: Tue, 09 Dec 2025 01:16:49 GMT  
		Size: 210.4 MB (210390369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98a1152bc52b7a3b71f46ee24a68cada28bffe3f96ae2d818b03ce4f46c6d464`  
		Last Modified: Tue, 09 Dec 2025 02:30:22 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f1b74625ae77a3590be15aba518cfd4968844b4adfaa947d032d4e9a01b02b6`  
		Last Modified: Tue, 09 Dec 2025 02:30:24 GMT  
		Size: 15.6 MB (15647611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:791a83bafbc0923acbf7795aa96ef4762e80a1fde2caa96847eb64bee2af05a8`  
		Last Modified: Tue, 09 Dec 2025 02:30:22 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-threaded-bookworm` - unknown; unknown

```console
$ docker pull perl@sha256:cd236b85321e20cd3ce934f3827fd634e41f2339f97e237a336a03c5e95d15b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.9 MB (15864506 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7148c965da29262e3538c4d68b411e096f98c8258f5332bc520478b309d02e5b`

```dockerfile
```

-	Layers:
	-	`sha256:5435ec5e74e5aebebb2abda924cf5a7c0249586a45533e1d99e1d430b619f52e`  
		Last Modified: Tue, 09 Dec 2025 05:48:52 GMT  
		Size: 15.8 MB (15846827 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:de84ae50bc6bc3aa82c72224d59e0715620c21136e09eb1d316136cb1a1861ad`  
		Last Modified: Tue, 09 Dec 2025 05:48:53 GMT  
		Size: 17.7 KB (17679 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-threaded-bookworm` - linux; mips64le

```console
$ docker pull perl@sha256:b83e69cc7603159acc094624605ea5453e4add15153e986e4eb6bfaa6b4f9e59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **341.2 MB (341233406 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9847bca2949d5565c84e6569a754ddf79302951613aa9e10d4066090ccd8ba1`
-	Default Command: `["perl5.43.5","-de0"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 19:40:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 22:11:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 23:31:19 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 19 Nov 2025 05:38:09 GMT
WORKDIR /usr/src/perl
# Tue, 25 Nov 2025 17:53:14 GMT
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/C/CO/CONTRA/perl-5.43.5.tar.gz -o perl-5.43.5.tar.gz     && echo '4232e7a164873e687df929152ee7bbbf075c1d547bccba3d50353f81a897c259 *perl-5.43.5.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.43.5.tar.gz -C /usr/src/perl     && rm perl-5.43.5.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.091.tar.gz'     && echo 'c5996e7335912a5c99e06bdb47ff39df309a857cbd8fd2627a021cefdb53cf54 *IO-Socket-SSL-2.091.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.091.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.091* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Tue, 25 Nov 2025 17:53:15 GMT
WORKDIR /usr/src/app
# Tue, 25 Nov 2025 17:53:15 GMT
CMD ["perl5.43.5" "-de0"]
```

-	Layers:
	-	`sha256:6d4a3f53f449c0e9b84d889c71d1f21df5764d821465bd1337060660aa78c65e`  
		Last Modified: Tue, 18 Nov 2025 01:11:17 GMT  
		Size: 48.8 MB (48760956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:754bf41c56cb3beefc6b6211c26bdc048d41c337f12bc0bbfcfa89dfb5de99b7`  
		Last Modified: Tue, 18 Nov 2025 19:40:58 GMT  
		Size: 23.6 MB (23614038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c7a4cb619dbd7fcb3e0be3246f973ccbe692039c1fd01a193751c60045de0d3`  
		Last Modified: Tue, 18 Nov 2025 22:12:34 GMT  
		Size: 63.3 MB (63309296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54792da20c74ed4e30224cf94214dd511807467c2d7da651ead9787b6581a9ef`  
		Last Modified: Wed, 19 Nov 2025 02:24:32 GMT  
		Size: 190.2 MB (190228318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de095f274d3999813c3b4cc696f9a13e9f84c874e8281957b07d5eb152606640`  
		Last Modified: Wed, 19 Nov 2025 06:02:54 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d38115223c4f4807a0328a8bb84acf3b038438b999d1ae9ee702cba502a71ddc`  
		Last Modified: Tue, 25 Nov 2025 17:54:26 GMT  
		Size: 15.3 MB (15320530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:798bc958ccc5ffc25f534c100768b77bceb8a4d34346c673e2f1752d2b98256f`  
		Last Modified: Tue, 25 Nov 2025 17:54:24 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-threaded-bookworm` - unknown; unknown

```console
$ docker pull perl@sha256:3f4555420543c794818672eacea057eafca5ed10ada33cebd6f0e1a330ea2d63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.5 KB (17548 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6d327443d78c4b504b25e7fa04c7f05cc6b0dd0521394a750894931f9b4f618`

```dockerfile
```

-	Layers:
	-	`sha256:1e8502191041b036f1e489fb7605e5e12e95b6df358dad3448b43078207d5649`  
		Last Modified: Tue, 25 Nov 2025 20:40:46 GMT  
		Size: 17.5 KB (17548 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-threaded-bookworm` - linux; ppc64le

```console
$ docker pull perl@sha256:7da0eb4aec03906b16696b835384687449c6c1697d48843cb8b71bb53caabc1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **378.5 MB (378478999 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ccd076881d6931bcb1b781574103af7dad7f31bd65ae2de68de11679e21e878`
-	Default Command: `["perl5.43.5","-de0"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1765152000'
# Mon, 08 Dec 2025 22:28:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 23:21:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 02:09:57 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 07:29:04 GMT
WORKDIR /usr/src/perl
# Tue, 09 Dec 2025 07:59:06 GMT
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/C/CO/CONTRA/perl-5.43.5.tar.gz -o perl-5.43.5.tar.gz     && echo '4232e7a164873e687df929152ee7bbbf075c1d547bccba3d50353f81a897c259 *perl-5.43.5.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.43.5.tar.gz -C /usr/src/perl     && rm perl-5.43.5.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.091.tar.gz'     && echo 'c5996e7335912a5c99e06bdb47ff39df309a857cbd8fd2627a021cefdb53cf54 *IO-Socket-SSL-2.091.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.091.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.091* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Tue, 09 Dec 2025 07:59:07 GMT
WORKDIR /usr/src/app
# Tue, 09 Dec 2025 07:59:07 GMT
CMD ["perl5.43.5" "-de0"]
```

-	Layers:
	-	`sha256:c088128ea77bb5c706bb00930020ea2fba147060275f49c5a7be6b54af5ca7c8`  
		Last Modified: Mon, 08 Dec 2025 22:17:06 GMT  
		Size: 52.3 MB (52326977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4109a037ac4c69c3ce26e6d14e10c867842083c363485abd63db45502611991`  
		Last Modified: Mon, 08 Dec 2025 22:28:59 GMT  
		Size: 25.7 MB (25672209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd2b93c70c0b05a907d16ae217d77a407e9aa88f69499ffbfee4375b49ab6c01`  
		Last Modified: Mon, 08 Dec 2025 23:22:14 GMT  
		Size: 69.8 MB (69846008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cc15b235f2d99c9b8cb7f5511247453daa35498d32335b3432bc90fb1d754bd`  
		Last Modified: Tue, 09 Dec 2025 02:11:48 GMT  
		Size: 214.5 MB (214498018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a610e26b9f8c1494ad48ff536c2c162fc15b6c894363f75236a5d98dc7d2958`  
		Last Modified: Tue, 09 Dec 2025 07:37:06 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d427542d3650cea05602f23aef49aa123326710725b3bd72d877999f8094f04`  
		Last Modified: Tue, 09 Dec 2025 08:00:02 GMT  
		Size: 16.1 MB (16135520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97b3a1be382ecc71385fa2305c2d53efa9687bdb49a189e39d36afaeafced224`  
		Last Modified: Tue, 09 Dec 2025 08:00:01 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-threaded-bookworm` - unknown; unknown

```console
$ docker pull perl@sha256:59148577ec21da49e0f7bed59ed7ba91d770b4602bd581913e030a4b308c3052
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.9 MB (15862860 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a29420174f0bdde8d273ffbc55925a152fcea87fdd3f434135c3dbb0bf271894`

```dockerfile
```

-	Layers:
	-	`sha256:8e85591a33750ae92393be4632726212b5669765336f7a44cf39dd3351b36fc1`  
		Last Modified: Tue, 09 Dec 2025 08:43:08 GMT  
		Size: 15.8 MB (15845116 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e58cc32062bd233e3de79bc6faeef25bd2f851040a3ca8c59febe10950920388`  
		Last Modified: Tue, 09 Dec 2025 08:43:09 GMT  
		Size: 17.7 KB (17744 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-threaded-bookworm` - linux; s390x

```console
$ docker pull perl@sha256:c0fb385ff06dbfd531582c3d4b396e475cb58111bebec4b250e6866883e5e52c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **334.6 MB (334615325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d785bcf543aec0eb25e3e0f2a10bcbbb6020ce6d22dbf9fab16166b1949b8e0f`
-	Default Command: `["perl5.43.5","-de0"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1765152000'
# Tue, 09 Dec 2025 00:10:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 01:45:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 02:57:14 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 06:24:27 GMT
WORKDIR /usr/src/perl
# Tue, 09 Dec 2025 06:30:05 GMT
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/C/CO/CONTRA/perl-5.43.5.tar.gz -o perl-5.43.5.tar.gz     && echo '4232e7a164873e687df929152ee7bbbf075c1d547bccba3d50353f81a897c259 *perl-5.43.5.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.43.5.tar.gz -C /usr/src/perl     && rm perl-5.43.5.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.091.tar.gz'     && echo 'c5996e7335912a5c99e06bdb47ff39df309a857cbd8fd2627a021cefdb53cf54 *IO-Socket-SSL-2.091.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.091.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.091* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Tue, 09 Dec 2025 06:30:05 GMT
WORKDIR /usr/src/app
# Tue, 09 Dec 2025 06:30:05 GMT
CMD ["perl5.43.5" "-de0"]
```

-	Layers:
	-	`sha256:f1896ba83f603ad81e0d8cb48b496e763b4b781a68efe11f1b6de9da929514ea`  
		Last Modified: Mon, 08 Dec 2025 22:15:09 GMT  
		Size: 47.1 MB (47137665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4635598f3b0f128359fc25d526138bfeb1cfd50aa2df3f8a5a9214cdae1551f`  
		Last Modified: Tue, 09 Dec 2025 00:10:58 GMT  
		Size: 24.0 MB (24027286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67c85977b1427cc2c2afbab15cfdcc745e64492465bdc1299648a91c7787a768`  
		Last Modified: Tue, 09 Dec 2025 01:46:34 GMT  
		Size: 63.5 MB (63501228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:021709bd5f44ac18c83367b46ae0ee36d6bf3bfbaaee7f0fc2b3f5a37fa60847`  
		Last Modified: Tue, 09 Dec 2025 03:16:04 GMT  
		Size: 183.5 MB (183497520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d628f1c2f9bc880a89b76b02df177b298c4ad3293cd9eace37f486c534a34c96`  
		Last Modified: Tue, 09 Dec 2025 06:30:36 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68d9b45bbc3de381a238019dfca7fdc441b8a08d63c0158c1a2211cb29fc262a`  
		Last Modified: Tue, 09 Dec 2025 06:30:37 GMT  
		Size: 16.5 MB (16451363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8417f5d1d2aec7451af9f972e241975fcf202af1acb77f101fab0817ea64224`  
		Last Modified: Tue, 09 Dec 2025 06:30:36 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-threaded-bookworm` - unknown; unknown

```console
$ docker pull perl@sha256:6ee1206a785cd3b13ff75d6802701db8c41ef743ca910d313cc8b0945533d579
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.7 MB (15693909 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13c1469f8f51f74c851fc92de3bf11ed98453f87c26841621ccba839d7251db4`

```dockerfile
```

-	Layers:
	-	`sha256:6faf56e82c177ffd9edb6aad0f9b7f3efcf45e028b45ec3d46ca06606dacba5e`  
		Last Modified: Tue, 09 Dec 2025 08:43:27 GMT  
		Size: 15.7 MB (15676203 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:89ee2637e392f6491aa5ab94e0eaa9461db8d63fb944f115a125a190fc5ab7d6`  
		Last Modified: Tue, 09 Dec 2025 08:43:28 GMT  
		Size: 17.7 KB (17706 bytes)  
		MIME: application/vnd.in-toto+json
