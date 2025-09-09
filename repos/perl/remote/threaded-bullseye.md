## `perl:threaded-bullseye`

```console
$ docker pull perl@sha256:a8278900e266fcebf6457d69dd71512af99490f384d71ea0211af5a8dacc7a90
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

### `perl:threaded-bullseye` - linux; amd64

```console
$ docker pull perl@sha256:137b4a282bbd4dfa16c77cd129c56c3b0b347698d5748675191847b57b73464c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **337.4 MB (337362326 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf1c2b7fb84b1a0d1eceaee5b42208a7176526933c8fe198c7dbfe07ed2e4d33`
-	Default Command: `["perl5.42.0","-de0"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1757289600'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 24 Aug 2025 06:40:17 GMT
WORKDIR /usr/src/perl
# Sun, 24 Aug 2025 06:40:17 GMT
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/B/BO/BOOK/perl-5.42.0.tar.gz -o perl-5.42.0.tar.gz     && echo 'e093ef184d7f9a1b9797e2465296f55510adb6dab8842b0c3ed53329663096dc *perl-5.42.0.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.42.0.tar.gz -C /usr/src/perl     && rm perl-5.42.0.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.091.tar.gz'     && echo 'c5996e7335912a5c99e06bdb47ff39df309a857cbd8fd2627a021cefdb53cf54 *IO-Socket-SSL-2.091.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.091.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.091* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Sun, 24 Aug 2025 06:40:17 GMT
WORKDIR /usr/src/app
# Sun, 24 Aug 2025 06:40:17 GMT
CMD ["perl5.42.0" "-de0"]
```

-	Layers:
	-	`sha256:035115815e46101f9c9956e02e706f2f3ec8748e2b415f0d232b51eb76a6a779`  
		Last Modified: Mon, 08 Sep 2025 21:12:56 GMT  
		Size: 53.8 MB (53755396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aebbe40dd6978ce6b51e9d84d91a658eb2959635aec29cb2475587fda81e28d1`  
		Last Modified: Mon, 08 Sep 2025 21:54:22 GMT  
		Size: 15.8 MB (15765345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b969d43370836ef53860df2c53e721ccfdd06653f3db3f7100570314bf509d12`  
		Last Modified: Mon, 08 Sep 2025 22:13:40 GMT  
		Size: 54.8 MB (54757246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c6412c7204557d8c521d4b9da4c0a744f9cd8038936537301a90b9395815640`  
		Last Modified: Mon, 08 Sep 2025 22:39:07 GMT  
		Size: 197.1 MB (197146531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:129eeee85ec2b25ebbd4eba1d893585760d296e541b50cdb8c87177dd621d735`  
		Last Modified: Mon, 08 Sep 2025 23:21:27 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca2dd9610e0f50333da97c9b17869e473aaed46d5a7d9d5f5435dde0908c8629`  
		Last Modified: Tue, 09 Sep 2025 02:40:00 GMT  
		Size: 15.9 MB (15937542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf1720f60b3513ebafa8ba59d6f5910ad6bc5c0e4842edc1a3f394a42013942a`  
		Last Modified: Mon, 08 Sep 2025 23:21:30 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:threaded-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:2533ae9ac54d18bd03ea5108caf3a29546f0b0db1d865cd6bd914479afeb81a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15482654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:863b39bb35acf0f7d9565bea76c4813d45a72082ee484181b124f7050c9c5dab`

```dockerfile
```

-	Layers:
	-	`sha256:2d2e80226c26b936a850e5917978f82318773be21a54f650f6ca21e749f6a32c`  
		Last Modified: Tue, 09 Sep 2025 01:38:45 GMT  
		Size: 15.5 MB (15464344 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a3052ab6d8d0ab812d767b946c3f51c98f2832806a59595d99d378e3ea7e22b7`  
		Last Modified: Tue, 09 Sep 2025 01:38:46 GMT  
		Size: 18.3 KB (18310 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:threaded-bullseye` - linux; arm variant v7

```console
$ docker pull perl@sha256:9fbea56ef5f7ef7c797bfd093283be30fa94f236f6acaf0ecbee6bbce8835954
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.1 MB (297140234 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:545660c7bc594434059e3d6e6869077591b7992edbd19c938c00536d5bbe6524`
-	Default Command: `["perl5.42.0","-de0"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1754870400'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 17 Aug 2025 07:01:39 GMT
WORKDIR /usr/src/perl
# Sun, 17 Aug 2025 07:01:39 GMT
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/B/BO/BOOK/perl-5.42.0.tar.gz -o perl-5.42.0.tar.gz     && echo 'e093ef184d7f9a1b9797e2465296f55510adb6dab8842b0c3ed53329663096dc *perl-5.42.0.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.42.0.tar.gz -C /usr/src/perl     && rm perl-5.42.0.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.091.tar.gz'     && echo 'c5996e7335912a5c99e06bdb47ff39df309a857cbd8fd2627a021cefdb53cf54 *IO-Socket-SSL-2.091.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.091.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.091* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Sun, 17 Aug 2025 07:01:39 GMT
WORKDIR /usr/src/app
# Sun, 17 Aug 2025 07:01:39 GMT
CMD ["perl5.42.0" "-de0"]
```

-	Layers:
	-	`sha256:27a0e70a6a342a82d61d13664b90c890c24d71590db74ef7eb6f4dc1b731387c`  
		Last Modified: Tue, 12 Aug 2025 20:46:51 GMT  
		Size: 49.0 MB (49044404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ae3c82b80881167fea789bb8cf043d4de732e7b062431e2c261928679dcd3b3`  
		Last Modified: Wed, 13 Aug 2025 00:15:42 GMT  
		Size: 14.9 MB (14880786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99e7e2d995d706697c0af2f117145d4dbab9dacbc5f34e7d500b3d99b0062c6f`  
		Last Modified: Wed, 13 Aug 2025 06:47:54 GMT  
		Size: 50.6 MB (50632440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1442f1d0f4f434d42cc2cb968a36d89906e276d8e6a54625dc785435cff2500b`  
		Last Modified: Wed, 13 Aug 2025 13:54:09 GMT  
		Size: 167.6 MB (167590147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb4f638a5e4b6e665f24ec4190333dad8d705291c7a674036b4b20e6fb5e192a`  
		Last Modified: Wed, 13 Aug 2025 22:20:56 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32b172d7d810ff3b9de3c51d28066bd52f1ec4742de2d62b9960a80c78d5799e`  
		Last Modified: Mon, 18 Aug 2025 18:55:03 GMT  
		Size: 15.0 MB (14992188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2642573af2d373f22e9fc69beb96a8de7cee88e1d998aae5de0f842ec2ffa60e`  
		Last Modified: Mon, 18 Aug 2025 18:55:01 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:threaded-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:5a3e5bb5cd324e0784fbabd3bbcba9262a349f5df362ee4c542af38cf52a9045
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15282081 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13b8e97cb25dca120c6b9015b390b116b570b3b1439b71cdbf7670e0a6cabcb4`

```dockerfile
```

-	Layers:
	-	`sha256:13823e16486e8b95784af3abb366784f08b6a0e66787851056922bb7376df604`  
		Last Modified: Mon, 18 Aug 2025 19:41:21 GMT  
		Size: 15.3 MB (15263686 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e769c4ebc9369803a10b4d479ef544f31564a110d516859874e4b51fedaaac5e`  
		Last Modified: Mon, 18 Aug 2025 19:41:22 GMT  
		Size: 18.4 KB (18395 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:threaded-bullseye` - linux; arm64 variant v8

```console
$ docker pull perl@sha256:f43b07c03343967c80bf956eab73884616f8a2762a26e834b0e19bec4be106d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **328.8 MB (328753669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21c5351825d2c127456ba7038f14368054a314aa83d0c3c6f90e19f3f5edd38e`
-	Default Command: `["perl5.42.0","-de0"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1757289600'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 24 Aug 2025 06:40:17 GMT
WORKDIR /usr/src/perl
# Sun, 24 Aug 2025 06:40:17 GMT
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/B/BO/BOOK/perl-5.42.0.tar.gz -o perl-5.42.0.tar.gz     && echo 'e093ef184d7f9a1b9797e2465296f55510adb6dab8842b0c3ed53329663096dc *perl-5.42.0.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.42.0.tar.gz -C /usr/src/perl     && rm perl-5.42.0.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.091.tar.gz'     && echo 'c5996e7335912a5c99e06bdb47ff39df309a857cbd8fd2627a021cefdb53cf54 *IO-Socket-SSL-2.091.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.091.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.091* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Sun, 24 Aug 2025 06:40:17 GMT
WORKDIR /usr/src/app
# Sun, 24 Aug 2025 06:40:17 GMT
CMD ["perl5.42.0" "-de0"]
```

-	Layers:
	-	`sha256:7df02cb4a974a4e8a9eb65ffcff7274f9dca341d29aaa763294c42e49805ca19`  
		Last Modified: Mon, 08 Sep 2025 21:15:41 GMT  
		Size: 52.2 MB (52248370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32c26dea2f52a9cb0633591a828e9fd53a32d89290a8c2b4b5d5286f76f5332d`  
		Last Modified: Mon, 08 Sep 2025 22:20:05 GMT  
		Size: 15.8 MB (15750666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3b8f2ae237d2864fee9f12b950708d56b6e76bc6595e309bb307eade128f989`  
		Last Modified: Tue, 09 Sep 2025 02:13:06 GMT  
		Size: 54.9 MB (54855949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f44207777d295a97c712d1b0b80ae39856817d02533603ebe80cfadca571ebfa`  
		Last Modified: Tue, 09 Sep 2025 03:12:10 GMT  
		Size: 190.1 MB (190058398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85ffaa04cf3f0bd25b8b71a8e18cbcbc23eec4ea4cec9e573201d63ea08f8ad8`  
		Last Modified: Tue, 09 Sep 2025 05:15:24 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61d1f147b6f66edf73753460fca37b5881b9b4755b412d5a4930e396ad0a05f5`  
		Last Modified: Tue, 09 Sep 2025 07:38:41 GMT  
		Size: 15.8 MB (15840019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faf7251cb9b298c8b38055c65f43dd29c4c4c275171f372bcd4a40fccc2b4fda`  
		Last Modified: Tue, 09 Sep 2025 05:15:26 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:threaded-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:c1684b9bfb68fd9d91950063f3c59dfccb76c0762e8d53848602df93d56fcc3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15484751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97319344274481098a2d09b67127278351392c07dcc90fd3bb978451fc41be40`

```dockerfile
```

-	Layers:
	-	`sha256:60dd0e2ae9c92a0b38427bc6ae67405eca261e99c3f02f63243f569ee568350b`  
		Last Modified: Tue, 09 Sep 2025 07:38:39 GMT  
		Size: 15.5 MB (15466325 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b4cd9fc9bd40401df8fba7deb91d5d96752879cbedfc9584a9d62bb2a110be99`  
		Last Modified: Tue, 09 Sep 2025 07:38:41 GMT  
		Size: 18.4 KB (18426 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:threaded-bullseye` - linux; 386

```console
$ docker pull perl@sha256:7f76a651919cd367ec161cec2c924a068e829da743d905f9dc2fdedc40bee4f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **342.5 MB (342532579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a8b07894b15413bacfe17577ab74b253c2ff7df33857f95391fe464f9cbaef3`
-	Default Command: `["perl5.42.0","-de0"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1757289600'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 24 Aug 2025 06:40:17 GMT
WORKDIR /usr/src/perl
# Sun, 24 Aug 2025 06:40:17 GMT
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/B/BO/BOOK/perl-5.42.0.tar.gz -o perl-5.42.0.tar.gz     && echo 'e093ef184d7f9a1b9797e2465296f55510adb6dab8842b0c3ed53329663096dc *perl-5.42.0.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.42.0.tar.gz -C /usr/src/perl     && rm perl-5.42.0.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.091.tar.gz'     && echo 'c5996e7335912a5c99e06bdb47ff39df309a857cbd8fd2627a021cefdb53cf54 *IO-Socket-SSL-2.091.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.091.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.091* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Sun, 24 Aug 2025 06:40:17 GMT
WORKDIR /usr/src/app
# Sun, 24 Aug 2025 06:40:17 GMT
CMD ["perl5.42.0" "-de0"]
```

-	Layers:
	-	`sha256:21d761bd0e7544a956d2e6eb27c7a89e081fa93136574d1836ddae535c60eb08`  
		Last Modified: Mon, 08 Sep 2025 21:20:56 GMT  
		Size: 54.7 MB (54690513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0956db1fbb0de06709cacad88eee1a92edcd3eb326031290d4f6e321e68d7c6d`  
		Last Modified: Mon, 08 Sep 2025 21:55:16 GMT  
		Size: 16.3 MB (16268970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8151bbc2095026ddf31b19dbad5daa6653efd5a630af32432a4736a4ce7bc56`  
		Last Modified: Mon, 08 Sep 2025 22:13:43 GMT  
		Size: 56.1 MB (56050010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bf0f4fdfc6cc8075bf66208e6134f6010af73c42995332cfaabb80108c050da`  
		Last Modified: Mon, 08 Sep 2025 22:40:00 GMT  
		Size: 200.0 MB (200047763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5590aec368dfd5894211107bea8a266820be5cabf553189a65478660bf2e7ad`  
		Last Modified: Mon, 08 Sep 2025 23:17:08 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:088637916f3572646b603105b8ecf74aa8133a6afc7b8cb7d395e42bdc016ca1`  
		Last Modified: Tue, 09 Sep 2025 07:38:40 GMT  
		Size: 15.5 MB (15475057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaa375e16f1791a4fb7f5560522a9f2acf4d357602567e5a23f121398670ffa1`  
		Last Modified: Mon, 08 Sep 2025 23:17:12 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:threaded-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:1db314a7b1f1ae54961cd795bdbf4dab7ff703366fd5edf3c35797231a821c5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15470618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9589ccd5d5e781e4c1cc7584640c31ba6613d14451a1ba36795521a911c812ba`

```dockerfile
```

-	Layers:
	-	`sha256:8e8671173d2cde8a8ae5d27baa5ab28bb9df4d00c594f7ebd1c7e49e98924a26`  
		Last Modified: Tue, 09 Sep 2025 01:39:25 GMT  
		Size: 15.5 MB (15452344 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e1f572dc99bf95ab0dd769d8b300654957aa2e5199db6e7ecab395c83a99df06`  
		Last Modified: Tue, 09 Sep 2025 01:39:26 GMT  
		Size: 18.3 KB (18274 bytes)  
		MIME: application/vnd.in-toto+json
