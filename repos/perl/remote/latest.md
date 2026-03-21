## `perl:latest`

```console
$ docker pull perl@sha256:76fbab4f66fa3812e0b1e305b58f289968b2c1663739718a072935dbd140014e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 14
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v5
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `perl:latest` - linux; amd64

```console
$ docker pull perl@sha256:a099dde7c967c4b2bc4d1251bba0e27ecb9f9324fcaac8e688f224fdc704244a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **394.7 MB (394686642 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ea64dfe0e697e59c19f3e446c97993246933989a87898ce23ab63b489cfd8d5`
-	Default Command: `["perl5.42.1","-de0"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1773619200'
# Mon, 16 Mar 2026 22:38:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Mon, 16 Mar 2026 23:25:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 17 Mar 2026 00:20:14 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
# Tue, 17 Mar 2026 01:46:31 GMT
WORKDIR /usr/src/perl
# Tue, 17 Mar 2026 01:50:47 GMT
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/S/SH/SHAY/perl-5.42.1.tar.gz -o perl-5.42.1.tar.gz     && echo '6f84e6dc8cce97181d1c6aeeb552c13775c91ded3c6c73743c9211af87b16bf8 *perl-5.42.1.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.42.1.tar.gz -C /usr/src/perl     && rm perl-5.42.1.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7048.tar.gz     && echo '59b60907ab9fa4f72ca2004fbe6054911439ae9a906890b4d842a87b25f20f3c *App-cpanminus-1.7048.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7048.tar.gz && cd App-cpanminus-1.7048     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.098.tar.gz'     && echo 'b38473be20256b1a06447dd6769ad162bfad6a258234ed2c7e2e1819c16c4df7 *IO-Socket-SSL-2.098.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.098.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.998003/cpm -o /usr/local/bin/cpm     && echo '6a27e528cf37635773e738db36c4b4ab4345d5a9d00b8cbd2f2dc01abc73177d */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.098* /usr/src/perl /usr/src/App-cpanminus-1.7048* /tmp/*     && cpanm --version && cpm --version # buildkit
# Tue, 17 Mar 2026 01:50:47 GMT
WORKDIR /usr/src/app
# Tue, 17 Mar 2026 01:50:47 GMT
CMD ["perl5.42.1" "-de0"]
```

-	Layers:
	-	`sha256:8f6ad858d0a46fa8ee628532c70b8dc82d06179d543b0b09ec19fc03d4c5b373`  
		Last Modified: Mon, 16 Mar 2026 21:53:17 GMT  
		Size: 49.3 MB (49297530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b012eb15dff0bce418c03ec940325aee6aa4300d771c325728855697e620c63a`  
		Last Modified: Mon, 16 Mar 2026 22:38:25 GMT  
		Size: 25.6 MB (25621715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee3a0e7d77f0c84203cab438fcf345647c8121bbd80506a3c692f8608a14c4f4`  
		Last Modified: Mon, 16 Mar 2026 23:25:57 GMT  
		Size: 67.8 MB (67780758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8688d0f2f567884eb217c6f80efa063bdb13a1951e92e6c5cac1ae5b736f5e1b`  
		Last Modified: Tue, 17 Mar 2026 00:21:01 GMT  
		Size: 236.1 MB (236079671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c68d36b0bbb2b967deb383ec474eba174563adf507370688695a1a6c09d641e`  
		Last Modified: Tue, 17 Mar 2026 01:51:06 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cccb3ba3cbfffbacfaa570a6aebb56a4ce216c0129b7dcbabde082a30fb32ea`  
		Last Modified: Tue, 17 Mar 2026 01:51:07 GMT  
		Size: 15.9 MB (15906702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f527864ccdb9271858cf7fd9bfa4d4134345f152f5440461c6648066d72e9b5`  
		Last Modified: Tue, 17 Mar 2026 01:51:06 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:latest` - unknown; unknown

```console
$ docker pull perl@sha256:f648ed12a9794a19fd215abdc30907012bc1063b4c12d6594d1123c4226a274e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.2 MB (17231381 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:570e423aed89c2ecc49a905b97a2dd66388173489c0e1cb254380f3719490818`

```dockerfile
```

-	Layers:
	-	`sha256:c5b79576e96364234712f306e964f9c09c053a051923eeff37947c8ec8e9b338`  
		Last Modified: Tue, 17 Mar 2026 01:51:07 GMT  
		Size: 17.2 MB (17211824 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6fd0762bc0cc6cbf991d027385123f847c1b8504fd51bdd8d7c46c1030bf3e1a`  
		Last Modified: Tue, 17 Mar 2026 01:51:06 GMT  
		Size: 19.6 KB (19557 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:latest` - linux; arm variant v5

```console
$ docker pull perl@sha256:5b55beec3dcc567eedeebf0c6abaf539b3d29f2830a3021adb7c934c51e5a4d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **358.2 MB (358163138 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e9f230c8ac4f9b4ac3f0cb9955db7a115f529d542f3ab663bbd803c91507584`
-	Default Command: `["perl5.42.1","-de0"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1773619200'
# Mon, 16 Mar 2026 23:16:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 17 Mar 2026 01:08:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 17 Mar 2026 02:19:17 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
# Tue, 17 Mar 2026 03:22:06 GMT
WORKDIR /usr/src/perl
# Tue, 17 Mar 2026 03:27:30 GMT
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/S/SH/SHAY/perl-5.42.1.tar.gz -o perl-5.42.1.tar.gz     && echo '6f84e6dc8cce97181d1c6aeeb552c13775c91ded3c6c73743c9211af87b16bf8 *perl-5.42.1.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.42.1.tar.gz -C /usr/src/perl     && rm perl-5.42.1.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7048.tar.gz     && echo '59b60907ab9fa4f72ca2004fbe6054911439ae9a906890b4d842a87b25f20f3c *App-cpanminus-1.7048.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7048.tar.gz && cd App-cpanminus-1.7048     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.098.tar.gz'     && echo 'b38473be20256b1a06447dd6769ad162bfad6a258234ed2c7e2e1819c16c4df7 *IO-Socket-SSL-2.098.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.098.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.998003/cpm -o /usr/local/bin/cpm     && echo '6a27e528cf37635773e738db36c4b4ab4345d5a9d00b8cbd2f2dc01abc73177d */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.098* /usr/src/perl /usr/src/App-cpanminus-1.7048* /tmp/*     && cpanm --version && cpm --version # buildkit
# Tue, 17 Mar 2026 03:27:30 GMT
WORKDIR /usr/src/app
# Tue, 17 Mar 2026 03:27:30 GMT
CMD ["perl5.42.1" "-de0"]
```

-	Layers:
	-	`sha256:8524aea9c07f7c3a1779bfcb961bdcea323ac7abd571c794a134ffeb31a825be`  
		Last Modified: Mon, 16 Mar 2026 21:52:54 GMT  
		Size: 47.5 MB (47460612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4a10acd8de7c2ea5feeb4bbe7b5147fdee10ce64d8ad5f6db26957ab6ab82a0`  
		Last Modified: Mon, 16 Mar 2026 23:17:07 GMT  
		Size: 24.4 MB (24364203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:043762e26fc507e51d741404184de0ffa48c048233f8091ab9a9f0a36a848703`  
		Last Modified: Tue, 17 Mar 2026 01:08:51 GMT  
		Size: 65.3 MB (65316059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8c68fb49833128a0e871517930af2b90f7664e7e4693c07588b34ef9db2a4ae`  
		Last Modified: Tue, 17 Mar 2026 02:19:57 GMT  
		Size: 205.8 MB (205798566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0c171d15d4befa5b1282bf5fd18bfc8747a4d3d24420f0dbcd38ff94ac3856c`  
		Last Modified: Tue, 17 Mar 2026 03:27:49 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:866cc52af134839dad27216f5ae332fc988dda86ec2cc2d8b56fa54411e41f38`  
		Last Modified: Tue, 17 Mar 2026 03:27:50 GMT  
		Size: 15.2 MB (15223432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c81399a16d2154e7e95e7436ea17733027d6f3e09187c1e3ca6626d7d9c6c6bd`  
		Last Modified: Tue, 17 Mar 2026 03:27:49 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:latest` - unknown; unknown

```console
$ docker pull perl@sha256:bd642f1ef611683ff41fb50301ee84e52be17ed8a17c065a9a672b017c6d2fd1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.0 MB (16993763 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1a151b8caaff8781ea05ac9a7de23e026836cc846695107eeaa84cdd0e0b4a8`

```dockerfile
```

-	Layers:
	-	`sha256:362fbdfe50f49e27b9802002c36edb3b893a580d3a6ddc0fc69a60b55e1bedd5`  
		Last Modified: Tue, 17 Mar 2026 03:27:50 GMT  
		Size: 17.0 MB (16974078 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1840a4824e5bbbd2ea48a70efe836e1621c26600affe1bd6a974ba5a22957c41`  
		Last Modified: Tue, 17 Mar 2026 03:27:49 GMT  
		Size: 19.7 KB (19685 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:latest` - linux; arm variant v7

```console
$ docker pull perl@sha256:f3baaf6596779fc889f0b8fc4adce397bfaf1e3958a5b1da63036801a5b10e10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **340.5 MB (340472399 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0dc5a25dfa1c2a9d8092b8df926f806a2dcad2bcb5e31f1a0c6ea49ee57196b`
-	Default Command: `["perl5.42.1","-de0"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1773619200'
# Tue, 17 Mar 2026 00:27:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 17 Mar 2026 01:15:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 17 Mar 2026 02:17:49 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
# Tue, 17 Mar 2026 03:22:31 GMT
WORKDIR /usr/src/perl
# Tue, 17 Mar 2026 03:27:39 GMT
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/S/SH/SHAY/perl-5.42.1.tar.gz -o perl-5.42.1.tar.gz     && echo '6f84e6dc8cce97181d1c6aeeb552c13775c91ded3c6c73743c9211af87b16bf8 *perl-5.42.1.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.42.1.tar.gz -C /usr/src/perl     && rm perl-5.42.1.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7048.tar.gz     && echo '59b60907ab9fa4f72ca2004fbe6054911439ae9a906890b4d842a87b25f20f3c *App-cpanminus-1.7048.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7048.tar.gz && cd App-cpanminus-1.7048     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.098.tar.gz'     && echo 'b38473be20256b1a06447dd6769ad162bfad6a258234ed2c7e2e1819c16c4df7 *IO-Socket-SSL-2.098.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.098.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.998003/cpm -o /usr/local/bin/cpm     && echo '6a27e528cf37635773e738db36c4b4ab4345d5a9d00b8cbd2f2dc01abc73177d */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.098* /usr/src/perl /usr/src/App-cpanminus-1.7048* /tmp/*     && cpanm --version && cpm --version # buildkit
# Tue, 17 Mar 2026 03:27:39 GMT
WORKDIR /usr/src/app
# Tue, 17 Mar 2026 03:27:39 GMT
CMD ["perl5.42.1" "-de0"]
```

-	Layers:
	-	`sha256:83d3fd32d825865515469d080b5a8d89e630e2ed8f99a18d7b80d9c437631ab6`  
		Last Modified: Mon, 16 Mar 2026 21:53:25 GMT  
		Size: 45.7 MB (45732648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cceb46da040530c459a3d55c1b9d0ccf68be7e284352029649a82437d5fc663`  
		Last Modified: Tue, 17 Mar 2026 00:27:35 GMT  
		Size: 23.6 MB (23637012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e536a24ef93e50bf0d2984c667c771026334af7e30ed6318f85d146e4ff7a306`  
		Last Modified: Tue, 17 Mar 2026 01:15:28 GMT  
		Size: 62.7 MB (62713901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86f696900d4222bf2837e3b49ef63fc1177cb3ecebfcfa488c398c25b057bd61`  
		Last Modified: Tue, 17 Mar 2026 02:18:26 GMT  
		Size: 193.4 MB (193352535 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:024b4fcda47540c58765dca19b2918e0930c1540647f7f8f987f91172e292414`  
		Last Modified: Tue, 17 Mar 2026 03:28:01 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ac7285dc630a54c452aaf71b47ffcd40c5636e3373bab13ab2594fbe79c1b35`  
		Last Modified: Tue, 17 Mar 2026 03:28:01 GMT  
		Size: 15.0 MB (15036039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd155a6034d348a71f2ca7875dee98a8cf429248df2bb026aa2fbcf1aee01f35`  
		Last Modified: Tue, 17 Mar 2026 03:28:01 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:latest` - unknown; unknown

```console
$ docker pull perl@sha256:920414f61d740e9f22f3f5bc187a8ec04e9eb964d8b78f278377e08b8a351881
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.0 MB (16999552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:095821dc312cddaa4b67c514435f67f9cbc3fce85be0853e60f76b93997dad14`

```dockerfile
```

-	Layers:
	-	`sha256:415d502da416e648a1980f867e670e4e1d8e557f55c3b3ec2fc387d627eb0e96`  
		Last Modified: Tue, 17 Mar 2026 03:28:01 GMT  
		Size: 17.0 MB (16979868 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b8acf91f6b7838b0daa6de67543d882e83edfb59f511578df51e520cddb1880f`  
		Last Modified: Tue, 17 Mar 2026 03:28:00 GMT  
		Size: 19.7 KB (19684 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:latest` - linux; arm64 variant v8

```console
$ docker pull perl@sha256:8b5cac5e8126c1b9e418ae97ee435a8154b82052255e06d3a668b61a9d0494c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **384.3 MB (384337617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ecd07cf848aadf42eba52c31d78be9cd411a1f31c046c28866066eaa702997a5`
-	Default Command: `["perl5.42.1","-de0"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1773619200'
# Mon, 16 Mar 2026 22:40:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Mon, 16 Mar 2026 23:30:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 17 Mar 2026 00:20:05 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
# Tue, 17 Mar 2026 01:48:31 GMT
WORKDIR /usr/src/perl
# Tue, 17 Mar 2026 01:53:08 GMT
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/S/SH/SHAY/perl-5.42.1.tar.gz -o perl-5.42.1.tar.gz     && echo '6f84e6dc8cce97181d1c6aeeb552c13775c91ded3c6c73743c9211af87b16bf8 *perl-5.42.1.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.42.1.tar.gz -C /usr/src/perl     && rm perl-5.42.1.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7048.tar.gz     && echo '59b60907ab9fa4f72ca2004fbe6054911439ae9a906890b4d842a87b25f20f3c *App-cpanminus-1.7048.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7048.tar.gz && cd App-cpanminus-1.7048     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.098.tar.gz'     && echo 'b38473be20256b1a06447dd6769ad162bfad6a258234ed2c7e2e1819c16c4df7 *IO-Socket-SSL-2.098.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.098.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.998003/cpm -o /usr/local/bin/cpm     && echo '6a27e528cf37635773e738db36c4b4ab4345d5a9d00b8cbd2f2dc01abc73177d */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.098* /usr/src/perl /usr/src/App-cpanminus-1.7048* /tmp/*     && cpanm --version && cpm --version # buildkit
# Tue, 17 Mar 2026 01:53:08 GMT
WORKDIR /usr/src/app
# Tue, 17 Mar 2026 01:53:08 GMT
CMD ["perl5.42.1" "-de0"]
```

-	Layers:
	-	`sha256:deab8db42772fcfeb45003461fe0eb7bf63bdb29199a4fb76242b9493437c28b`  
		Last Modified: Mon, 16 Mar 2026 21:53:03 GMT  
		Size: 49.7 MB (49664953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6778b62bd97b31237948877e89abc29ad2b2c003f3b965027457c8c90d4f44e0`  
		Last Modified: Mon, 16 Mar 2026 22:40:45 GMT  
		Size: 25.0 MB (25023728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d16813bdedcf0a1acbd78336c5bed6fbfaee2674574408140ba7e896cd49cb95`  
		Last Modified: Mon, 16 Mar 2026 23:31:00 GMT  
		Size: 67.6 MB (67584568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86cdc6c7463a47d1f18421cbc086ad744c8d50c71a79c199d3f739370d14f166`  
		Last Modified: Tue, 17 Mar 2026 00:20:49 GMT  
		Size: 226.2 MB (226205219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6544d05ac52b6eae087975ef9f493faa59392a6c8202e7bdc8acc8e070c5ab9d`  
		Last Modified: Tue, 17 Mar 2026 01:53:30 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:055f37782f4b504bf1285868977343422a7ea892725686dcb9bf6d441a6ed160`  
		Last Modified: Tue, 17 Mar 2026 01:53:30 GMT  
		Size: 15.9 MB (15858883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70c81c756e682bf3d938978e54a5cdff1731e15eb6b09def9e1bb80d7e46b52e`  
		Last Modified: Tue, 17 Mar 2026 01:53:30 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:latest` - unknown; unknown

```console
$ docker pull perl@sha256:2f0d0e6c9c5ef3a97f23273e7c43de8917545181cba332769adcfc5065d36a92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.3 MB (17315935 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:653a614ec28cf7931264d4c38a0f1fe0c6820f918fffa42da6c5b5927bfa52cf`

```dockerfile
```

-	Layers:
	-	`sha256:70cf53946682b96aa7d9e527ebb073cfa5d4386e896fd033f6eed76a5af1e928`  
		Last Modified: Tue, 17 Mar 2026 01:53:30 GMT  
		Size: 17.3 MB (17296202 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:862fa5ae27885a8e65e962d7e589987b2bf29fd3617a9b35fc519edc02fdef7f`  
		Last Modified: Tue, 17 Mar 2026 01:53:30 GMT  
		Size: 19.7 KB (19733 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:latest` - linux; ppc64le

```console
$ docker pull perl@sha256:6535a83b6de175bb344da24e9266e70435dfec87fc8269761e08ddb0096cebfe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **400.2 MB (400243049 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f31799bbff4d184827178b4eb3676dba34161386236ae8f079f3dff9585692c`
-	Default Command: `["perl5.42.1","-de0"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1773619200'
# Tue, 17 Mar 2026 01:50:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 17 Mar 2026 06:05:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 17 Mar 2026 08:24:23 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
# Tue, 17 Mar 2026 14:04:32 GMT
WORKDIR /usr/src/perl
# Tue, 17 Mar 2026 14:15:02 GMT
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/S/SH/SHAY/perl-5.42.1.tar.gz -o perl-5.42.1.tar.gz     && echo '6f84e6dc8cce97181d1c6aeeb552c13775c91ded3c6c73743c9211af87b16bf8 *perl-5.42.1.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.42.1.tar.gz -C /usr/src/perl     && rm perl-5.42.1.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7048.tar.gz     && echo '59b60907ab9fa4f72ca2004fbe6054911439ae9a906890b4d842a87b25f20f3c *App-cpanminus-1.7048.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7048.tar.gz && cd App-cpanminus-1.7048     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.098.tar.gz'     && echo 'b38473be20256b1a06447dd6769ad162bfad6a258234ed2c7e2e1819c16c4df7 *IO-Socket-SSL-2.098.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.098.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.998003/cpm -o /usr/local/bin/cpm     && echo '6a27e528cf37635773e738db36c4b4ab4345d5a9d00b8cbd2f2dc01abc73177d */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.098* /usr/src/perl /usr/src/App-cpanminus-1.7048* /tmp/*     && cpanm --version && cpm --version # buildkit
# Tue, 17 Mar 2026 14:15:04 GMT
WORKDIR /usr/src/app
# Tue, 17 Mar 2026 14:15:04 GMT
CMD ["perl5.42.1" "-de0"]
```

-	Layers:
	-	`sha256:616ed6c40b4f1136ebcda954e46e021bcee567aad248468321da4f4065f4a14d`  
		Last Modified: Mon, 16 Mar 2026 21:55:32 GMT  
		Size: 53.1 MB (53118350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e76fd6649d6d35f910f2df9456726122ef27f29bb48c2f6e7ffbc7d318e0c0f`  
		Last Modified: Tue, 17 Mar 2026 01:51:12 GMT  
		Size: 27.0 MB (27013391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7e880a549306a0c27a7c0db6951a348b972ff41cbbc4c467d5d3c95c7797075`  
		Last Modified: Tue, 17 Mar 2026 06:06:09 GMT  
		Size: 73.0 MB (73033284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad9316a36149e2b5d350920e8ac524970c623231b0efef70b4ab1af7d3eb70e2`  
		Last Modified: Tue, 17 Mar 2026 08:25:46 GMT  
		Size: 231.2 MB (231196585 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0eb36ca95ed91cba2f61e3cbe7102e3a8e45945bae2d7f149e0e7f02882a640`  
		Last Modified: Tue, 17 Mar 2026 14:15:52 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc854e818d54f8baca9f7f7766887f9a2e7bff23e31f9689ae03eeadadbaee09`  
		Last Modified: Tue, 17 Mar 2026 14:15:52 GMT  
		Size: 15.9 MB (15881175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b2a3f27bc6e818962e4c440bea9379a268b2b1a34e54c084e3924297d99ec7b`  
		Last Modified: Tue, 17 Mar 2026 14:15:52 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:latest` - unknown; unknown

```console
$ docker pull perl@sha256:1fea66b20088f74bfbffa05fe4a48a63ffcbd43827236e9c4a1760d59f7049a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.2 MB (17217052 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:258c4e7138d40cd145d25d071a683ced8081a0c9d7f2a02a82c19753b64fb5b2`

```dockerfile
```

-	Layers:
	-	`sha256:906b94b39d3e71d525c6fcb2f364e0db4ec469835c9093e937a5cd51fdb85a59`  
		Last Modified: Tue, 17 Mar 2026 14:15:53 GMT  
		Size: 17.2 MB (17197417 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:90036643d85faa7c96883483cdac12eff95e73c2bfb563df07bf9c09fb2bbfd8`  
		Last Modified: Tue, 17 Mar 2026 14:15:52 GMT  
		Size: 19.6 KB (19635 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:latest` - linux; riscv64

```console
$ docker pull perl@sha256:6a070a66349ba186e2371e5ef59a695be594fcb49e860c034169bff7b9291c27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **477.8 MB (477806099 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c0cdfbef9a1d7157ebac22d247727a3724f20d2991ee26f1542f67d29ceec63`
-	Default Command: `["perl5.42.1","-de0"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1773619200'
# Wed, 18 Mar 2026 05:11:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Thu, 19 Mar 2026 05:31:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Sat, 21 Mar 2026 02:46:11 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
# Sat, 21 Mar 2026 17:26:26 GMT
WORKDIR /usr/src/perl
# Sat, 21 Mar 2026 18:33:00 GMT
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/S/SH/SHAY/perl-5.42.1.tar.gz -o perl-5.42.1.tar.gz     && echo '6f84e6dc8cce97181d1c6aeeb552c13775c91ded3c6c73743c9211af87b16bf8 *perl-5.42.1.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.42.1.tar.gz -C /usr/src/perl     && rm perl-5.42.1.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7048.tar.gz     && echo '59b60907ab9fa4f72ca2004fbe6054911439ae9a906890b4d842a87b25f20f3c *App-cpanminus-1.7048.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7048.tar.gz && cd App-cpanminus-1.7048     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.098.tar.gz'     && echo 'b38473be20256b1a06447dd6769ad162bfad6a258234ed2c7e2e1819c16c4df7 *IO-Socket-SSL-2.098.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.098.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.998003/cpm -o /usr/local/bin/cpm     && echo '6a27e528cf37635773e738db36c4b4ab4345d5a9d00b8cbd2f2dc01abc73177d */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.098* /usr/src/perl /usr/src/App-cpanminus-1.7048* /tmp/*     && cpanm --version && cpm --version # buildkit
# Sat, 21 Mar 2026 18:33:00 GMT
WORKDIR /usr/src/app
# Sat, 21 Mar 2026 18:33:00 GMT
CMD ["perl5.42.1" "-de0"]
```

-	Layers:
	-	`sha256:90acba8ac92ad141ae919a99e64549b2f417e5b2ec79f1a99dbc8efba0fea96b`  
		Last Modified: Mon, 16 Mar 2026 22:09:11 GMT  
		Size: 47.8 MB (47792328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8d52d7ab982f4bfd5cfc38caa0eefe3bfddcb1b2f76f02a38e1b10725b762ee`  
		Last Modified: Wed, 18 Mar 2026 05:13:23 GMT  
		Size: 25.0 MB (24954925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fc9a450c15c86147b6c308f2cb25a618ec75f2ab5a64203aa728b5e309ab137`  
		Last Modified: Thu, 19 Mar 2026 05:35:26 GMT  
		Size: 66.7 MB (66662504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85f6bc50f98c9426c1cbc86b6a57067e5cf240684e827203ca98d393b1722732`  
		Last Modified: Sat, 21 Mar 2026 03:01:35 GMT  
		Size: 323.0 MB (323020173 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bca1f5f1fcdd5d2fdc2f6309780be109490cfd17f8079e078cc061cf9aabb82d`  
		Last Modified: Sat, 21 Mar 2026 18:41:05 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d54468bafa7d58eaab6fadc95993c494ea50faa8f40e26dbdc99d9b935a4c24e`  
		Last Modified: Sat, 21 Mar 2026 18:41:10 GMT  
		Size: 15.4 MB (15375903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05248ad3bd5ae864900cd4673dfa0b2ffa5e98813a41864e85fa4dc0c38cfa04`  
		Last Modified: Sat, 21 Mar 2026 18:41:05 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:latest` - unknown; unknown

```console
$ docker pull perl@sha256:ee1ad0ad1c0f8b6ff16ee3a548e60ca4d794cf75ec5f5d49353dff68252e8508
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.3 MB (17287696 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c1173488b5007212f5b9be90de10af39f53de02c2e244910afd7ad3dbd0305e`

```dockerfile
```

-	Layers:
	-	`sha256:7e6080b116c8907b2e6e59e62c87da726af6df4b68bdb86ec9b6058b63988e1c`  
		Last Modified: Sat, 21 Mar 2026 18:41:10 GMT  
		Size: 17.3 MB (17268060 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6d42475fb6a562d68a4261a691c2fb11ea3356051b3180d286c89db899dbb7de`  
		Last Modified: Sat, 21 Mar 2026 18:41:05 GMT  
		Size: 19.6 KB (19636 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:latest` - linux; s390x

```console
$ docker pull perl@sha256:271a3bbd22030f66e20218460d211beb490f158ca3d22e88c891d0cdba8a788e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **367.9 MB (367850666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5864dcba39d646c3b35c877e428c30cf2022b51aa62c3ac87f300f274f154161`
-	Default Command: `["perl5.42.1","-de0"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1773619200'
# Mon, 16 Mar 2026 23:45:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 17 Mar 2026 01:34:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 17 Mar 2026 02:17:59 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
# Tue, 17 Mar 2026 07:24:38 GMT
WORKDIR /usr/src/perl
# Tue, 17 Mar 2026 07:31:52 GMT
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/S/SH/SHAY/perl-5.42.1.tar.gz -o perl-5.42.1.tar.gz     && echo '6f84e6dc8cce97181d1c6aeeb552c13775c91ded3c6c73743c9211af87b16bf8 *perl-5.42.1.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.42.1.tar.gz -C /usr/src/perl     && rm perl-5.42.1.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7048.tar.gz     && echo '59b60907ab9fa4f72ca2004fbe6054911439ae9a906890b4d842a87b25f20f3c *App-cpanminus-1.7048.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7048.tar.gz && cd App-cpanminus-1.7048     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.098.tar.gz'     && echo 'b38473be20256b1a06447dd6769ad162bfad6a258234ed2c7e2e1819c16c4df7 *IO-Socket-SSL-2.098.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.098.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.998003/cpm -o /usr/local/bin/cpm     && echo '6a27e528cf37635773e738db36c4b4ab4345d5a9d00b8cbd2f2dc01abc73177d */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.098* /usr/src/perl /usr/src/App-cpanminus-1.7048* /tmp/*     && cpanm --version && cpm --version # buildkit
# Tue, 17 Mar 2026 07:31:52 GMT
WORKDIR /usr/src/app
# Tue, 17 Mar 2026 07:31:52 GMT
CMD ["perl5.42.1" "-de0"]
```

-	Layers:
	-	`sha256:7bc76783a6155f9347e92234e4b5c38bd02638c6de782f4623d0736c769250f0`  
		Last Modified: Mon, 16 Mar 2026 21:52:57 GMT  
		Size: 49.4 MB (49364775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8371259f6819197ae08830e46db090d1aad241011f8c2483f8e3205359263dcd`  
		Last Modified: Mon, 16 Mar 2026 23:45:50 GMT  
		Size: 26.8 MB (26803190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6990bcd0cd48258f05a5e1da913e50e516d08ed7812badfbb9d8451ec894a6a6`  
		Last Modified: Tue, 17 Mar 2026 01:34:59 GMT  
		Size: 68.6 MB (68628445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47057cfd6a92f3d99db284d930f4e069c4ad4f63f130f90e61f4d7667173d2e1`  
		Last Modified: Tue, 17 Mar 2026 02:19:02 GMT  
		Size: 206.6 MB (206580881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e012dcdb1acf1a3badf52d09477e4ca661a48e27f8c53b29220f20846712bc18`  
		Last Modified: Tue, 17 Mar 2026 07:32:36 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17f567f308be90480f3bd64cd139b8f8d112f92dcadb8fe084d48e43e058a01b`  
		Last Modified: Tue, 17 Mar 2026 07:32:37 GMT  
		Size: 16.5 MB (16473110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4fb5af430d1153c828866e99970bec3e4460345c0bcf78d9c4dd715ab805a7c`  
		Last Modified: Tue, 17 Mar 2026 07:32:36 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:latest` - unknown; unknown

```console
$ docker pull perl@sha256:a63acbcd91536de53ca78b961101de861bb66e3e544eb759c7d9f731997b477b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.0 MB (17008614 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8af8d2401bac71bb83b3a41f7a7a32e3279ebd4c6f197d4a3f510ff1df0b5c7f`

```dockerfile
```

-	Layers:
	-	`sha256:d9af60eaf0a1553c6d41fdd5823951023712ecc21f98846e58d46cd21fc05c8e`  
		Last Modified: Tue, 17 Mar 2026 07:32:37 GMT  
		Size: 17.0 MB (16989057 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7251396bf542343881c85d4316cac6683999e2f67c74df126b87141d0830a022`  
		Last Modified: Tue, 17 Mar 2026 07:32:36 GMT  
		Size: 19.6 KB (19557 bytes)  
		MIME: application/vnd.in-toto+json
