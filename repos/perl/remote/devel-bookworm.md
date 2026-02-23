## `perl:devel-bookworm`

```console
$ docker pull perl@sha256:2ef6ba41390d6eada5d1330e4141582290f04f695dd237b9714e92a951b3b541
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
$ docker pull perl@sha256:6b63d1705e8e2f3000a049fab4688c6946b060177505acc77d5013a9605d0a3a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **364.5 MB (364542488 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62ae0c2ed60aaaf50bbee05224c5395ca34dc900c6de35fe0267ac2a6514dc77`
-	Default Command: `["perl5.43.8","-de0"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 02:41:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 03:28:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 04:17:08 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 Feb 2026 18:50:19 GMT
WORKDIR /usr/src/perl
# Mon, 23 Feb 2026 18:54:29 GMT
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/H/HY/HYDAHY/perl-5.43.8.tar.gz -o perl-5.43.8.tar.gz     && echo '44bc66a00ca494b66ed3f5221ad8b89271d8dca397a1fd0f5f6d0f047db0a2ca *perl-5.43.8.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.43.8.tar.gz -C /usr/src/perl     && rm perl-5.43.8.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.091.tar.gz'     && echo 'c5996e7335912a5c99e06bdb47ff39df309a857cbd8fd2627a021cefdb53cf54 *IO-Socket-SSL-2.091.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.091.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.091* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Mon, 23 Feb 2026 18:54:29 GMT
WORKDIR /usr/src/app
# Mon, 23 Feb 2026 18:54:29 GMT
CMD ["perl5.43.8" "-de0"]
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
	-	`sha256:ed65c0d66c03df75092b91883fced2a440c1b46e329646918215307bc6554592`  
		Last Modified: Mon, 23 Feb 2026 18:54:50 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58b16d7c2530e6d7362688a1a5d4099ec265eb7a9d3f1907a5d382e192202658`  
		Last Modified: Mon, 23 Feb 2026 18:54:50 GMT  
		Size: 16.1 MB (16142960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc02f3b7a27d1742ef6cff0f685782d47e8b1b06c9383fc1eaf27d1c1f8a0e1f`  
		Last Modified: Mon, 23 Feb 2026 18:54:50 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-bookworm` - unknown; unknown

```console
$ docker pull perl@sha256:2a46a1c2147fe2ba2b6c5aa8b81a6872daa7268b5c460b3ed9efead42fcd3e4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.9 MB (15886853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5040a0732323291d2dbf7d0b04f8156414aba04a0af1545f2fb7676a41b93118`

```dockerfile
```

-	Layers:
	-	`sha256:691bd80c5ad25f2b1d52da2bd04158370c36caf295c7935ad4241bc00b1e2fc1`  
		Last Modified: Mon, 23 Feb 2026 18:54:50 GMT  
		Size: 15.9 MB (15869248 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8081fa02e1e97eee64b04073dd4f3df36dfdb73ae9b790c05ca72894933c7bf0`  
		Last Modified: Mon, 23 Feb 2026 18:54:50 GMT  
		Size: 17.6 KB (17605 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-bookworm` - linux; arm variant v5

```console
$ docker pull perl@sha256:08bd620826afc6d147c33aa79634fbc00308838cad3413c5fe7b365a6fd4f51f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **330.9 MB (330912503 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:856a511dfcac63b4208d156d81690754bdd41ceb2779447bb497448f76eaceea`
-	Default Command: `["perl5.43.8","-de0"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 03:25:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 05:17:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 06:17:38 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 Feb 2026 18:50:05 GMT
WORKDIR /usr/src/perl
# Mon, 23 Feb 2026 18:55:34 GMT
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/H/HY/HYDAHY/perl-5.43.8.tar.gz -o perl-5.43.8.tar.gz     && echo '44bc66a00ca494b66ed3f5221ad8b89271d8dca397a1fd0f5f6d0f047db0a2ca *perl-5.43.8.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.43.8.tar.gz -C /usr/src/perl     && rm perl-5.43.8.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.091.tar.gz'     && echo 'c5996e7335912a5c99e06bdb47ff39df309a857cbd8fd2627a021cefdb53cf54 *IO-Socket-SSL-2.091.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.091.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.091* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Mon, 23 Feb 2026 18:55:34 GMT
WORKDIR /usr/src/app
# Mon, 23 Feb 2026 18:55:34 GMT
CMD ["perl5.43.8" "-de0"]
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
	-	`sha256:c57076f14091d4c19ddd08d87eb6f31a0d25c16550f48d9edb6ec99efcb9823b`  
		Last Modified: Mon, 23 Feb 2026 18:54:41 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e660a9386c436c63705af3d9c07d6b85da9a4e79df8f95cad6a1ac143d27970`  
		Last Modified: Mon, 23 Feb 2026 18:55:56 GMT  
		Size: 15.4 MB (15435572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dde0fe9dabd0e207810f86655f8f65066945b21d223b839f7c07c4202ac46958`  
		Last Modified: Mon, 23 Feb 2026 18:55:55 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-bookworm` - unknown; unknown

```console
$ docker pull perl@sha256:52873ac6b5474e09e658df9d5e9f272787e02a8a35536ce9321838319460eceb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.7 MB (15683917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:751a37079aef8df894f1065cbe6dda60bbd22c8a25b416740ed5fef556d0174b`

```dockerfile
```

-	Layers:
	-	`sha256:00cb5454e4a123b89bc0efb565bf827357e90ec604ea328cdd13f20dd0e0b43f`  
		Last Modified: Mon, 23 Feb 2026 18:55:56 GMT  
		Size: 15.7 MB (15666240 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:02be13a0b0dba07a04a8a58fec25609b6dff06fafa61909f49c069aa0299584b`  
		Last Modified: Mon, 23 Feb 2026 18:55:55 GMT  
		Size: 17.7 KB (17677 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-bookworm` - linux; arm variant v7

```console
$ docker pull perl@sha256:03a0dd992ad814a9bf1b09b104eeb162e232d7adb87ff4dcfd727062041df2e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **316.4 MB (316380307 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a14afad244fe63fd0e50443a3ef31a7a9f896721f1915b9e6a864f6a524dd6fc`
-	Default Command: `["perl5.43.8","-de0"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 03:29:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 04:59:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 05:21:37 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 Feb 2026 18:50:04 GMT
WORKDIR /usr/src/perl
# Mon, 23 Feb 2026 18:55:22 GMT
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/H/HY/HYDAHY/perl-5.43.8.tar.gz -o perl-5.43.8.tar.gz     && echo '44bc66a00ca494b66ed3f5221ad8b89271d8dca397a1fd0f5f6d0f047db0a2ca *perl-5.43.8.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.43.8.tar.gz -C /usr/src/perl     && rm perl-5.43.8.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.091.tar.gz'     && echo 'c5996e7335912a5c99e06bdb47ff39df309a857cbd8fd2627a021cefdb53cf54 *IO-Socket-SSL-2.091.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.091.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.091* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Mon, 23 Feb 2026 18:55:22 GMT
WORKDIR /usr/src/app
# Mon, 23 Feb 2026 18:55:22 GMT
CMD ["perl5.43.8" "-de0"]
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
	-	`sha256:c57076f14091d4c19ddd08d87eb6f31a0d25c16550f48d9edb6ec99efcb9823b`  
		Last Modified: Mon, 23 Feb 2026 18:54:41 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94ca0d4be4549a02b14075f9c75292fa6693074e3ed57c45e32b8c08d78b0560`  
		Last Modified: Mon, 23 Feb 2026 18:55:42 GMT  
		Size: 15.2 MB (15209349 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e327cb53fcfb607ec590284bc3725175622d3eaee63d9d91fd40ef6653b2934`  
		Last Modified: Mon, 23 Feb 2026 18:55:42 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-bookworm` - unknown; unknown

```console
$ docker pull perl@sha256:2899e63eabc9b7e275d5169139d1db637b88da3a67626b22474da294abe4e8b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.7 MB (15689393 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54f053bb07d862e90be8379f172bc66670689be0a18a56866a0531b93b24fa8a`

```dockerfile
```

-	Layers:
	-	`sha256:33ca1a0f051a30e6ba026ea11eb2b0569e6ca95eb040d280ea743d9e7d1195a6`  
		Last Modified: Mon, 23 Feb 2026 18:55:43 GMT  
		Size: 15.7 MB (15671716 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:df09c22d2b8eae2da63dbc9e6d7bbe6a1f9d227b3809e2ddee95995d7e053e77`  
		Last Modified: Mon, 23 Feb 2026 18:55:41 GMT  
		Size: 17.7 KB (17677 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-bookworm` - linux; arm64 variant v8

```console
$ docker pull perl@sha256:45fc8e1883226d6157d229280f52c4d63852e845a7f66f354bf8a84257dc26fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **355.6 MB (355565455 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd820676274638c77bab63a7c25a872aa720a787fbc52fc1623b5d0a39659c32`
-	Default Command: `["perl5.43.8","-de0"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 02:44:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 03:46:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 04:17:02 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 Feb 2026 18:50:06 GMT
WORKDIR /usr/src/perl
# Mon, 23 Feb 2026 18:54:43 GMT
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/H/HY/HYDAHY/perl-5.43.8.tar.gz -o perl-5.43.8.tar.gz     && echo '44bc66a00ca494b66ed3f5221ad8b89271d8dca397a1fd0f5f6d0f047db0a2ca *perl-5.43.8.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.43.8.tar.gz -C /usr/src/perl     && rm perl-5.43.8.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.091.tar.gz'     && echo 'c5996e7335912a5c99e06bdb47ff39df309a857cbd8fd2627a021cefdb53cf54 *IO-Socket-SSL-2.091.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.091.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.091* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Mon, 23 Feb 2026 18:54:43 GMT
WORKDIR /usr/src/app
# Mon, 23 Feb 2026 18:54:43 GMT
CMD ["perl5.43.8" "-de0"]
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
	-	`sha256:c57076f14091d4c19ddd08d87eb6f31a0d25c16550f48d9edb6ec99efcb9823b`  
		Last Modified: Mon, 23 Feb 2026 18:54:41 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43123bc8b611e942b401cab91fecec7e45a028d6bd561925a9a34259bff30291`  
		Last Modified: Mon, 23 Feb 2026 18:55:05 GMT  
		Size: 16.1 MB (16094686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1efce2454ab8a2c44179e28db058c30babea4d5040af5d8c01173dae16df64a0`  
		Last Modified: Mon, 23 Feb 2026 18:55:04 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-bookworm` - unknown; unknown

```console
$ docker pull perl@sha256:69366bc50e30a99324fa5a1e83d22b30dbf558078e0c398472d8fbd4b6c3567b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.9 MB (15915459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acd42c738f29cf93e624539376d50438b8f3746a7f14cd5070d62c0a9b72abc8`

```dockerfile
```

-	Layers:
	-	`sha256:1907b69e0375bd7c3c7106805d426be1c5e9d6cbafac4070dbb487bafe48ecf3`  
		Last Modified: Mon, 23 Feb 2026 18:55:05 GMT  
		Size: 15.9 MB (15897762 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b964d28491984b410f58a115dfc98b466f6d001d2cd74683ccc6ba2002cc53c2`  
		Last Modified: Mon, 23 Feb 2026 18:55:04 GMT  
		Size: 17.7 KB (17697 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-bookworm` - linux; 386

```console
$ docker pull perl@sha256:03d6b63a33f7cb2866bbac1b18527d64650b264e3123a10932142ecd3c6aa534
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **366.6 MB (366626948 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d0356717f961d828070a2a5240e7e6d0777725c07de7a0be9a8c636a3ddee15`
-	Default Command: `["perl5.43.8","-de0"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 02:49:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 03:24:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 04:17:05 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 Feb 2026 18:50:02 GMT
WORKDIR /usr/src/perl
# Mon, 23 Feb 2026 18:54:54 GMT
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/H/HY/HYDAHY/perl-5.43.8.tar.gz -o perl-5.43.8.tar.gz     && echo '44bc66a00ca494b66ed3f5221ad8b89271d8dca397a1fd0f5f6d0f047db0a2ca *perl-5.43.8.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.43.8.tar.gz -C /usr/src/perl     && rm perl-5.43.8.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.091.tar.gz'     && echo 'c5996e7335912a5c99e06bdb47ff39df309a857cbd8fd2627a021cefdb53cf54 *IO-Socket-SSL-2.091.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.091.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.091* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Mon, 23 Feb 2026 18:54:54 GMT
WORKDIR /usr/src/app
# Mon, 23 Feb 2026 18:54:54 GMT
CMD ["perl5.43.8" "-de0"]
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
	-	`sha256:f980492c4288535abf64bf130ff75212b76f3d22d7960e4d9524d611541c2700`  
		Last Modified: Mon, 23 Feb 2026 18:55:15 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:038034728f3b71ff378a5672fea9363582753d397daf46db48a11ed4b8a1d2c0`  
		Last Modified: Mon, 23 Feb 2026 18:55:16 GMT  
		Size: 15.6 MB (15635569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0f1570491ae6b234f590e04c7acae94e7bb77a8d5811fa13c5f652037ea5ddd`  
		Last Modified: Mon, 23 Feb 2026 18:55:16 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-bookworm` - unknown; unknown

```console
$ docker pull perl@sha256:aa6789cf7ae2f5b3af1168de3dfe539ab2df18644c75104d8701eca03858b58e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.9 MB (15865047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:529f1ecfc3c8068961995b58f54952fe808b37bb818487492cd15f471c695292`

```dockerfile
```

-	Layers:
	-	`sha256:9bebf11a930152c195f8b5129286d465df7d141a928d21caa719038000551596`  
		Last Modified: Mon, 23 Feb 2026 18:55:16 GMT  
		Size: 15.8 MB (15847469 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:415edaa5e68d17b4bdd950627e1eef2d5e7d649c43fc066401987da44ea3364c`  
		Last Modified: Mon, 23 Feb 2026 18:55:15 GMT  
		Size: 17.6 KB (17578 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-bookworm` - linux; mips64le

```console
$ docker pull perl@sha256:ae3e49655a4255e1dbcc7c065902bb28c482ad22558c6929af09bd033e026513
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **341.3 MB (341291462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b69c4917040b3d60e89c9b96971af40442068b16d1731b9d014bfb54f65e784d`
-	Default Command: `["perl5.43.8","-de0"]`

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
# Mon, 23 Feb 2026 19:12:50 GMT
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/H/HY/HYDAHY/perl-5.43.8.tar.gz -o perl-5.43.8.tar.gz     && echo '44bc66a00ca494b66ed3f5221ad8b89271d8dca397a1fd0f5f6d0f047db0a2ca *perl-5.43.8.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.43.8.tar.gz -C /usr/src/perl     && rm perl-5.43.8.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.091.tar.gz'     && echo 'c5996e7335912a5c99e06bdb47ff39df309a857cbd8fd2627a021cefdb53cf54 *IO-Socket-SSL-2.091.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.091.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.091* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Mon, 23 Feb 2026 19:12:52 GMT
WORKDIR /usr/src/app
# Mon, 23 Feb 2026 19:12:52 GMT
CMD ["perl5.43.8" "-de0"]
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
	-	`sha256:98e847dd796eee7169d0ac620bc653494c6f62bc114e07546c5298c0846c20d0`  
		Last Modified: Mon, 23 Feb 2026 19:13:56 GMT  
		Size: 15.3 MB (15348814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ece9e961b5df818dd4a0d5c40b2ba07f6be670c4494488b2064b1532734d633`  
		Last Modified: Mon, 23 Feb 2026 19:13:55 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-bookworm` - unknown; unknown

```console
$ docker pull perl@sha256:77fcca279ba401dcea7afbd4fbde92391255d0505df79454c25d48664a66a446
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.4 KB (17446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4fddf1534f8849d948ece738b00174f91b77d28a3e9037aa088da9ab6eeb38d`

```dockerfile
```

-	Layers:
	-	`sha256:79fcd7aa0c2e2683f1ff502657dbb30b15414b412e811b5c7b5c865c7519860e`  
		Last Modified: Mon, 23 Feb 2026 19:13:55 GMT  
		Size: 17.4 KB (17446 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-bookworm` - linux; ppc64le

```console
$ docker pull perl@sha256:02a24cce93f853175786a6d0c5a5c1561335fc42a51288d0aa13de9b084e7c70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **378.5 MB (378512065 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56d749d9522c493a688eb846c1c1590d8905aa5de609804294b6d9ca34ec09c2`
-	Default Command: `["perl5.43.8","-de0"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 05:22:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 10:35:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 12:40:17 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 Feb 2026 18:48:23 GMT
WORKDIR /usr/src/perl
# Mon, 23 Feb 2026 18:57:19 GMT
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/H/HY/HYDAHY/perl-5.43.8.tar.gz -o perl-5.43.8.tar.gz     && echo '44bc66a00ca494b66ed3f5221ad8b89271d8dca397a1fd0f5f6d0f047db0a2ca *perl-5.43.8.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.43.8.tar.gz -C /usr/src/perl     && rm perl-5.43.8.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.091.tar.gz'     && echo 'c5996e7335912a5c99e06bdb47ff39df309a857cbd8fd2627a021cefdb53cf54 *IO-Socket-SSL-2.091.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.091.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.091* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Mon, 23 Feb 2026 18:57:19 GMT
WORKDIR /usr/src/app
# Mon, 23 Feb 2026 18:57:19 GMT
CMD ["perl5.43.8" "-de0"]
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
	-	`sha256:28f7c993bdb3f25657ed3bc094c83b36b40059f5313d96d6f7097e964beb11b9`  
		Last Modified: Mon, 23 Feb 2026 18:58:01 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db4540cc798b110e23a7d90a4ca263c7483a875bb7545400fc9a94301d0cbdbd`  
		Last Modified: Mon, 23 Feb 2026 18:58:38 GMT  
		Size: 16.1 MB (16137759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7d47b0e130ade5b36855bb1554ca747a70495f481bb19bea5a146119cb5c03f`  
		Last Modified: Mon, 23 Feb 2026 18:58:37 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-bookworm` - unknown; unknown

```console
$ docker pull perl@sha256:e26bbd1160c3db0beb7eec91a648ccea0db492d43f214e88db1733cc7992938f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.9 MB (15863404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:625a72c5b889315f3f981ae1ebc925e110c4b391ea5a934771edfe833b572c8c`

```dockerfile
```

-	Layers:
	-	`sha256:e2b11731666d396d6d948f93c50ed642389d45d05c9fcb1dcef72966031530db`  
		Last Modified: Mon, 23 Feb 2026 18:58:38 GMT  
		Size: 15.8 MB (15845761 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8b8c47f99d10bc95bd56b1f52bd17bc0aaaaf2564a63293648369e6511e8d0d9`  
		Last Modified: Mon, 23 Feb 2026 18:58:37 GMT  
		Size: 17.6 KB (17643 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-bookworm` - linux; s390x

```console
$ docker pull perl@sha256:b643d69260c80c6339ae8c08d5d01831a77205cb5ea8319bb1a783ba3134b078
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **334.7 MB (334674788 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe792ec8faa34fde158150d5fedfdff7b70beba3e5d0f695ceb2174c64602d17`
-	Default Command: `["perl5.43.8","-de0"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 03:44:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 05:28:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 06:14:15 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 23 Feb 2026 18:49:03 GMT
WORKDIR /usr/src/perl
# Mon, 23 Feb 2026 18:57:11 GMT
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/H/HY/HYDAHY/perl-5.43.8.tar.gz -o perl-5.43.8.tar.gz     && echo '44bc66a00ca494b66ed3f5221ad8b89271d8dca397a1fd0f5f6d0f047db0a2ca *perl-5.43.8.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.43.8.tar.gz -C /usr/src/perl     && rm perl-5.43.8.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047     && perl -pi -E 's{http://(www\.cpan\.org|backpan\.perl\.org|cpan\.metacpan\.org|fastapi\.metacpan\.org|cpanmetadb\.plackperl\.org)}{https://$1}g' bin/cpanm     && perl -pi -E 's{try_lwp=>1}{try_lwp=>0}g' bin/cpanm     && perl bin/cpanm . && cd /root     && curl -fLO 'https://www.cpan.org/authors/id/C/CH/CHRISN/Net-SSLeay-1.94.tar.gz'     && echo '9d7be8a56d1bedda05c425306cc504ba134307e0c09bda4a788c98744ebcd95d *Net-SSLeay-1.94.tar.gz' | sha256sum --strict --check -     && cpanm --notest --from $PWD Net-SSLeay-1.94.tar.gz     && curl -fLO 'https://www.cpan.org/authors/id/S/SU/SULLR/IO-Socket-SSL-2.091.tar.gz'     && echo 'c5996e7335912a5c99e06bdb47ff39df309a857cbd8fd2627a021cefdb53cf54 *IO-Socket-SSL-2.091.tar.gz' | sha256sum --strict --check -     && SSL_CERT_DIR=/etc/ssl/certs cpanm --from $PWD IO-Socket-SSL-2.091.tar.gz     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /root/Net-SSLeay-1.94* /root/IO-Socket-SSL-2.091* /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Mon, 23 Feb 2026 18:57:12 GMT
WORKDIR /usr/src/app
# Mon, 23 Feb 2026 18:57:12 GMT
CMD ["perl5.43.8" "-de0"]
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
	-	`sha256:95a7261c59b3d82f84fcd122a5566dfee39f912949865b25e41c3c714ca18208`  
		Last Modified: Mon, 23 Feb 2026 18:58:17 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69eb5ade024675567feb758e54932361800b766ed22c9421daaf637f842da63e`  
		Last Modified: Mon, 23 Feb 2026 18:58:18 GMT  
		Size: 16.5 MB (16490022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5489b8988f96c8e7f27169c53ebe860cfa1bc40fc726e2a6cf10d03a6461aed3`  
		Last Modified: Mon, 23 Feb 2026 18:58:17 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-bookworm` - unknown; unknown

```console
$ docker pull perl@sha256:a4536b7829f946557d4f1f7da682447f30231c9db2c413dff6fdcafc9cb21c1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.7 MB (15694451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52697c90a57d9a817b0b479a75b4452cc1c87650b4722fbd766c1353cab04b66`

```dockerfile
```

-	Layers:
	-	`sha256:4e1511c93c041ce6603a28ad79924416315d5dd9fecb392c4ddfe34a2a5339bb`  
		Last Modified: Mon, 23 Feb 2026 18:58:18 GMT  
		Size: 15.7 MB (15676846 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b7c2d0139461019a4872add2e0a644e6b6ba8e5fcc6285e9442e1b01665f47fc`  
		Last Modified: Mon, 23 Feb 2026 18:58:17 GMT  
		Size: 17.6 KB (17605 bytes)  
		MIME: application/vnd.in-toto+json
