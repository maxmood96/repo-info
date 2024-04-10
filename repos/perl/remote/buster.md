## `perl:buster`

```console
$ docker pull perl@sha256:d70ef392d41d0d796743cf53ccff4ddfe9dbf992979775e04cb7601527f02e52
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

### `perl:buster` - linux; amd64

```console
$ docker pull perl@sha256:9e616a049968731b2c73cf672e0b3e9a4be58bb7ea3b3e859ae748ea8ec094dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **327.6 MB (327597673 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c95429cf8ae49708df1aa6b491371eae362b58e4663c7bd8a2418b7219140e9c`
-	Default Command: `["perl5.38.2","-de0"]`

```dockerfile
# Thu, 21 Mar 2024 18:18:23 GMT
ADD file:c76ecdf17d2140aebb59f0261fd464e159af74b6489e79a1a10ad55941a63582 in / 
# Thu, 21 Mar 2024 18:18:23 GMT
CMD ["bash"]
# Thu, 21 Mar 2024 18:18:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 21 Mar 2024 18:18:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 21 Mar 2024 18:18:23 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 21 Mar 2024 18:18:23 GMT
WORKDIR /usr/src/perl
# Thu, 21 Mar 2024 18:18:23 GMT
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/P/PE/PEVANS/perl-5.38.2.tar.gz -o perl-5.38.2.tar.gz     && echo 'a0a31534451eb7b83c7d6594a497543a54d488bc90ca00f5e34762577f40655e *perl-5.38.2.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.38.2.tar.gz -C /usr/src/perl     && rm perl-5.38.2.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997014/cpm -o /usr/local/bin/cpm     && echo 'ee525f2493e36c6f688eddabaf53a51c4d3b2a4ebaa81576ac8b9f78ab57f4a1 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Thu, 21 Mar 2024 18:18:23 GMT
WORKDIR /usr/src/app
# Thu, 21 Mar 2024 18:18:23 GMT
CMD ["perl5.38.2" "-de0"]
```

-	Layers:
	-	`sha256:13dc5104e330a0605d2251ca4b7184ca5c05c0c068e626b00515daf54ba1a917`  
		Last Modified: Wed, 10 Apr 2024 01:56:34 GMT  
		Size: 50.5 MB (50504020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56a2be0394bca1f01401189d28d39b1fb8bded550d9905f371ad19c22c885f00`  
		Last Modified: Wed, 10 Apr 2024 05:36:56 GMT  
		Size: 17.6 MB (17585819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff192bd22402b8fc49beab8169860334a7e3ed795e392e8146c5ab943a7b5558`  
		Last Modified: Wed, 10 Apr 2024 05:37:12 GMT  
		Size: 51.9 MB (51895071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b021d9f9c794a69ecba98598d11f0a7ef02e0a248ee4a7333f38a9e7fdcdf0cb`  
		Last Modified: Wed, 10 Apr 2024 05:37:42 GMT  
		Size: 191.9 MB (191944262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cf19225dde8b618372345feda96271f37e3717000d7fb3193957774418741f0`  
		Last Modified: Wed, 10 Apr 2024 07:01:02 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46310d76e9c9a88675abf17b7ef558bbadc42eac9148d1fc5d865b11f6680e37`  
		Last Modified: Wed, 10 Apr 2024 07:01:02 GMT  
		Size: 15.7 MB (15668234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee8cf2443f4afea6b2b4798bf66092b5b79b95778cceabcf1224f41d6adb469c`  
		Last Modified: Wed, 10 Apr 2024 07:01:02 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:buster` - unknown; unknown

```console
$ docker pull perl@sha256:61aaa41e99ed77bc897cad3c64d93ab1f06722cdcb6300bde06d960087e145a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.6 MB (15625927 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:859c39f0a5be3c7331a32f700cade9c030121a62ca1ef6d5b14c967bf5c7f3d1`

```dockerfile
```

-	Layers:
	-	`sha256:c4513e85299e4aa60e29017af28a6fea6987896ef57234d93cd9b80ace24f74b`  
		Last Modified: Wed, 10 Apr 2024 07:01:02 GMT  
		Size: 15.6 MB (15609660 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1574410c33d11639b51c5b58d86f1a6122730e70da70f2f2226327173cdc25e5`  
		Last Modified: Wed, 10 Apr 2024 07:01:02 GMT  
		Size: 16.3 KB (16267 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:buster` - linux; arm variant v7

```console
$ docker pull perl@sha256:63992b79dee39c8b205c808acb6ebf75e0980d72143b5c5de6b9a1bd11260015
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.5 MB (292509272 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca794a463ea29e7a8d92f852e15e20c548318dc1e727a6933104e51af65ff247`
-	Default Command: `["perl5.38.2","-de0"]`

```dockerfile
# Fri, 23 Feb 2024 16:07:57 GMT
ADD file:5f3389726cf59e3b1d0650186a49490baa1e933702b9cf9df5fca7adacd54104 in / 
# Fri, 23 Feb 2024 16:07:57 GMT
CMD ["bash"]
# Fri, 23 Feb 2024 16:07:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 23 Feb 2024 16:07:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 23 Feb 2024 16:07:57 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 23 Feb 2024 16:07:57 GMT
WORKDIR /usr/src/perl
# Fri, 23 Feb 2024 16:07:57 GMT
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/P/PE/PEVANS/perl-5.38.2.tar.gz -o perl-5.38.2.tar.gz     && echo 'a0a31534451eb7b83c7d6594a497543a54d488bc90ca00f5e34762577f40655e *perl-5.38.2.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.38.2.tar.gz -C /usr/src/perl     && rm perl-5.38.2.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997014/cpm -o /usr/local/bin/cpm     && echo 'ee525f2493e36c6f688eddabaf53a51c4d3b2a4ebaa81576ac8b9f78ab57f4a1 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Fri, 23 Feb 2024 16:07:57 GMT
WORKDIR /usr/src/app
# Fri, 23 Feb 2024 16:07:57 GMT
CMD ["perl5.38.2" "-de0"]
```

-	Layers:
	-	`sha256:4218e49953a4d45c8fc0862a697fdc774311ff33abed887ac34cc7b5b03ef005`  
		Last Modified: Tue, 12 Mar 2024 01:04:44 GMT  
		Size: 46.0 MB (45967270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ef5888a68a0506ce77bb71273482bc253eb745caed538f2af7471c91fef2983`  
		Last Modified: Tue, 12 Mar 2024 02:22:23 GMT  
		Size: 16.2 MB (16216521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec28d557d3104596d3ba5ab227e1e527ff8f93195f04af289dd5da1316ba29d9`  
		Last Modified: Tue, 12 Mar 2024 02:22:40 GMT  
		Size: 47.4 MB (47410735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb141b0531169976182ab39baba3c902bed903a2c25a2e2045f8c6cee114563c`  
		Last Modified: Tue, 12 Mar 2024 02:23:15 GMT  
		Size: 168.1 MB (168133921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:489ac8fb666ed52eb6c4a405ad038d8af77ccfd6ba94d5fd104f7cd60e39f1f0`  
		Last Modified: Wed, 13 Mar 2024 01:14:06 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac5445c0ee8c66c01fb5e83d3e9beab1d163728118283d89ab95e82642abbf5b`  
		Last Modified: Wed, 13 Mar 2024 01:14:08 GMT  
		Size: 14.8 MB (14780559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6d3c98035a5f71427a997372b3359a5fa0ff2d35655684ec8c7148cf2856de0`  
		Last Modified: Wed, 13 Mar 2024 01:14:08 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:buster` - unknown; unknown

```console
$ docker pull perl@sha256:e63bfd4e9c51d4eda814e7d5dcbb248d0431ef80e698ff6a35ea2cff27d35ddb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 MB (15427972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:336d81f253955885f42b303cc54f32586f491c950a57494b489a780f16088316`

```dockerfile
```

-	Layers:
	-	`sha256:127f72808ce4dbca873976e8bdadedf86d6e8c78bc972fc482f742445ab4b0f9`  
		Last Modified: Wed, 13 Mar 2024 01:14:06 GMT  
		Size: 15.4 MB (15411626 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:068711b6c7bf7a76374cecc0cce547d00b29b540c88c5e83656a0f3df531a16f`  
		Last Modified: Wed, 13 Mar 2024 01:14:05 GMT  
		Size: 16.3 KB (16346 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:buster` - linux; arm64 variant v8

```console
$ docker pull perl@sha256:dc3d6138b6800c0e5505c96ca526a405d30591bd8fa8a07226adef9aaddee0c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **318.1 MB (318095498 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c08780913d2a085a9c5b3b0b8e2222ada1c6d17a1b6a034c08ca4701ff1d865b`
-	Default Command: `["perl5.38.2","-de0"]`

```dockerfile
# Fri, 23 Feb 2024 16:07:57 GMT
ADD file:969a4e1bb3ace306012b0fdb34a936b1c5aff4ed7670a054b38ce31e3c70ddcb in / 
# Fri, 23 Feb 2024 16:07:57 GMT
CMD ["bash"]
# Fri, 23 Feb 2024 16:07:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 23 Feb 2024 16:07:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 23 Feb 2024 16:07:57 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 23 Feb 2024 16:07:57 GMT
WORKDIR /usr/src/perl
# Fri, 23 Feb 2024 16:07:57 GMT
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/P/PE/PEVANS/perl-5.38.2.tar.gz -o perl-5.38.2.tar.gz     && echo 'a0a31534451eb7b83c7d6594a497543a54d488bc90ca00f5e34762577f40655e *perl-5.38.2.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.38.2.tar.gz -C /usr/src/perl     && rm perl-5.38.2.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997014/cpm -o /usr/local/bin/cpm     && echo 'ee525f2493e36c6f688eddabaf53a51c4d3b2a4ebaa81576ac8b9f78ab57f4a1 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Fri, 23 Feb 2024 16:07:57 GMT
WORKDIR /usr/src/app
# Fri, 23 Feb 2024 16:07:57 GMT
CMD ["perl5.38.2" "-de0"]
```

-	Layers:
	-	`sha256:8f2867cba3550760f11e3707290af4ab014e08a6171620407549210c558e3429`  
		Last Modified: Tue, 12 Mar 2024 00:49:48 GMT  
		Size: 49.3 MB (49289836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f662d0fd286524f0287f1ab689d234c733c6bd6efb38a645b2231168bbe94949`  
		Last Modified: Tue, 12 Mar 2024 01:36:44 GMT  
		Size: 17.5 MB (17455473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8987ebef52bd1e6f6f20b38f5dd0fa9030c75a5089144eabf4a20c7b2aa2605a`  
		Last Modified: Tue, 12 Mar 2024 01:36:57 GMT  
		Size: 52.2 MB (52225028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fe09b4296b95b0c32948c55d4f978937b58f5a899208693bb4c304804492322`  
		Last Modified: Tue, 12 Mar 2024 01:37:27 GMT  
		Size: 183.5 MB (183517797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95ecf2bdf0a8342978e12ddb18e41908f67f647b04f3758fad716598257f6d86`  
		Last Modified: Tue, 12 Mar 2024 22:57:22 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4aaf9e8eac1ff1f58af04d012497fa750b585da1ad421d9a287609dbb14744f3`  
		Last Modified: Tue, 12 Mar 2024 22:57:24 GMT  
		Size: 15.6 MB (15607098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebc38de4e83206dfec06f79761abbc00097bd620c99460cb7606f7d9fc79a9fc`  
		Last Modified: Tue, 12 Mar 2024 22:57:24 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:buster` - unknown; unknown

```console
$ docker pull perl@sha256:7232d033cd99644a930a03d821950fbb088a8a6604581c8b6b7ba2f16629a572
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.6 MB (15616607 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b292896105edd7de0b30dd385894b4a240a56390baa490ce970a2da80535df58`

```dockerfile
```

-	Layers:
	-	`sha256:9e9449c1b309d7d1c562ca6b5af29e67937526516201bda7453bbd5a3dafaff5`  
		Last Modified: Tue, 12 Mar 2024 22:57:23 GMT  
		Size: 15.6 MB (15600327 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ab273ac2df4f5808b3b79f80086af226dca2df83fb1e3009e3c5e61f8ad8f517`  
		Last Modified: Tue, 12 Mar 2024 22:57:22 GMT  
		Size: 16.3 KB (16280 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:buster` - linux; 386

```console
$ docker pull perl@sha256:1101bd0da057584a5277da1d46eb6000687bcc39e8b9f8d63ad1b3e06d0395f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **336.5 MB (336520925 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53f51c765b86b32bd0c60328fb3695941b670c866015e1b9e62b92c2945e35e9`
-	Default Command: `["perl5.38.2","-de0"]`

```dockerfile
# Thu, 21 Mar 2024 18:18:23 GMT
ADD file:b0be520dbc93fbc08e051c8ea8793595dbd38e91643b1d941ad956d2a4397f8f in / 
# Thu, 21 Mar 2024 18:18:23 GMT
CMD ["bash"]
# Thu, 21 Mar 2024 18:18:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 21 Mar 2024 18:18:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 21 Mar 2024 18:18:23 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 21 Mar 2024 18:18:23 GMT
WORKDIR /usr/src/perl
# Thu, 21 Mar 2024 18:18:23 GMT
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/P/PE/PEVANS/perl-5.38.2.tar.gz -o perl-5.38.2.tar.gz     && echo 'a0a31534451eb7b83c7d6594a497543a54d488bc90ca00f5e34762577f40655e *perl-5.38.2.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.38.2.tar.gz -C /usr/src/perl     && rm perl-5.38.2.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997014/cpm -o /usr/local/bin/cpm     && echo 'ee525f2493e36c6f688eddabaf53a51c4d3b2a4ebaa81576ac8b9f78ab57f4a1 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Thu, 21 Mar 2024 18:18:23 GMT
WORKDIR /usr/src/app
# Thu, 21 Mar 2024 18:18:23 GMT
CMD ["perl5.38.2" "-de0"]
```

-	Layers:
	-	`sha256:f0d58f6fa9239b96dd44a4bb70c4da4650d0ca0b4b35f492bda37d153b9ed6ba`  
		Last Modified: Wed, 10 Apr 2024 01:03:15 GMT  
		Size: 51.3 MB (51256498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f83de192d57649c06466addcbc7b9ccd636e9d291c22fdf5d7e4a4e6c59450d`  
		Last Modified: Wed, 10 Apr 2024 08:08:28 GMT  
		Size: 18.1 MB (18099188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59bc8c20df52365967a4f48f20656372016f14141f60753323f354ed4eca05f0`  
		Last Modified: Wed, 10 Apr 2024 08:08:48 GMT  
		Size: 53.5 MB (53492155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1042163e6e1fe3d8805f02202161cd324efea6901ddca3f722950dc6c835431b`  
		Last Modified: Wed, 10 Apr 2024 08:09:32 GMT  
		Size: 198.5 MB (198498026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf8aeacbe4372456607acba0749f9b47c84515d2bcb3e6698d5a35db23d19510`  
		Last Modified: Wed, 10 Apr 2024 09:03:11 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ceb7cf30cc4b5c139b156d59fc755e8cc8bd69a1287c0230b166f75bf1e62e7`  
		Last Modified: Wed, 10 Apr 2024 09:03:12 GMT  
		Size: 15.2 MB (15174791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1183ebea0a5ae9d8f203b905cee2ae8853652fcc4c72f8ca5a1c8fb21533e629`  
		Last Modified: Wed, 10 Apr 2024 09:03:10 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:buster` - unknown; unknown

```console
$ docker pull perl@sha256:c61f54c04b2d70ae9183cb2d44802e19b3a0820655c13bd8581b7237a5d892a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.6 MB (15631475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc47145b94c4a85c88cb39f873b0dda4b5c48d16de60efbdd8460318a15166d3`

```dockerfile
```

-	Layers:
	-	`sha256:08bd8d632d6f14a1e59f59bdaf74b5ee2798502aba6b8b6390d06237809c20d9`  
		Last Modified: Wed, 10 Apr 2024 09:03:11 GMT  
		Size: 15.6 MB (15615242 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:efa3aea62419c1e00f9fd09764271aa8d4e8dafdba5a0da9fe918111f44e5898`  
		Last Modified: Wed, 10 Apr 2024 09:03:10 GMT  
		Size: 16.2 KB (16233 bytes)  
		MIME: application/vnd.in-toto+json
