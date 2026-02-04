## `perl:bookworm`

```console
$ docker pull perl@sha256:102e3b63031915b0011cabc8b8d49baaf773dcc68a1b6c6db44b3ed81bf379a0
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

### `perl:bookworm` - linux; amd64

```console
$ docker pull perl@sha256:dfabc3ea15a2f2bc1475b4d9f422805e941c94fbe54a46d3c46faa00ec19cccb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **364.3 MB (364298409 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72fafee92419ada0950985fb3a28b5cfd5d1812c711a3ba39b025aaf9f1789f2`
-	Default Command: `["perl5.42.0","-de0"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 02:41:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 03:28:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 04:17:08 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 05:21:24 GMT
WORKDIR /usr/src/perl
# Tue, 03 Feb 2026 05:25:21 GMT
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/B/BO/BOOK/perl-5.42.0.tar.gz -o perl-5.42.0.tar.gz     && echo 'e093ef184d7f9a1b9797e2465296f55510adb6dab8842b0c3ed53329663096dc *perl-5.42.0.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.42.0.tar.gz -C /usr/src/perl     && rm perl-5.42.0.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.091.tar.gz'     && echo 'c5996e7335912a5c99e06bdb47ff39df309a857cbd8fd2627a021cefdb53cf54 *IO-Socket-SSL-2.091.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.091.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.091* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Tue, 03 Feb 2026 05:25:21 GMT
WORKDIR /usr/src/app
# Tue, 03 Feb 2026 05:25:21 GMT
CMD ["perl5.42.0" "-de0"]
```

-	Layers:
	-	`sha256:6bc9f599b3efabc64230fd3b969d7654fcd6c6c98ad7cf7470093fe85274a7fc`  
		Last Modified: Tue, 03 Feb 2026 01:13:20 GMT  
		Size: 48.5 MB (48481483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89edcaae7ec479668d9bf0891145726173a305c809a8c4165723ceaf15b5a05f`  
		Last Modified: Tue, 03 Feb 2026 02:41:49 GMT  
		Size: 24.0 MB (24038446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbceb003542957cee7df7b79249eaf0a71d21c5203d086969b565fb6dec85d86`  
		Last Modified: Tue, 03 Feb 2026 03:28:33 GMT  
		Size: 64.4 MB (64395971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dc8224e38b60eab6eeca2f231116d0a569bbe1e6c566947cbcba7ce45fd5451`  
		Last Modified: Tue, 03 Feb 2026 04:17:48 GMT  
		Size: 211.5 MB (211483360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9903e508e422176dcd56f8ddd0c2a3583ef4ccc351163357eccb9b1ec8dcd05a`  
		Last Modified: Tue, 03 Feb 2026 05:25:37 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d92950105a47a69f1c5beab5804a0f543a12c6972614b547aa67c8bbf6f0835a`  
		Last Modified: Tue, 03 Feb 2026 05:25:38 GMT  
		Size: 15.9 MB (15898880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a3e18c2bdf8a1f9f85576cad8205e1c77bea6e36bda8a7629ea103739cbcfbe`  
		Last Modified: Tue, 03 Feb 2026 05:25:37 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:bookworm` - unknown; unknown

```console
$ docker pull perl@sha256:c30c4433bc60ac5056a519b250130d02276299c4722c409f3432cb0921659817
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.9 MB (15887981 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09f8d645d8966fe9ab3bccea09785f20f8ff1ba65e9b79e2b6dd86795b854b44`

```dockerfile
```

-	Layers:
	-	`sha256:b67237fb320ab0eb1cf79fe119527b2afb23f37b155b0df7337d55f76b668281`  
		Last Modified: Tue, 03 Feb 2026 05:25:38 GMT  
		Size: 15.9 MB (15869850 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b6c23e7f54b0d57325510a9df2588609aca9781837e5dfc1cce615abd5b0f9d1`  
		Last Modified: Tue, 03 Feb 2026 05:25:37 GMT  
		Size: 18.1 KB (18131 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:bookworm` - linux; arm variant v5

```console
$ docker pull perl@sha256:dc7b1345939ae00d56d10e29c0253043cd870519b59472c0b6edc6b2670abbc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **330.7 MB (330656963 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:398ba5e4bbafe0bd3cd2713366dbd7c2978e6aeeaafbaec73f296fb2eead2db2`
-	Default Command: `["perl5.42.0","-de0"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 03:25:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 05:17:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 06:17:38 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 07:20:18 GMT
WORKDIR /usr/src/perl
# Tue, 03 Feb 2026 07:25:44 GMT
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/B/BO/BOOK/perl-5.42.0.tar.gz -o perl-5.42.0.tar.gz     && echo 'e093ef184d7f9a1b9797e2465296f55510adb6dab8842b0c3ed53329663096dc *perl-5.42.0.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.42.0.tar.gz -C /usr/src/perl     && rm perl-5.42.0.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.091.tar.gz'     && echo 'c5996e7335912a5c99e06bdb47ff39df309a857cbd8fd2627a021cefdb53cf54 *IO-Socket-SSL-2.091.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.091.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.091* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Tue, 03 Feb 2026 07:25:44 GMT
WORKDIR /usr/src/app
# Tue, 03 Feb 2026 07:25:44 GMT
CMD ["perl5.42.0" "-de0"]
```

-	Layers:
	-	`sha256:48989bca0bd1f08c49cfd2a8eae58c5ffcacc0f005e701953d88f28a5e398ee1`  
		Last Modified: Tue, 03 Feb 2026 01:13:21 GMT  
		Size: 46.0 MB (46016664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca8c031851c0852eda9cc103afa92ccd1ccefa07dd936a71f291d45de349d70b`  
		Last Modified: Tue, 03 Feb 2026 03:26:08 GMT  
		Size: 22.7 MB (22713907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2787358314b0b690e6368b20e1faf8551e6eaee19cdf0cf05d8e0a7e3fd0707`  
		Last Modified: Tue, 03 Feb 2026 05:17:27 GMT  
		Size: 62.0 MB (62008804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ade017f6e55e3995aed4fb2ab52a0b546fc96fe91f71aa940378d128db0d9901`  
		Last Modified: Tue, 03 Feb 2026 06:18:14 GMT  
		Size: 184.7 MB (184737288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54554c53d48df820c78e34034b335dc6fb66cf6d8e5a4c45812ab5eb301908da`  
		Last Modified: Tue, 03 Feb 2026 07:26:05 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70666348c36a66d464d0bb0ac931c6ed7b562992b58a716e795f5dedf0f3d9f5`  
		Last Modified: Tue, 03 Feb 2026 07:26:06 GMT  
		Size: 15.2 MB (15180031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efba8d67bd7007635a5505a73a98523818bd438baedc5f3af9c534a13c31a975`  
		Last Modified: Tue, 03 Feb 2026 07:26:05 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:bookworm` - unknown; unknown

```console
$ docker pull perl@sha256:5f7229e5b46210b9c93733f2ec8c936babb63a1f3b9ce1de41a875a236f16dd7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.7 MB (15685077 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d2cf3c3ba4f8afffa048574c5b21af268ed23f50d25f732162cce3e465b2015`

```dockerfile
```

-	Layers:
	-	`sha256:cbd755827135503d45cab0147588ec89adef7a939d1d2cc65e95bf16f4e0a1a5`  
		Last Modified: Tue, 03 Feb 2026 07:26:05 GMT  
		Size: 15.7 MB (15666858 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5ce75b9b04b129ac5722672bac289296308832860ea87ae90bc0b524ac53a62b`  
		Last Modified: Tue, 03 Feb 2026 07:26:05 GMT  
		Size: 18.2 KB (18219 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:bookworm` - linux; arm variant v7

```console
$ docker pull perl@sha256:7f3ef2ce48bef3b900d04f32b826d013aea28ce8beea3dc3773b184aabfb3102
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **316.2 MB (316150617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e16ae45fa6521902c824769890dda682005a72cba6a9123e6778164eafb0f41f`
-	Default Command: `["perl5.42.0","-de0"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 03:29:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 04:59:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 05:21:37 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 06:21:53 GMT
WORKDIR /usr/src/perl
# Tue, 03 Feb 2026 06:27:13 GMT
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/B/BO/BOOK/perl-5.42.0.tar.gz -o perl-5.42.0.tar.gz     && echo 'e093ef184d7f9a1b9797e2465296f55510adb6dab8842b0c3ed53329663096dc *perl-5.42.0.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.42.0.tar.gz -C /usr/src/perl     && rm perl-5.42.0.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.091.tar.gz'     && echo 'c5996e7335912a5c99e06bdb47ff39df309a857cbd8fd2627a021cefdb53cf54 *IO-Socket-SSL-2.091.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.091.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.091* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Tue, 03 Feb 2026 06:27:13 GMT
WORKDIR /usr/src/app
# Tue, 03 Feb 2026 06:27:13 GMT
CMD ["perl5.42.0" "-de0"]
```

-	Layers:
	-	`sha256:424cab4c9a6a41cd57ee6de8e95726c4d76fe3e913bd9c7731865fd244771971`  
		Last Modified: Tue, 03 Feb 2026 01:13:26 GMT  
		Size: 44.2 MB (44198733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b7fc27aeb6b79b5764735a819c5fdf5feb13c904bdffa0dee2b4c1c5f3935e7`  
		Last Modified: Tue, 03 Feb 2026 03:30:05 GMT  
		Size: 21.9 MB (21942045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cb0551578bad740c3a20b6a29166ce3ad8980e037c23d30c90a060f62da5338`  
		Last Modified: Tue, 03 Feb 2026 05:00:10 GMT  
		Size: 59.7 MB (59651962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a26aa406f0a951d371ca60b4cd835f6ce3e8dbf1e242b32d7b26932ac98930e0`  
		Last Modified: Tue, 03 Feb 2026 05:22:11 GMT  
		Size: 175.4 MB (175377949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9538697035ba458d91411e75070f5b9e00b3cb9db4dd7a8f67e508648e0abd1`  
		Last Modified: Tue, 03 Feb 2026 06:27:31 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d71026724fb46df9004fbf5f5b124274d2ab6de4b4b79956ee680ae0e41d8bf`  
		Last Modified: Tue, 03 Feb 2026 06:27:32 GMT  
		Size: 15.0 MB (14979660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e909f321749f0201a7f9ff1a74e520ab471f621da59207d4a2bae5e0a41c016a`  
		Last Modified: Tue, 03 Feb 2026 06:27:31 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:bookworm` - unknown; unknown

```console
$ docker pull perl@sha256:e30b261d0f93b72deb62cfdd76069d2debc15adcadc3a2e18bd8855ffd02ab0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.7 MB (15690553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c8ce51948c652043739187232551c0a07bb3f6a91330b3bc888e5ca12787ef6`

```dockerfile
```

-	Layers:
	-	`sha256:63f5efd636d72a63f11caee484dfc990a729ce60021142b9ff0cecf965752229`  
		Last Modified: Tue, 03 Feb 2026 06:27:32 GMT  
		Size: 15.7 MB (15672334 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e92c5c9e4f1d4b5da79341721646ee1e7834088cc63add684785be434c7bb549`  
		Last Modified: Tue, 03 Feb 2026 06:27:31 GMT  
		Size: 18.2 KB (18219 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:bookworm` - linux; arm64 variant v8

```console
$ docker pull perl@sha256:f5c6c9c39b5cf7db158fa7c3b03b5474a26f0689147f77e187cfacde6ee98b3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **355.3 MB (355331134 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:816f4c8cf5320223682bc8d0865a5dd95eda696148fb5a48412d98c929469e5d`
-	Default Command: `["perl5.42.0","-de0"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 02:44:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 03:46:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 04:17:02 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 05:22:12 GMT
WORKDIR /usr/src/perl
# Tue, 03 Feb 2026 05:26:35 GMT
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/B/BO/BOOK/perl-5.42.0.tar.gz -o perl-5.42.0.tar.gz     && echo 'e093ef184d7f9a1b9797e2465296f55510adb6dab8842b0c3ed53329663096dc *perl-5.42.0.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.42.0.tar.gz -C /usr/src/perl     && rm perl-5.42.0.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.091.tar.gz'     && echo 'c5996e7335912a5c99e06bdb47ff39df309a857cbd8fd2627a021cefdb53cf54 *IO-Socket-SSL-2.091.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.091.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.091* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Tue, 03 Feb 2026 05:26:35 GMT
WORKDIR /usr/src/app
# Tue, 03 Feb 2026 05:26:35 GMT
CMD ["perl5.42.0" "-de0"]
```

-	Layers:
	-	`sha256:64e8f4c09e7ac936ecc3deb0e61613f653224c28b2e35fa9d8e6e11cbdb5f911`  
		Last Modified: Tue, 03 Feb 2026 01:13:22 GMT  
		Size: 48.4 MB (48365956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:404413e6e45accf116074dace885c7ccf2917479ae04f2f46c046b6ae1909254`  
		Last Modified: Tue, 03 Feb 2026 02:44:54 GMT  
		Size: 23.6 MB (23604842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1e9aa4982c2a67e202ea283fc3760e94d8d8b16966c616e01ad0238abbaac82`  
		Last Modified: Tue, 03 Feb 2026 03:46:50 GMT  
		Size: 64.5 MB (64479687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65d574c1c687183c16f0b081ada8360957554f72a0100ca93ba1642b15723a98`  
		Last Modified: Tue, 03 Feb 2026 04:17:42 GMT  
		Size: 203.0 MB (203020015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:357a72f97327f69ede8cd6141c890ca12cea0ae41eca43a0ca6cb4f384473e51`  
		Last Modified: Tue, 03 Feb 2026 05:26:53 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f3036f55003021346babe9cfdfbbecb1e503bd49a22e13391cfcd879696b97a`  
		Last Modified: Tue, 03 Feb 2026 05:26:54 GMT  
		Size: 15.9 MB (15860368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0df2a4f5445e2ed6b6701cf4e716f9674a70f03cd9e80a44621eaac45ad46033`  
		Last Modified: Tue, 03 Feb 2026 05:26:53 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:bookworm` - unknown; unknown

```console
$ docker pull perl@sha256:76520f6a65891849c74232f5545439bd3b7c1d4f1860d6a33a5160ac63c58fab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.9 MB (15916635 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38db9b7dbed09bf5ad61cc09b3dab440e0ef6018d556689d296f806feeb34823`

```dockerfile
```

-	Layers:
	-	`sha256:ed316b367f03f204f48612b719d663c81c0195500fa5268e59e1348a107d1806`  
		Last Modified: Tue, 03 Feb 2026 05:26:54 GMT  
		Size: 15.9 MB (15898388 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3bafc26cf99f85f322bdbd4906866db83733f962c6373f69970fe618bc8c07e2`  
		Last Modified: Tue, 03 Feb 2026 05:26:53 GMT  
		Size: 18.2 KB (18247 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:bookworm` - linux; 386

```console
$ docker pull perl@sha256:546b0f82bff284d70d082e7328d6855cffde554837fb3a07502dfcd7f16cccb6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **366.4 MB (366385034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0037c42fef49d267933bce59b0c4993abca62518d5124d6a79b0b3bfe5acdd28`
-	Default Command: `["perl5.42.0","-de0"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 02:49:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 03:24:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 04:17:05 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 05:15:03 GMT
WORKDIR /usr/src/perl
# Tue, 03 Feb 2026 05:19:58 GMT
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/B/BO/BOOK/perl-5.42.0.tar.gz -o perl-5.42.0.tar.gz     && echo 'e093ef184d7f9a1b9797e2465296f55510adb6dab8842b0c3ed53329663096dc *perl-5.42.0.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.42.0.tar.gz -C /usr/src/perl     && rm perl-5.42.0.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.091.tar.gz'     && echo 'c5996e7335912a5c99e06bdb47ff39df309a857cbd8fd2627a021cefdb53cf54 *IO-Socket-SSL-2.091.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.091.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.091* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Tue, 03 Feb 2026 05:19:58 GMT
WORKDIR /usr/src/app
# Tue, 03 Feb 2026 05:19:58 GMT
CMD ["perl5.42.0" "-de0"]
```

-	Layers:
	-	`sha256:a7f977a794a5fd56ece19f51541cec3b8ba447f10234ab001213bf850f92f64d`  
		Last Modified: Tue, 03 Feb 2026 01:13:34 GMT  
		Size: 49.5 MB (49468454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e50ea552b26a58c13b4166d933269500891fb4897db09bc72d932372276b158f`  
		Last Modified: Tue, 03 Feb 2026 02:49:31 GMT  
		Size: 24.9 MB (24872100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cc15e0cd687cd62190081200fbe30ab5102ae840cc68b0386259c387aef2b9a`  
		Last Modified: Tue, 03 Feb 2026 03:25:00 GMT  
		Size: 66.2 MB (66234564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8546516d2639f1f1b48ec08126291bf1c785668047fb362bdcd53981253c53d9`  
		Last Modified: Tue, 03 Feb 2026 04:17:44 GMT  
		Size: 210.4 MB (210415991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3064dd986ee0805647bb506f2dba5266d106f7f3b128fb3771d6bb18cd6426e0`  
		Last Modified: Tue, 03 Feb 2026 05:20:19 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:927d5c1216386675ae9d6e5ca2e3eda3effa569cec10aad5b64d7a2be0e94499`  
		Last Modified: Tue, 03 Feb 2026 05:20:20 GMT  
		Size: 15.4 MB (15393655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32a0c0bac86737f7b41ca90e58f5600396d605f79af164d0c9aa06eafb30390d`  
		Last Modified: Tue, 03 Feb 2026 05:20:19 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:bookworm` - unknown; unknown

```console
$ docker pull perl@sha256:d9652a5a2b443876df1742ef5d0497db221f53554769588b5236edea5ff40e0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.9 MB (15866155 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7f1b4af9be957dee4a1d15946a29549aee80f5ca53456f99c4d3f0472953546`

```dockerfile
```

-	Layers:
	-	`sha256:28fb88e1d94b3660d76f862f5a8472c7b058f260522c7f01a9817611b18ddec6`  
		Last Modified: Tue, 03 Feb 2026 05:20:20 GMT  
		Size: 15.8 MB (15848061 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:822a60faf7236c1ab4130075f6b90ea21fe9f7b4f5a83c0157e551dc931bc2e0`  
		Last Modified: Tue, 03 Feb 2026 05:20:19 GMT  
		Size: 18.1 KB (18094 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:bookworm` - linux; mips64le

```console
$ docker pull perl@sha256:18c0d3b13708932020e5f2dced498126168b2e8f4769af3c88078dcd4db0eefc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **341.1 MB (341054761 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:767a46fd381ef0a0fe050097054a5e6c5d971f25ff8548fc7adc7f287854f549`
-	Default Command: `["perl5.42.0","-de0"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 16:06:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 21:28:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 22:13:27 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 04 Feb 2026 00:32:06 GMT
WORKDIR /usr/src/perl
# Wed, 04 Feb 2026 00:56:09 GMT
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/B/BO/BOOK/perl-5.42.0.tar.gz -o perl-5.42.0.tar.gz     && echo 'e093ef184d7f9a1b9797e2465296f55510adb6dab8842b0c3ed53329663096dc *perl-5.42.0.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.42.0.tar.gz -C /usr/src/perl     && rm perl-5.42.0.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.091.tar.gz'     && echo 'c5996e7335912a5c99e06bdb47ff39df309a857cbd8fd2627a021cefdb53cf54 *IO-Socket-SSL-2.091.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.091.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.091* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Wed, 04 Feb 2026 00:56:10 GMT
WORKDIR /usr/src/app
# Wed, 04 Feb 2026 00:56:10 GMT
CMD ["perl5.42.0" "-de0"]
```

-	Layers:
	-	`sha256:001d31ce76be3df3174382025b0b9e2985ddc96d785143497e14a46cdcdcf951`  
		Last Modified: Tue, 03 Feb 2026 01:12:32 GMT  
		Size: 48.8 MB (48763257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e910e12f1ba466db5d640f799037fd1161885165d6ef1a46de53b55b08cfb02`  
		Last Modified: Tue, 03 Feb 2026 16:07:24 GMT  
		Size: 23.6 MB (23615398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6e0ad746711a3754afd4dc1df1be9308a858da3b48f46cc1d318cd1dbf2cb47`  
		Last Modified: Tue, 03 Feb 2026 21:29:58 GMT  
		Size: 63.3 MB (63310108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8dcbde3e87bb22f75629b0dc4ffe06e760eb4211178024075579c18fee0e9fa`  
		Last Modified: Tue, 03 Feb 2026 22:16:40 GMT  
		Size: 190.3 MB (190253616 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc6c7aeca79b8c3a1bbbbd0b875839e68f46faf8b7e8889d9eaa39120ef1241a`  
		Last Modified: Wed, 04 Feb 2026 00:57:13 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a4fb755ff5df937cd6b4996954a55cc9cce7164e8c5b984a616ba71751af6cd`  
		Last Modified: Wed, 04 Feb 2026 00:57:15 GMT  
		Size: 15.1 MB (15112114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34625c4fdf02c3d7a8b9649dee76ab93e5f4dcde2e0cce7a08b8aeed2af09730`  
		Last Modified: Wed, 04 Feb 2026 00:57:13 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:bookworm` - unknown; unknown

```console
$ docker pull perl@sha256:0a9cfebedd0963af36c3d2e923c54a8300a5f2a3c5e2c4cafb2a75cb1eab70a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.0 KB (17991 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8049b50f0f271e9389a39bb73365e0864129a674556b91b6c56fd0f510e5181`

```dockerfile
```

-	Layers:
	-	`sha256:2c793a0983c32cda1279e2f5dbfb8e244dae1c65fd14ac51e20a94edaa21df09`  
		Last Modified: Wed, 04 Feb 2026 00:57:13 GMT  
		Size: 18.0 KB (17991 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:bookworm` - linux; ppc64le

```console
$ docker pull perl@sha256:86bba497a4b6a13ac06a1f3d799a3f47d5716a2f8d81313faff5f4fa34023bc4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **378.3 MB (378272531 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d74ba4ce2881b331a491a0517fe6ccb7ff731e1ab5307f718ea578403f2f566`
-	Default Command: `["perl5.42.0","-de0"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 05:22:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 10:35:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 12:40:17 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 16:39:35 GMT
WORKDIR /usr/src/perl
# Tue, 03 Feb 2026 16:48:05 GMT
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/B/BO/BOOK/perl-5.42.0.tar.gz -o perl-5.42.0.tar.gz     && echo 'e093ef184d7f9a1b9797e2465296f55510adb6dab8842b0c3ed53329663096dc *perl-5.42.0.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.42.0.tar.gz -C /usr/src/perl     && rm perl-5.42.0.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.091.tar.gz'     && echo 'c5996e7335912a5c99e06bdb47ff39df309a857cbd8fd2627a021cefdb53cf54 *IO-Socket-SSL-2.091.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.091.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.091* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Tue, 03 Feb 2026 16:48:06 GMT
WORKDIR /usr/src/app
# Tue, 03 Feb 2026 16:48:06 GMT
CMD ["perl5.42.0" "-de0"]
```

-	Layers:
	-	`sha256:5e189aacb842725e8d1d9877c9ab9af09e14901412b6665e179393112b5bca51`  
		Last Modified: Tue, 03 Feb 2026 01:12:57 GMT  
		Size: 52.3 MB (52327289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a1311f6670d65067c1adb8d518ab8836a9d3d42058afdd776824845f91935c9`  
		Last Modified: Tue, 03 Feb 2026 05:22:25 GMT  
		Size: 25.7 MB (25671343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d3c21a9818f8ca2f73ccd29b595b5a2bc7818b3057c3895ec555bee901eb365`  
		Last Modified: Tue, 03 Feb 2026 10:36:21 GMT  
		Size: 69.8 MB (69846016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d3cd1984006b3a1ea75bcfb5aaf414d967e1b46277e9ce2c62c0efa3843fe34`  
		Last Modified: Tue, 03 Feb 2026 12:41:39 GMT  
		Size: 214.5 MB (214529389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:469fac046c47bb3b377a690e1fe8b079a4955f1b371fad680991d6d4220f54da`  
		Last Modified: Tue, 03 Feb 2026 16:48:47 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59eac9dc2080b54b4c69643ec444610b5d0cb95510e43baf04004d9f11d3c943`  
		Last Modified: Tue, 03 Feb 2026 16:48:48 GMT  
		Size: 15.9 MB (15898225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41e885989672311fb1ca47b4dede2e09ba8cf98d7a7cc5a44b0a174b44bb319a`  
		Last Modified: Tue, 03 Feb 2026 16:48:47 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:bookworm` - unknown; unknown

```console
$ docker pull perl@sha256:c13673e0d342fe72234f53273d98db899b3261caa8971ac1b57006218a02a5ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.9 MB (15864556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ab81c915e7757ecdcd60b4bb00126a97b49db41a48f9c77ec5e671bb620b189`

```dockerfile
```

-	Layers:
	-	`sha256:2a156976c56b9a0a424ad6fe27b2fc3d8e4eb5f7d3ebfe4d8b0907c0a27a27b3`  
		Last Modified: Tue, 03 Feb 2026 16:48:48 GMT  
		Size: 15.8 MB (15846375 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1d88d98445ff5da1007fc674906d215efa404118c5cb834aa7969ac39b05828c`  
		Last Modified: Tue, 03 Feb 2026 16:48:47 GMT  
		Size: 18.2 KB (18181 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:bookworm` - linux; s390x

```console
$ docker pull perl@sha256:3ae6b38b399c7d9dc72419c07ab153b58554ccadd409ecbcd7118945b504fdce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **334.4 MB (334415672 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53b8c504c777b650edd273d11822cf9ae008e686037a29b69bcc962f06d8f1c1`
-	Default Command: `["perl5.42.0","-de0"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 03:44:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 05:28:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 06:14:15 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 09:08:03 GMT
WORKDIR /usr/src/perl
# Tue, 03 Feb 2026 09:15:43 GMT
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/B/BO/BOOK/perl-5.42.0.tar.gz -o perl-5.42.0.tar.gz     && echo 'e093ef184d7f9a1b9797e2465296f55510adb6dab8842b0c3ed53329663096dc *perl-5.42.0.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.42.0.tar.gz -C /usr/src/perl     && rm perl-5.42.0.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.091.tar.gz'     && echo 'c5996e7335912a5c99e06bdb47ff39df309a857cbd8fd2627a021cefdb53cf54 *IO-Socket-SSL-2.091.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.091.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.091* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Tue, 03 Feb 2026 09:15:43 GMT
WORKDIR /usr/src/app
# Tue, 03 Feb 2026 09:15:43 GMT
CMD ["perl5.42.0" "-de0"]
```

-	Layers:
	-	`sha256:4c4c4621da5085342b3b0d8d8ef57e5e44004eedf5818268af30c41a02cb6cf2`  
		Last Modified: Tue, 03 Feb 2026 01:12:48 GMT  
		Size: 47.1 MB (47138343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3072e3eb8c224dc593a4e18a3785b06d51467102b1cd9dd426d3d31d0e6831b8`  
		Last Modified: Tue, 03 Feb 2026 03:44:33 GMT  
		Size: 24.0 MB (24033633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61724404ca7e7ee67a943113b2e679af71546a07f66af094570e811bbc9fa743`  
		Last Modified: Tue, 03 Feb 2026 05:29:11 GMT  
		Size: 63.5 MB (63501320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02377bb24487c52031d5d5472b3522d2e281a9e72b2998ef6a56f3eb2698a921`  
		Last Modified: Tue, 03 Feb 2026 06:15:07 GMT  
		Size: 183.5 MB (183511202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45db3ebc84a1d048289bb17e705f0c37ed341142861f1816dfb64f05a9c8019b`  
		Last Modified: Tue, 03 Feb 2026 09:16:22 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d95d3717e097d20b982f6abe869ac0a1db04299c6705e74bc71679d8ba43e94`  
		Last Modified: Tue, 03 Feb 2026 09:16:23 GMT  
		Size: 16.2 MB (16230906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9975a72ecf8a1542855a916bea713ae84952a799fa69959ca4af35d18086c84`  
		Last Modified: Tue, 03 Feb 2026 09:16:22 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:bookworm` - unknown; unknown

```console
$ docker pull perl@sha256:87b22f2c70365d1d3f679f96748de29483f5981b61a41c29d843bfff9d47b80a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.7 MB (15695579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ae25d776f778c4d3faad46d2b2b1a107b510727fa255c7331fade5acaae63fc`

```dockerfile
```

-	Layers:
	-	`sha256:65903534eb7c8d911643665d1ceaaaaa9b8486b44648125f9915f904bd6198b1`  
		Last Modified: Tue, 03 Feb 2026 09:16:23 GMT  
		Size: 15.7 MB (15677448 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:47c1c93397b2054e903e4b94cce251a73291f04049c9ebd8ef049df5ace8e119`  
		Last Modified: Tue, 03 Feb 2026 09:16:22 GMT  
		Size: 18.1 KB (18131 bytes)  
		MIME: application/vnd.in-toto+json
