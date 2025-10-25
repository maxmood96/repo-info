## `perl:devel-threaded-bookworm`

```console
$ docker pull perl@sha256:0630fe70f613de2ffa1b9e13cafbf26f368999bb93e3dd06092d9248de6f3c0e
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
$ docker pull perl@sha256:de9836e2729e7162aa3219a7f4c17644411d432bd1383f36fc3bebc7dbb2813c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **364.4 MB (364440655 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd9b4f847aaf9608982c8dc33625dc63fbb7268dceb06e910899748994cbc990`
-	Default Command: `["perl5.43.4","-de0"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1760918400'
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
	-	`sha256:fe1bb01113bf96177b354eb9a4a97be13af787e8a302fbae85adfbbb4749d379`  
		Last Modified: Fri, 24 Oct 2025 19:47:56 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1194b923bdea5e8f961e0d7bc61865db4e7aa73b608cba6cca5f0f11bffb1582`  
		Last Modified: Fri, 24 Oct 2025 19:47:58 GMT  
		Size: 16.1 MB (16084588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a6e542b711c56e9fddb4af5bfc26debeb8782b3441ec6df98f460088413a2c8`  
		Last Modified: Fri, 24 Oct 2025 19:47:56 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-threaded-bookworm` - unknown; unknown

```console
$ docker pull perl@sha256:884be575bb73442a6ef94d4e66efc48b90b9f271056f758790fe958f6d8bfc03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.9 MB (15886355 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b44b78ae6ce745091afd87735179f65ff2dced9f6fb7dc2bae77711c48aeb7ae`

```dockerfile
```

-	Layers:
	-	`sha256:3e15208f7e1675a417301102f0af1efede8c97d381e161ab1e824db5f5cfc764`  
		Last Modified: Fri, 24 Oct 2025 22:48:14 GMT  
		Size: 15.9 MB (15868605 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:afc06dc4a81a34f1daf94f5787282e718643e31e6eca20fea9a8d99bdcbff172`  
		Last Modified: Fri, 24 Oct 2025 22:48:15 GMT  
		Size: 17.8 KB (17750 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-threaded-bookworm` - linux; arm variant v5

```console
$ docker pull perl@sha256:06c9f205965633f736bf9371e6bdca5b4304180678504b94413cfff7c45c74ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **330.8 MB (330770660 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:955a81c6ae53cf436668c368f431159f247f6267012823a501b2513e6f7eecd9`
-	Default Command: `["perl5.43.4","-de0"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1760918400'
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
	-	`sha256:6bd6a25b2c14693a32761826d00353fb027e4461f37acd9ff5c43a29e45584b6`  
		Last Modified: Fri, 24 Oct 2025 19:22:35 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3925177182a0fea81417bbafeaba7edf356bdda8b864e948eae24fed62789f92`  
		Last Modified: Fri, 24 Oct 2025 19:22:37 GMT  
		Size: 15.3 MB (15339793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00ac97d7c35fe0f4c768a2ede91cadc2891487c7b2b983df79c7a8c64915dff2`  
		Last Modified: Fri, 24 Oct 2025 19:22:35 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-threaded-bookworm` - unknown; unknown

```console
$ docker pull perl@sha256:773ba1c08706ac5ade50e74975b08f3611aa78d7d2a609300730d2a6c1ef3c06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.7 MB (15683419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:daa60c58d701b0dec22b209b8f63ade9aba6a7ea52cfbbd4aae7c7b408ab1e56`

```dockerfile
```

-	Layers:
	-	`sha256:d909ebecef87e21b3aa2e6b9b01671a820579caaa782cdb9b684ff544581ebc8`  
		Last Modified: Fri, 24 Oct 2025 22:48:31 GMT  
		Size: 15.7 MB (15665597 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2d835f6ba6b17f0f425205866ed15bf65a086844a514db92d3c5ef53b0947352`  
		Last Modified: Fri, 24 Oct 2025 22:48:32 GMT  
		Size: 17.8 KB (17822 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-threaded-bookworm` - linux; arm variant v7

```console
$ docker pull perl@sha256:38b5419a4bf979337fa3feb778dd5ff77e8c117566dba4205132bbe027e9c4d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **316.3 MB (316264474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28846111a9a02fc75844ad0de95585493434edf5ef530e9b44cfe13e1f7e9ef7`
-	Default Command: `["perl5.43.4","-de0"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1760918400'
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
	-	`sha256:e5ec87983693368c6340d1fc078cbfc8655f9d7c5f8638c8b8b67d89189b0e42`  
		Last Modified: Fri, 24 Oct 2025 20:36:23 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:482ca5ac53873b45d0c0804c4b7399312717a4c38fa42ab028a46b5c18710015`  
		Last Modified: Fri, 24 Oct 2025 20:36:26 GMT  
		Size: 15.1 MB (15126097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3cd325cc03e1bbdbd7de7c14dd76c852508a41c2ebe7901aa249b42d5de3bc4`  
		Last Modified: Fri, 24 Oct 2025 20:36:23 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-threaded-bookworm` - unknown; unknown

```console
$ docker pull perl@sha256:e252332d8167b791864a385016d3717479e2de713dcd6ddc49f20b09dee4e263
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.7 MB (15688895 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6268e78659bb3926e8f5c798927318acf12d5f126303ffab575c32bab11b85f8`

```dockerfile
```

-	Layers:
	-	`sha256:0d93d917b1e2b42dc0127ecb4bd6271877c00cb2154311b7aede5f9adca4bd49`  
		Last Modified: Fri, 24 Oct 2025 22:48:46 GMT  
		Size: 15.7 MB (15671073 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e944caa7db18aea7a4ac3e92fbb5b3f046bcbaee15bb13c35a179aba062af992`  
		Last Modified: Fri, 24 Oct 2025 22:48:47 GMT  
		Size: 17.8 KB (17822 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-threaded-bookworm` - linux; arm64 variant v8

```console
$ docker pull perl@sha256:66a371a79272e33a4aedbbbeca707117026df3f737e0241fc54f18092d5c4604
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **355.3 MB (355325648 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b6f38d048f0b5cd358e32eff5148db01117803ea34f12ddeee4d597aaec3f0a`
-	Default Command: `["perl5.43.4","-de0"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1760918400'
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
	-	`sha256:b87a45b39b6627b88248aad46b1f050ee81e7417a7021401b8c28b4ee5d984f6`  
		Last Modified: Fri, 24 Oct 2025 19:43:01 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:649c1b3757561d1d1a6dfdb261ceb220fc9ea02383551b3f2f6205d9ad7699a5`  
		Last Modified: Fri, 24 Oct 2025 19:43:03 GMT  
		Size: 16.0 MB (16038779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5230679fb6127bca3aeee3aa26051469f595686212381c9815063f14f6fc825a`  
		Last Modified: Fri, 24 Oct 2025 19:43:01 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-threaded-bookworm` - unknown; unknown

```console
$ docker pull perl@sha256:a4b63e1d90e677da52673c023a8cfc56bbc4eef752ae9485ebe8aabe20f920b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.9 MB (15914961 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a38624a5beaae87461eb51041665807665745dc809f2bfe2cc37911900c265b`

```dockerfile
```

-	Layers:
	-	`sha256:5232ea9839b5068dba45d081eb9bfb49be013d1dfbd6b995a3263af1a6788e3a`  
		Last Modified: Fri, 24 Oct 2025 22:49:01 GMT  
		Size: 15.9 MB (15897119 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:27dde1b2762a31707a56605b6ad8972f6ad5dc5924e951728f524d9417da2eb2`  
		Last Modified: Fri, 24 Oct 2025 22:49:02 GMT  
		Size: 17.8 KB (17842 bytes)  
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
$ docker pull perl@sha256:652eccc678d3eab3d5358fe5eeacb1453705290898bb317c1fabf7d6d6837399
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **341.2 MB (341208526 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0169aaf1bd2eed90eac7f4660577634204989aae42e39243a0d2792ef480ac84`
-	Default Command: `["perl5.43.4","-de0"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1760918400'
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
	-	`sha256:9d9c20388b6d870521bb6440d39c2724cecb2559bc2d7051e5e606e16669cd34`  
		Last Modified: Fri, 24 Oct 2025 22:14:59 GMT  
		Size: 15.3 MB (15303124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5364a197ce5b6218041834c9806cf3d68c283311306e84a27fb775bf8f14d05`  
		Last Modified: Fri, 24 Oct 2025 22:14:58 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-threaded-bookworm` - unknown; unknown

```console
$ docker pull perl@sha256:65748c5684b38de076931967db9f0077223f89b1abf2c6467f91776489d39826
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.6 KB (17592 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d27828e6ddc552d6ff7ea1f85b3e206b73fe6a0a8375485837d34808a6c7a9f1`

```dockerfile
```

-	Layers:
	-	`sha256:e2fa5ab1c5040d46d60d525146df46e8443efbd1b4b948d752a01c0324b99c8a`  
		Last Modified: Sat, 25 Oct 2025 01:44:16 GMT  
		Size: 17.6 KB (17592 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-threaded-bookworm` - linux; ppc64le

```console
$ docker pull perl@sha256:0d5e9b17c319c6d32392f50a47c0314355c2cb97d1e2a5fa09a8c8b1775da78d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **378.5 MB (378457522 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e2d239fe0d6100124e694a9cc623b2cdd0c7c211051264aca6db39e27a4c2e5`
-	Default Command: `["perl5.43.4","-de0"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1760918400'
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
	-	`sha256:9e5742218b40ff47e0c0037fa01cf1b17dbd8185020a846606a16343e1e06fca`  
		Last Modified: Sat, 25 Oct 2025 01:21:43 GMT  
		Size: 16.1 MB (16122826 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f19fccd1d049014c95794f16f1505272d02341603ce2a9899107d64396e36c7`  
		Last Modified: Sat, 25 Oct 2025 01:21:42 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-threaded-bookworm` - unknown; unknown

```console
$ docker pull perl@sha256:90cfa45c1a905e2bcb558663697aba0347f3628ba6a4d43bcb215c36a249aa72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.9 MB (15862903 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9308ae8ab790c55fece3fb23cbc692ed8d5df8977634533a32e2297eb169e77d`

```dockerfile
```

-	Layers:
	-	`sha256:b2727b7953497bc651d172e75b3b9fe8e6bbab58d3cd854c09e569b3265328ea`  
		Last Modified: Sat, 25 Oct 2025 04:40:58 GMT  
		Size: 15.8 MB (15845116 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:473a9ccb97116dcc809a066af0078bd6155e80c6140310d3a4fd233716e1bad2`  
		Last Modified: Sat, 25 Oct 2025 04:40:59 GMT  
		Size: 17.8 KB (17787 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-threaded-bookworm` - linux; s390x

```console
$ docker pull perl@sha256:1d379d0c605e137e4fb6cf672ba24b8a865b6cf2cb03578e7705fc159dd053d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **334.6 MB (334582948 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8cd1db7d1f515e35d0a35d433259973071ec07c64affbf81642b1a29a8b524f8`
-	Default Command: `["perl5.43.4","-de0"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1760918400'
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
	-	`sha256:4e0df75b17f647ce7d55bc8b7bf4696bae115f1b08e9efba2c717f7aa46613e7`  
		Last Modified: Sat, 25 Oct 2025 00:29:34 GMT  
		Size: 16.4 MB (16431176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb053f09a7a2f3de3d81ee9bc942e44498e6d5752c42e2e7c9ce6906b1a1b5cc`  
		Last Modified: Sat, 25 Oct 2025 00:29:32 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-threaded-bookworm` - unknown; unknown

```console
$ docker pull perl@sha256:ea938a25de28b24fd417909661606bc5f65e58d606d8887cf03887cb805bb1cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.7 MB (15693953 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eff28f128e7c3faf6b285bdd8c4ee279e03864690d4b52156b389ca4380175dd`

```dockerfile
```

-	Layers:
	-	`sha256:503f0dcbde23a55292b466b67f2e4494b0953f7bd36c2d4e0b787a9182009b9c`  
		Last Modified: Sat, 25 Oct 2025 01:44:30 GMT  
		Size: 15.7 MB (15676203 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3cc98c3f1ae83eff0f38a223471a17ace7941fcbf2103879d2bc48ad7936e4ee`  
		Last Modified: Sat, 25 Oct 2025 01:44:30 GMT  
		Size: 17.8 KB (17750 bytes)  
		MIME: application/vnd.in-toto+json
