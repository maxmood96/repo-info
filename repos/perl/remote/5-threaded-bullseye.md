## `perl:5-threaded-bullseye`

```console
$ docker pull perl@sha256:9c1ab21f7e370e5718415d4687e1c7ba3089346d3923cd40a9584c4e123cd29f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 8
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; s390x

### `perl:5-threaded-bullseye` - linux; amd64

```console
$ docker pull perl@sha256:3175d0310f7b5d6f3b808eda8708999eb9d728f652b33dbd630f70ff771c4f7d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **336.4 MB (336407943 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f27e4549381bc3fd8a39bdbc300827f1f7742aae65188317847421fc836fd89d`
-	Default Command: `["perl5.34.0","-de0"]`

```dockerfile
# Thu, 17 Mar 2022 04:03:47 GMT
ADD file:19873be7a1c793d8edefb5d64edb99fe05ac5b1d304d167661ac3d8f21b4bd65 in / 
# Thu, 17 Mar 2022 04:03:47 GMT
CMD ["bash"]
# Fri, 18 Mar 2022 06:29:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Mar 2022 06:30:05 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 18 Mar 2022 06:30:34 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Fri, 18 Mar 2022 06:31:39 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Mar 2022 10:15:23 GMT
LABEL maintainer=Peter Martini <PeterCMartini@GMail.com>, Zak B. Elep <zakame@cpan.org>
# Fri, 18 Mar 2022 10:15:23 GMT
COPY file:3744c5cc39cdbdcae10db09a1f0f399005a79f93c237b387a72ff5710cdd458c in /usr/src/perl/ 
# Fri, 18 Mar 2022 10:15:23 GMT
WORKDIR /usr/src/perl
# Fri, 18 Mar 2022 10:51:55 GMT
RUN true     && curl -SL https://www.cpan.org/src/5.0/perl-5.34.0.tar.xz -o perl-5.34.0.tar.xz     && echo '82c2e5e5c71b0e10487a80d79140469ab1f8056349ca8545140a224dbbed7ded *perl-5.34.0.tar.xz' | sha256sum -c -     && tar --strip-components=1 -xaf perl-5.34.0.tar.xz -C /usr/src/perl     && rm perl-5.34.0.tar.xz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -LO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7044.tar.gz     && echo '9b60767fe40752ef7a9d3f13f19060a63389a5c23acc3e9827e19b75500f81f3 *App-cpanminus-1.7044.tar.gz' | sha256sum -c -     && tar -xzf App-cpanminus-1.7044.tar.gz && cd App-cpanminus-1.7044 && perl bin/cpanm . && cd /root     && true     && rm -fr ./cpanm /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7044* /tmp/*
# Fri, 18 Mar 2022 10:51:55 GMT
WORKDIR /
# Fri, 18 Mar 2022 10:51:55 GMT
CMD ["perl5.34.0" "-de0"]
```

-	Layers:
	-	`sha256:5492f66d270062ddb73f28649d80eef162f2c9376d53973a3557158390af4f30`  
		Last Modified: Thu, 17 Mar 2022 04:09:37 GMT  
		Size: 54.9 MB (54922831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:540ff8c0841d610e4cc2ad3b9ed4c6edcad4f5be2add8765f416515fbc2be2a8`  
		Last Modified: Fri, 18 Mar 2022 07:03:14 GMT  
		Size: 5.2 MB (5153360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0bf850a0df065fb202ebf8a3527699dc18322469c34733a6cb7f412a7aaefa6`  
		Last Modified: Fri, 18 Mar 2022 07:03:15 GMT  
		Size: 10.9 MB (10871980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d751dc38ae511bbc21c148bffa7e863057cbc7b4a8ff5155f2eca7e8d03740c6`  
		Last Modified: Fri, 18 Mar 2022 07:03:40 GMT  
		Size: 54.6 MB (54577140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9720a112e8860134f8c112605b4ff865d333e824edc4300ee976303d693f372f`  
		Last Modified: Fri, 18 Mar 2022 07:04:32 GMT  
		Size: 196.5 MB (196538368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1360888621b2a00c4972a13e6e33c6a47cef1516ab906c26c07f3b5572eaec1`  
		Last Modified: Fri, 18 Mar 2022 14:08:19 GMT  
		Size: 202.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f9ebce1ee9e2b2ab74c15f4fd2ee9ac65bd3aff89771c8949dbc4f8f8ee4482`  
		Last Modified: Fri, 18 Mar 2022 14:09:56 GMT  
		Size: 14.3 MB (14344062 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `perl:5-threaded-bullseye` - linux; arm variant v5

```console
$ docker pull perl@sha256:722734bbac553bbe6426bd629a8f2a5f177fa6982dd8927f20566ac216e5d2b5
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **308.8 MB (308787840 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43d7785e00311f19293dcb3ed58dcc90fc20df775fd970a3239dc3d678569e11`
-	Default Command: `["perl5.34.1","-de0"]`

```dockerfile
# Thu, 17 Mar 2022 05:19:10 GMT
ADD file:711abc0c0a502fe727f811a82e7e6175c753593bc9f6d477a47b889fc3fe8ff6 in / 
# Thu, 17 Mar 2022 05:19:11 GMT
CMD ["bash"]
# Thu, 17 Mar 2022 19:15:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 17 Mar 2022 19:15:57 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 17 Mar 2022 19:16:52 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 17 Mar 2022 19:19:04 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Mar 2022 13:06:34 GMT
LABEL maintainer=Peter Martini <PeterCMartini@GMail.com>, Zak B. Elep <zakame@cpan.org>
# Fri, 18 Mar 2022 13:06:35 GMT
COPY file:3744c5cc39cdbdcae10db09a1f0f399005a79f93c237b387a72ff5710cdd458c in /usr/src/perl/ 
# Fri, 18 Mar 2022 13:06:35 GMT
WORKDIR /usr/src/perl
# Sat, 19 Mar 2022 00:38:43 GMT
RUN true     && curl -SL https://www.cpan.org/src/5.0/perl-5.34.1.tar.xz -o perl-5.34.1.tar.xz     && echo '6d52cf833ff1af27bb5e986870a2c30cec73c044b41e3458cd991f94374039f7 *perl-5.34.1.tar.xz' | sha256sum -c -     && tar --strip-components=1 -xaf perl-5.34.1.tar.xz -C /usr/src/perl     && rm perl-5.34.1.tar.xz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -LO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7044.tar.gz     && echo '9b60767fe40752ef7a9d3f13f19060a63389a5c23acc3e9827e19b75500f81f3 *App-cpanminus-1.7044.tar.gz' | sha256sum -c -     && tar -xzf App-cpanminus-1.7044.tar.gz && cd App-cpanminus-1.7044 && perl bin/cpanm . && cd /root     && true     && rm -fr ./cpanm /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7044* /tmp/*
# Sat, 19 Mar 2022 00:38:43 GMT
WORKDIR /
# Sat, 19 Mar 2022 00:38:44 GMT
CMD ["perl5.34.1" "-de0"]
```

-	Layers:
	-	`sha256:f6db9b0909e16205c253a4a6e736ed382b68f85839d7822d22d5ddd35fd2fda4`  
		Last Modified: Thu, 17 Mar 2022 05:34:11 GMT  
		Size: 52.5 MB (52470250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbd49582c7f6675ebcf6ce05a8c46ca03963dcb872a6609647908e9f3ec1bdab`  
		Last Modified: Thu, 17 Mar 2022 19:40:09 GMT  
		Size: 5.1 MB (5063869 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc5be2734ad2363ae06404b77e944bcdb8496677704f50b8b579838e015ab189`  
		Last Modified: Thu, 17 Mar 2022 19:40:11 GMT  
		Size: 10.6 MB (10570982 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5e806b3e4bd3a2bcc0347f8ed2951681ef09caa248f10c65740a1e875c73a0f`  
		Last Modified: Thu, 17 Mar 2022 19:40:52 GMT  
		Size: 52.3 MB (52316691 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7166a5ed27b6af8f7b1519b72230e19ab19b41ecbaed3d06fa3dbb148e159380`  
		Last Modified: Thu, 17 Mar 2022 19:42:07 GMT  
		Size: 174.8 MB (174755426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a370b7375060e70e9674754cddbcb028028d00ac4747f9d1c4a769e1cae70a4d`  
		Last Modified: Fri, 18 Mar 2022 15:45:25 GMT  
		Size: 204.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bf483b2099150c80f194b36317f3259c09ee0bd6e1721ec75d1e91f5cfd236a`  
		Last Modified: Sat, 19 Mar 2022 03:02:03 GMT  
		Size: 13.6 MB (13610418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `perl:5-threaded-bullseye` - linux; arm variant v7

```console
$ docker pull perl@sha256:5ab43a58f6a63019d6a8c1e794a833ad31af7f3d4807f1550db96a52c2c7bf8a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **296.0 MB (296007866 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:355cbc38884bcc4b3d22aed169422b2f85da48c63e340a4a0cf361aa17ebc2ea`
-	Default Command: `["perl5.34.1","-de0"]`

```dockerfile
# Thu, 17 Mar 2022 09:30:27 GMT
ADD file:a76bfdf79974fef637725f4c4d8afd998baacd9f3852ac94ce4db52fd65edd8c in / 
# Thu, 17 Mar 2022 09:30:28 GMT
CMD ["bash"]
# Sat, 19 Mar 2022 02:52:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 02:52:48 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 19 Mar 2022 02:53:37 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 02:55:27 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 04:29:06 GMT
LABEL maintainer=Peter Martini <PeterCMartini@GMail.com>, Zak B. Elep <zakame@cpan.org>
# Sat, 19 Mar 2022 04:29:06 GMT
COPY file:3744c5cc39cdbdcae10db09a1f0f399005a79f93c237b387a72ff5710cdd458c in /usr/src/perl/ 
# Sat, 19 Mar 2022 04:29:07 GMT
WORKDIR /usr/src/perl
# Sat, 19 Mar 2022 05:25:51 GMT
RUN true     && curl -SL https://www.cpan.org/src/5.0/perl-5.34.1.tar.xz -o perl-5.34.1.tar.xz     && echo '6d52cf833ff1af27bb5e986870a2c30cec73c044b41e3458cd991f94374039f7 *perl-5.34.1.tar.xz' | sha256sum -c -     && tar --strip-components=1 -xaf perl-5.34.1.tar.xz -C /usr/src/perl     && rm perl-5.34.1.tar.xz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -LO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7044.tar.gz     && echo '9b60767fe40752ef7a9d3f13f19060a63389a5c23acc3e9827e19b75500f81f3 *App-cpanminus-1.7044.tar.gz' | sha256sum -c -     && tar -xzf App-cpanminus-1.7044.tar.gz && cd App-cpanminus-1.7044 && perl bin/cpanm . && cd /root     && true     && rm -fr ./cpanm /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7044* /tmp/*
# Sat, 19 Mar 2022 05:25:52 GMT
WORKDIR /
# Sat, 19 Mar 2022 05:25:52 GMT
CMD ["perl5.34.1" "-de0"]
```

-	Layers:
	-	`sha256:4a0c373b7fd878320ee1d0810692c38f8079bd0783a53740b236b67ccd6eab4f`  
		Last Modified: Thu, 17 Mar 2022 09:45:54 GMT  
		Size: 50.1 MB (50122251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49a9d199c77419ab8067bd77407cb0151e23cf09849e1fc7f550156c8d5ff053`  
		Last Modified: Sat, 19 Mar 2022 03:29:05 GMT  
		Size: 4.9 MB (4922780 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a175e3c76032f69174aba6e645720559d1bef82bbf1946d37266a8543cec9b75`  
		Last Modified: Sat, 19 Mar 2022 03:29:07 GMT  
		Size: 10.2 MB (10216952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8ef8cc586469458a5d1e2e47026303e46cf29e47935386efe16d91d34fe708c`  
		Last Modified: Sat, 19 Mar 2022 03:29:56 GMT  
		Size: 50.3 MB (50328447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:291fb16f7bcc8b0503109f50011e8ac9d4d161603ba3b1cf31678c8cb42e60d8`  
		Last Modified: Sat, 19 Mar 2022 03:31:44 GMT  
		Size: 167.0 MB (166993565 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6228a6637948e1e479515a5ca28b082fb8226711fcccb227539ebf43014e2015`  
		Last Modified: Sat, 19 Mar 2022 09:05:28 GMT  
		Size: 203.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6d0cb614bb1a2c247f49724561cec25edff39cb40201d609cf4201e716100aa`  
		Last Modified: Sat, 19 Mar 2022 09:08:17 GMT  
		Size: 13.4 MB (13423668 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `perl:5-threaded-bullseye` - linux; arm64 variant v8

```console
$ docker pull perl@sha256:61919c3d85df8dbb6e3ed2a81b0f5f3389dd07f216747d113334655696be9f1f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **327.6 MB (327608104 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df78578d10f1712431670fb9b214cc2ee36985a9285831f2793725e59d6a3154`
-	Default Command: `["perl5.34.0","-de0"]`

```dockerfile
# Thu, 17 Mar 2022 03:21:41 GMT
ADD file:5effc7e0ab7312f14a7ee81c06c71400aae31219d477ebe1a4f7a9156797c42a in / 
# Thu, 17 Mar 2022 03:21:42 GMT
CMD ["bash"]
# Thu, 17 Mar 2022 22:10:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 17 Mar 2022 22:11:03 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 17 Mar 2022 22:11:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 17 Mar 2022 22:12:04 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Mar 2022 02:05:17 GMT
LABEL maintainer=Peter Martini <PeterCMartini@GMail.com>, Zak B. Elep <zakame@cpan.org>
# Fri, 18 Mar 2022 02:05:18 GMT
COPY file:3744c5cc39cdbdcae10db09a1f0f399005a79f93c237b387a72ff5710cdd458c in /usr/src/perl/ 
# Fri, 18 Mar 2022 02:05:19 GMT
WORKDIR /usr/src/perl
# Fri, 18 Mar 2022 02:25:38 GMT
RUN true     && curl -SL https://www.cpan.org/src/5.0/perl-5.34.0.tar.xz -o perl-5.34.0.tar.xz     && echo '82c2e5e5c71b0e10487a80d79140469ab1f8056349ca8545140a224dbbed7ded *perl-5.34.0.tar.xz' | sha256sum -c -     && tar --strip-components=1 -xaf perl-5.34.0.tar.xz -C /usr/src/perl     && rm perl-5.34.0.tar.xz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -LO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7044.tar.gz     && echo '9b60767fe40752ef7a9d3f13f19060a63389a5c23acc3e9827e19b75500f81f3 *App-cpanminus-1.7044.tar.gz' | sha256sum -c -     && tar -xzf App-cpanminus-1.7044.tar.gz && cd App-cpanminus-1.7044 && perl bin/cpanm . && cd /root     && true     && rm -fr ./cpanm /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7044* /tmp/*
# Fri, 18 Mar 2022 02:25:39 GMT
WORKDIR /
# Fri, 18 Mar 2022 02:25:40 GMT
CMD ["perl5.34.0" "-de0"]
```

-	Layers:
	-	`sha256:260ad8146ed2447d5587608b10fed4f80de80cdc559e619f3a235d3ba09eaf7b`  
		Last Modified: Thu, 17 Mar 2022 03:28:04 GMT  
		Size: 53.6 MB (53616308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1399f445da611be3789923cf26d158e3f4f80449b7295fa069a8eaecaaf137e6`  
		Last Modified: Thu, 17 Mar 2022 22:20:58 GMT  
		Size: 4.9 MB (4937558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cd9e43777fa6c09c341f3aa922f47b5b3ace26de1d779124afd2f1d435731d9`  
		Last Modified: Thu, 17 Mar 2022 22:20:58 GMT  
		Size: 10.7 MB (10655858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f81267e40a2df9e572fe797e45dbc086008422eb2216df18b7a91f1cf13e22b`  
		Last Modified: Thu, 17 Mar 2022 22:21:21 GMT  
		Size: 54.7 MB (54671322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:460c4ae3ed9f0c0fe1ee94e09cfb3993206231793fc9e841ad8f0975895ddb9e`  
		Last Modified: Thu, 17 Mar 2022 22:22:00 GMT  
		Size: 189.5 MB (189453989 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74a3318085adda56f0955b1da37fb63e594a29d4238b1db1a8b64d97f49696ac`  
		Last Modified: Fri, 18 Mar 2022 03:48:13 GMT  
		Size: 179.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eaf5d49cf7ae8aa0505589ee3b8920a1b5ec8b3d03cdd1d9038559e5702d4005`  
		Last Modified: Fri, 18 Mar 2022 03:50:04 GMT  
		Size: 14.3 MB (14272890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `perl:5-threaded-bullseye` - linux; 386

```console
$ docker pull perl@sha256:8491ea403c079c589ea243bc5107babbbc9661faac73dbfef7d2e53a65b36c49
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **341.7 MB (341711807 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ec1ec2bb583e27c60635bb52859b34cf697ce0c1f765b6720eac6dc1527df67`
-	Default Command: `["perl5.34.0","-de0"]`

```dockerfile
# Tue, 01 Mar 2022 02:07:15 GMT
ADD file:4341f64e7f1accc7f9737a9896bf50c6ba8f51698e52c594d9421fe4f2374e2a in / 
# Tue, 01 Mar 2022 02:07:15 GMT
CMD ["bash"]
# Tue, 01 Mar 2022 05:40:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 05:41:00 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 01 Mar 2022 05:41:22 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 05:42:16 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 10:42:31 GMT
LABEL maintainer=Peter Martini <PeterCMartini@GMail.com>, Zak B. Elep <zakame@cpan.org>
# Tue, 01 Mar 2022 10:42:31 GMT
COPY file:3744c5cc39cdbdcae10db09a1f0f399005a79f93c237b387a72ff5710cdd458c in /usr/src/perl/ 
# Tue, 01 Mar 2022 10:42:31 GMT
WORKDIR /usr/src/perl
# Tue, 01 Mar 2022 11:50:19 GMT
RUN true     && curl -SL https://www.cpan.org/src/5.0/perl-5.34.0.tar.xz -o perl-5.34.0.tar.xz     && echo '82c2e5e5c71b0e10487a80d79140469ab1f8056349ca8545140a224dbbed7ded *perl-5.34.0.tar.xz' | sha256sum -c -     && tar --strip-components=1 -xaf perl-5.34.0.tar.xz -C /usr/src/perl     && rm perl-5.34.0.tar.xz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -LO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7044.tar.gz     && echo '9b60767fe40752ef7a9d3f13f19060a63389a5c23acc3e9827e19b75500f81f3 *App-cpanminus-1.7044.tar.gz' | sha256sum -c -     && tar -xzf App-cpanminus-1.7044.tar.gz && cd App-cpanminus-1.7044 && perl bin/cpanm . && cd /root     && true     && rm -fr ./cpanm /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7044* /tmp/*
# Tue, 01 Mar 2022 11:50:19 GMT
WORKDIR /
# Tue, 01 Mar 2022 11:50:19 GMT
CMD ["perl5.34.0" "-de0"]
```

-	Layers:
	-	`sha256:5cf8159e9217c5f37fe58b260cacc1d132c2e21ca58c769d29c6eb720993a304`  
		Last Modified: Tue, 01 Mar 2022 02:15:15 GMT  
		Size: 55.9 MB (55938747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1700db29f99e559f6f1909315637ddbda6667a35bd437b9e5d8c3beb373c6c1f`  
		Last Modified: Tue, 01 Mar 2022 05:51:55 GMT  
		Size: 5.3 MB (5283081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff041f2862924d1932eb1f5d7b01079bf8015dcc0dbb94a23d2475b8684d875a`  
		Last Modified: Tue, 01 Mar 2022 05:51:56 GMT  
		Size: 11.3 MB (11250640 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15ec658b51a80445b805d19e0462b4112f90132f61a78d8d7f5b29f6903e1e44`  
		Last Modified: Tue, 01 Mar 2022 05:52:25 GMT  
		Size: 55.9 MB (55919550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c521c932bdc70dee07f2e9d3855b55daf6b88fc4779ebf2235da1cd4f2647de`  
		Last Modified: Tue, 01 Mar 2022 05:53:24 GMT  
		Size: 199.5 MB (199458740 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd6a714fa60b072bbdbe58e0cee144fed6283ec25b4b55930502e6f4b6e2e5fc`  
		Last Modified: Tue, 01 Mar 2022 14:59:19 GMT  
		Size: 202.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1be70b47c7a034025d9d55ce54e713818a529bb5d5059f96f5d6531b0d4b0a10`  
		Last Modified: Tue, 01 Mar 2022 15:01:40 GMT  
		Size: 13.9 MB (13860847 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `perl:5-threaded-bullseye` - linux; mips64le

```console
$ docker pull perl@sha256:0b143289435d5486ba97436ca53716d808035f98a7805552845cdcfc74d303f8
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **314.3 MB (314347025 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64ffe0675605942bd165a16f66c1a26dbe8fd02677b22b6b0e60181d6455c407`
-	Default Command: `["perl5.34.1","-de0"]`

```dockerfile
# Thu, 17 Mar 2022 08:52:25 GMT
ADD file:f2f4496058901761fb8d3cc93b176b91332f07b531477abcf8b4e96df093d60a in / 
# Thu, 17 Mar 2022 08:52:29 GMT
CMD ["bash"]
# Thu, 17 Mar 2022 19:20:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 17 Mar 2022 19:21:07 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 17 Mar 2022 19:23:05 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 17 Mar 2022 19:28:34 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 17 Mar 2022 21:56:52 GMT
LABEL maintainer=Peter Martini <PeterCMartini@GMail.com>, Zak B. Elep <zakame@cpan.org>
# Thu, 17 Mar 2022 21:56:57 GMT
COPY file:3744c5cc39cdbdcae10db09a1f0f399005a79f93c237b387a72ff5710cdd458c in /usr/src/perl/ 
# Thu, 17 Mar 2022 21:57:03 GMT
WORKDIR /usr/src/perl
# Sat, 19 Mar 2022 08:19:03 GMT
RUN true     && curl -SL https://www.cpan.org/src/5.0/perl-5.34.1.tar.xz -o perl-5.34.1.tar.xz     && echo '6d52cf833ff1af27bb5e986870a2c30cec73c044b41e3458cd991f94374039f7 *perl-5.34.1.tar.xz' | sha256sum -c -     && tar --strip-components=1 -xaf perl-5.34.1.tar.xz -C /usr/src/perl     && rm perl-5.34.1.tar.xz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -LO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7044.tar.gz     && echo '9b60767fe40752ef7a9d3f13f19060a63389a5c23acc3e9827e19b75500f81f3 *App-cpanminus-1.7044.tar.gz' | sha256sum -c -     && tar -xzf App-cpanminus-1.7044.tar.gz && cd App-cpanminus-1.7044 && perl bin/cpanm . && cd /root     && true     && rm -fr ./cpanm /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7044* /tmp/*
# Sat, 19 Mar 2022 08:19:10 GMT
WORKDIR /
# Sat, 19 Mar 2022 08:19:16 GMT
CMD ["perl5.34.1" "-de0"]
```

-	Layers:
	-	`sha256:73de72abc870c163c22dfe15cfe1ed937cb3f6a4bba21ece0d7fac49af0e3cc0`  
		Last Modified: Thu, 17 Mar 2022 10:42:38 GMT  
		Size: 53.2 MB (53187444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cb7b2d10882abf71983dbea94cab908337239922a3f811e1a7bf38adea36a37`  
		Last Modified: Thu, 17 Mar 2022 19:50:49 GMT  
		Size: 4.9 MB (4910812 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fd267fe158b034479e5b906b37e6448e4abf719a073250d1670bc4859f1ea46`  
		Last Modified: Thu, 17 Mar 2022 19:50:52 GMT  
		Size: 10.7 MB (10658789 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3fd9f036e1e2b8bfe724c10bc3139cd9d66d005d798076c93e9d660332db9dd`  
		Last Modified: Thu, 17 Mar 2022 19:51:42 GMT  
		Size: 53.3 MB (53297407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a3d37ae79ce294f853f603b9d536ce65193c708322b05ef07479c67ace893ea`  
		Last Modified: Thu, 17 Mar 2022 19:53:45 GMT  
		Size: 178.7 MB (178684568 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea6763743ef1ce0c66c419de24f8ab6289eb9cd88a47d2e6635a46cc74f4ebd5`  
		Last Modified: Fri, 18 Mar 2022 06:05:46 GMT  
		Size: 179.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d366cedd68a4526e740b48fa0f53c5267b8f436672811b822322178817c6fcf6`  
		Last Modified: Sat, 19 Mar 2022 12:06:14 GMT  
		Size: 13.6 MB (13607826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `perl:5-threaded-bullseye` - linux; ppc64le

```console
$ docker pull perl@sha256:3c6f2fcb621796ffbea7ad57a8f899fece6964782376aa571eec822fd03c8b89
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **345.0 MB (345016520 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab4a27f9a0d043680fe93567e6311d55670a668ca4002512eb1b3d294737bfbd`
-	Default Command: `["perl5.34.1","-de0"]`

```dockerfile
# Thu, 17 Mar 2022 11:17:18 GMT
ADD file:c923f87aafa36beb6a65a06ebafd39557c7aa7cbd28e30202aae5219292bb1f7 in / 
# Thu, 17 Mar 2022 11:17:22 GMT
CMD ["bash"]
# Sat, 19 Mar 2022 05:39:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 05:39:56 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 19 Mar 2022 05:41:09 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 05:47:52 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 07:55:55 GMT
LABEL maintainer=Peter Martini <PeterCMartini@GMail.com>, Zak B. Elep <zakame@cpan.org>
# Sat, 19 Mar 2022 07:55:56 GMT
COPY file:3744c5cc39cdbdcae10db09a1f0f399005a79f93c237b387a72ff5710cdd458c in /usr/src/perl/ 
# Sat, 19 Mar 2022 07:55:58 GMT
WORKDIR /usr/src/perl
# Sat, 19 Mar 2022 08:45:18 GMT
RUN true     && curl -SL https://www.cpan.org/src/5.0/perl-5.34.1.tar.xz -o perl-5.34.1.tar.xz     && echo '6d52cf833ff1af27bb5e986870a2c30cec73c044b41e3458cd991f94374039f7 *perl-5.34.1.tar.xz' | sha256sum -c -     && tar --strip-components=1 -xaf perl-5.34.1.tar.xz -C /usr/src/perl     && rm perl-5.34.1.tar.xz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -LO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7044.tar.gz     && echo '9b60767fe40752ef7a9d3f13f19060a63389a5c23acc3e9827e19b75500f81f3 *App-cpanminus-1.7044.tar.gz' | sha256sum -c -     && tar -xzf App-cpanminus-1.7044.tar.gz && cd App-cpanminus-1.7044 && perl bin/cpanm . && cd /root     && true     && rm -fr ./cpanm /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7044* /tmp/*
# Sat, 19 Mar 2022 08:45:22 GMT
WORKDIR /
# Sat, 19 Mar 2022 08:45:26 GMT
CMD ["perl5.34.1" "-de0"]
```

-	Layers:
	-	`sha256:3eba077833cc07e760f6d7835470f68bfa37da9e30e164c5acb55a2be317cb9a`  
		Last Modified: Thu, 17 Mar 2022 11:27:38 GMT  
		Size: 58.8 MB (58842629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:606a8f23e2e92dfe52c8d6766e424128de38f3daf03ac630fcb4485deab4f2d5`  
		Last Modified: Sat, 19 Mar 2022 06:39:33 GMT  
		Size: 5.4 MB (5402016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f42cb9c0e6100c969995a76b5e25614396bdb4079794a9e37b61a6e13a0badd`  
		Last Modified: Sat, 19 Mar 2022 06:39:34 GMT  
		Size: 11.6 MB (11626006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cf6a22b7fd2790b3af2d142ff1f5f3601c6fbcaf889c3b37511fca470154f99`  
		Last Modified: Sat, 19 Mar 2022 06:40:22 GMT  
		Size: 58.9 MB (58854408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19f4bb633d127e55dbbfa2fce49955f044b7dd4cc21212dd1ecb2ffb1633ff7e`  
		Last Modified: Sat, 19 Mar 2022 06:42:12 GMT  
		Size: 195.9 MB (195920453 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:716857d25cff31296312c40f66109cbfa55c599ff95298a9bc96f7a58d683892`  
		Last Modified: Sat, 19 Mar 2022 11:38:22 GMT  
		Size: 202.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b88f5cf4d4dfad8b2c28a44ed777b7a277f69945471a17251e747ca5818a029e`  
		Last Modified: Sat, 19 Mar 2022 11:40:40 GMT  
		Size: 14.4 MB (14370806 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `perl:5-threaded-bullseye` - linux; s390x

```console
$ docker pull perl@sha256:7152bb45f89a4e2917ee5f6b0cae25f339a2c3d36fc571dc506a870bb6f81487
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **310.4 MB (310387074 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:326b825fe3a352f845f5dd1532d9ad89305af2f3e5e4893534d2dd3d42379fc6`
-	Default Command: `["perl5.34.1","-de0"]`

```dockerfile
# Thu, 17 Mar 2022 03:06:38 GMT
ADD file:75b45e65d2ec2c6822b1ddc46ff159dd10ac56bf9dff8b0996ac589a1ede22ff in / 
# Thu, 17 Mar 2022 03:06:42 GMT
CMD ["bash"]
# Thu, 17 Mar 2022 18:20:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 17 Mar 2022 18:20:43 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 17 Mar 2022 18:21:02 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 17 Mar 2022 18:21:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Mar 2022 12:50:26 GMT
LABEL maintainer=Peter Martini <PeterCMartini@GMail.com>, Zak B. Elep <zakame@cpan.org>
# Fri, 18 Mar 2022 12:50:27 GMT
COPY file:3744c5cc39cdbdcae10db09a1f0f399005a79f93c237b387a72ff5710cdd458c in /usr/src/perl/ 
# Fri, 18 Mar 2022 12:50:27 GMT
WORKDIR /usr/src/perl
# Sat, 19 Mar 2022 03:17:20 GMT
RUN true     && curl -SL https://www.cpan.org/src/5.0/perl-5.34.1.tar.xz -o perl-5.34.1.tar.xz     && echo '6d52cf833ff1af27bb5e986870a2c30cec73c044b41e3458cd991f94374039f7 *perl-5.34.1.tar.xz' | sha256sum -c -     && tar --strip-components=1 -xaf perl-5.34.1.tar.xz -C /usr/src/perl     && rm perl-5.34.1.tar.xz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -LO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7044.tar.gz     && echo '9b60767fe40752ef7a9d3f13f19060a63389a5c23acc3e9827e19b75500f81f3 *App-cpanminus-1.7044.tar.gz' | sha256sum -c -     && tar -xzf App-cpanminus-1.7044.tar.gz && cd App-cpanminus-1.7044 && perl bin/cpanm . && cd /root     && true     && rm -fr ./cpanm /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7044* /tmp/*
# Sat, 19 Mar 2022 03:17:22 GMT
WORKDIR /
# Sat, 19 Mar 2022 03:17:22 GMT
CMD ["perl5.34.1" "-de0"]
```

-	Layers:
	-	`sha256:ae9f1a186a2633be1ad71c317c2f195b221cef89502f9edc510b3a2049723758`  
		Last Modified: Thu, 17 Mar 2022 03:12:26 GMT  
		Size: 53.2 MB (53217527 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0d6229369d1bac8aa97bfefe6dd7990a66c0a3e98f420c282a39a279df7c391`  
		Last Modified: Thu, 17 Mar 2022 18:29:06 GMT  
		Size: 5.1 MB (5137013 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cf171d8059efb2bc6c026904c68dddd3487a129cd53d33def9589665326d56f`  
		Last Modified: Thu, 17 Mar 2022 18:29:07 GMT  
		Size: 10.8 MB (10761392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58cdad8e45654b094c248eb6bc86e3e0d8dda7b0e1df7c2792f2abb3a0d18cc8`  
		Last Modified: Thu, 17 Mar 2022 18:29:23 GMT  
		Size: 54.0 MB (54044974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9e2828c31b6d51c45569d0b8f772cf386976b6fe283da599e6548b290f167d0`  
		Last Modified: Thu, 17 Mar 2022 18:29:49 GMT  
		Size: 172.5 MB (172540992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19d01256dcc79614112ad2cf28e7273cc1bae7b91599b8499c10fe0ad9148713`  
		Last Modified: Fri, 18 Mar 2022 14:02:12 GMT  
		Size: 202.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7631278c649d7e96560b86df6832acb28d9737a4636d4c224e258724a10eb96`  
		Last Modified: Sat, 19 Mar 2022 04:16:53 GMT  
		Size: 14.7 MB (14684974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
