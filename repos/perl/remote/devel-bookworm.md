## `perl:devel-bookworm`

```console
$ docker pull perl@sha256:90d29068df4cc31988afb926257a78d39db2531dc468a3eb19bb092c463fc585
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
$ docker pull perl@sha256:b5b27b50236a1fc2d688e9c22acc98f74ed9895ed81a588b55f05400b547eb08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **364.9 MB (364911594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff7500cda77c1ef81dde917e4e70ddd77dc04838e80031479dcf331bbec0ec3e`
-	Default Command: `["perl5.39.10","-de0"]`

```dockerfile
# Mon, 29 Apr 2024 09:51:00 GMT
ADD file:b9a9fc37b874060c713002ae1ac220f097edd7c6576116c22bb15aad8229b1b3 in / 
# Mon, 29 Apr 2024 09:51:00 GMT
CMD ["bash"]
# Mon, 29 Apr 2024 09:51:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 29 Apr 2024 09:51:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 29 Apr 2024 09:51:00 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 29 Apr 2024 09:51:00 GMT
WORKDIR /usr/src/perl
# Mon, 29 Apr 2024 09:51:00 GMT
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/P/PE/PEVANS/perl-5.39.10.tar.gz -o perl-5.39.10.tar.gz     && echo '4b7ffb3e068583fa5c8413390c998b2c15214f205ce737acc485b40932b9f419 *perl-5.39.10.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.39.10.tar.gz -C /usr/src/perl     && rm perl-5.39.10.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997014/cpm -o /usr/local/bin/cpm     && echo 'ee525f2493e36c6f688eddabaf53a51c4d3b2a4ebaa81576ac8b9f78ab57f4a1 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Mon, 29 Apr 2024 09:51:00 GMT
WORKDIR /usr/src/app
# Mon, 29 Apr 2024 09:51:00 GMT
CMD ["perl5.39.10" "-de0"]
```

-	Layers:
	-	`sha256:c6cf28de8a067787ee0d08f8b01d7f1566a508b56f6e549687b41dfd375f12c7`  
		Last Modified: Tue, 14 May 2024 01:32:07 GMT  
		Size: 49.6 MB (49576390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:891494355808bdd3db5552f0d3723fd0fa826675f774853796fafa221d850d42`  
		Last Modified: Tue, 14 May 2024 03:04:06 GMT  
		Size: 24.1 MB (24050100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6582c62583ef22717db8d306b1d6a0c288089ff607d9c0d2d81c4f8973cbfee3`  
		Last Modified: Tue, 14 May 2024 03:04:25 GMT  
		Size: 64.1 MB (64142371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf2c3e352f3d2eed4eda4feeed44a1022a881058df20ac0584db70c138b041e2`  
		Last Modified: Tue, 14 May 2024 03:05:02 GMT  
		Size: 211.2 MB (211207185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8a8ab4e309de18fdfef00d08b1897b9f80f3ca59c08477bb1ef1b9f4576beda`  
		Last Modified: Tue, 14 May 2024 04:04:44 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:748ee8454856f7732a48496b35c21b51b7be8a573ae32a385a8835aef5bf3720`  
		Last Modified: Tue, 14 May 2024 04:05:04 GMT  
		Size: 15.9 MB (15935285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dd6c5a322fdee804b6fc92bcffc0f5ba13882ce9f4a258599843533ff95391c`  
		Last Modified: Tue, 14 May 2024 04:04:58 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-bookworm` - unknown; unknown

```console
$ docker pull perl@sha256:73379860cdb2be1182bc3869d1a2a3c257ce2a5322f53ca5933f1252e4190098
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 MB (15386003 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2448a14f5a441d516c1cb8ebc8af1ddc4b5c25817d158e613d53ff40718c3bd`

```dockerfile
```

-	Layers:
	-	`sha256:468753187e003ecae63d02e088b7e97c96d7a4d82bd4ab0dd51560a315b6b7a9`  
		Last Modified: Tue, 14 May 2024 04:04:59 GMT  
		Size: 15.4 MB (15369334 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2d419ce7aa050b3d012e9c652f284042cc30c83023ee80c0c9b75f8264b37f5b`  
		Last Modified: Tue, 14 May 2024 04:04:58 GMT  
		Size: 16.7 KB (16669 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-bookworm` - linux; arm variant v5

```console
$ docker pull perl@sha256:a16ab9f4559b4608b11a5877ced845137679738e9667a8c554dccc8ab08a49f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **331.3 MB (331325101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb0b39d66e033cf773283ebe5de77b9ce3a451bf04d99cc578728c41a96ec66f`
-	Default Command: `["perl5.39.10","-de0"]`

```dockerfile
# Mon, 29 Apr 2024 09:51:00 GMT
ADD file:cd62e5a70676cac6ab9314bf7583f7ed4056908c492f302f1243edbd35066bfd in / 
# Mon, 29 Apr 2024 09:51:00 GMT
CMD ["bash"]
# Mon, 29 Apr 2024 09:51:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 29 Apr 2024 09:51:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 29 Apr 2024 09:51:00 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 29 Apr 2024 09:51:00 GMT
WORKDIR /usr/src/perl
# Mon, 29 Apr 2024 09:51:00 GMT
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/P/PE/PEVANS/perl-5.39.10.tar.gz -o perl-5.39.10.tar.gz     && echo '4b7ffb3e068583fa5c8413390c998b2c15214f205ce737acc485b40932b9f419 *perl-5.39.10.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.39.10.tar.gz -C /usr/src/perl     && rm perl-5.39.10.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997014/cpm -o /usr/local/bin/cpm     && echo 'ee525f2493e36c6f688eddabaf53a51c4d3b2a4ebaa81576ac8b9f78ab57f4a1 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Mon, 29 Apr 2024 09:51:00 GMT
WORKDIR /usr/src/app
# Mon, 29 Apr 2024 09:51:00 GMT
CMD ["perl5.39.10" "-de0"]
```

-	Layers:
	-	`sha256:ec3129b1f3b893a7412a0ac12044f811ed32ddf7028d374141819005f9d4699f`  
		Last Modified: Tue, 14 May 2024 00:51:10 GMT  
		Size: 47.3 MB (47338294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c8516852dedc6ef6e011322d36853e449786d3c2d43553864edbb79abbe0ca5`  
		Last Modified: Tue, 14 May 2024 01:21:47 GMT  
		Size: 22.7 MB (22728407 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90f71408c4e77f143b3e9d4c1401b7c778766c63dc79d80a05870500825e7c8c`  
		Last Modified: Tue, 14 May 2024 01:22:09 GMT  
		Size: 61.5 MB (61517869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:779bb0cc1f42107df5966cbf82ca7be2fb113ac0edf35633f10fbd5d5cce3ada`  
		Last Modified: Tue, 14 May 2024 01:22:47 GMT  
		Size: 184.5 MB (184522613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:382d00edb7bb4141b1d16edacee7312590f10ec40758b551e1f9387a4a848732`  
		Last Modified: Tue, 14 May 2024 15:11:07 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a1344a8a5ae566f19ffc6347c7666e612c3a129641a28ce9f0e82efe65090fc`  
		Last Modified: Tue, 14 May 2024 17:31:32 GMT  
		Size: 15.2 MB (15217652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:295d1ba13c4dd3146822dd6b13ed497e7ea29d0de149a3161a10f6d2024f1880`  
		Last Modified: Tue, 14 May 2024 17:31:31 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-bookworm` - unknown; unknown

```console
$ docker pull perl@sha256:bf018690b53aa41371089a63741a4787444a0941b6b5fb85751889bada80ecc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.2 MB (15185804 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4f36745a63579c233202d3984d423276cd67a1ea2aed70a73fbf9a8bbb7326d`

```dockerfile
```

-	Layers:
	-	`sha256:7503f33dee8d3d9d196ed18c7d2af7ef5fa1536d14961f23eccd99b1250fc2a6`  
		Last Modified: Tue, 14 May 2024 17:31:32 GMT  
		Size: 15.2 MB (15169712 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f575c48a0aa8a977cc04c5e817d9d9365e5bdf58add64fb1c78b8caaf6b8bd9b`  
		Last Modified: Tue, 14 May 2024 17:31:31 GMT  
		Size: 16.1 KB (16092 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-bookworm` - linux; arm variant v7

```console
$ docker pull perl@sha256:91499c630fd9051484ef4341b07c30b3a34cb631a4be78ff57bf8ae5a5ac76b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **316.5 MB (316519905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba4900dc20773b2ec5d6415a9b2f64d4e380dd59c1219712a7a64d5af08ebfc7`
-	Default Command: `["perl5.39.10","-de0"]`

```dockerfile
# Mon, 29 Apr 2024 09:51:00 GMT
ADD file:1e106a38a0e44ca74d4d29c6d797780e7a29ffe249e473c48ee2aea553fc013b in / 
# Mon, 29 Apr 2024 09:51:00 GMT
CMD ["bash"]
# Mon, 29 Apr 2024 09:51:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 29 Apr 2024 09:51:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 29 Apr 2024 09:51:00 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 29 Apr 2024 09:51:00 GMT
WORKDIR /usr/src/perl
# Mon, 29 Apr 2024 09:51:00 GMT
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/P/PE/PEVANS/perl-5.39.10.tar.gz -o perl-5.39.10.tar.gz     && echo '4b7ffb3e068583fa5c8413390c998b2c15214f205ce737acc485b40932b9f419 *perl-5.39.10.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.39.10.tar.gz -C /usr/src/perl     && rm perl-5.39.10.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997014/cpm -o /usr/local/bin/cpm     && echo 'ee525f2493e36c6f688eddabaf53a51c4d3b2a4ebaa81576ac8b9f78ab57f4a1 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Mon, 29 Apr 2024 09:51:00 GMT
WORKDIR /usr/src/app
# Mon, 29 Apr 2024 09:51:00 GMT
CMD ["perl5.39.10" "-de0"]
```

-	Layers:
	-	`sha256:dfc3b4ca62816a9cbf2bdfbdd78bf692a522e7f48a280492b9f87d55b2f4aa2e`  
		Last Modified: Tue, 14 May 2024 01:12:21 GMT  
		Size: 45.2 MB (45174745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:641d6443415d538c3bf0e0d6ecc0f6b7603b4caf6c79708d0670bc082e9721c5`  
		Last Modified: Tue, 14 May 2024 01:46:47 GMT  
		Size: 22.0 MB (21953893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94dd085f2eef9c35615ce8d6f2e7b6340a6bcadb37fe8fd6698911eab87e371c`  
		Last Modified: Tue, 14 May 2024 01:47:09 GMT  
		Size: 59.2 MB (59217124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb1ddacc8c148925155abdd912bfb78a553326599c4da7b21c01a76f7616a464`  
		Last Modified: Tue, 14 May 2024 01:47:48 GMT  
		Size: 175.2 MB (175175139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abb4e06d7ba8ed3c651052596293309bb6403d235c1dbf7f39b9cd875480a4d6`  
		Last Modified: Wed, 15 May 2024 04:25:16 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b2c952ae172a70a94a24919bfe12e96c9bdc5b811bd483572b7edb0ea928a87`  
		Last Modified: Wed, 15 May 2024 06:45:25 GMT  
		Size: 15.0 MB (14998739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:505bcbf9943b3cb0c083d20f9320cca4cf7fd05622b14b6a89312df7ad40de38`  
		Last Modified: Wed, 15 May 2024 06:45:24 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-bookworm` - unknown; unknown

```console
$ docker pull perl@sha256:c657e0374787ffd34a423857428a391b3609d119893b79ef536ff5842ea74dc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.2 MB (15191278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf47bbb135cdb57ef69f67244c27a77f59c4a4e576048ddca2eda241afa1502e`

```dockerfile
```

-	Layers:
	-	`sha256:2f14d93092b2d9137ac6242db9d45acb380c12aaec710af2fae33162d2422b91`  
		Last Modified: Wed, 15 May 2024 06:45:25 GMT  
		Size: 15.2 MB (15175186 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:407f3d8dbd9470d338bdaa58adb3170ff51aae08b6e13d351f80d00aee4921f3`  
		Last Modified: Wed, 15 May 2024 06:45:24 GMT  
		Size: 16.1 KB (16092 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-bookworm` - linux; arm64 variant v8

```console
$ docker pull perl@sha256:9f8393ed2d24891c9a9e5941fcd3be4842b2df06abf0c93fcb25afa744890475
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **355.7 MB (355658993 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54f3e27903d695a32845f6ba31bfebe3412c72b509c76827c97d06e9cf26a3db`
-	Default Command: `["perl5.39.10","-de0"]`

```dockerfile
# Wed, 24 Apr 2024 04:10:30 GMT
ADD file:07ae70ad05f39a24007b6bde4418c9934bc3865fe855dfcf62a44d8a30375739 in / 
# Wed, 24 Apr 2024 04:10:31 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 08:32:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 08:32:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 08:33:19 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 29 Apr 2024 09:51:00 GMT
WORKDIR /usr/src/perl
# Mon, 29 Apr 2024 09:51:00 GMT
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/P/PE/PEVANS/perl-5.39.10.tar.gz -o perl-5.39.10.tar.gz     && echo '4b7ffb3e068583fa5c8413390c998b2c15214f205ce737acc485b40932b9f419 *perl-5.39.10.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.39.10.tar.gz -C /usr/src/perl     && rm perl-5.39.10.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997014/cpm -o /usr/local/bin/cpm     && echo 'ee525f2493e36c6f688eddabaf53a51c4d3b2a4ebaa81576ac8b9f78ab57f4a1 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Mon, 29 Apr 2024 09:51:00 GMT
WORKDIR /usr/src/app
# Mon, 29 Apr 2024 09:51:00 GMT
CMD ["perl5.39.10" "-de0"]
```

-	Layers:
	-	`sha256:60bdaf986dbe787297bb85c9f6a28d13ea7b9608b95206ef7ce6cdea50cd5505`  
		Last Modified: Wed, 24 Apr 2024 04:13:43 GMT  
		Size: 49.6 MB (49613341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e100ddc6b415c632410507293430c0fe6bb4228ab320ed59548c6dc030b4e4a`  
		Last Modified: Wed, 24 Apr 2024 08:41:28 GMT  
		Size: 23.6 MB (23586795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba9a57bc3c0cb0c1ea5d28dc03fb4451ae05dc271b53941c27edf70eaf70b6e6`  
		Last Modified: Wed, 24 Apr 2024 08:41:47 GMT  
		Size: 64.0 MB (63994806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7476478a1e1450b999421118cb8f193aa62f1816e0cadd988a084385cf0a5696`  
		Last Modified: Wed, 24 Apr 2024 08:42:20 GMT  
		Size: 202.6 MB (202575289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4134be3c1b4a49cdf7692197a2226b0bb514f0cdb490ffc740deb64d13bdc933`  
		Last Modified: Tue, 30 Apr 2024 04:50:41 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ff525f59b7573530bd502e60f608241e5e3240969afcc5e76d52107775774c3`  
		Last Modified: Tue, 30 Apr 2024 04:50:42 GMT  
		Size: 15.9 MB (15888497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13274147421901585903dd9827ad1b0274bca0930b3d8598c7a192a8eb0e17ec`  
		Last Modified: Tue, 30 Apr 2024 04:50:41 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-bookworm` - unknown; unknown

```console
$ docker pull perl@sha256:25384a4b8ac63a42150574b10a77a2c66c9b1a6e3707ad176a9fdb09bf5fb789
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 MB (15414388 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b656c7c127186f5ca0083517d2bdccc5f8bfab5928bb8495ce798727e4b039d7`

```dockerfile
```

-	Layers:
	-	`sha256:b0034fe8c8e0d2035e3a615888a7024d7c904d2579d852954f37e02a1963641f`  
		Last Modified: Tue, 30 Apr 2024 04:50:42 GMT  
		Size: 15.4 MB (15397705 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f8a3213a8b5c47022f075c7a2de196a83624d0d5c19067b10f8f731e9dfad0aa`  
		Last Modified: Tue, 30 Apr 2024 04:50:41 GMT  
		Size: 16.7 KB (16683 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-bookworm` - linux; 386

```console
$ docker pull perl@sha256:d35f35c7508f54443ec7b0edfbc7fe589bbeea3d015c95ce0d29c298daf13a39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **367.0 MB (367037798 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd9e4af0482d153cb5d76228ac322e2f0dbc25b311317fdeaa669705ff978043`
-	Default Command: `["perl5.39.10","-de0"]`

```dockerfile
# Mon, 29 Apr 2024 09:51:00 GMT
ADD file:35709674a3b845511a896af16ea37a6022e7d48992d3198d0760c0c3208fe4ed in / 
# Mon, 29 Apr 2024 09:51:00 GMT
CMD ["bash"]
# Mon, 29 Apr 2024 09:51:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 29 Apr 2024 09:51:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 29 Apr 2024 09:51:00 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 29 Apr 2024 09:51:00 GMT
WORKDIR /usr/src/perl
# Mon, 29 Apr 2024 09:51:00 GMT
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/P/PE/PEVANS/perl-5.39.10.tar.gz -o perl-5.39.10.tar.gz     && echo '4b7ffb3e068583fa5c8413390c998b2c15214f205ce737acc485b40932b9f419 *perl-5.39.10.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.39.10.tar.gz -C /usr/src/perl     && rm perl-5.39.10.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997014/cpm -o /usr/local/bin/cpm     && echo 'ee525f2493e36c6f688eddabaf53a51c4d3b2a4ebaa81576ac8b9f78ab57f4a1 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Mon, 29 Apr 2024 09:51:00 GMT
WORKDIR /usr/src/app
# Mon, 29 Apr 2024 09:51:00 GMT
CMD ["perl5.39.10" "-de0"]
```

-	Layers:
	-	`sha256:4f2f2f6205661e555e772749ae7fd294fb04fc0d06cbc67a50a11fbb4ef44242`  
		Last Modified: Tue, 14 May 2024 00:51:31 GMT  
		Size: 50.6 MB (50602424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d849fa81a6965e2bbc8dd9af462f55a46b59aeb701fb0a26992522fd43ce5c03`  
		Last Modified: Tue, 14 May 2024 09:13:04 GMT  
		Size: 24.9 MB (24888551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5d6250e2e75fd4f1cdc533096df2c601817950e8c3f1096f46dfeea2b609cee`  
		Last Modified: Tue, 14 May 2024 09:13:29 GMT  
		Size: 66.0 MB (65988940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54e0a2d5e90c1a7093dbeeaddbb7c833c828015d2e8991c1721c4a269c4faf42`  
		Last Modified: Tue, 14 May 2024 09:14:20 GMT  
		Size: 210.1 MB (210128367 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25b8a4c562b195023e801319b6943753da8a644bda1149834621602af9f9ef6e`  
		Last Modified: Tue, 14 May 2024 10:05:58 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:def4497984588c58169cb311673340be416f9446e4d64b26d99db39f6f9a2ef7`  
		Last Modified: Tue, 14 May 2024 10:05:59 GMT  
		Size: 15.4 MB (15429252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f28661e531f2116d80471f69ac773e28cb33d58333f38ee947ab70cbce0346b7`  
		Last Modified: Tue, 14 May 2024 10:05:59 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-bookworm` - unknown; unknown

```console
$ docker pull perl@sha256:0935f729f085042b7afbda564ef16d3b74b3d650960abb47221278f576124fc0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 MB (15365021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49b5282e33ab42ed9f890a9503cd922c2a3e74a7a8a972967792a438b28d36ae`

```dockerfile
```

-	Layers:
	-	`sha256:82dfae568495fe35566047528ed8a2ae7ef889da64b715da02b198f2849c67ea`  
		Last Modified: Tue, 14 May 2024 10:05:59 GMT  
		Size: 15.3 MB (15348391 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:14bfd313267196edecc9887ec42300eb32ae3970c8233e86fca7eed93f732662`  
		Last Modified: Tue, 14 May 2024 10:05:59 GMT  
		Size: 16.6 KB (16630 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-bookworm` - linux; mips64le

```console
$ docker pull perl@sha256:66a14f154ad1573f9b7fdde75db8cb67023903f85f094cd33c494d3440d2c969
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **340.9 MB (340873931 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:029fdf3f60c8f4c91aebe89446a81c214c64761a2300e39e11661826cc5f4a37`
-	Default Command: `["perl5.39.10","-de0"]`

```dockerfile
# Wed, 24 Apr 2024 03:13:30 GMT
ADD file:bd5e48bc3973f1ba0b2958f5feb2ef619d1da33cebe3daa160741598f3a64020 in / 
# Wed, 24 Apr 2024 03:13:35 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 03:54:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 03:56:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 04:01:35 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 29 Apr 2024 09:51:00 GMT
WORKDIR /usr/src/perl
# Mon, 29 Apr 2024 09:51:00 GMT
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/P/PE/PEVANS/perl-5.39.10.tar.gz -o perl-5.39.10.tar.gz     && echo '4b7ffb3e068583fa5c8413390c998b2c15214f205ce737acc485b40932b9f419 *perl-5.39.10.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.39.10.tar.gz -C /usr/src/perl     && rm perl-5.39.10.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997014/cpm -o /usr/local/bin/cpm     && echo 'ee525f2493e36c6f688eddabaf53a51c4d3b2a4ebaa81576ac8b9f78ab57f4a1 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Mon, 29 Apr 2024 09:51:00 GMT
WORKDIR /usr/src/app
# Mon, 29 Apr 2024 09:51:00 GMT
CMD ["perl5.39.10" "-de0"]
```

-	Layers:
	-	`sha256:128b5268b494ed46f2601900fdc8201341f67542053dd84964164d230083ab26`  
		Last Modified: Wed, 24 Apr 2024 03:24:37 GMT  
		Size: 49.6 MB (49582786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1db7c75a6accf74d8a7a5baea9ca05e0af438c130a33d48ca96a5c26a8fd29ff`  
		Last Modified: Wed, 24 Apr 2024 04:30:27 GMT  
		Size: 23.4 MB (23438128 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e32516c9efb0754d31d8a9019f45fa9c88d3bdc96aca1c8a6cced34b949b6b7`  
		Last Modified: Wed, 24 Apr 2024 04:31:20 GMT  
		Size: 63.0 MB (62968465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6017c9766ed85b6acea7bb176207059bcb96d8c5056168e97cb57dd3a2b5c7e`  
		Last Modified: Wed, 24 Apr 2024 04:33:29 GMT  
		Size: 189.7 MB (189742660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c39b049e807d28a87a1ce1bef0b65108bbf7f8045118408b1714f5e80a36e205`  
		Last Modified: Mon, 29 Apr 2024 20:00:27 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90277f37367f4aa703d26912d1d8903e8b337ece7f8cba9f1654abbafd1e14f6`  
		Last Modified: Mon, 29 Apr 2024 20:00:29 GMT  
		Size: 15.1 MB (15141627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7a6ffe49d97e5e7198e3d0abad94d0a793720a45aa232d0e8c6780511ab4964`  
		Last Modified: Mon, 29 Apr 2024 20:00:27 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-bookworm` - unknown; unknown

```console
$ docker pull perl@sha256:2a2aa7ba2b1b172fc617df57da2a0b27c22d85d0ddac5c1ac92da00cb9c58c12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.5 KB (16523 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:638ad89d02e60460b9c893f9dd0a69ddeb80b97502ec55578dd3658d00854bf8`

```dockerfile
```

-	Layers:
	-	`sha256:16f60c591560fa091de17eccc5ad594d671a7d8bcd85c6e696d82d4694c4068a`  
		Last Modified: Mon, 29 Apr 2024 20:00:27 GMT  
		Size: 16.5 KB (16523 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-bookworm` - linux; ppc64le

```console
$ docker pull perl@sha256:1c2f9aa3f494263f2de3abb8a36c5b9e8a1f340f6ec1d8086da994503f82ab9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **379.0 MB (379030819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f3c56c432d69e28aabbb87cfd28b8a1d6c1c995fca0c3554489ede30315489e`
-	Default Command: `["perl5.39.10","-de0"]`

```dockerfile
# Mon, 29 Apr 2024 09:51:00 GMT
ADD file:fdb5c89e2970bd3b21a7b4e39491c1719b957f54babefd52ad455ea72a77bd3f in / 
# Mon, 29 Apr 2024 09:51:00 GMT
CMD ["bash"]
# Mon, 29 Apr 2024 09:51:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 29 Apr 2024 09:51:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 29 Apr 2024 09:51:00 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 29 Apr 2024 09:51:00 GMT
WORKDIR /usr/src/perl
# Mon, 29 Apr 2024 09:51:00 GMT
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/P/PE/PEVANS/perl-5.39.10.tar.gz -o perl-5.39.10.tar.gz     && echo '4b7ffb3e068583fa5c8413390c998b2c15214f205ce737acc485b40932b9f419 *perl-5.39.10.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.39.10.tar.gz -C /usr/src/perl     && rm perl-5.39.10.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997014/cpm -o /usr/local/bin/cpm     && echo 'ee525f2493e36c6f688eddabaf53a51c4d3b2a4ebaa81576ac8b9f78ab57f4a1 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Mon, 29 Apr 2024 09:51:00 GMT
WORKDIR /usr/src/app
# Mon, 29 Apr 2024 09:51:00 GMT
CMD ["perl5.39.10" "-de0"]
```

-	Layers:
	-	`sha256:9027b64136d8b1ece1ad24cca3199e496689a33f47b8d112dbdd112c682e665f`  
		Last Modified: Tue, 14 May 2024 01:23:40 GMT  
		Size: 53.6 MB (53579748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18e147daa0a988c77940b565d177a661a73270a0e821c65283b9e531ae38ebc4`  
		Last Modified: Tue, 14 May 2024 07:10:25 GMT  
		Size: 25.7 MB (25699676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b88d9ff0405bb000dedfa15a3a34739370c3daa10367599bff02a57fd19a3564`  
		Last Modified: Tue, 14 May 2024 07:10:47 GMT  
		Size: 69.6 MB (69584088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b80be54620660eb7b908f8c79a7ad14bedcac29ae46f620f4ede820441dc65d`  
		Last Modified: Tue, 14 May 2024 07:11:29 GMT  
		Size: 214.2 MB (214234653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48db44180cd4b960d87217d1d2cf26fe6c49229b345e25566eb8aa5e5ed4f705`  
		Last Modified: Wed, 15 May 2024 01:28:49 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91fe12ff52226127a564cc322cda22a433420d8decc3c5566b889c1d7fb18967`  
		Last Modified: Wed, 15 May 2024 02:47:27 GMT  
		Size: 15.9 MB (15932391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edc57ffa4570c55448464db8cddc05c6c4f7e1a9cfc28524411a031120fbc588`  
		Last Modified: Wed, 15 May 2024 02:47:26 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-bookworm` - unknown; unknown

```console
$ docker pull perl@sha256:b7e5e436561a738bd60fbaa0c8364214400f6d0d359b050ea51429a5dd7fbe5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 MB (15362076 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:814826e4529d553e45d2aa4981debb45694af6463470788b58e9b25fce7c6d19`

```dockerfile
```

-	Layers:
	-	`sha256:6fe784e7c4b4ca226f4a5f28492052c880118fa056f764b58121afd79cb56a62`  
		Last Modified: Wed, 15 May 2024 02:47:27 GMT  
		Size: 15.3 MB (15346020 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:03a6df14bb37e405ff947d611e09ff7c7f342dbcd90bc366ca64a53d277b1c93`  
		Last Modified: Wed, 15 May 2024 02:47:26 GMT  
		Size: 16.1 KB (16056 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-bookworm` - linux; s390x

```console
$ docker pull perl@sha256:a764f4076f02d0912db13404c34b3d9825663b1ed94c59317a3492b715f47e74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **334.6 MB (334624571 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65a1ec5ad01a9bae3fbd7f86b3a550db134c08edff0170e47fa48a1a86918bbe`
-	Default Command: `["perl5.39.10","-de0"]`

```dockerfile
# Mon, 29 Apr 2024 09:51:00 GMT
ADD file:d24c16f113416f94273813df324360fe934245f0f7f2973b6def2799e5605f1f in / 
# Mon, 29 Apr 2024 09:51:00 GMT
CMD ["bash"]
# Mon, 29 Apr 2024 09:51:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 29 Apr 2024 09:51:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 29 Apr 2024 09:51:00 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 29 Apr 2024 09:51:00 GMT
WORKDIR /usr/src/perl
# Mon, 29 Apr 2024 09:51:00 GMT
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/P/PE/PEVANS/perl-5.39.10.tar.gz -o perl-5.39.10.tar.gz     && echo '4b7ffb3e068583fa5c8413390c998b2c15214f205ce737acc485b40932b9f419 *perl-5.39.10.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.39.10.tar.gz -C /usr/src/perl     && rm perl-5.39.10.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997014/cpm -o /usr/local/bin/cpm     && echo 'ee525f2493e36c6f688eddabaf53a51c4d3b2a4ebaa81576ac8b9f78ab57f4a1 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Mon, 29 Apr 2024 09:51:00 GMT
WORKDIR /usr/src/app
# Mon, 29 Apr 2024 09:51:00 GMT
CMD ["perl5.39.10" "-de0"]
```

-	Layers:
	-	`sha256:b9285660d64168cd1c05bdfee5186da3634a289a06300d8ea12e57df80e4648b`  
		Last Modified: Tue, 14 May 2024 00:47:17 GMT  
		Size: 47.9 MB (47942190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c304d55d9ae47fcef54a6044634995ffbdbd5e4d3e409198127615b4043fa8b`  
		Last Modified: Tue, 14 May 2024 01:29:23 GMT  
		Size: 24.0 MB (24046857 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:943219d44d0b66fa3c53413ccd4b689951925725722eba1e47eec984778d3640`  
		Last Modified: Tue, 14 May 2024 01:29:39 GMT  
		Size: 63.1 MB (63130182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57dd19c695c401ade3f0a1af6a11007c474b68b17b925095492dbfc5a8f2a538`  
		Last Modified: Tue, 14 May 2024 01:30:07 GMT  
		Size: 183.2 MB (183236787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9de7775fafba5b05fe1fdd1b97c4744dffda25f4d094e7c58e92021c74dd2695`  
		Last Modified: Tue, 14 May 2024 18:21:26 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d1487df9b6fb47e53a14894970e99b0d1261f288cbf58387d1e869808190b20`  
		Last Modified: Tue, 14 May 2024 21:52:25 GMT  
		Size: 16.3 MB (16268290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2295029f096b8d97ce7e998f109b047cbbff9015fbb25be504614a9171afc50`  
		Last Modified: Tue, 14 May 2024 21:52:24 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-bookworm` - unknown; unknown

```console
$ docker pull perl@sha256:6c1211a735b54f91a33794c7f1cc11ca833e3ee1333ca1eb6d376e84b2c8e7f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.2 MB (15200022 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bed1b2d7d4620f1315a3c4a59e4027c4651d4cf405372d2b6a3cfe44d726145a`

```dockerfile
```

-	Layers:
	-	`sha256:4195c4a0d6228e21c75b0240512f501d724cfe7af3f756d5cda856f4ee5cc680`  
		Last Modified: Tue, 14 May 2024 21:52:24 GMT  
		Size: 15.2 MB (15184016 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3865d82551b49f9424d92509b92ba8d1dc30c49095de8159a072df7514a67428`  
		Last Modified: Tue, 14 May 2024 21:52:24 GMT  
		Size: 16.0 KB (16006 bytes)  
		MIME: application/vnd.in-toto+json
