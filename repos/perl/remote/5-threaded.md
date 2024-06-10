## `perl:5-threaded`

```console
$ docker pull perl@sha256:63542e7788d70beae13b200cb02f729d182e3653ada5e9531a682d0372de3a92
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

### `perl:5-threaded` - linux; amd64

```console
$ docker pull perl@sha256:97a7e41ba607343fbdb6eaf04e85e9429d95913ac9ec83baece2a3fa56483e05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **364.7 MB (364693046 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73cb3363f4c3126ea7191b766cc2d99eb73793d2433d833bcbe926982e073c36`
-	Default Command: `["perl5.38.2","-de0"]`

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
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/P/PE/PEVANS/perl-5.38.2.tar.gz -o perl-5.38.2.tar.gz     && echo 'a0a31534451eb7b83c7d6594a497543a54d488bc90ca00f5e34762577f40655e *perl-5.38.2.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.38.2.tar.gz -C /usr/src/perl     && rm perl-5.38.2.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997014/cpm -o /usr/local/bin/cpm     && echo 'ee525f2493e36c6f688eddabaf53a51c4d3b2a4ebaa81576ac8b9f78ab57f4a1 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Mon, 29 Apr 2024 09:51:00 GMT
WORKDIR /usr/src/app
# Mon, 29 Apr 2024 09:51:00 GMT
CMD ["perl5.38.2" "-de0"]
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
	-	`sha256:cc435a008fc9387e9e4de3821fb8d3a95e55ac42b10569f67b4daefbf7197b6c`  
		Last Modified: Tue, 14 May 2024 04:04:54 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a479d5a9ee7ee348631dd03f585e52bb0b7e035b5ec04e0e74dd02e9993b6a3`  
		Last Modified: Tue, 14 May 2024 04:05:36 GMT  
		Size: 15.7 MB (15716735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2bc155bf536919bd53ecd8ca9fa783624eb491d16769cf65251b110225f4fbc`  
		Last Modified: Tue, 14 May 2024 04:05:35 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:5-threaded` - unknown; unknown

```console
$ docker pull perl@sha256:88e9661f33a5d256a8ad0c652ce13ba8a49e5da8ed4214e23905c7e275d05d04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 MB (15388653 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7eabb6828b046965af293dd2e59827c3f9636c4d24241163fde1c2f7fee8edaf`

```dockerfile
```

-	Layers:
	-	`sha256:7c861d60d18474e05e4617593db75b4e48e1ee37d9aedd60ffe60a9cafa753a2`  
		Last Modified: Tue, 14 May 2024 04:05:36 GMT  
		Size: 15.4 MB (15370676 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7026a7869360dd0f71a7853b39fb5f66d2265edd7f85983fc268ac770905bdca`  
		Last Modified: Tue, 14 May 2024 04:05:35 GMT  
		Size: 18.0 KB (17977 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:5-threaded` - linux; arm variant v5

```console
$ docker pull perl@sha256:75d63bc77facb392eeae2e664c32fc17994b1a94450de3d8535f58a474c7d404
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **331.4 MB (331379561 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a101a2b51e8cec95d7c0e3951817f58f839e3033951319fba6e4dcab9b268c6`
-	Default Command: `["perl5.40.0","-de0"]`

```dockerfile
# Tue, 14 May 2024 00:48:25 GMT
ADD file:cd62e5a70676cac6ab9314bf7583f7ed4056908c492f302f1243edbd35066bfd in / 
# Tue, 14 May 2024 00:48:26 GMT
CMD ["bash"]
# Tue, 14 May 2024 01:11:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 14 May 2024 01:11:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 14 May 2024 01:13:15 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 10 Jun 2024 03:33:39 GMT
WORKDIR /usr/src/perl
# Mon, 10 Jun 2024 03:33:39 GMT
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/H/HA/HAARG/perl-5.40.0.tar.gz -o perl-5.40.0.tar.gz     && echo 'c740348f357396327a9795d3e8323bafd0fe8a5c7835fc1cbaba0cc8dfe7161f *perl-5.40.0.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.40.0.tar.gz -C /usr/src/perl     && rm perl-5.40.0.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Mon, 10 Jun 2024 03:33:39 GMT
WORKDIR /usr/src/app
# Mon, 10 Jun 2024 03:33:39 GMT
CMD ["perl5.40.0" "-de0"]
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
	-	`sha256:64e7b881b51fc21052bd19d67b2f0e2fe1d79fdc899549a588c5d3a3cd4c6759`  
		Last Modified: Mon, 10 Jun 2024 21:09:52 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6eeeb194da09aa663fd8c2cc9d76f20a8dcd55d6b209f59bfa747db41110d48`  
		Last Modified: Mon, 10 Jun 2024 21:38:35 GMT  
		Size: 15.3 MB (15272110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1e1c1a8dba8f02b50a68ecbfe58a198fe4d6b020d8734ce5ac35cfb2e32aee0`  
		Last Modified: Mon, 10 Jun 2024 21:38:35 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:5-threaded` - unknown; unknown

```console
$ docker pull perl@sha256:1b24157bdca21e397c9f48e812f676a0265f07c6bd3348b53a43c598f3152675
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.2 MB (15188565 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76207d7cc6b39d87ef7813ce18bad19ddc662cd1fd6bb7e3063db0bdbba6989f`

```dockerfile
```

-	Layers:
	-	`sha256:07081e929873cb9e2a8db168e6613debc1d6af215bcf10d0d59b4381226669d8`  
		Last Modified: Mon, 10 Jun 2024 21:38:35 GMT  
		Size: 15.2 MB (15171085 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:31a5dcb8339ba083a18f8fa2ba87a77f7baeda8b0075489570d5cb455fab541c`  
		Last Modified: Mon, 10 Jun 2024 21:38:34 GMT  
		Size: 17.5 KB (17480 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:5-threaded` - linux; arm variant v7

```console
$ docker pull perl@sha256:128566c6ee3b33d6ecc62253d5d799ab560e1385572e9dcc4df8a3e0b70a2c82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **316.6 MB (316575210 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36eba1223626b70d942ab89e52171ab5fe57c8841f3df968c2fb705c06133c58`
-	Default Command: `["perl5.40.0","-de0"]`

```dockerfile
# Tue, 14 May 2024 01:08:35 GMT
ADD file:1e106a38a0e44ca74d4d29c6d797780e7a29ffe249e473c48ee2aea553fc013b in / 
# Tue, 14 May 2024 01:08:36 GMT
CMD ["bash"]
# Tue, 14 May 2024 01:35:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 14 May 2024 01:35:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 14 May 2024 01:36:53 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 10 Jun 2024 03:33:39 GMT
WORKDIR /usr/src/perl
# Mon, 10 Jun 2024 03:33:39 GMT
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/H/HA/HAARG/perl-5.40.0.tar.gz -o perl-5.40.0.tar.gz     && echo 'c740348f357396327a9795d3e8323bafd0fe8a5c7835fc1cbaba0cc8dfe7161f *perl-5.40.0.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.40.0.tar.gz -C /usr/src/perl     && rm perl-5.40.0.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Mon, 10 Jun 2024 03:33:39 GMT
WORKDIR /usr/src/app
# Mon, 10 Jun 2024 03:33:39 GMT
CMD ["perl5.40.0" "-de0"]
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
	-	`sha256:623c5a4038d72aaf82e91ef329caf9411acadc2c45563a0cb54ab19938fc8709`  
		Last Modified: Mon, 10 Jun 2024 21:01:12 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dcf87958992681fbfe718d50ff62acc19604f235e23b4a2ba85354dd8661552`  
		Last Modified: Mon, 10 Jun 2024 21:43:16 GMT  
		Size: 15.1 MB (15054040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f5a1755917f128352f33c8e3b34bbf4795cd6a591f60fcfffc9fa1757db2087`  
		Last Modified: Mon, 10 Jun 2024 21:43:15 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:5-threaded` - unknown; unknown

```console
$ docker pull perl@sha256:e3fda6a004d17b855206f051e635d4bb1593e7ec2fc26337478599e84b731952
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.2 MB (15194039 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af72a5b73528c4d8776327a0e160135cf127ab57bbbc9e9efb57894c6fcc030e`

```dockerfile
```

-	Layers:
	-	`sha256:cbc5654e10894e75a59b170c25fceb005cc2fad31e09d093261d28ec82a87f70`  
		Last Modified: Mon, 10 Jun 2024 21:43:15 GMT  
		Size: 15.2 MB (15176559 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cc1213ba788f58126b305c302ce96d2cc438cc0ce83eee2ed780da0de9a1017d`  
		Last Modified: Mon, 10 Jun 2024 21:43:15 GMT  
		Size: 17.5 KB (17480 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:5-threaded` - linux; arm64 variant v8

```console
$ docker pull perl@sha256:68c893b301fb5b7ca7e0ec5e8a6727713acee8405a4058175458ec800d0b9534
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **355.5 MB (355454732 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8dbd84d68ff1ed2137b9720b1b2d4970036ec7be09b360829cd06af46068559e`
-	Default Command: `["perl5.38.2","-de0"]`

```dockerfile
# Mon, 29 Apr 2024 09:51:00 GMT
ADD file:b7c55dda8ded4219a7cdc9fbd91dfb5996c4886d4394b85751c2f956defe3287 in / 
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
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/P/PE/PEVANS/perl-5.38.2.tar.gz -o perl-5.38.2.tar.gz     && echo 'a0a31534451eb7b83c7d6594a497543a54d488bc90ca00f5e34762577f40655e *perl-5.38.2.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.38.2.tar.gz -C /usr/src/perl     && rm perl-5.38.2.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997014/cpm -o /usr/local/bin/cpm     && echo 'ee525f2493e36c6f688eddabaf53a51c4d3b2a4ebaa81576ac8b9f78ab57f4a1 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Mon, 29 Apr 2024 09:51:00 GMT
WORKDIR /usr/src/app
# Mon, 29 Apr 2024 09:51:00 GMT
CMD ["perl5.38.2" "-de0"]
```

-	Layers:
	-	`sha256:91e301773f03e9e0fabc5c177fe6bfe8daf14e992ab816f151692b814ddc462c`  
		Last Modified: Tue, 14 May 2024 00:42:35 GMT  
		Size: 49.6 MB (49613388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15856ca26414127b85cee6d10acbc4cee6eba9070f3f5a04b9cc72ce95abfa7f`  
		Last Modified: Tue, 14 May 2024 01:52:50 GMT  
		Size: 23.6 MB (23586610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30ed4c12791345d3f20f66024e1f22275ce507868c508509b83dcf231b1c9adc`  
		Last Modified: Tue, 14 May 2024 01:53:09 GMT  
		Size: 64.0 MB (63994370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:feb30c5ba2d151512d29ff4b92109a740559509ef6f3072a86c5006a1379397b`  
		Last Modified: Tue, 14 May 2024 01:53:41 GMT  
		Size: 202.6 MB (202593312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0629cbbbee4a00b3485d4369c30738dbdc1a8479e429de884a8915f844885ad2`  
		Last Modified: Wed, 15 May 2024 10:42:13 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23782a4c96b5dd5b77c18efa2ead77bb1aa3c6779945aa1f3ddfd203a5dd4507`  
		Last Modified: Wed, 15 May 2024 11:12:41 GMT  
		Size: 15.7 MB (15666785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efff4df158358ed631e6c9faeb2cac59388903d63e8c1c825c021ccb597b1afb`  
		Last Modified: Wed, 15 May 2024 11:12:40 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:5-threaded` - unknown; unknown

```console
$ docker pull perl@sha256:9ba52a631a9584b10bf2f53419d51fd76384b07109b4cbb56307bd0abad52315
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 MB (15416535 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e005694ced56d30f2f6860c73d886ed642a799b05cc5337b1f04c9e2948dec98`

```dockerfile
```

-	Layers:
	-	`sha256:0b0ecb3b12d88d70ee583547acbfee0e59ab7c3a989041b346eeb0fc88587519`  
		Last Modified: Wed, 15 May 2024 11:12:41 GMT  
		Size: 15.4 MB (15399199 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:afdd7b36ccaccc5315c7b01c4a19b7b870addad4ae26ffac2b8efc45670ad182`  
		Last Modified: Wed, 15 May 2024 11:12:40 GMT  
		Size: 17.3 KB (17336 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:5-threaded` - linux; 386

```console
$ docker pull perl@sha256:deb46bd5657336856972c4db3f402dcda1844a09909dd5ba91a663fa4b1e5c98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **367.2 MB (367173035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f957c3f91cc2019df3cca6ea274c83d9a90dbad84d603e8c3cf10b801cb53a2c`
-	Default Command: `["perl5.40.0","-de0"]`

```dockerfile
# Tue, 14 May 2024 00:47:00 GMT
ADD file:35709674a3b845511a896af16ea37a6022e7d48992d3198d0760c0c3208fe4ed in / 
# Tue, 14 May 2024 00:47:01 GMT
CMD ["bash"]
# Tue, 14 May 2024 09:01:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 14 May 2024 09:01:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 14 May 2024 09:02:47 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 10 Jun 2024 03:33:39 GMT
WORKDIR /usr/src/perl
# Mon, 10 Jun 2024 03:33:39 GMT
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/H/HA/HAARG/perl-5.40.0.tar.gz -o perl-5.40.0.tar.gz     && echo 'c740348f357396327a9795d3e8323bafd0fe8a5c7835fc1cbaba0cc8dfe7161f *perl-5.40.0.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.40.0.tar.gz -C /usr/src/perl     && rm perl-5.40.0.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Mon, 10 Jun 2024 03:33:39 GMT
WORKDIR /usr/src/app
# Mon, 10 Jun 2024 03:33:39 GMT
CMD ["perl5.40.0" "-de0"]
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
	-	`sha256:9adaf648c655db718cb9edf24d6c897251a50d1236aeca8f722c59ea103cfad7`  
		Last Modified: Mon, 10 Jun 2024 21:05:11 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85514abd4f096c36a80b99fca7a5dbaaa44d150cb1e241b0330448a24a0e1936`  
		Last Modified: Mon, 10 Jun 2024 21:05:12 GMT  
		Size: 15.6 MB (15564486 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3d34395d049387f219c7f1b88f0ff6ae0093d7d7d7e568ad0ce57353691e04c`  
		Last Modified: Mon, 10 Jun 2024 21:05:11 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:5-threaded` - unknown; unknown

```console
$ docker pull perl@sha256:70667c3bdab34106f35c94dd7a693024b4cb01173b483426bbed6edbab83d72a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 MB (15367015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5de84dc858e488173e2f71d50513b6a9780aa5208be2121050ba99fc3d015396`

```dockerfile
```

-	Layers:
	-	`sha256:07872cbb34ce2bc521f95b212b61a7c0db3599e9ecd2c6221c4f77d15acea130`  
		Last Modified: Mon, 10 Jun 2024 21:05:12 GMT  
		Size: 15.3 MB (15349712 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:89fc24506f01e1f3b24719b4123f1746255a792513b43d746971b53d1e4ef44b`  
		Last Modified: Mon, 10 Jun 2024 21:05:10 GMT  
		Size: 17.3 KB (17303 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:5-threaded` - linux; mips64le

```console
$ docker pull perl@sha256:ba09dac947119611e97cdb81c296dba21a1566e7d6d8ba091d618eb5355d060f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **340.7 MB (340686981 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3876407b072758bd2b48445d72336515ced103c555dc72f5bba83b7f80d31345`
-	Default Command: `["perl5.38.2","-de0"]`

```dockerfile
# Mon, 29 Apr 2024 09:51:00 GMT
ADD file:95717416297a85e0b38d171b3bf8d2b48e941bd725e476ee4f88033fed4ffee2 in / 
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
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/P/PE/PEVANS/perl-5.38.2.tar.gz -o perl-5.38.2.tar.gz     && echo 'a0a31534451eb7b83c7d6594a497543a54d488bc90ca00f5e34762577f40655e *perl-5.38.2.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.38.2.tar.gz -C /usr/src/perl     && rm perl-5.38.2.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997014/cpm -o /usr/local/bin/cpm     && echo 'ee525f2493e36c6f688eddabaf53a51c4d3b2a4ebaa81576ac8b9f78ab57f4a1 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Mon, 29 Apr 2024 09:51:00 GMT
WORKDIR /usr/src/app
# Mon, 29 Apr 2024 09:51:00 GMT
CMD ["perl5.38.2" "-de0"]
```

-	Layers:
	-	`sha256:0fd7e383bbed45ca14b36b1e22f1591a0b2bddc34b2b6e2b34d4cd54b528e75f`  
		Last Modified: Tue, 14 May 2024 01:21:36 GMT  
		Size: 49.6 MB (49582338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5ce1d8a69726b5d3330ae01a246efbb18fb60d54fb0d08b741a960e37d8b115`  
		Last Modified: Tue, 14 May 2024 11:37:05 GMT  
		Size: 23.4 MB (23438164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e3667485c8dcf18ff23740eff9103874ec0aba9a4d45bade2f98f9f85fe0f63`  
		Last Modified: Tue, 14 May 2024 11:37:57 GMT  
		Size: 63.0 MB (62968511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb3514ef59a25de65d0663fc4a360de7a712214c493290dd77858247edbd0dac`  
		Last Modified: Tue, 14 May 2024 11:40:05 GMT  
		Size: 189.8 MB (189771182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b02d0a84b492665206cb876f29c96b490a9bd1cc4699fccbb71b6ff9dbca531`  
		Last Modified: Wed, 15 May 2024 19:49:31 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:093c8b0df0c57ddc3286663e11575f4edb860e0d9f51afa0054a4e8326f27ce7`  
		Last Modified: Wed, 15 May 2024 20:41:43 GMT  
		Size: 14.9 MB (14926521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75412be803b3bf33b97fb34c114eb25289e00db565030f7fe3088675c731e4f7`  
		Last Modified: Wed, 15 May 2024 20:41:41 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:5-threaded` - unknown; unknown

```console
$ docker pull perl@sha256:d5200559c42eae03a53daab87fb01be52727aad2b57ca5369c46902f954bc1d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.2 KB (17206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5b29160db2213fffcc82acd65cfb4e0b33afc328501837bd0c2ef1c80e828c5`

```dockerfile
```

-	Layers:
	-	`sha256:8bb82c5c6512d058d0dae50b75b82eca41328b611c741634f434f03ff4ddfeeb`  
		Last Modified: Wed, 15 May 2024 20:41:41 GMT  
		Size: 17.2 KB (17206 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:5-threaded` - linux; ppc64le

```console
$ docker pull perl@sha256:3680bf4f2f44606ef10426d544d0032dabac92e4ed14a062b82ccdef159f655c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **379.2 MB (379153180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9f75ed74f1ed8c9522c8ebfcfff5b4222fcd2f6f318566a2ee1542731ad72d5`
-	Default Command: `["perl5.40.0","-de0"]`

```dockerfile
# Tue, 14 May 2024 01:19:48 GMT
ADD file:fdb5c89e2970bd3b21a7b4e39491c1719b957f54babefd52ad455ea72a77bd3f in / 
# Tue, 14 May 2024 01:19:50 GMT
CMD ["bash"]
# Tue, 14 May 2024 06:55:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 14 May 2024 06:55:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 14 May 2024 06:57:32 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 10 Jun 2024 03:33:39 GMT
WORKDIR /usr/src/perl
# Mon, 10 Jun 2024 03:33:39 GMT
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/H/HA/HAARG/perl-5.40.0.tar.gz -o perl-5.40.0.tar.gz     && echo 'c740348f357396327a9795d3e8323bafd0fe8a5c7835fc1cbaba0cc8dfe7161f *perl-5.40.0.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.40.0.tar.gz -C /usr/src/perl     && rm perl-5.40.0.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Mon, 10 Jun 2024 03:33:39 GMT
WORKDIR /usr/src/app
# Mon, 10 Jun 2024 03:33:39 GMT
CMD ["perl5.40.0" "-de0"]
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
	-	`sha256:1a585e0ee2f803bf13a5bc56bac561e218d4eb3f84aa788cbf2c103de84e9e4e`  
		Last Modified: Mon, 10 Jun 2024 21:02:55 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c76341e31aa74a04700744603da77bee73803f1b4bd9d87c684a0888600fa691`  
		Last Modified: Mon, 10 Jun 2024 21:29:42 GMT  
		Size: 16.1 MB (16054746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e38dfeb5191d6f47ffd9d7248bb51c8b66fc7a678fcc1857c7dbe345eeb29f2e`  
		Last Modified: Mon, 10 Jun 2024 21:29:16 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:5-threaded` - unknown; unknown

```console
$ docker pull perl@sha256:03b62fd64c4328f4983306fb001bb28a3cf896193a6206be5a336d332baa4e59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 MB (15364821 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8552f7e9139034098729731dc5d4ad79cfa7aa6ddbca118bad1cacdf82cb652`

```dockerfile
```

-	Layers:
	-	`sha256:4b124f31e1a9b4c8e1f890916d8b5593c7436d35d73cdfd800f9adec2b357907`  
		Last Modified: Mon, 10 Jun 2024 21:29:41 GMT  
		Size: 15.3 MB (15347385 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eac6e6aa330bb9c4853391f5fde887694a09e4c6c2fbfdbbff6e584c1651fdbf`  
		Last Modified: Mon, 10 Jun 2024 21:29:41 GMT  
		Size: 17.4 KB (17436 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:5-threaded` - linux; s390x

```console
$ docker pull perl@sha256:728bd0cedf31b5911734b48f137bfdafc40ec4b40708bf8d9915a96331281df9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **334.7 MB (334709450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:378823e3630bf3fa6a878e3259a7e97749d5501bf7991d3ebff11049c0239813`
-	Default Command: `["perl5.40.0","-de0"]`

```dockerfile
# Tue, 14 May 2024 00:42:19 GMT
ADD file:d24c16f113416f94273813df324360fe934245f0f7f2973b6def2799e5605f1f in / 
# Tue, 14 May 2024 00:42:21 GMT
CMD ["bash"]
# Tue, 14 May 2024 01:19:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 14 May 2024 01:20:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 14 May 2024 01:21:16 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 10 Jun 2024 03:33:39 GMT
WORKDIR /usr/src/perl
# Mon, 10 Jun 2024 03:33:39 GMT
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/H/HA/HAARG/perl-5.40.0.tar.gz -o perl-5.40.0.tar.gz     && echo 'c740348f357396327a9795d3e8323bafd0fe8a5c7835fc1cbaba0cc8dfe7161f *perl-5.40.0.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.40.0.tar.gz -C /usr/src/perl     && rm perl-5.40.0.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Mon, 10 Jun 2024 03:33:39 GMT
WORKDIR /usr/src/app
# Mon, 10 Jun 2024 03:33:39 GMT
CMD ["perl5.40.0" "-de0"]
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
	-	`sha256:3d1096c1a2e6edba763a77cd4c09fbaf0ac50d71260f9babadd07a09106bd365`  
		Last Modified: Mon, 10 Jun 2024 21:09:13 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a47bb3ed81105eeddca4370b55ec5d2531b1ef3046ea9d30b25e8a05dc771916`  
		Last Modified: Mon, 10 Jun 2024 21:41:48 GMT  
		Size: 16.4 MB (16353166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec7d5a4904171f41216d76dfa9f627bc4ff417ae58e21f4ec5e2097d10076ccb`  
		Last Modified: Mon, 10 Jun 2024 21:41:48 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:5-threaded` - unknown; unknown

```console
$ docker pull perl@sha256:e11f91b9a9beb45910cac96fdc38a3989df4e1d81cbba7ed8eda49c23870b8f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.2 MB (15202719 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d79eff5f046e7c12d82a78a1da31b450c95c213affc318fc57cd25fa60635f00`

```dockerfile
```

-	Layers:
	-	`sha256:8f9883f511da4eeddf5a0274848f7b86e9f82ee1468acc10f4235aac92eb171a`  
		Last Modified: Mon, 10 Jun 2024 21:41:48 GMT  
		Size: 15.2 MB (15185357 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8fe5b24feeaf69cea735a576177fa51120e0d0cc0234d2f7df456e4cc287ce0c`  
		Last Modified: Mon, 10 Jun 2024 21:41:47 GMT  
		Size: 17.4 KB (17362 bytes)  
		MIME: application/vnd.in-toto+json
