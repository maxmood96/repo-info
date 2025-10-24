## `perl:devel-threaded-bookworm`

```console
$ docker pull perl@sha256:370114733bdfc236710bf2d2667dee30922d3c1ff7c727c050aee2fc3cfc5fc4
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
$ docker pull perl@sha256:6ea82c1ae32b34edd1d29cdf519b6aabfa6bbf7f2f8fed96ad24c10af1962452
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **364.3 MB (364330265 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d96e27caf847112b5f798c856b1d2e153a636cb9d6d4f76978117b163868671`
-	Default Command: `["perl5.43.2","-de0"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1760918400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 24 Aug 2025 06:40:17 GMT
WORKDIR /usr/src/perl
# Sun, 24 Aug 2025 06:40:17 GMT
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/E/ET/ETHER/perl-5.43.2.tar.gz -o perl-5.43.2.tar.gz     && echo '202dc989a29e461bef175dc23ac0ba0d7eef49ea10e1fefe696f19ede210dc29 *perl-5.43.2.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.43.2.tar.gz -C /usr/src/perl     && rm perl-5.43.2.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.091.tar.gz'     && echo 'c5996e7335912a5c99e06bdb47ff39df309a857cbd8fd2627a021cefdb53cf54 *IO-Socket-SSL-2.091.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.091.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.091* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Sun, 24 Aug 2025 06:40:17 GMT
WORKDIR /usr/src/app
# Sun, 24 Aug 2025 06:40:17 GMT
CMD ["perl5.43.2" "-de0"]
```

-	Layers:
	-	`sha256:cd01849e3cbdfc6993640303768edbb56372cf9f1ae101d516334c8d462341af`  
		Last Modified: Tue, 21 Oct 2025 00:19:25 GMT  
		Size: 48.5 MB (48480563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f279d33abc52c7384e0cbbb666ea22064ea29b50a968ec29ae3ad817f62e16e7`  
		Last Modified: Tue, 21 Oct 2025 04:46:37 GMT  
		Size: 24.0 MB (24028898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5daa5a418829f3daa90a80438cd84706b5f7fa0c795eb7936874864ef1ab7b0c`  
		Last Modified: Tue, 21 Oct 2025 04:47:27 GMT  
		Size: 64.4 MB (64396405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da3556d62e9bd977c17e315ad64979017739fd90fc5a2a89ec07cf82348133f3`  
		Last Modified: Tue, 21 Oct 2025 10:21:00 GMT  
		Size: 211.4 MB (211449932 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7601a2a79e909e5d9081dd92cd10f5796b2240749761ac2bd3a41b572de3c46d`  
		Last Modified: Tue, 21 Oct 2025 11:28:15 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:626797dfc6f5cf6e6c9274c103468b78b161b2d6ef454a13cb9313a863d2bc59`  
		Last Modified: Tue, 21 Oct 2025 11:42:53 GMT  
		Size: 16.0 MB (15974200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:847d18dcc37c7799f129bb0a63679a3e19d8baf8c2d9dd2d3a2fed4cb7a6b70b`  
		Last Modified: Tue, 21 Oct 2025 11:42:49 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-threaded-bookworm` - unknown; unknown

```console
$ docker pull perl@sha256:10f7e74f41a776ad372460f11da703e414f8c28e89110337192ab4b219860461
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.9 MB (15886353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44d0ba6e1dc4686b61e306fabb82c6eea2cad64f249c99b8e2e43c2cb7c6640f`

```dockerfile
```

-	Layers:
	-	`sha256:cdb4cb25b8360edbe0c0e916a386d2ba23c3920849a27496286c13a784bb24d4`  
		Last Modified: Tue, 21 Oct 2025 13:43:07 GMT  
		Size: 15.9 MB (15868605 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:75a315960f9a828c58b606ce3004605740c5db0a485cecdef04ceb9fc3ce2823`  
		Last Modified: Tue, 21 Oct 2025 13:43:08 GMT  
		Size: 17.7 KB (17748 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-threaded-bookworm` - linux; arm variant v5

```console
$ docker pull perl@sha256:6ff5cb17d4ff1c0c07b0dfaf94a4d49bb41119381230a7c6d5bf92e0b17873ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **330.7 MB (330670883 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b75162ff1a2a55e401985f050527052488b99d8495d157024845d4a1898356f6`
-	Default Command: `["perl5.43.2","-de0"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1760918400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 24 Aug 2025 06:40:17 GMT
WORKDIR /usr/src/perl
# Sun, 24 Aug 2025 06:40:17 GMT
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/E/ET/ETHER/perl-5.43.2.tar.gz -o perl-5.43.2.tar.gz     && echo '202dc989a29e461bef175dc23ac0ba0d7eef49ea10e1fefe696f19ede210dc29 *perl-5.43.2.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.43.2.tar.gz -C /usr/src/perl     && rm perl-5.43.2.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.091.tar.gz'     && echo 'c5996e7335912a5c99e06bdb47ff39df309a857cbd8fd2627a021cefdb53cf54 *IO-Socket-SSL-2.091.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.091.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.091* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Sun, 24 Aug 2025 06:40:17 GMT
WORKDIR /usr/src/app
# Sun, 24 Aug 2025 06:40:17 GMT
CMD ["perl5.43.2" "-de0"]
```

-	Layers:
	-	`sha256:d6b0ca95b13ee68ac33e867e046c01d5a40daee1d76922dab47dd1edf2533e94`  
		Last Modified: Tue, 21 Oct 2025 00:19:45 GMT  
		Size: 46.0 MB (46015580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f052363c254a265c1c1981af32f1173b8e1aaed39bd939fefe1c6df9415293e8`  
		Last Modified: Tue, 21 Oct 2025 02:31:20 GMT  
		Size: 22.7 MB (22705272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44b133760d8b3858f3734b5cb15f7cdb7c053d326bcfb50d307307a330761b3f`  
		Last Modified: Tue, 21 Oct 2025 03:56:21 GMT  
		Size: 62.0 MB (62010513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de2f0d85bad27dcc72c31efff2b02e49c817947a3cb10eee5d68de4cee1e1020`  
		Last Modified: Tue, 21 Oct 2025 05:14:10 GMT  
		Size: 184.7 MB (184699235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:640dc404e4bc2d1857064b3a3fccccba218c2d0496f87417d84607e70729c0e3`  
		Last Modified: Tue, 21 Oct 2025 05:21:37 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c30ceebe1368a8f9350b659c94c2724406a68515b1c7b496d18879ec1cca5f41`  
		Last Modified: Tue, 21 Oct 2025 05:45:16 GMT  
		Size: 15.2 MB (15240018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a759bc2fa503d82dce2f1de12b0780ea0e99020dceaf28b04b086e27916017f`  
		Last Modified: Tue, 21 Oct 2025 05:45:14 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-threaded-bookworm` - unknown; unknown

```console
$ docker pull perl@sha256:faca3f6caa68adb5c1284681b8f04cc876b33af9100545df79d0d934bc72e77d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.7 MB (15683417 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b081f28ac305d1b184d80bc3a6dbc00da105b8b437b552ca48317ccf7b9e79c1`

```dockerfile
```

-	Layers:
	-	`sha256:4fd750f9e3467ee2ab7390b96f93e0fb125e32aa4f017a0eae12e47ec99669b6`  
		Last Modified: Tue, 21 Oct 2025 07:45:11 GMT  
		Size: 15.7 MB (15665597 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4102e91374034c9bef53cdeaeb326784582fb9a422c253874f4a92b28d3a2872`  
		Last Modified: Tue, 21 Oct 2025 07:45:12 GMT  
		Size: 17.8 KB (17820 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-threaded-bookworm` - linux; arm variant v7

```console
$ docker pull perl@sha256:2b982b0735dd76a6117d7e3ab39d76c0c13293c09eae34b6d1580239a9541541
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **316.2 MB (316158436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b528aa4f06e79959056a95e50e1ef2f4a5558aed1f70a97185d7bd37e2eea09`
-	Default Command: `["perl5.43.2","-de0"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1760918400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 24 Aug 2025 06:40:17 GMT
WORKDIR /usr/src/perl
# Sun, 24 Aug 2025 06:40:17 GMT
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/E/ET/ETHER/perl-5.43.2.tar.gz -o perl-5.43.2.tar.gz     && echo '202dc989a29e461bef175dc23ac0ba0d7eef49ea10e1fefe696f19ede210dc29 *perl-5.43.2.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.43.2.tar.gz -C /usr/src/perl     && rm perl-5.43.2.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.091.tar.gz'     && echo 'c5996e7335912a5c99e06bdb47ff39df309a857cbd8fd2627a021cefdb53cf54 *IO-Socket-SSL-2.091.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.091.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.091* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Sun, 24 Aug 2025 06:40:17 GMT
WORKDIR /usr/src/app
# Sun, 24 Aug 2025 06:40:17 GMT
CMD ["perl5.43.2" "-de0"]
```

-	Layers:
	-	`sha256:5dbe800c0d6104b6df988b153994b0d1b5c022197b54cf928820e3c23d00c7eb`  
		Last Modified: Tue, 21 Oct 2025 01:16:21 GMT  
		Size: 44.2 MB (44195910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:178651637d26f6ae6fc6c2a3297b37f8bbef12e80d822930b05b14f51a262382`  
		Last Modified: Tue, 21 Oct 2025 02:43:48 GMT  
		Size: 21.9 MB (21934505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14411cad8875b2a42f951ec95179ed8a844d1522990ec8b96f1c4d269ce3c71f`  
		Last Modified: Tue, 21 Oct 2025 04:11:04 GMT  
		Size: 59.7 MB (59652688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:934fb9fcc0f174aa356a518c85a7e2e8a62dd5902afe2a8dbbf58f5f8b37166b`  
		Last Modified: Tue, 21 Oct 2025 06:17:29 GMT  
		Size: 175.4 MB (175355007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ea42d207d7dc361157c9331734830289e0b0b17699ecb01558b7afd17a00c09`  
		Last Modified: Tue, 21 Oct 2025 06:30:39 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8afb91bbc8aeff28d64ea7730e4d59ab7e951f8d29b6d0166ebf7fc53de40e3b`  
		Last Modified: Tue, 21 Oct 2025 06:48:46 GMT  
		Size: 15.0 MB (15020059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2872284730a6e7f640f40af9d0dcc27f16e16f246f184ab7644d0ffcc6c1338`  
		Last Modified: Tue, 21 Oct 2025 06:48:44 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-threaded-bookworm` - unknown; unknown

```console
$ docker pull perl@sha256:f6e988de153ce328310b3f3c54902b468cef563982c3da67eb45473f87ab2ed3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.7 MB (15688893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aaa863e1611b279b76004932556b2c3ac82743fcbf6a9f0665584a543e380dc3`

```dockerfile
```

-	Layers:
	-	`sha256:42d33ac8f04df1230486473b23e5abd5925ad5ebf008b82b7ecde788f2dbedcf`  
		Last Modified: Tue, 21 Oct 2025 10:50:36 GMT  
		Size: 15.7 MB (15671073 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:69d8f00fa1fd1fd769cfa16865632c1465c9b4062164074994b12b3a0fa494a2`  
		Last Modified: Tue, 21 Oct 2025 10:50:36 GMT  
		Size: 17.8 KB (17820 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-threaded-bookworm` - linux; arm64 variant v8

```console
$ docker pull perl@sha256:3ca6efe52417e4629ab7c089d0a1bb964a641ce81610cb47e277672e57171ec1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **355.2 MB (355207928 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:732e691596f1f5b0a0f91a941aab5e155391cb670e31a1369464500e8185a140`
-	Default Command: `["perl5.43.2","-de0"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1760918400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 24 Aug 2025 06:40:17 GMT
WORKDIR /usr/src/perl
# Sun, 24 Aug 2025 06:40:17 GMT
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/E/ET/ETHER/perl-5.43.2.tar.gz -o perl-5.43.2.tar.gz     && echo '202dc989a29e461bef175dc23ac0ba0d7eef49ea10e1fefe696f19ede210dc29 *perl-5.43.2.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.43.2.tar.gz -C /usr/src/perl     && rm perl-5.43.2.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.091.tar.gz'     && echo 'c5996e7335912a5c99e06bdb47ff39df309a857cbd8fd2627a021cefdb53cf54 *IO-Socket-SSL-2.091.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.091.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.091* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Sun, 24 Aug 2025 06:40:17 GMT
WORKDIR /usr/src/app
# Sun, 24 Aug 2025 06:40:17 GMT
CMD ["perl5.43.2" "-de0"]
```

-	Layers:
	-	`sha256:394d8e61f78f890cc5a49345ac4d4eb6176cdcf6b4b6af62502ae74b1662e421`  
		Last Modified: Tue, 21 Oct 2025 00:18:41 GMT  
		Size: 48.4 MB (48358996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:add7397bc0ae282f3ecd02217ad720d86eab3a3d325f0bfed57fc864c2281a58`  
		Last Modified: Tue, 21 Oct 2025 01:46:17 GMT  
		Size: 23.6 MB (23597991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd15270faa4e93fc4bcc62caecce8d2f5dfc1443d3c99572dfb689973b24c0a4`  
		Last Modified: Tue, 21 Oct 2025 02:35:23 GMT  
		Size: 64.4 MB (64370931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6803b5e31b40492f4747e974e6e4ae692982b12beb2b87ed9d9ffbdaedefcfd4`  
		Last Modified: Tue, 21 Oct 2025 04:13:43 GMT  
		Size: 203.0 MB (202958684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:067d61df1e08b704bef866f6a77218068b7dc493aae7bc06ceb8c9e1c40d82a3`  
		Last Modified: Tue, 21 Oct 2025 04:32:20 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ad854174b29ae89a0abcf2060649c0ff48438ba4f4663488329de1b7569ea39`  
		Last Modified: Tue, 21 Oct 2025 04:42:18 GMT  
		Size: 15.9 MB (15921061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a2bf3eeb7b2208f1cfdcb5328e8f9376210a3d5d991ad0e5f436ba6bedf57fa`  
		Last Modified: Tue, 21 Oct 2025 04:42:16 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-threaded-bookworm` - unknown; unknown

```console
$ docker pull perl@sha256:d16c606bc4f70a51d01faa70298db0ad4d18966d89078049c277b5bd00a4b886
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.9 MB (15914959 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96d15e08a08d85f23e865f9cc00f04173693d92bd9ba1d8c900bc7a9b2ab1556`

```dockerfile
```

-	Layers:
	-	`sha256:2eacc72bb34e5e9061789b496e8d9eb1e9ac93c0a62101c2b0c388edd8a475c8`  
		Last Modified: Tue, 21 Oct 2025 10:50:51 GMT  
		Size: 15.9 MB (15897119 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cd90cf88701e2fcd82c8f33175d818de1699c4508f5c1f21a7d768301b458473`  
		Last Modified: Tue, 21 Oct 2025 10:50:52 GMT  
		Size: 17.8 KB (17840 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-threaded-bookworm` - linux; 386

```console
$ docker pull perl@sha256:956452997640dccfd8f67faa20934d64b410999d071765efb5611a4617dfe098
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **366.6 MB (366571294 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af478c17b46c874c6a579cc1eda5a0accc80aaea585e6137980cdc85061fa9b5`
-	Default Command: `["perl5.43.4","-de0"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1760918400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 24 Oct 2025 07:13:41 GMT
WORKDIR /usr/src/perl
# Fri, 24 Oct 2025 07:13:41 GMT
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/E/EH/EHERMAN/perl-5.43.4.tar.gz -o perl-5.43.4.tar.gz     && echo '75676cc02c1d4d6f4577f7fd953e07ab5d06f71cf4201753ab6e2b0ddb5a4931 *perl-5.43.4.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.43.4.tar.gz -C /usr/src/perl     && rm perl-5.43.4.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.091.tar.gz'     && echo 'c5996e7335912a5c99e06bdb47ff39df309a857cbd8fd2627a021cefdb53cf54 *IO-Socket-SSL-2.091.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.091.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.091* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Fri, 24 Oct 2025 07:13:41 GMT
WORKDIR /usr/src/app
# Fri, 24 Oct 2025 07:13:41 GMT
CMD ["perl5.43.4" "-de0"]
```

-	Layers:
	-	`sha256:3426ba65368da59a25d050cab9d7713d7873264014ab6dfaa6b0c33f0632cb80`  
		Last Modified: Tue, 21 Oct 2025 00:20:21 GMT  
		Size: 49.5 MB (49466720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f14d3e3fda83046fcd165bb976221020273830b54d963f634e53e7796b47053`  
		Last Modified: Tue, 21 Oct 2025 01:52:59 GMT  
		Size: 24.9 MB (24864208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39058bc352da86cee9643b9b447133a3295983ec455cdba2fac6cbbed8726db6`  
		Last Modified: Tue, 21 Oct 2025 02:35:47 GMT  
		Size: 66.2 MB (66231902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed15f8c1488a55d242a6bf3226b75c0d0de56631f3ea18bb327cec39013003bd`  
		Last Modified: Tue, 21 Oct 2025 04:13:40 GMT  
		Size: 210.4 MB (210381245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:849028cb15ef7a2d111eed6d02e46355b6feffd7fb963aa7f6be9a0a5ed66e03`  
		Last Modified: Fri, 24 Oct 2025 19:00:16 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe6dc8514474a6a5cae3866cd125664c3753cee6991f46fdd8093be70ce7aafc`  
		Last Modified: Fri, 24 Oct 2025 19:00:17 GMT  
		Size: 15.6 MB (15626951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65b4a8490f668ea22f5041b5b5138cd14ab178bd39d7dcded7eea79f1b6bd6df`  
		Last Modified: Fri, 24 Oct 2025 19:00:17 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-threaded-bookworm` - unknown; unknown

```console
$ docker pull perl@sha256:39b53d76c01c136f9caed5be579e64825d5b5f6c2f227193320d3f9e10a5c3df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.9 MB (15864550 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9340c13b0763a194f0e56091bcd3266417ea0ff8edc672361e237e523327856b`

```dockerfile
```

-	Layers:
	-	`sha256:4b600b298e92c72ea4f1d2a09d63b91a2682655103d9513b892213143738309d`  
		Last Modified: Fri, 24 Oct 2025 19:43:19 GMT  
		Size: 15.8 MB (15846827 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:683da4d930b2cad574713d26e42d47de774b12dcdfca4a4b70486b8e13223205`  
		Last Modified: Fri, 24 Oct 2025 19:43:20 GMT  
		Size: 17.7 KB (17723 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-threaded-bookworm` - linux; mips64le

```console
$ docker pull perl@sha256:545b5ad38f048803dbba536f9304124b7d9e05a45da01cbb1c59640309570d5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **341.1 MB (341096082 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d2ceb6934ee6b7408f2d21c952effe0686d6e7173bb00193d190c4e3f7dc38f`
-	Default Command: `["perl5.43.2","-de0"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1760918400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 24 Aug 2025 06:40:17 GMT
WORKDIR /usr/src/perl
# Sun, 24 Aug 2025 06:40:17 GMT
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/E/ET/ETHER/perl-5.43.2.tar.gz -o perl-5.43.2.tar.gz     && echo '202dc989a29e461bef175dc23ac0ba0d7eef49ea10e1fefe696f19ede210dc29 *perl-5.43.2.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.43.2.tar.gz -C /usr/src/perl     && rm perl-5.43.2.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.091.tar.gz'     && echo 'c5996e7335912a5c99e06bdb47ff39df309a857cbd8fd2627a021cefdb53cf54 *IO-Socket-SSL-2.091.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.091.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.091* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Sun, 24 Aug 2025 06:40:17 GMT
WORKDIR /usr/src/app
# Sun, 24 Aug 2025 06:40:17 GMT
CMD ["perl5.43.2" "-de0"]
```

-	Layers:
	-	`sha256:4ff7a7a0be4afa0c088333063434d872e5a67b49bc2165e0d5f1c8b45e31c387`  
		Last Modified: Tue, 21 Oct 2025 00:19:28 GMT  
		Size: 48.8 MB (48760743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ada83e05f36ace3b39ede326eee5e8c640f47f0d217601cc47ce49334a0f7e2`  
		Last Modified: Tue, 21 Oct 2025 17:26:33 GMT  
		Size: 23.6 MB (23613801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20eca72dd31bb50cadfd79b7ad12f89f5688c744f6a098004e516ee38f52407c`  
		Last Modified: Tue, 21 Oct 2025 23:43:20 GMT  
		Size: 63.3 MB (63309417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:814bc6bdb04fa99c9a89fc3a90aaa9ea2da7c62e2933ad85bf543e1690ab23cb`  
		Last Modified: Wed, 22 Oct 2025 01:21:38 GMT  
		Size: 190.2 MB (190221174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:316cb09e21bd477d5cd9f2bd3e252be1737efffe126dd8c3d122cc1d140d9377`  
		Last Modified: Wed, 22 Oct 2025 03:41:56 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f876214534ebd03a978264cd1903ebbbf792197cf2d741d512dce264537fec5c`  
		Last Modified: Wed, 22 Oct 2025 06:42:44 GMT  
		Size: 15.2 MB (15190679 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f9d69fa294874a1ada4fbb0ae115c2314184b03f969a9db20e320fe378666fd`  
		Last Modified: Wed, 22 Oct 2025 06:42:43 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-threaded-bookworm` - unknown; unknown

```console
$ docker pull perl@sha256:bf62e22538fa1a5e31b17d0fed959a4943f285ab45f4d7ca0d8cd361516bd5d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.6 KB (17590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a83a64038be56c37a81f64b5f9d1e5d87ab8c48be09da50e7190bd55075ff5b2`

```dockerfile
```

-	Layers:
	-	`sha256:308a5410c42ddf2733d526e9683ab2fb69d168d7f79a47499453f4640c44f42b`  
		Last Modified: Wed, 22 Oct 2025 07:43:42 GMT  
		Size: 17.6 KB (17590 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-threaded-bookworm` - linux; ppc64le

```console
$ docker pull perl@sha256:c6d56f6fa9f770955e81074bbca0e9760b97f95c4afc1ea782875f84edd6e82f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **378.3 MB (378343195 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e881a314222e6be98327f5bc20654c6309bfb923ed9c0438e9e5f744670328fe`
-	Default Command: `["perl5.43.2","-de0"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1760918400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 24 Aug 2025 06:40:17 GMT
WORKDIR /usr/src/perl
# Sun, 24 Aug 2025 06:40:17 GMT
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/E/ET/ETHER/perl-5.43.2.tar.gz -o perl-5.43.2.tar.gz     && echo '202dc989a29e461bef175dc23ac0ba0d7eef49ea10e1fefe696f19ede210dc29 *perl-5.43.2.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.43.2.tar.gz -C /usr/src/perl     && rm perl-5.43.2.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.091.tar.gz'     && echo 'c5996e7335912a5c99e06bdb47ff39df309a857cbd8fd2627a021cefdb53cf54 *IO-Socket-SSL-2.091.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.091.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.091* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Sun, 24 Aug 2025 06:40:17 GMT
WORKDIR /usr/src/app
# Sun, 24 Aug 2025 06:40:17 GMT
CMD ["perl5.43.2" "-de0"]
```

-	Layers:
	-	`sha256:297b234228c60cb6a9bc0156bdf582119f3c4f22112d7d2e8128e4d1403158cb`  
		Last Modified: Tue, 21 Oct 2025 00:19:36 GMT  
		Size: 52.3 MB (52326787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c665a6d4e6976a738d68a77f188daf2501160c6ad54e4788282d2395e926b5e6`  
		Last Modified: Tue, 21 Oct 2025 07:42:57 GMT  
		Size: 25.7 MB (25672119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc9014e4879ede8e5983b7a1a0f265054143b5d897d5a848c01fe4c938fdaa27`  
		Last Modified: Tue, 21 Oct 2025 17:30:59 GMT  
		Size: 69.8 MB (69845634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56011ccaf4727bb2311ac874db524178647f03b759d374824a9593362ec2964a`  
		Last Modified: Wed, 22 Oct 2025 01:54:45 GMT  
		Size: 214.5 MB (214489889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed964dd8ec8a02ad2743d3fa0e545f7258c8cc2c77a5bd1105b112aa0f225790`  
		Last Modified: Wed, 22 Oct 2025 05:25:32 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ba108cf4a1a03017d54e280f4bf521e66f164fa647af144987667d12a3cd812`  
		Last Modified: Wed, 22 Oct 2025 07:13:29 GMT  
		Size: 16.0 MB (16008499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aab4530067485e5b0f03f8495f45c2cfed5c2d28cdb1aee041d425206971f1df`  
		Last Modified: Wed, 22 Oct 2025 07:13:26 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-threaded-bookworm` - unknown; unknown

```console
$ docker pull perl@sha256:32adb6d2781d0d715f6ab89607f42def0de5ec8c144192b6e2a891b6b19563f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.9 MB (15862901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc70d9fb316cb8b4c00357d86bd61414eb0e5d951cbde95368158dfb34609acb`

```dockerfile
```

-	Layers:
	-	`sha256:155580c2cf6cd44f613f747ba7b6a4650de7f8632ace133bf9b5f3ae163a539b`  
		Last Modified: Wed, 22 Oct 2025 10:40:44 GMT  
		Size: 15.8 MB (15845116 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1042aedf99376df03e03c0606c13b8293c81bfeb35e3d81f0c59967889b0ce41`  
		Last Modified: Wed, 22 Oct 2025 10:40:45 GMT  
		Size: 17.8 KB (17785 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-threaded-bookworm` - linux; s390x

```console
$ docker pull perl@sha256:a863d58459b8d00f44f5dfb1903bbe496b61175ff465ebe12daea56e77f2a5c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **334.5 MB (334465777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c925e1b0052ef58f975cfd96f2aaa192b6756d18348535082f66d02cc8c7d386`
-	Default Command: `["perl5.43.2","-de0"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1760918400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 24 Aug 2025 06:40:17 GMT
WORKDIR /usr/src/perl
# Sun, 24 Aug 2025 06:40:17 GMT
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/E/ET/ETHER/perl-5.43.2.tar.gz -o perl-5.43.2.tar.gz     && echo '202dc989a29e461bef175dc23ac0ba0d7eef49ea10e1fefe696f19ede210dc29 *perl-5.43.2.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.43.2.tar.gz -C /usr/src/perl     && rm perl-5.43.2.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.091.tar.gz'     && echo 'c5996e7335912a5c99e06bdb47ff39df309a857cbd8fd2627a021cefdb53cf54 *IO-Socket-SSL-2.091.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.091.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.091* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Sun, 24 Aug 2025 06:40:17 GMT
WORKDIR /usr/src/app
# Sun, 24 Aug 2025 06:40:17 GMT
CMD ["perl5.43.2" "-de0"]
```

-	Layers:
	-	`sha256:769a86a44e9ad2fad1b0132047fcc9c080f859777f09d3856b818bc85f1c5895`  
		Last Modified: Tue, 21 Oct 2025 01:19:50 GMT  
		Size: 47.1 MB (47137521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3ca271e8b0e27269a77c65ea555986eaaadf5db02b1ac24f66f8ce2e45a475b`  
		Last Modified: Tue, 21 Oct 2025 22:50:23 GMT  
		Size: 24.0 MB (24027291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:944e6bdda425b877e973cde5b6c8eeabf7eed45bfaba0fd705b4f180a07f001f`  
		Last Modified: Wed, 22 Oct 2025 06:00:23 GMT  
		Size: 63.5 MB (63501423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e7d40c47b93ce5dc5166e5aa44baae913a478ae1ba5f7865fe24556acef9200`  
		Last Modified: Wed, 22 Oct 2025 14:21:48 GMT  
		Size: 183.5 MB (183485270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c2b45647c5eaabb3bc37a1959a8faa49d6ccddd67e9b90f21e7f12d318ff58a`  
		Last Modified: Wed, 22 Oct 2025 18:12:35 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c12b769eefcfedf39dc199a0bf9d87233d307bcc9224de3f9afe397c7d1c90d`  
		Last Modified: Wed, 22 Oct 2025 18:58:57 GMT  
		Size: 16.3 MB (16314004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4c0b390d5b39cfadc34f3c2b29bf6ab0c561cafa1f8397f1366815bc5a1c2c8`  
		Last Modified: Wed, 22 Oct 2025 18:58:55 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-threaded-bookworm` - unknown; unknown

```console
$ docker pull perl@sha256:dc7ded453c90fc29c66bbdb7071de4f9758bf97f79655768d28869a5ec1f5016
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.7 MB (15693950 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7306e47e1397dc79242b9784a786076fa8adddb999f38c1a46617057ecb9e049`

```dockerfile
```

-	Layers:
	-	`sha256:f437d42e4a2a19f44719f8f3842ac0cf4a69a4e98cf3c8769c1c0002301db803`  
		Last Modified: Wed, 22 Oct 2025 19:41:48 GMT  
		Size: 15.7 MB (15676203 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:458f0470efded1b5c7410047c9a3a267106a4f5e409e93ed62af9a7f7f7ef608`  
		Last Modified: Wed, 22 Oct 2025 19:41:49 GMT  
		Size: 17.7 KB (17747 bytes)  
		MIME: application/vnd.in-toto+json
