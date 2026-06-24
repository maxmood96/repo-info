## `perl:5-bookworm`

```console
$ docker pull perl@sha256:dccb64208d7d83aca97fbdb8b78fbbc8a229d0179a3ff45c56b826628fdf14f1
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

### `perl:5-bookworm` - linux; amd64

```console
$ docker pull perl@sha256:364f501a8e6414d459459d5ef13715ae817f2d9fd426e66022b0319930ac6ba5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **364.5 MB (364460359 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9bc072e82fe9be451a37bfa37f2fe73356429133806635c0002da47fb8b33948`
-	Default Command: `["perl5.42.2","-de0"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1782172800'
# Wed, 24 Jun 2026 01:41:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 02:28:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 03:17:35 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 04:21:42 GMT
WORKDIR /usr/src/perl
# Wed, 24 Jun 2026 04:25:43 GMT
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/S/SH/SHAY/perl-5.42.2.tar.gz -o perl-5.42.2.tar.gz     && echo '9384e8deb75b7b1695e5637971b752281aaecd025a3d5d4734d33c1d0adfee47 *perl-5.42.2.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.42.2.tar.gz -C /usr/src/perl     && rm perl-5.42.2.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7049.tar.gz     && echo 'b9ffb88e62a06aa91bd7d5a28ef6bdbb942608aea90e3969aa29b33640035214 *App-cpanminus-1.7049.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7049.tar.gz && cd App-cpanminus-1.7049     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.96.tar.gz'     && echo 'ab213691685fb2a576c669cbc8d9266f8165a31563ad15b7c4030b94adfc0753 *Net-SSLeay-1.96.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.96.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.098.tar.gz'     && echo 'b38473be20256b1a06447dd6769ad162bfad6a258234ed2c7e2e1819c16c4df7 *IO-Socket-SSL-2.098.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.098.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.998003/cpm -o /usr/local/bin/cpm     && echo '6a27e528cf37635773e738db36c4b4ab4345d5a9d00b8cbd2f2dc01abc73177d */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /root/Net-SSLeay-1.96* /root/IO-Socket-SSL-2.098* /usr/src/perl /usr/src/App-cpanminus-1.7049* /tmp/*     && cpanm --version && cpm --version # buildkit
# Wed, 24 Jun 2026 04:25:43 GMT
WORKDIR /usr/src/app
# Wed, 24 Jun 2026 04:25:43 GMT
CMD ["perl5.42.2" "-de0"]
```

-	Layers:
	-	`sha256:425befdf76e52426879d2abe42093a00dca59a893e7b4fa2a7679b0180b71d4b`  
		Last Modified: Wed, 24 Jun 2026 00:27:40 GMT  
		Size: 48.5 MB (48502210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4fd7bf6f6036613e20f62549df75ed694b99118002358bea5a81baf3929d1ff`  
		Last Modified: Wed, 24 Jun 2026 01:41:33 GMT  
		Size: 24.0 MB (24044046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:791c68bc2063683c3d15907b8ed1b777cf14ca153c6f8e5b12db0868dfa7e38a`  
		Last Modified: Wed, 24 Jun 2026 02:28:33 GMT  
		Size: 64.4 MB (64404017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9eb598f63f1e9867f81313f86224109c84b2af9646d8fca29113217b94315956`  
		Last Modified: Wed, 24 Jun 2026 03:18:16 GMT  
		Size: 211.6 MB (211602331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dfad669ac2eeed7973f6baa5b8907efe51c48a9e6aaa54654618d0e96006722`  
		Last Modified: Wed, 24 Jun 2026 04:25:59 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e41dde02f2b02ef11778745ee0c8f8d2d12c115437f2ba28fa6920b783b6a9ba`  
		Last Modified: Wed, 24 Jun 2026 04:26:00 GMT  
		Size: 15.9 MB (15907488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a51b4caa29ba4002112675fe828c66caf4e3bb36f1ec5fd65d79c3c68ddfc7bc`  
		Last Modified: Wed, 24 Jun 2026 04:26:00 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:5-bookworm` - unknown; unknown

```console
$ docker pull perl@sha256:46ea0b751d1a98c32b578b44ed28f0aaf9706dc2b39bc6aeba67154c627aa43e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.9 MB (15886531 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c2ea859536ee90f77e17f40113fc8776990cb1a8d2dcc777736f50f19efc570`

```dockerfile
```

-	Layers:
	-	`sha256:e9415a69a4897017e2c29cc6402c1d8bf799f747195954788003aa4e2471aa8c`  
		Last Modified: Wed, 24 Jun 2026 04:26:00 GMT  
		Size: 15.9 MB (15868400 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c1173d83c2408655e03723283eafe10f87ac30d910c3ce20573357b30fa5a9e2`  
		Last Modified: Wed, 24 Jun 2026 04:25:59 GMT  
		Size: 18.1 KB (18131 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:5-bookworm` - linux; arm variant v5

```console
$ docker pull perl@sha256:de9f79022119fbf986d8e0d9dc265f27a0f23e709ca31345c8a038400e9be4f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **330.8 MB (330826088 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65872fc8b63a87ff9bbe03d14e00c567e4c05ebda0e2cde16b4fcd6d97f84e78`
-	Default Command: `["perl5.42.2","-de0"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1782172800'
# Wed, 24 Jun 2026 02:19:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 04:13:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 05:13:50 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 07:19:29 GMT
WORKDIR /usr/src/perl
# Wed, 24 Jun 2026 07:25:03 GMT
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/S/SH/SHAY/perl-5.42.2.tar.gz -o perl-5.42.2.tar.gz     && echo '9384e8deb75b7b1695e5637971b752281aaecd025a3d5d4734d33c1d0adfee47 *perl-5.42.2.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.42.2.tar.gz -C /usr/src/perl     && rm perl-5.42.2.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7049.tar.gz     && echo 'b9ffb88e62a06aa91bd7d5a28ef6bdbb942608aea90e3969aa29b33640035214 *App-cpanminus-1.7049.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7049.tar.gz && cd App-cpanminus-1.7049     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.96.tar.gz'     && echo 'ab213691685fb2a576c669cbc8d9266f8165a31563ad15b7c4030b94adfc0753 *Net-SSLeay-1.96.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.96.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.098.tar.gz'     && echo 'b38473be20256b1a06447dd6769ad162bfad6a258234ed2c7e2e1819c16c4df7 *IO-Socket-SSL-2.098.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.098.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.998003/cpm -o /usr/local/bin/cpm     && echo '6a27e528cf37635773e738db36c4b4ab4345d5a9d00b8cbd2f2dc01abc73177d */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /root/Net-SSLeay-1.96* /root/IO-Socket-SSL-2.098* /usr/src/perl /usr/src/App-cpanminus-1.7049* /tmp/*     && cpanm --version && cpm --version # buildkit
# Wed, 24 Jun 2026 07:25:03 GMT
WORKDIR /usr/src/app
# Wed, 24 Jun 2026 07:25:03 GMT
CMD ["perl5.42.2" "-de0"]
```

-	Layers:
	-	`sha256:9b6f26285ba03744a306577b3de61c2f71cba83b0beff1d4a59aef5f7dab736b`  
		Last Modified: Wed, 24 Jun 2026 00:27:23 GMT  
		Size: 46.0 MB (46038207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2576c00204f880be8e3a137f521b0b0f1c2054ec6a7e9d73dd6d20fdf1707cd9`  
		Last Modified: Wed, 24 Jun 2026 02:19:23 GMT  
		Size: 22.7 MB (22718190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81160f0df179da45da421db0ce97a5d8701f99ba34b208c1f3b395a79afd440c`  
		Last Modified: Wed, 24 Jun 2026 04:14:15 GMT  
		Size: 62.0 MB (62022636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:051e255ff76a6a247d3a1e0e9f9ecb076f20cd5ca66898aa1798502072e084fa`  
		Last Modified: Wed, 24 Jun 2026 05:14:27 GMT  
		Size: 184.9 MB (184854196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f50fc43d4aa863aeb0595349ecbee0c57359d35b43c3e7d2075f8117983c87bd`  
		Last Modified: Wed, 24 Jun 2026 07:25:23 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e04da14c9523456b061ee9e8b47dd101f7ee273a4566a5a0c1d5933805910202`  
		Last Modified: Wed, 24 Jun 2026 07:25:24 GMT  
		Size: 15.2 MB (15192592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18fe9953ba57292afaacf4ba68ef805adbbc68b46f08177c49cde1963d23a00f`  
		Last Modified: Wed, 24 Jun 2026 07:25:23 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:5-bookworm` - unknown; unknown

```console
$ docker pull perl@sha256:c1b40d2e94f14d4c5260ef04e786138e87727e10ca7b606617b0265f00b801a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.7 MB (15683627 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:039ab2c3447b1349098321d1b025c7d0cfc039e93fa6099df555de4d9d03aaef`

```dockerfile
```

-	Layers:
	-	`sha256:6069dd8e0763ac80c944e119ec59ffaddbbff7caceebedc5d50b110d85a35e9d`  
		Last Modified: Wed, 24 Jun 2026 07:25:24 GMT  
		Size: 15.7 MB (15665408 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3a6a3d163882240423484c9f64025689512a0d3c2bb6710da002ff51c946c049`  
		Last Modified: Wed, 24 Jun 2026 07:25:24 GMT  
		Size: 18.2 KB (18219 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:5-bookworm` - linux; arm variant v7

```console
$ docker pull perl@sha256:839ee8558f78e0c6d85a69ce3870523c87f5957d254d4a30a3acc5a12ab4b725
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **316.3 MB (316296358 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6bab692d97230f88c254a13210689960d833878ddde6eecaf408be30fdb3da0`
-	Default Command: `["perl5.42.2","-de0"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1782172800'
# Wed, 24 Jun 2026 02:22:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 03:54:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 04:17:45 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 05:20:14 GMT
WORKDIR /usr/src/perl
# Wed, 24 Jun 2026 05:25:41 GMT
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/S/SH/SHAY/perl-5.42.2.tar.gz -o perl-5.42.2.tar.gz     && echo '9384e8deb75b7b1695e5637971b752281aaecd025a3d5d4734d33c1d0adfee47 *perl-5.42.2.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.42.2.tar.gz -C /usr/src/perl     && rm perl-5.42.2.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7049.tar.gz     && echo 'b9ffb88e62a06aa91bd7d5a28ef6bdbb942608aea90e3969aa29b33640035214 *App-cpanminus-1.7049.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7049.tar.gz && cd App-cpanminus-1.7049     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.96.tar.gz'     && echo 'ab213691685fb2a576c669cbc8d9266f8165a31563ad15b7c4030b94adfc0753 *Net-SSLeay-1.96.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.96.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.098.tar.gz'     && echo 'b38473be20256b1a06447dd6769ad162bfad6a258234ed2c7e2e1819c16c4df7 *IO-Socket-SSL-2.098.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.098.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.998003/cpm -o /usr/local/bin/cpm     && echo '6a27e528cf37635773e738db36c4b4ab4345d5a9d00b8cbd2f2dc01abc73177d */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /root/Net-SSLeay-1.96* /root/IO-Socket-SSL-2.098* /usr/src/perl /usr/src/App-cpanminus-1.7049* /tmp/*     && cpanm --version && cpm --version # buildkit
# Wed, 24 Jun 2026 05:25:41 GMT
WORKDIR /usr/src/app
# Wed, 24 Jun 2026 05:25:41 GMT
CMD ["perl5.42.2" "-de0"]
```

-	Layers:
	-	`sha256:3622debffba3838b917703fb6dd9c161a4d93d9fd97c61d3e8400a2245f93c67`  
		Last Modified: Wed, 24 Jun 2026 00:27:30 GMT  
		Size: 44.2 MB (44208145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d0df8de55f365d832099cabf27409104999d59b26292d91202ca6e160c4b513`  
		Last Modified: Wed, 24 Jun 2026 02:22:52 GMT  
		Size: 21.9 MB (21949935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d16c85bf5ff1b42ae66f83fdb64a6cd05a854ea2289dfe1b0ae9e4ee6a806d0a`  
		Last Modified: Wed, 24 Jun 2026 03:54:41 GMT  
		Size: 59.7 MB (59661949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db8aeb3259226bf05c8cdeb78f528aef9d5e19adf28e71540d132fb654168072`  
		Last Modified: Wed, 24 Jun 2026 04:18:20 GMT  
		Size: 175.5 MB (175502691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbd20547e79aa597cfe11354265c7666019e0693276fd70c94e554567ba1132d`  
		Last Modified: Wed, 24 Jun 2026 05:26:01 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d507e025f958eb79d7427d9e4a11e66dc158c9103759586852ea64ef17db1efc`  
		Last Modified: Wed, 24 Jun 2026 05:26:02 GMT  
		Size: 15.0 MB (14973371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:797c54c22d344a2f45d0f07df1a1ce98bf8088932b8d520c82ae91e9fec3f048`  
		Last Modified: Wed, 24 Jun 2026 05:26:01 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:5-bookworm` - unknown; unknown

```console
$ docker pull perl@sha256:e8432264f5365c3bb92fd9480d3132883e0ff0141bb849ceb754d9973ed959f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.7 MB (15689103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7eb242b884ab0a54fbe2af2ae2d02060b9657e9856e696eb84aeb746b1ad63b`

```dockerfile
```

-	Layers:
	-	`sha256:7d25a8c142906d23e9cdf7fd5f2cd6e07ccbdff9f0a639327c9eef3971b3c08b`  
		Last Modified: Wed, 24 Jun 2026 05:26:02 GMT  
		Size: 15.7 MB (15670884 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:316ea7dab99d61ad7fb42f63ce1a1ed0eccb8559f861a473fe4ddac7702d448b`  
		Last Modified: Wed, 24 Jun 2026 05:26:01 GMT  
		Size: 18.2 KB (18219 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:5-bookworm` - linux; arm64 variant v8

```console
$ docker pull perl@sha256:5272bfcd0cc61abbd18b8e4904b3dea20b964f3653e770a3750b419a9929bde7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **355.5 MB (355490365 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ae5c69f0c0fdd14c011b92026d844f8411daeca207b4d19da7f867bf5fcfb5e`
-	Default Command: `["perl5.42.2","-de0"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1782172800'
# Wed, 24 Jun 2026 01:44:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 02:35:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 03:16:32 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 04:21:44 GMT
WORKDIR /usr/src/perl
# Wed, 24 Jun 2026 04:26:16 GMT
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/S/SH/SHAY/perl-5.42.2.tar.gz -o perl-5.42.2.tar.gz     && echo '9384e8deb75b7b1695e5637971b752281aaecd025a3d5d4734d33c1d0adfee47 *perl-5.42.2.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.42.2.tar.gz -C /usr/src/perl     && rm perl-5.42.2.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7049.tar.gz     && echo 'b9ffb88e62a06aa91bd7d5a28ef6bdbb942608aea90e3969aa29b33640035214 *App-cpanminus-1.7049.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7049.tar.gz && cd App-cpanminus-1.7049     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.96.tar.gz'     && echo 'ab213691685fb2a576c669cbc8d9266f8165a31563ad15b7c4030b94adfc0753 *Net-SSLeay-1.96.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.96.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.098.tar.gz'     && echo 'b38473be20256b1a06447dd6769ad162bfad6a258234ed2c7e2e1819c16c4df7 *IO-Socket-SSL-2.098.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.098.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.998003/cpm -o /usr/local/bin/cpm     && echo '6a27e528cf37635773e738db36c4b4ab4345d5a9d00b8cbd2f2dc01abc73177d */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /root/Net-SSLeay-1.96* /root/IO-Socket-SSL-2.098* /usr/src/perl /usr/src/App-cpanminus-1.7049* /tmp/*     && cpanm --version && cpm --version # buildkit
# Wed, 24 Jun 2026 04:26:16 GMT
WORKDIR /usr/src/app
# Wed, 24 Jun 2026 04:26:16 GMT
CMD ["perl5.42.2" "-de0"]
```

-	Layers:
	-	`sha256:0fb1189398e2e4b474d43aac6502510d0da0318e70137a377c21087f198814db`  
		Last Modified: Wed, 24 Jun 2026 00:27:19 GMT  
		Size: 48.4 MB (48389201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03ebca214f1a4b66acfdb0bd20aa3ee139d1747885ef4b0f3d07aa2a68459230`  
		Last Modified: Wed, 24 Jun 2026 01:44:48 GMT  
		Size: 23.6 MB (23613316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:533bb0e918720911be6cb7a1a5ba9ad0e1a308fcbf24961a23aba0cd220df6cf`  
		Last Modified: Wed, 24 Jun 2026 02:35:28 GMT  
		Size: 64.5 MB (64487706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cae401c24fa4bb4f22bb94674a5eb530bff1cfd2e063ec20053ecb9a5509556`  
		Last Modified: Wed, 24 Jun 2026 03:17:13 GMT  
		Size: 203.1 MB (203132913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fedbc74ac98f34c8f359a9680d103a8a20849c956373989bad028149a34b140`  
		Last Modified: Wed, 24 Jun 2026 04:26:34 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f722eb68fcc0e19a4ac8dcc33bbc3d7f490570b1f3086f09a1ddfe9f006a4e97`  
		Last Modified: Wed, 24 Jun 2026 04:26:35 GMT  
		Size: 15.9 MB (15866963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5132f75a0a7b9722d7f6910c9d110096c164dd2740efa915d7d8ceb06e07c58`  
		Last Modified: Wed, 24 Jun 2026 04:26:34 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:5-bookworm` - unknown; unknown

```console
$ docker pull perl@sha256:6664d15290d92b84efb7b4d02ef9d608bef7824156a925d6f65b51401e9c8fb4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.9 MB (15915185 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67f23db9b283f1b796cda5d9aa4f0bf3c3479a254ed5e3d865f85752cb87ca4b`

```dockerfile
```

-	Layers:
	-	`sha256:2a2a906c2ff7e0624c24f138a89111aa66a5e774b2f099349c60dff7ef2542f6`  
		Last Modified: Wed, 24 Jun 2026 04:26:35 GMT  
		Size: 15.9 MB (15896938 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:912bf1d07b032cedd1c0d407596f989da77e84c2d7462b4afc339f370441aabc`  
		Last Modified: Wed, 24 Jun 2026 04:26:34 GMT  
		Size: 18.2 KB (18247 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:5-bookworm` - linux; 386

```console
$ docker pull perl@sha256:adbdb00705d769c4c437beab360060455d20a9116fdc8011dba34fe80b7f923b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **366.5 MB (366546305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e51cf642ad84884c9cdc5d2b5cef16391229a833335a04eb930fd72af6125339`
-	Default Command: `["perl5.42.2","-de0"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1782172800'
# Wed, 24 Jun 2026 01:43:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 02:34:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 03:18:09 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 04:14:52 GMT
WORKDIR /usr/src/perl
# Wed, 24 Jun 2026 04:19:52 GMT
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/S/SH/SHAY/perl-5.42.2.tar.gz -o perl-5.42.2.tar.gz     && echo '9384e8deb75b7b1695e5637971b752281aaecd025a3d5d4734d33c1d0adfee47 *perl-5.42.2.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.42.2.tar.gz -C /usr/src/perl     && rm perl-5.42.2.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7049.tar.gz     && echo 'b9ffb88e62a06aa91bd7d5a28ef6bdbb942608aea90e3969aa29b33640035214 *App-cpanminus-1.7049.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7049.tar.gz && cd App-cpanminus-1.7049     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.96.tar.gz'     && echo 'ab213691685fb2a576c669cbc8d9266f8165a31563ad15b7c4030b94adfc0753 *Net-SSLeay-1.96.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.96.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.098.tar.gz'     && echo 'b38473be20256b1a06447dd6769ad162bfad6a258234ed2c7e2e1819c16c4df7 *IO-Socket-SSL-2.098.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.098.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.998003/cpm -o /usr/local/bin/cpm     && echo '6a27e528cf37635773e738db36c4b4ab4345d5a9d00b8cbd2f2dc01abc73177d */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /root/Net-SSLeay-1.96* /root/IO-Socket-SSL-2.098* /usr/src/perl /usr/src/App-cpanminus-1.7049* /tmp/*     && cpanm --version && cpm --version # buildkit
# Wed, 24 Jun 2026 04:19:52 GMT
WORKDIR /usr/src/app
# Wed, 24 Jun 2026 04:19:52 GMT
CMD ["perl5.42.2" "-de0"]
```

-	Layers:
	-	`sha256:96cbacad9c1883b9ae87f68a0550ac0bd7e0b7ba2b15b142a793b89b5a5f36ad`  
		Last Modified: Wed, 24 Jun 2026 00:27:48 GMT  
		Size: 49.5 MB (49491378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b45c9ce5ae5ea6ab37787312be8b0a9732642c1221f97d5689baacac874b4cd`  
		Last Modified: Wed, 24 Jun 2026 01:43:48 GMT  
		Size: 24.9 MB (24879740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6db0110899c29fd647e62f912bfb740fc8af5310cdc227454d8f086f16cba33e`  
		Last Modified: Wed, 24 Jun 2026 02:35:05 GMT  
		Size: 66.2 MB (66244204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33d35d0ef7b0d342bb15591580b2f53dedb16d47cf8b5adeb9bc453fd0b71b9b`  
		Last Modified: Wed, 24 Jun 2026 03:18:51 GMT  
		Size: 210.5 MB (210534885 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9686f273d79af1d963840770d426c2b7483317781f90d7bd851bf2218918495`  
		Last Modified: Wed, 24 Jun 2026 04:20:13 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d9ecd6f816f00cdf0f5a7fcd8e7b2e7b2f10b4085950a0045b8430a26ea21fe`  
		Last Modified: Wed, 24 Jun 2026 04:20:13 GMT  
		Size: 15.4 MB (15395833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:010273512bb7fd0dffc669f5fd3ade894b075ca639c6d69cb700db53a204c362`  
		Last Modified: Wed, 24 Jun 2026 04:20:13 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:5-bookworm` - unknown; unknown

```console
$ docker pull perl@sha256:c229807798ade64ac19d012f8858afbb53fec0a8d7b94b69974c44d176322b8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.9 MB (15864706 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37447861e1c62034f6158cb4ec0f70a58a28fa5cfca4bd9380aa6dee959f3213`

```dockerfile
```

-	Layers:
	-	`sha256:f6be69d1576b083995bc2473b7361edaae6c667a3b0c2b389c8c4436f6f7b06b`  
		Last Modified: Wed, 24 Jun 2026 04:20:13 GMT  
		Size: 15.8 MB (15846613 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:970961e3aa9112f42ee9a1dff72ce17c67d9d0e3fd4bae43c9c5837c3d674deb`  
		Last Modified: Wed, 24 Jun 2026 04:20:13 GMT  
		Size: 18.1 KB (18093 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:5-bookworm` - linux; mips64le

```console
$ docker pull perl@sha256:b5a86e78557aff5b4361d35de0e88471b825a2663665a9f9be65f7bd36f9cca4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **341.2 MB (341202014 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9881731b5468865eda93bd9db229a07085ec81b3f154eba992be75957ef93988`
-	Default Command: `["perl5.42.2","-de0"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1781049600'
# Thu, 11 Jun 2026 17:08:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 12 Jun 2026 01:00:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 12 Jun 2026 01:25:21 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 12 Jun 2026 04:39:45 GMT
WORKDIR /usr/src/perl
# Fri, 12 Jun 2026 05:17:59 GMT
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/S/SH/SHAY/perl-5.42.2.tar.gz -o perl-5.42.2.tar.gz     && echo '9384e8deb75b7b1695e5637971b752281aaecd025a3d5d4734d33c1d0adfee47 *perl-5.42.2.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.42.2.tar.gz -C /usr/src/perl     && rm perl-5.42.2.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7049.tar.gz     && echo 'b9ffb88e62a06aa91bd7d5a28ef6bdbb942608aea90e3969aa29b33640035214 *App-cpanminus-1.7049.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7049.tar.gz && cd App-cpanminus-1.7049     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.96.tar.gz'     && echo 'ab213691685fb2a576c669cbc8d9266f8165a31563ad15b7c4030b94adfc0753 *Net-SSLeay-1.96.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.96.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.098.tar.gz'     && echo 'b38473be20256b1a06447dd6769ad162bfad6a258234ed2c7e2e1819c16c4df7 *IO-Socket-SSL-2.098.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.098.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.998003/cpm -o /usr/local/bin/cpm     && echo '6a27e528cf37635773e738db36c4b4ab4345d5a9d00b8cbd2f2dc01abc73177d */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /root/Net-SSLeay-1.96* /root/IO-Socket-SSL-2.098* /usr/src/perl /usr/src/App-cpanminus-1.7049* /tmp/*     && cpanm --version && cpm --version # buildkit
# Fri, 12 Jun 2026 05:18:00 GMT
WORKDIR /usr/src/app
# Fri, 12 Jun 2026 05:18:00 GMT
CMD ["perl5.42.2" "-de0"]
```

-	Layers:
	-	`sha256:c4a18bb29be3659c76b4d9b55eb7f69e2b6fcb341523ef1670ac059503a592b9`  
		Last Modified: Wed, 10 Jun 2026 23:39:38 GMT  
		Size: 48.8 MB (48792711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d391bb145fa329ccce2ad9a5e686a519ff55f48ee4a211ba2c146ad64db56d80`  
		Last Modified: Thu, 11 Jun 2026 17:09:36 GMT  
		Size: 23.6 MB (23624039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:270c086020bbce3335fe9eece6ed9bd8f5bc1e45eed6579e81e64181addffb83`  
		Last Modified: Fri, 12 Jun 2026 01:02:23 GMT  
		Size: 63.3 MB (63315954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cabc0d09590f6c3174b92d8abd0703508147f87e3c896edd58df6a33c30e4c61`  
		Last Modified: Fri, 12 Jun 2026 01:28:57 GMT  
		Size: 190.4 MB (190354833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38e8f54012e8311c2a64dd102322bc1b436c19cea729f2b4fd2eabf339118c3a`  
		Last Modified: Fri, 12 Jun 2026 05:19:19 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a3c0836004d9e3aab12c3594b35c2e6934cc6a6583a5ebb597512d33638d505`  
		Last Modified: Fri, 12 Jun 2026 05:19:21 GMT  
		Size: 15.1 MB (15114211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fbd356667bc61c7bc6a717b9aa56b8e1239d04012a24fb07a0faa217e1ebcae`  
		Last Modified: Fri, 12 Jun 2026 05:19:19 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:5-bookworm` - unknown; unknown

```console
$ docker pull perl@sha256:d7f45be523510425fd9365518f85d60effa21737a17ea8fbecdf7d26c50ba921
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.0 KB (17991 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd5cbbabc45f1ca1c5223b2fc1bdb5e4cd5af062e6d6083c7ce49bd3073400d0`

```dockerfile
```

-	Layers:
	-	`sha256:b4be13ab290bdd4156cad3b06889ddb5a924999101743ae20628322d503117ea`  
		Last Modified: Fri, 12 Jun 2026 05:19:19 GMT  
		Size: 18.0 KB (17991 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:5-bookworm` - linux; ppc64le

```console
$ docker pull perl@sha256:5eeaf70eba57cfa7de882c3d7c771e5a5a117283ebd7b19871ddd525b2d572f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **378.4 MB (378430427 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:495cd70e0c2f13086a64940d88eaf27dc22fbe5ca62f0d252ae34f694a171711`
-	Default Command: `["perl5.42.2","-de0"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1781049600'
# Thu, 11 Jun 2026 04:43:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 10:26:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 12:45:00 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 16:56:50 GMT
WORKDIR /usr/src/perl
# Thu, 11 Jun 2026 17:05:41 GMT
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/S/SH/SHAY/perl-5.42.2.tar.gz -o perl-5.42.2.tar.gz     && echo '9384e8deb75b7b1695e5637971b752281aaecd025a3d5d4734d33c1d0adfee47 *perl-5.42.2.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.42.2.tar.gz -C /usr/src/perl     && rm perl-5.42.2.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7049.tar.gz     && echo 'b9ffb88e62a06aa91bd7d5a28ef6bdbb942608aea90e3969aa29b33640035214 *App-cpanminus-1.7049.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7049.tar.gz && cd App-cpanminus-1.7049     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.96.tar.gz'     && echo 'ab213691685fb2a576c669cbc8d9266f8165a31563ad15b7c4030b94adfc0753 *Net-SSLeay-1.96.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.96.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.098.tar.gz'     && echo 'b38473be20256b1a06447dd6769ad162bfad6a258234ed2c7e2e1819c16c4df7 *IO-Socket-SSL-2.098.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.098.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.998003/cpm -o /usr/local/bin/cpm     && echo '6a27e528cf37635773e738db36c4b4ab4345d5a9d00b8cbd2f2dc01abc73177d */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /root/Net-SSLeay-1.96* /root/IO-Socket-SSL-2.098* /usr/src/perl /usr/src/App-cpanminus-1.7049* /tmp/*     && cpanm --version && cpm --version # buildkit
# Thu, 11 Jun 2026 17:05:41 GMT
WORKDIR /usr/src/app
# Thu, 11 Jun 2026 17:05:41 GMT
CMD ["perl5.42.2" "-de0"]
```

-	Layers:
	-	`sha256:88b94a58fac236a778527a3293ccd0ff4d309bff0bf314017ea5af603908fa2e`  
		Last Modified: Thu, 11 Jun 2026 00:21:34 GMT  
		Size: 52.3 MB (52346670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45654aeab75acaade8b0e13728139de28feb7f503c7e094076fcb9a6e4ed987e`  
		Last Modified: Thu, 11 Jun 2026 04:43:46 GMT  
		Size: 25.7 MB (25686794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47b3af7c755dce470b1c44918153cc71bc2ea3bed1cbf9108bce1ad1d4579fb5`  
		Last Modified: Thu, 11 Jun 2026 10:27:04 GMT  
		Size: 69.9 MB (69853632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea21655a17d2ee83d21538915d2102860b4542a5b2c3753a90e0b3aa19415b42`  
		Last Modified: Thu, 11 Jun 2026 12:46:18 GMT  
		Size: 214.6 MB (214640105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b304ca2ac7c6f9d2245cff91e4612ee2937d4da89a588d1d0bd55696ba39c9b7`  
		Last Modified: Thu, 11 Jun 2026 17:06:31 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d50172722f14ed823330d5f06ee35797a1b4dc182855f881d10d65fb4d3a0404`  
		Last Modified: Thu, 11 Jun 2026 17:06:33 GMT  
		Size: 15.9 MB (15902960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa702d246952f2b581733489bc4d146b61c1bab8dcc0741d86762e42e2540c1b`  
		Last Modified: Thu, 11 Jun 2026 17:06:31 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:5-bookworm` - unknown; unknown

```console
$ docker pull perl@sha256:dc5fcae0a0edf995f264608202f986bee1f0f4f4a8ee3365ca9905c8c887c4b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.9 MB (15863102 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8198af7d8b027f85dd7642b8dbd7da0d23ba3e4139b24385c7e2ae6dec1346f`

```dockerfile
```

-	Layers:
	-	`sha256:83e2f949bf54c1cfb0063226271dcbd07dd1ae9f69dd30d57ccda7e2866dba9c`  
		Last Modified: Thu, 11 Jun 2026 17:06:32 GMT  
		Size: 15.8 MB (15844921 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:48dd1df7d84109d7df1bb954c431a22da191cc7392cc9da4587b4e5ca069488a`  
		Last Modified: Thu, 11 Jun 2026 17:06:31 GMT  
		Size: 18.2 KB (18181 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:5-bookworm` - linux; s390x

```console
$ docker pull perl@sha256:a71d8a777a970474ac906122c21b9c283690c08af4c7066ee503cb0738401ca8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **334.6 MB (334565548 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6019a08699db12a421f1028f641ed68d59c8cddd1b265192f0b18aaf417ba4c`
-	Default Command: `["perl5.42.2","-de0"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1781049600'
# Thu, 11 Jun 2026 01:43:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 03:26:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 04:15:16 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 07:37:13 GMT
WORKDIR /usr/src/perl
# Thu, 11 Jun 2026 07:44:49 GMT
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/S/SH/SHAY/perl-5.42.2.tar.gz -o perl-5.42.2.tar.gz     && echo '9384e8deb75b7b1695e5637971b752281aaecd025a3d5d4734d33c1d0adfee47 *perl-5.42.2.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.42.2.tar.gz -C /usr/src/perl     && rm perl-5.42.2.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7049.tar.gz     && echo 'b9ffb88e62a06aa91bd7d5a28ef6bdbb942608aea90e3969aa29b33640035214 *App-cpanminus-1.7049.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7049.tar.gz && cd App-cpanminus-1.7049     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.96.tar.gz'     && echo 'ab213691685fb2a576c669cbc8d9266f8165a31563ad15b7c4030b94adfc0753 *Net-SSLeay-1.96.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.96.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.098.tar.gz'     && echo 'b38473be20256b1a06447dd6769ad162bfad6a258234ed2c7e2e1819c16c4df7 *IO-Socket-SSL-2.098.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.098.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.998003/cpm -o /usr/local/bin/cpm     && echo '6a27e528cf37635773e738db36c4b4ab4345d5a9d00b8cbd2f2dc01abc73177d */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /root/Net-SSLeay-1.96* /root/IO-Socket-SSL-2.098* /usr/src/perl /usr/src/App-cpanminus-1.7049* /tmp/*     && cpanm --version && cpm --version # buildkit
# Thu, 11 Jun 2026 07:44:49 GMT
WORKDIR /usr/src/app
# Thu, 11 Jun 2026 07:44:49 GMT
CMD ["perl5.42.2" "-de0"]
```

-	Layers:
	-	`sha256:b041a55a85cc0e47dd570746852cc1b0fee042f3a03eb250b9f896ac4aa74a3d`  
		Last Modified: Wed, 10 Jun 2026 23:41:01 GMT  
		Size: 47.2 MB (47161500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dc0f0bf9684619796dace2f15b323a1fcec3fdfd4a5712e33f82ae28ed815bf`  
		Last Modified: Thu, 11 Jun 2026 01:43:58 GMT  
		Size: 24.0 MB (24038950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f33cb3e3ab28182d2640ab8d60069099e6c4d1dd9ee3f806d20e366f1901797`  
		Last Modified: Thu, 11 Jun 2026 03:26:38 GMT  
		Size: 63.5 MB (63498201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1ff3f7a67e23169f7ca69b49e30014a5c74ff53c62dbec259b93c844556a24a`  
		Last Modified: Thu, 11 Jun 2026 04:16:09 GMT  
		Size: 183.6 MB (183623488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c562a33bbba75b21798e8c36e7af0684dd656418b063afb02d96ce58097b54f1`  
		Last Modified: Thu, 11 Jun 2026 07:45:24 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea7930a483ff86bbc407a83131f1ba097d1cda78d816287088b2f93c14e3f892`  
		Last Modified: Thu, 11 Jun 2026 07:45:24 GMT  
		Size: 16.2 MB (16243142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25eb2324d664e14f7b3b35638c3998118077d9dec9cd1308e766a9190d34f092`  
		Last Modified: Thu, 11 Jun 2026 07:45:24 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:5-bookworm` - unknown; unknown

```console
$ docker pull perl@sha256:d75b5407b427569a29c5c0927c91c15477033e15e658f355814d025bf731e7d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.7 MB (15694129 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82edde96f7456b7a757c6622da9a9093e627069eb45f6c42dedff3dc5dd8e9a7`

```dockerfile
```

-	Layers:
	-	`sha256:8ef6cee57ca46a2e7a26a0b37eb9bb78482d6527da6842e4ad16ae8e0894c5a5`  
		Last Modified: Thu, 11 Jun 2026 07:45:24 GMT  
		Size: 15.7 MB (15675998 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0ec74c775f70ca7082fa015187335874bcadd49369e09c2d1c989a923f2f60f0`  
		Last Modified: Thu, 11 Jun 2026 07:45:24 GMT  
		Size: 18.1 KB (18131 bytes)  
		MIME: application/vnd.in-toto+json
