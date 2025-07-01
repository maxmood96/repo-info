## `perl:devel-threaded-bullseye`

```console
$ docker pull perl@sha256:6a5fb51ed5780a81d603b62c83346a2e37a2553f59cf8d20dc1ddb688e9192f7
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
$ docker pull perl@sha256:2a6015df6b88cb3799574bfbffa2bd0d54a3fda7bb5536d0d9715b556be8e0eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **337.3 MB (337347350 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86e0ee401f21ef689897fbe7750610038c0fde870cfc9debf89e04cda538123b`
-	Default Command: `["perl5.41.13","-de0"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1751241600'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 13 Jun 2025 11:40:07 GMT
WORKDIR /usr/src/perl
# Fri, 13 Jun 2025 11:40:07 GMT
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/B/BO/BOOK/perl-5.41.13.tar.gz -o perl-5.41.13.tar.gz     && echo '394f23c7731f6e83bde81b4995884fe2dd51e6867a57a0b53bd29b11c6a3a514 *perl-5.41.13.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.41.13.tar.gz -C /usr/src/perl     && rm perl-5.41.13.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.091.tar.gz'     && echo 'c5996e7335912a5c99e06bdb47ff39df309a857cbd8fd2627a021cefdb53cf54 *IO-Socket-SSL-2.091.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.091.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.091* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Fri, 13 Jun 2025 11:40:07 GMT
WORKDIR /usr/src/app
# Fri, 13 Jun 2025 11:40:07 GMT
CMD ["perl5.41.13" "-de0"]
```

-	Layers:
	-	`sha256:2d765646d883a37610a09973a079fbba4c7596e54d18d0447bdfff142389d1f7`  
		Last Modified: Tue, 01 Jul 2025 01:14:44 GMT  
		Size: 53.8 MB (53754822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06408a499c9b569e198473b636afa8c383e459ee6fe76ba4159b758c84e68f10`  
		Last Modified: Tue, 01 Jul 2025 02:25:30 GMT  
		Size: 15.8 MB (15765336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06772a4eff3df697497bb68b4dcdeb97fdb9338b5e7dde7d1a53579c3203c9ba`  
		Last Modified: Tue, 01 Jul 2025 03:20:06 GMT  
		Size: 54.8 MB (54757481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fd49c17bd36c59d7bf7afe446ee52f36cad8a6393628526989f2db44b4486c1`  
		Last Modified: Tue, 01 Jul 2025 05:11:29 GMT  
		Size: 197.1 MB (197142751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3264289d9249434045896109de21cdb20998ccb4d7f5fc1c25c18f51b179c11`  
		Last Modified: Tue, 01 Jul 2025 05:22:26 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5c254939d334fa607faa687a3af7ce228847dd13c6fe7edb32aae23321cc1d3`  
		Last Modified: Tue, 01 Jul 2025 05:22:27 GMT  
		Size: 15.9 MB (15926693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87c776d8b66cb42371698cfcd8348d7324482bfdfe30fe4353b8544237a631f1`  
		Last Modified: Tue, 01 Jul 2025 05:22:26 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-threaded-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:cd1d161ba50c38b5e6c50f09240d400eb14fd497faa494b101377d49d4c30dde
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15481367 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4bc08ef2ea4d4c910934e33cf2f65c49b0c989a614bb1bcc5392ffd678c04c0`

```dockerfile
```

-	Layers:
	-	`sha256:c210b0cf4788b3de9ba28e2f587c04f64742f8bbbf99aeb0cd9d2f92cf8dbbc2`  
		Last Modified: Tue, 01 Jul 2025 07:43:29 GMT  
		Size: 15.5 MB (15463630 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f2a00e6e01dcbbdadded0b5d9859732278ee581f25b0686f8a3869f6fc5f4fe6`  
		Last Modified: Tue, 01 Jul 2025 07:43:29 GMT  
		Size: 17.7 KB (17737 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-threaded-bullseye` - linux; arm variant v7

```console
$ docker pull perl@sha256:4c76b68f6c86910ec8529fee3c84ae294e3feeef57308c24b308e1f0df17d2b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.6 MB (297632393 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8f1aa82c34f34c6346542b75063033fa799a17f1130712347bc7a2abda225d6`
-	Default Command: `["perl5.41.13","-de0"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1749513600'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 13 Jun 2025 11:40:07 GMT
WORKDIR /usr/src/perl
# Fri, 13 Jun 2025 11:40:07 GMT
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/B/BO/BOOK/perl-5.41.13.tar.gz -o perl-5.41.13.tar.gz     && echo '394f23c7731f6e83bde81b4995884fe2dd51e6867a57a0b53bd29b11c6a3a514 *perl-5.41.13.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.41.13.tar.gz -C /usr/src/perl     && rm perl-5.41.13.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.091.tar.gz'     && echo 'c5996e7335912a5c99e06bdb47ff39df309a857cbd8fd2627a021cefdb53cf54 *IO-Socket-SSL-2.091.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.091.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.091* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Fri, 13 Jun 2025 11:40:07 GMT
WORKDIR /usr/src/app
# Fri, 13 Jun 2025 11:40:07 GMT
CMD ["perl5.41.13" "-de0"]
```

-	Layers:
	-	`sha256:c43258def9bd93af20e1c5bd4e42a71d9db281a9fc468bbb5eb78d7a51c6472a`  
		Last Modified: Tue, 10 Jun 2025 22:47:56 GMT  
		Size: 49.0 MB (49043954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:319bc9ba38020b34f4e3f562e110c9ab25e658493eaf95bfc783a633f2d4b036`  
		Last Modified: Wed, 11 Jun 2025 20:11:47 GMT  
		Size: 14.9 MB (14880672 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc07acb5bb3458d1880be716fdb2bcc90e78327b21f1c1531b5e4bd0941213a8`  
		Last Modified: Wed, 11 Jun 2025 13:12:55 GMT  
		Size: 50.6 MB (50630824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:734851a2b324bac96f57123943a6df950697f3e23e8b67c0c61d1bf8cb6ebe94`  
		Last Modified: Wed, 11 Jun 2025 20:11:59 GMT  
		Size: 168.1 MB (168096630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca527fefa70561a2257a6018684f4fa57d148e5be92e8fa30670c94dda4897d7`  
		Last Modified: Fri, 13 Jun 2025 17:46:41 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:490fb9bdc3e0e44ef3345e8dd85e004831f5b06017e422f8b7ed76e1315264dd`  
		Last Modified: Fri, 13 Jun 2025 20:43:00 GMT  
		Size: 15.0 MB (14980045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:722820f97e20ab59955ae06e2431859c6d103d2941e72cbdb1f0391b2b07b424`  
		Last Modified: Fri, 13 Jun 2025 20:42:59 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-threaded-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:0c7b34f883419dc98207190545a7c5e1a40923f1dfb28784afef8a156bdc5fc6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15280689 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92262294d9c5580ca343cfdb15ff1a66cc3a88c3e1b1a3c5c00764a5190e36ed`

```dockerfile
```

-	Layers:
	-	`sha256:57c8183217f6f9308ffbcd01dc4a770ca7993af1dc7452ddbed321fc1d46d690`  
		Last Modified: Fri, 13 Jun 2025 22:41:51 GMT  
		Size: 15.3 MB (15262884 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:18e1073f4f1b148be030ff2171119bfcbc4bdc61e9e68f623ea4feb2b98592a3`  
		Last Modified: Fri, 13 Jun 2025 22:41:52 GMT  
		Size: 17.8 KB (17805 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-threaded-bullseye` - linux; arm64 variant v8

```console
$ docker pull perl@sha256:ae1f3d4746c7bb3adb01ef38529918b92bdd4991886161f8eade9c07798ae746
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **329.3 MB (329289956 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d18d25331b7bc9e1bd85a2809a5905f2e1fd1c0e69b2629511e502d5132dfe30`
-	Default Command: `["perl5.41.13","-de0"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1749513600'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 13 Jun 2025 11:40:07 GMT
WORKDIR /usr/src/perl
# Fri, 13 Jun 2025 11:40:07 GMT
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/B/BO/BOOK/perl-5.41.13.tar.gz -o perl-5.41.13.tar.gz     && echo '394f23c7731f6e83bde81b4995884fe2dd51e6867a57a0b53bd29b11c6a3a514 *perl-5.41.13.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.41.13.tar.gz -C /usr/src/perl     && rm perl-5.41.13.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.091.tar.gz'     && echo 'c5996e7335912a5c99e06bdb47ff39df309a857cbd8fd2627a021cefdb53cf54 *IO-Socket-SSL-2.091.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.091.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.091* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Fri, 13 Jun 2025 11:40:07 GMT
WORKDIR /usr/src/app
# Fri, 13 Jun 2025 11:40:07 GMT
CMD ["perl5.41.13" "-de0"]
```

-	Layers:
	-	`sha256:01b9f05048bbb73f25cf8fdb677f6390611ed20f4945645387ddce6122b5075e`  
		Last Modified: Tue, 10 Jun 2025 22:49:07 GMT  
		Size: 52.3 MB (52252301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db6f3b6fbce84c42871ea80f05b2c61e622e08647f7164e9a95a391926c1f714`  
		Last Modified: Wed, 11 Jun 2025 02:56:50 GMT  
		Size: 15.8 MB (15750566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc7850095446c84fa9107622e378378aa7daf4b928caeecbc1149118900d32f7`  
		Last Modified: Wed, 11 Jun 2025 10:33:17 GMT  
		Size: 54.9 MB (54853082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a2fd7e06d1539d559e26d6be731f625763a107e4ea18988324824efe75999cc`  
		Last Modified: Wed, 11 Jun 2025 19:39:52 GMT  
		Size: 190.6 MB (190602978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3245ba7a4fa2183767b50739d942500b9d68de71d31f8adad94ba648c1508c5a`  
		Last Modified: Fri, 13 Jun 2025 17:15:09 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78f90dbc2976c7e72526e861d3ca7dee7b9568e77136251d38fa0b05b076bbf4`  
		Last Modified: Fri, 13 Jun 2025 19:36:38 GMT  
		Size: 15.8 MB (15830764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9f65e8750d34612922f148cb46c546bd6bc244c8b8a51c9b0934df8438c5c4d`  
		Last Modified: Fri, 13 Jun 2025 19:36:37 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-threaded-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:78aa37a4f502bea7d50a6addd876a4329448f9d8ae590ce41b5f5cb275f6b032
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15485136 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0993b7303ee5477512efe53d554b798b6da38fcc4e67f042de0e0ce265fc5116`

```dockerfile
```

-	Layers:
	-	`sha256:805296c1ab412d4868058a22289a25883166da2ffadd2b3f626939a3a664c739`  
		Last Modified: Fri, 13 Jun 2025 22:42:03 GMT  
		Size: 15.5 MB (15467307 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c79db6a6a12d0c7a5a567dae289f56a728c680edfc84891aaccdb3adc535bf14`  
		Last Modified: Fri, 13 Jun 2025 22:42:04 GMT  
		Size: 17.8 KB (17829 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-threaded-bullseye` - linux; 386

```console
$ docker pull perl@sha256:fce7bb68d3cb3ced9b3cede75d5bbaeb183f650b34a6f7871dc5da9bf8dd1e5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **342.5 MB (342513503 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cee1328a0a591f381a07739fc82828a39c5c994bc17a666b355e309176d612a4`
-	Default Command: `["perl5.41.13","-de0"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1751241600'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 13 Jun 2025 11:40:07 GMT
WORKDIR /usr/src/perl
# Fri, 13 Jun 2025 11:40:07 GMT
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/B/BO/BOOK/perl-5.41.13.tar.gz -o perl-5.41.13.tar.gz     && echo '394f23c7731f6e83bde81b4995884fe2dd51e6867a57a0b53bd29b11c6a3a514 *perl-5.41.13.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.41.13.tar.gz -C /usr/src/perl     && rm perl-5.41.13.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.091.tar.gz'     && echo 'c5996e7335912a5c99e06bdb47ff39df309a857cbd8fd2627a021cefdb53cf54 *IO-Socket-SSL-2.091.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.091.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.091* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Fri, 13 Jun 2025 11:40:07 GMT
WORKDIR /usr/src/app
# Fri, 13 Jun 2025 11:40:07 GMT
CMD ["perl5.41.13" "-de0"]
```

-	Layers:
	-	`sha256:7813ab6958459e0b769c4eaa51def1096dfab337ff7338a6ea28a8bdd9011dfb`  
		Last Modified: Tue, 01 Jul 2025 01:15:00 GMT  
		Size: 54.7 MB (54689934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:113be81052ec8e8323c4db158dc9c99295355934e950a6367e5c27038fd1e04c`  
		Last Modified: Tue, 01 Jul 2025 02:24:43 GMT  
		Size: 16.3 MB (16268907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a05b439f6df174e28bd21dc59eead603def3bcbd47ec6462f86b7758c4db6ef`  
		Last Modified: Tue, 01 Jul 2025 03:19:57 GMT  
		Size: 56.0 MB (56049937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d170ad31938c07c5739c923eaf5f7569c644e2ea2ead929bbc107d7eac895f78`  
		Last Modified: Tue, 01 Jul 2025 05:11:30 GMT  
		Size: 200.0 MB (200043566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02b0900c5056d02932712f6eef67968543db9feb7e3cefc5a5f1c1febf90a616`  
		Last Modified: Tue, 01 Jul 2025 05:21:26 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69aefc899448c047f399fdaf7423b4fc4a137ee7e8513388b93cc8d6e53a1e19`  
		Last Modified: Tue, 01 Jul 2025 05:21:27 GMT  
		Size: 15.5 MB (15460893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:330074276614c350813103ed5a251a4a2edec133964c38547e3ca42234a9530a`  
		Last Modified: Tue, 01 Jul 2025 05:21:26 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-threaded-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:d9f68b7a31eb897d6bb693cd20441f2060848c8b33ab62f48c5ae3f54af80cf4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15469349 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1aaad9e846e80a603a6869efb03f1a922eb5be3c7dd69b18f20746de5402ff3e`

```dockerfile
```

-	Layers:
	-	`sha256:a995d2e81163c41cff77daa6de1764065ef276b1738815a21b1375673dfbf5c9`  
		Last Modified: Tue, 01 Jul 2025 07:44:10 GMT  
		Size: 15.5 MB (15451640 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e88b5ec784f1496a2a2258b6795c3fc7da321f6778044ddae273537a6e1459a3`  
		Last Modified: Tue, 01 Jul 2025 07:44:10 GMT  
		Size: 17.7 KB (17709 bytes)  
		MIME: application/vnd.in-toto+json
