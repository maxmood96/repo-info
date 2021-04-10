## `perl:5-threaded-stretch`

```console
$ docker pull perl@sha256:96f1e312175f238551d008bee05ea2171eee14e03239c70fc64b91e10978c5c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `perl:5-threaded-stretch` - linux; amd64

```console
$ docker pull perl@sha256:e5d043552d65c7d0a5ef1cdf35cb4b22a5656296bd14345b8fe9f9826afd2f80
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **339.3 MB (339275272 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8fc6339faffcc8ca24b95ae32942bfd9f697631307c3c23078237db1143176e`
-	Default Command: `["perl5.32.1","-de0"]`

```dockerfile
# Tue, 30 Mar 2021 21:50:43 GMT
ADD file:e52290391b221e1a4e52cf4e41ffe7e14f162475964fa01638e03b3ead673ba1 in / 
# Tue, 30 Mar 2021 21:50:43 GMT
CMD ["bash"]
# Tue, 30 Mar 2021 23:08:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 30 Mar 2021 23:08:09 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 30 Mar 2021 23:08:42 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 30 Mar 2021 23:10:06 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 31 Mar 2021 06:13:01 GMT
LABEL maintainer=Peter Martini <PeterCMartini@GMail.com>, Zak B. Elep <zakame@cpan.org>
# Wed, 31 Mar 2021 06:13:02 GMT
COPY file:3744c5cc39cdbdcae10db09a1f0f399005a79f93c237b387a72ff5710cdd458c in /usr/src/perl/ 
# Wed, 31 Mar 2021 06:13:02 GMT
WORKDIR /usr/src/perl
# Wed, 31 Mar 2021 07:04:10 GMT
RUN true     && curl -SL https://www.cpan.org/src/5.0/perl-5.32.1.tar.xz -o perl-5.32.1.tar.xz     && echo '57cc47c735c8300a8ce2fa0643507b44c4ae59012bfdad0121313db639e02309 *perl-5.32.1.tar.xz' | sha256sum -c -     && tar --strip-components=1 -xaf perl-5.32.1.tar.xz -C /usr/src/perl     && rm perl-5.32.1.tar.xz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -LO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7044.tar.gz     && echo '9b60767fe40752ef7a9d3f13f19060a63389a5c23acc3e9827e19b75500f81f3 *App-cpanminus-1.7044.tar.gz' | sha256sum -c -     && tar -xzf App-cpanminus-1.7044.tar.gz && cd App-cpanminus-1.7044 && perl bin/cpanm . && cd /root     && true     && rm -fr ./cpanm /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7044* /tmp/*
# Wed, 31 Mar 2021 07:04:11 GMT
WORKDIR /
# Wed, 31 Mar 2021 07:04:11 GMT
CMD ["perl5.32.1" "-de0"]
```

-	Layers:
	-	`sha256:00168f89dbe8f3c9985e536784c27517f6cc35ea56263469449a6b73e0bed595`  
		Last Modified: Tue, 30 Mar 2021 21:56:37 GMT  
		Size: 45.4 MB (45379949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da61ad49fa9961d6dfe53dc067fd690133f205498e8045e8f7ef6b9da0d42bd2`  
		Last Modified: Tue, 30 Mar 2021 23:17:25 GMT  
		Size: 11.3 MB (11286658 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af62e04c0f85ed10801df4314d8cb9ba5e6c391f6a3c1db1080a0a78c8d4ed9d`  
		Last Modified: Tue, 30 Mar 2021 23:17:23 GMT  
		Size: 4.3 MB (4342466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aae835e2c68ef1d48a4ffef72547a79926019aec6a2bbeb5372f1e832ef453dd`  
		Last Modified: Tue, 30 Mar 2021 23:17:49 GMT  
		Size: 49.8 MB (49787075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5254dc317968c943c4321cdbf0364a6a47c833296b3f45e3bd27aa4efe28c865`  
		Last Modified: Tue, 30 Mar 2021 23:18:46 GMT  
		Size: 214.3 MB (214347447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e6837288b3b1387c9b2f38b3fca5fef5ebc93e020adff7ed1da68c3fe32a52f`  
		Last Modified: Wed, 31 Mar 2021 09:43:00 GMT  
		Size: 203.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e315659118efce0893bb410d03411a90f81f7c65e92ecf2fb277cccea951302`  
		Last Modified: Wed, 31 Mar 2021 09:44:49 GMT  
		Size: 14.1 MB (14131474 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `perl:5-threaded-stretch` - linux; arm variant v7

```console
$ docker pull perl@sha256:49493d69b6f7ef73506fe8fb266a550512fd8f6eb5d70469b58d8293aa6e7175
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **310.4 MB (310372919 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b86a6561df47dfb971996e4af018a3fc3a405c1dd3e1879e4646c157f1e25fa`
-	Default Command: `["perl5.32.1","-de0"]`

```dockerfile
# Tue, 30 Mar 2021 23:11:31 GMT
ADD file:65b5cf73b0b90f1f459a64d5706f2420deed7cdc5a9e13abacf5bcb05cc3138d in / 
# Tue, 30 Mar 2021 23:11:34 GMT
CMD ["bash"]
# Wed, 31 Mar 2021 01:29:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 31 Mar 2021 01:29:13 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 31 Mar 2021 01:30:03 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 31 Mar 2021 01:32:31 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 31 Mar 2021 03:28:01 GMT
LABEL maintainer=Peter Martini <PeterCMartini@GMail.com>, Zak B. Elep <zakame@cpan.org>
# Wed, 31 Mar 2021 03:28:02 GMT
COPY file:3744c5cc39cdbdcae10db09a1f0f399005a79f93c237b387a72ff5710cdd458c in /usr/src/perl/ 
# Wed, 31 Mar 2021 03:28:03 GMT
WORKDIR /usr/src/perl
# Wed, 31 Mar 2021 04:18:41 GMT
RUN true     && curl -SL https://www.cpan.org/src/5.0/perl-5.32.1.tar.xz -o perl-5.32.1.tar.xz     && echo '57cc47c735c8300a8ce2fa0643507b44c4ae59012bfdad0121313db639e02309 *perl-5.32.1.tar.xz' | sha256sum -c -     && tar --strip-components=1 -xaf perl-5.32.1.tar.xz -C /usr/src/perl     && rm perl-5.32.1.tar.xz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -LO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7044.tar.gz     && echo '9b60767fe40752ef7a9d3f13f19060a63389a5c23acc3e9827e19b75500f81f3 *App-cpanminus-1.7044.tar.gz' | sha256sum -c -     && tar -xzf App-cpanminus-1.7044.tar.gz && cd App-cpanminus-1.7044 && perl bin/cpanm . && cd /root     && true     && rm -fr ./cpanm /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7044* /tmp/*
# Wed, 31 Mar 2021 04:18:42 GMT
WORKDIR /
# Wed, 31 Mar 2021 04:18:44 GMT
CMD ["perl5.32.1" "-de0"]
```

-	Layers:
	-	`sha256:80ad3ae4821828f32ce9b3e0f76c3c8f157a7f111e64ffad3ba40287904dfc63`  
		Last Modified: Tue, 30 Mar 2021 23:18:47 GMT  
		Size: 42.1 MB (42120250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24b448d9cdc0300784b14c4a254300d86c316aca568d8b068cdc585ff456ccca`  
		Last Modified: Wed, 31 Mar 2021 01:39:43 GMT  
		Size: 9.9 MB (9939722 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3845e857248fe8de10609204e4eb4db8efcbb33c6a2f9e10b7d3efe4c3c625be`  
		Last Modified: Wed, 31 Mar 2021 01:39:41 GMT  
		Size: 3.9 MB (3921214 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2026eb34d858c1a9d59647eb6a6d3c28cd258eaa588cf3b99b35ac0d590fab2a`  
		Last Modified: Wed, 31 Mar 2021 01:40:05 GMT  
		Size: 46.1 MB (46127566 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c54ee28f5fa017782798168c4413003d88659984a23db27ea45095dcd3b95114`  
		Last Modified: Wed, 31 Mar 2021 01:41:08 GMT  
		Size: 195.0 MB (195008044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ceab305c643b50e134cf33273056ba73af7e37d192240431bfa36dc0f9fc85e6`  
		Last Modified: Wed, 31 Mar 2021 07:13:36 GMT  
		Size: 201.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:957941add1be1f29da232393e04958b58e79a908ead29ef885bd20e7f76454bc`  
		Last Modified: Wed, 31 Mar 2021 07:15:16 GMT  
		Size: 13.3 MB (13255922 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `perl:5-threaded-stretch` - linux; arm64 variant v8

```console
$ docker pull perl@sha256:3efb9c0fe028fe144445c7a5406679764ec6cd63f89ace25237c7f3ee17d93a2
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **320.9 MB (320862408 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc77877aaa97d5c346abf42fcfdbb13d685b45b125c00c09fc9ac197154a5d7f`
-	Default Command: `["perl5.32.1","-de0"]`

```dockerfile
# Tue, 30 Mar 2021 21:49:45 GMT
ADD file:0546f28e5d1be54699d1e0756275203da731735b3212f2ff1a87cd7f8dcc9049 in / 
# Tue, 30 Mar 2021 21:49:50 GMT
CMD ["bash"]
# Wed, 31 Mar 2021 00:22:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 31 Mar 2021 00:22:46 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 31 Mar 2021 00:23:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 31 Mar 2021 00:25:43 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 31 Mar 2021 02:07:13 GMT
LABEL maintainer=Peter Martini <PeterCMartini@GMail.com>, Zak B. Elep <zakame@cpan.org>
# Wed, 31 Mar 2021 02:07:14 GMT
COPY file:3744c5cc39cdbdcae10db09a1f0f399005a79f93c237b387a72ff5710cdd458c in /usr/src/perl/ 
# Wed, 31 Mar 2021 02:07:15 GMT
WORKDIR /usr/src/perl
# Wed, 31 Mar 2021 02:57:50 GMT
RUN true     && curl -SL https://www.cpan.org/src/5.0/perl-5.32.1.tar.xz -o perl-5.32.1.tar.xz     && echo '57cc47c735c8300a8ce2fa0643507b44c4ae59012bfdad0121313db639e02309 *perl-5.32.1.tar.xz' | sha256sum -c -     && tar --strip-components=1 -xaf perl-5.32.1.tar.xz -C /usr/src/perl     && rm perl-5.32.1.tar.xz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -LO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7044.tar.gz     && echo '9b60767fe40752ef7a9d3f13f19060a63389a5c23acc3e9827e19b75500f81f3 *App-cpanminus-1.7044.tar.gz' | sha256sum -c -     && tar -xzf App-cpanminus-1.7044.tar.gz && cd App-cpanminus-1.7044 && perl bin/cpanm . && cd /root     && true     && rm -fr ./cpanm /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7044* /tmp/*
# Wed, 31 Mar 2021 02:57:51 GMT
WORKDIR /
# Wed, 31 Mar 2021 02:57:52 GMT
CMD ["perl5.32.1" "-de0"]
```

-	Layers:
	-	`sha256:9317dc7ea567b49ade0ea730b5530d1363b065549e8b75a198e0b60bdde1f1d7`  
		Last Modified: Tue, 30 Mar 2021 21:56:46 GMT  
		Size: 43.2 MB (43177588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4eaf1b7b1bdfdc23af33da7d1fc9670524e63a8408bb04de9aebdf95979c5635`  
		Last Modified: Wed, 31 Mar 2021 00:33:12 GMT  
		Size: 10.2 MB (10201033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f4446041554682b465ef9a0e853a5067e7d794fa1c840946d140beab2ddeb51`  
		Last Modified: Wed, 31 Mar 2021 00:33:09 GMT  
		Size: 4.1 MB (4096741 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb0b477e68dd7171c7df2dfc66cd994be553e0679dd5c2083048d10d5a29363a`  
		Last Modified: Wed, 31 Mar 2021 00:33:40 GMT  
		Size: 47.7 MB (47735121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a8e162dfd38e34eeb2178da6fcb11b12f16ffa8bd96bbd6f0207dd5eceb7732`  
		Last Modified: Wed, 31 Mar 2021 00:34:37 GMT  
		Size: 201.7 MB (201719845 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d75919eba788ebdfc207cf349755d8978c2b1677a60fc63267b2da72bd9389c`  
		Last Modified: Wed, 31 Mar 2021 05:52:45 GMT  
		Size: 202.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32e4fae924081a8ea38a56a7a039b970a2d25521021b3177062e30c614285f38`  
		Last Modified: Wed, 31 Mar 2021 05:54:13 GMT  
		Size: 13.9 MB (13931878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `perl:5-threaded-stretch` - linux; 386

```console
$ docker pull perl@sha256:9662389911354b58c8006e9231f5f10e5cf3bd2772924413c76991dc4f8bc9dd
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **346.4 MB (346356328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5f0dbcd5d5d891924a36fec8b7b8868b2303b6a76c11d3f568403aeb493bba1`
-	Default Command: `["perl5.32.1","-de0"]`

```dockerfile
# Sat, 10 Apr 2021 00:41:14 GMT
ADD file:cebeeb1ed904e9433778c60c09ed31939334fd4f1c9550cce191b3bff4df0272 in / 
# Sat, 10 Apr 2021 00:41:14 GMT
CMD ["bash"]
# Sat, 10 Apr 2021 03:22:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 10 Apr 2021 03:22:34 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 10 Apr 2021 03:23:14 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Sat, 10 Apr 2021 03:24:55 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 10 Apr 2021 04:14:43 GMT
LABEL maintainer=Peter Martini <PeterCMartini@GMail.com>, Zak B. Elep <zakame@cpan.org>
# Sat, 10 Apr 2021 04:14:44 GMT
COPY file:3744c5cc39cdbdcae10db09a1f0f399005a79f93c237b387a72ff5710cdd458c in /usr/src/perl/ 
# Sat, 10 Apr 2021 04:14:44 GMT
WORKDIR /usr/src/perl
# Sat, 10 Apr 2021 05:22:52 GMT
RUN true     && curl -SL https://www.cpan.org/src/5.0/perl-5.32.1.tar.xz -o perl-5.32.1.tar.xz     && echo '57cc47c735c8300a8ce2fa0643507b44c4ae59012bfdad0121313db639e02309 *perl-5.32.1.tar.xz' | sha256sum -c -     && tar --strip-components=1 -xaf perl-5.32.1.tar.xz -C /usr/src/perl     && rm perl-5.32.1.tar.xz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -LO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7044.tar.gz     && echo '9b60767fe40752ef7a9d3f13f19060a63389a5c23acc3e9827e19b75500f81f3 *App-cpanminus-1.7044.tar.gz' | sha256sum -c -     && tar -xzf App-cpanminus-1.7044.tar.gz && cd App-cpanminus-1.7044 && perl bin/cpanm . && cd /root     && true     && rm -fr ./cpanm /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7044* /tmp/*
# Sat, 10 Apr 2021 05:22:53 GMT
WORKDIR /
# Sat, 10 Apr 2021 05:22:53 GMT
CMD ["perl5.32.1" "-de0"]
```

-	Layers:
	-	`sha256:f8270215e0f4bee2960e85333265840385530ee75e6f553f8cfc3e5b0534bf0e`  
		Last Modified: Sat, 10 Apr 2021 00:48:47 GMT  
		Size: 46.1 MB (46098724 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e882cae824a5753e90da159075517ecd98fd4d38f11d907927f6664b6913c74`  
		Last Modified: Sat, 10 Apr 2021 03:34:01 GMT  
		Size: 11.3 MB (11336698 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95a143794ab784f7db99b9f4ced22f07b03e17145a1b2b5ce5b731f4a3bad3f8`  
		Last Modified: Sat, 10 Apr 2021 03:33:59 GMT  
		Size: 4.6 MB (4565009 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1929129fdd2546c216795ea9a1841aac230e86cc565cb6476fd2bbb168e6ebbe`  
		Last Modified: Sat, 10 Apr 2021 03:34:26 GMT  
		Size: 51.3 MB (51264698 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15801b27fa97d290ae18cf943529c3a36e1ca45ee01de3c84913551e78e89281`  
		Last Modified: Sat, 10 Apr 2021 03:35:27 GMT  
		Size: 219.4 MB (219421873 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d19b63a7b6b917412632973c36cd741d298d7a3e51075f3ec16df443b5b5a9d6`  
		Last Modified: Sat, 10 Apr 2021 08:08:24 GMT  
		Size: 206.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9326457334d791ab2f017144eb489a23a459a787021b2b0ebbbae3c8f763a64c`  
		Last Modified: Sat, 10 Apr 2021 08:10:43 GMT  
		Size: 13.7 MB (13669120 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
