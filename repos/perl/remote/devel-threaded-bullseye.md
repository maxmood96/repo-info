## `perl:devel-threaded-bullseye`

```console
$ docker pull perl@sha256:d476308d0893d7ff912ea8c481d029a9241fa57d1935eeb026e4c935f11f3caf
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `perl:devel-threaded-bullseye` - linux; amd64

```console
$ docker pull perl@sha256:176548c06a65c0e984a5fcf4ff7cd62a1f7e4e1308a752456bc09b8172d26c15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **337.4 MB (337439510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9265ccf60c325191ff690f6cb7d189e60aff9a6f15ec0828fa4315621e6cc5b`
-	Default Command: `["perl5.43.2","-de0"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1760918400'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
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
	-	`sha256:b6f830cd306f01980373f1e0120f2d00018fbe51a9506b7262f5d9e4bbda74f9`  
		Last Modified: Tue, 21 Oct 2025 00:19:19 GMT  
		Size: 53.8 MB (53756115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cfa9ab09db8d94503213f634b29be3505174979f2e0c6e3fd46c2acc0716c25`  
		Last Modified: Tue, 21 Oct 2025 04:46:42 GMT  
		Size: 15.8 MB (15764056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e663cb3204c49ebc21b005f5976ee62e4f00b632aaa8000dbe6db86d9cde2a1`  
		Last Modified: Tue, 21 Oct 2025 04:47:30 GMT  
		Size: 54.8 MB (54755162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bafbf91825be17f2ceae6674de95a31e6f8a5a24c7cb95ae123d19de9c63e61`  
		Last Modified: Tue, 21 Oct 2025 10:22:52 GMT  
		Size: 197.2 MB (197204867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d590f57e3661d3534934a98327c7075a06c8dfb8419f0962548731d25aceec60`  
		Last Modified: Tue, 21 Oct 2025 11:28:22 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c65f7bc1a3f4bfd80f44ae80c833360243d2b684f0de72f31e6d6289caa813a4`  
		Last Modified: Tue, 21 Oct 2025 11:42:52 GMT  
		Size: 16.0 MB (15959044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f07edc536305da44079c8fc42c41d5e02f864f011c3634f206210c670fd4278`  
		Last Modified: Tue, 21 Oct 2025 11:42:51 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-threaded-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:3dfaf5c7e8872dd99b886bcd673465801d17bce0e3d1df739b091c21f8eb3d5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15481454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:077e6959053a6855cfe5e3e8c52fad1a96cb806653abb8affa5a76534edda1d0`

```dockerfile
```

-	Layers:
	-	`sha256:502da7747d2eb1f1fe523cd77226f6640ffaf87295718eb17b95bf060af6ad1e`  
		Last Modified: Tue, 21 Oct 2025 13:43:16 GMT  
		Size: 15.5 MB (15463706 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:964d34bd69d3dfeaea048154175ddc70bbfebdbe3f75885454d69ea5bd07d984`  
		Last Modified: Tue, 21 Oct 2025 13:43:17 GMT  
		Size: 17.7 KB (17748 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-threaded-bullseye` - linux; arm variant v7

```console
$ docker pull perl@sha256:cc8660f2fd335822153caa598c23903df093fd930e442ad9049fb2f709dd31f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.5 MB (297539299 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae8c95abedabe50d68d16385a3001e1ffd0256fda425ce830d495ecb140fb9f5`
-	Default Command: `["perl5.43.2","-de0"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1760918400'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
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
	-	`sha256:680ed921e0c94a719af1d242eac2d0c1be8482153680a3940f3435ee5598303a`  
		Last Modified: Tue, 21 Oct 2025 00:20:24 GMT  
		Size: 49.0 MB (49046121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30c68013a317d7d802bb25c57a724c8753caec2fc7f0e78fc13f9a38fd22ecd4`  
		Last Modified: Tue, 21 Oct 2025 02:44:25 GMT  
		Size: 14.9 MB (14879264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:895fddf2807e047e5b02e5418fd04d343d3e9b5b393b2f3f0cd6704cad44b8f0`  
		Last Modified: Tue, 21 Oct 2025 04:10:49 GMT  
		Size: 50.6 MB (50628495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69ef331acdad14a3d1bfe859a1c645cb9f4b9526e16e3fed550eee6b86681db7`  
		Last Modified: Tue, 21 Oct 2025 06:17:35 GMT  
		Size: 168.0 MB (167976463 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2fc94b188cc3708829b7e07ca4b83e802c7d51bbfbd30b263ffd402a04f7592`  
		Last Modified: Tue, 21 Oct 2025 06:30:39 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfa4eafe49809960a3da207279fdff67270e3c2219b05fb059ddcffa83f7090a`  
		Last Modified: Tue, 21 Oct 2025 06:48:33 GMT  
		Size: 15.0 MB (15008689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fe8845d375798c80b94bb77b60016b82bc379c080e0401ce00666d2517fb755`  
		Last Modified: Tue, 21 Oct 2025 06:48:32 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-threaded-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:04f0393423eb6c1110e56d30136cc6e0d257ac4201123f47996ae16ad5431fc6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15280851 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b01b204255a37458b70808c7fcd9ea0a091f4c07cb0b3498ff6c845880abb50`

```dockerfile
```

-	Layers:
	-	`sha256:f30f551d1ea00ea8b3c2e6c961a540246c1139308c0d4d973727fe5c739f23c4`  
		Last Modified: Tue, 21 Oct 2025 10:50:34 GMT  
		Size: 15.3 MB (15263032 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:deace2f200de517e75f8b6be0f91677c919215f9970ba6ab5169d020cb3ded9f`  
		Last Modified: Tue, 21 Oct 2025 10:50:35 GMT  
		Size: 17.8 KB (17819 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-threaded-bullseye` - linux; arm64 variant v8

```console
$ docker pull perl@sha256:e385fe647305e93b6827383a6a9ffb420df9f399cf1cf987bef7abf736529f29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **328.8 MB (328822235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75677ea85bd8f9ec558dbdddb6d6305de122fefa24776d249cb8bed1c93f5b44`
-	Default Command: `["perl5.43.2","-de0"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1760918400'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
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
	-	`sha256:0a72c4e347b74aa6a0086cf3d1d928528ab02577a17bff4e22366a7df681f564`  
		Last Modified: Tue, 21 Oct 2025 00:19:19 GMT  
		Size: 52.3 MB (52257444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57f7bdca064e682157394f36dabd112bc9831aff9743216b035e2ccccf704cc3`  
		Last Modified: Tue, 21 Oct 2025 01:46:24 GMT  
		Size: 15.7 MB (15749510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecc7a49f7691cb1ac5f0f40edbe6f4beec62021b4fd2544c431d8f694b4b4647`  
		Last Modified: Tue, 21 Oct 2025 02:35:21 GMT  
		Size: 54.9 MB (54860806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0452b809e62b80ba90b1a217898e5cf7675ff6aac67b2967e58600172590649e`  
		Last Modified: Tue, 21 Oct 2025 04:14:12 GMT  
		Size: 190.1 MB (190097178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c43eadeda9f9ce33113c841d3debd55c6bf46d4b61d8214d2f19cf9207a84a27`  
		Last Modified: Tue, 21 Oct 2025 04:44:16 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f02f95291c7db8ee96c8c2f3c2cda9bdd8dad121b74f95e5dce173385912afa`  
		Last Modified: Tue, 21 Oct 2025 04:44:17 GMT  
		Size: 15.9 MB (15857034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ead0f474895823546c09871bec8bc9617552a03478d4ca4d0104e4faadbc348`  
		Last Modified: Tue, 21 Oct 2025 04:44:16 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-threaded-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:4ba22f52fe8a2c29b31c934b52b757b44e7dd06dbc3bd8396b29b1a5f44732d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15483503 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b0b23906b94d7c065db60f229232766863ca02c35215e1fbec155066d216daa`

```dockerfile
```

-	Layers:
	-	`sha256:fb52ce29cf59412001de01f256725c8047cd2b32e4c2951bf9bf420a96389309`  
		Last Modified: Tue, 21 Oct 2025 10:50:47 GMT  
		Size: 15.5 MB (15465663 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fa6c6b47a06c6d5146ce95259970c76c6cf0dd648d41668585519375cbe986cd`  
		Last Modified: Tue, 21 Oct 2025 10:50:48 GMT  
		Size: 17.8 KB (17840 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-threaded-bullseye` - linux; 386

```console
$ docker pull perl@sha256:09e2c6dd86b94a1b3f44e7d6e59d131d5ef202bd520f2e83e4c51ed7146b622a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **342.6 MB (342608755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71d0de35110f69794363ef358e51b0bbb37e555871abde892158e79ff25be3a3`
-	Default Command: `["perl5.43.2","-de0"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1760918400'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
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
	-	`sha256:10d430deaa3d2ab4898db053e80d62403503897839bf6efd17ed5412b18d7973`  
		Last Modified: Tue, 21 Oct 2025 00:20:39 GMT  
		Size: 54.7 MB (54699294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c453fe6b4c7a680d5464137a3450d263e01a7ec4d491659295432d36b0198bbc`  
		Last Modified: Tue, 21 Oct 2025 01:53:19 GMT  
		Size: 16.3 MB (16267847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96adc169c4af311ffba07fa68db5821d6b9b00d285e00f44dad87eff52496658`  
		Last Modified: Tue, 21 Oct 2025 02:35:42 GMT  
		Size: 56.0 MB (56048779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bd845a5707f187f6670f0831bc55034f6333f3aa3eede705f688f3c3342392e`  
		Last Modified: Tue, 21 Oct 2025 04:14:36 GMT  
		Size: 200.1 MB (200103484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4c5bdfcf439a7f2c7d41bebec6990eea4e046d9703f784ab417048ff8e6afd2`  
		Last Modified: Tue, 21 Oct 2025 04:22:53 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76ec96e703c6a7506d0cebacf377bd13e7031e64e9b30fd380e7f9304caa82ae`  
		Last Modified: Tue, 21 Oct 2025 04:28:15 GMT  
		Size: 15.5 MB (15489086 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dc98c74e2ed999df72415d4ee215240f319989bb943d70819740c611c803cf3`  
		Last Modified: Tue, 21 Oct 2025 04:28:15 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-threaded-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:2f3575430bd42903ce84dc0e54135813b940a13000934587d283505836e7b79b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15469437 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2b2df49d8948cedc2c89bfc5174f4f23636c2111629559dc0379b19a6d73fbf`

```dockerfile
```

-	Layers:
	-	`sha256:6071094f943fac10d6b7b7cc7048b3fd57650e04bea90cc10a9823150f85b5b2`  
		Last Modified: Tue, 21 Oct 2025 10:51:00 GMT  
		Size: 15.5 MB (15451716 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8f0c6a8653bd1f9203b903ef100fd963841861dd0a89d78874b91984618d6d30`  
		Last Modified: Tue, 21 Oct 2025 10:51:01 GMT  
		Size: 17.7 KB (17721 bytes)  
		MIME: application/vnd.in-toto+json
