## `perl:devel`

```console
$ docker pull perl@sha256:78b6e8494c0a2b1f07bc9174564f347a2e271a9950111c63528b8305db1d74b9
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

### `perl:devel` - linux; amd64

```console
$ docker pull perl@sha256:768a5d20363ef6cf9a68841b9d0fc480e0015df0e8e3fe78030651a1a4190b39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **364.7 MB (364718221 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c824b3a3b4c7129f1567ba6a48e585eaecb77a8e8a199d2269ed19f4c361932`
-	Default Command: `["perl5.39.6","-de0"]`

```dockerfile
# Sun, 31 Dec 2023 10:01:19 GMT
ADD file:077a3156bd8271f26498ae6ac3800e68a42b9277581bc81eea31fec1a123dca5 in / 
# Sun, 31 Dec 2023 10:01:19 GMT
CMD ["bash"]
# Sun, 31 Dec 2023 10:01:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Sun, 31 Dec 2023 10:01:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Sun, 31 Dec 2023 10:01:19 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Sun, 31 Dec 2023 10:01:19 GMT
WORKDIR /usr/src/perl
# Sun, 31 Dec 2023 10:01:19 GMT
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/B/BO/BOOK/perl-5.39.6.tar.gz -o perl-5.39.6.tar.gz     && echo 'cb8715636bc744cca6e8864b6daa16f388d16ca3a134df6e6f35bbbe39dd7f63 *perl-5.39.6.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.39.6.tar.gz -C /usr/src/perl     && rm perl-5.39.6.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997014/cpm -o /usr/local/bin/cpm     && echo 'ee525f2493e36c6f688eddabaf53a51c4d3b2a4ebaa81576ac8b9f78ab57f4a1 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Sun, 31 Dec 2023 10:01:19 GMT
WORKDIR /usr/src/app
# Sun, 31 Dec 2023 10:01:19 GMT
CMD ["perl5.39.6" "-de0"]
```

-	Layers:
	-	`sha256:1b13d4e1a46e5e969702ec92b7c787c1b6891bff7c21ad378ff6dbc9e751d5d4`  
		Last Modified: Thu, 11 Jan 2024 02:42:04 GMT  
		Size: 49.6 MB (49561490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c74526957fc2157e8b0989072dc99b9582b398c12d1dcd40270fd76231bab0c`  
		Last Modified: Thu, 11 Jan 2024 04:44:35 GMT  
		Size: 24.0 MB (24046494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30d85599795460b2d9d24c6b87c53ec60555b601705cc83bea31632240500980`  
		Last Modified: Wed, 17 Jan 2024 02:00:06 GMT  
		Size: 64.1 MB (64139892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad5739181616b815fae7edc6bba689496674acbcf44e48a57fc7cc13a379b3a2`  
		Last Modified: Wed, 17 Jan 2024 02:00:48 GMT  
		Size: 211.1 MB (211103999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5aedae4caaaef150cad8cd7bcafe1516d831352a0b7451737c483b36568080be`  
		Last Modified: Wed, 17 Jan 2024 03:57:28 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6dd09e87ca779eb7bcd3a01e5ef8087ac83df7aae42f4ff45604d3fc0109543`  
		Last Modified: Wed, 17 Jan 2024 03:57:29 GMT  
		Size: 15.9 MB (15866079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41eba7347effdf53a0a4bcceef7c4e3a2049c9620aee9a83d0738f6357c8caa8`  
		Last Modified: Wed, 17 Jan 2024 03:57:28 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel` - unknown; unknown

```console
$ docker pull perl@sha256:2b67d58d7e1a575e3945d0950a3cce2eaef4225a1015f3d5bf4b2662a09fd181
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.4 MB (13418625 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:780bcf073e051fbb75b3bd8da8d85effbd6d857fc34944ef35398b2fc6e0754c`

```dockerfile
```

-	Layers:
	-	`sha256:f999f5aad1324caaf68255e1e709b94a0adaadfbdd7fdf6c3122aa9a63c33882`  
		Last Modified: Wed, 17 Jan 2024 03:57:29 GMT  
		Size: 13.4 MB (13401983 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1a4b5548ea2ae9bb07aeb5d8e39c7bd0a1715bd15aa1c8a0bd5f211cd5b516e1`  
		Last Modified: Wed, 17 Jan 2024 03:57:28 GMT  
		Size: 16.6 KB (16642 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel` - linux; arm variant v5

```console
$ docker pull perl@sha256:d140508c4b1fdcccdefc3ae9976c5ca2349e39ccfac058afb43293ad7aa7031a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **331.1 MB (331130809 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5daccb1401b8e9ca6781b169c844aad3182c3314bb38b52f0157199dddb73f3b`
-	Default Command: `["perl5.39.6","-de0"]`

```dockerfile
# Sun, 31 Dec 2023 10:01:19 GMT
ADD file:a0f6aa0cd43d2f5d230b0fc0ff4408d84c08d1f2bb9c4a0b781f38a9be437f33 in / 
# Sun, 31 Dec 2023 10:01:19 GMT
CMD ["bash"]
# Sun, 31 Dec 2023 10:01:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Sun, 31 Dec 2023 10:01:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Sun, 31 Dec 2023 10:01:19 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Sun, 31 Dec 2023 10:01:19 GMT
WORKDIR /usr/src/perl
# Sun, 31 Dec 2023 10:01:19 GMT
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/B/BO/BOOK/perl-5.39.6.tar.gz -o perl-5.39.6.tar.gz     && echo 'cb8715636bc744cca6e8864b6daa16f388d16ca3a134df6e6f35bbbe39dd7f63 *perl-5.39.6.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.39.6.tar.gz -C /usr/src/perl     && rm perl-5.39.6.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997014/cpm -o /usr/local/bin/cpm     && echo 'ee525f2493e36c6f688eddabaf53a51c4d3b2a4ebaa81576ac8b9f78ab57f4a1 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Sun, 31 Dec 2023 10:01:19 GMT
WORKDIR /usr/src/app
# Sun, 31 Dec 2023 10:01:19 GMT
CMD ["perl5.39.6" "-de0"]
```

-	Layers:
	-	`sha256:4aaad31c96d846308a92a43b3da192033e7d93114975064de59eead39852d764`  
		Last Modified: Thu, 11 Jan 2024 01:53:38 GMT  
		Size: 47.3 MB (47319075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0152a384e8878c46118f3126b9adf0d1b37da59b15217012bce436250aca97ad`  
		Last Modified: Thu, 11 Jan 2024 07:05:51 GMT  
		Size: 22.7 MB (22724699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca93e1c73a3e924629183fbef48c0bdfa4c2dee03c4e924e6d5c99a7c4e4df48`  
		Last Modified: Wed, 17 Jan 2024 02:01:53 GMT  
		Size: 61.5 MB (61515317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce6d73b86dbe73f1f5c49661d4d4f94bb594cc277044fdd8740201c78665070c`  
		Last Modified: Wed, 17 Jan 2024 02:02:43 GMT  
		Size: 184.4 MB (184416665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c25e2b2d02a912cc6216d92dda429662cd1c75e036f6fda7537b23ca5d28a29d`  
		Last Modified: Wed, 17 Jan 2024 22:05:24 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc07fbc989bad63b28a8335007b4bdf4aa578778d43098fa267d09591715967a`  
		Last Modified: Thu, 18 Jan 2024 03:18:53 GMT  
		Size: 15.2 MB (15154785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0979a251208d9fb994701a81778399626d8e240c97028bad88a752db9f3f71ff`  
		Last Modified: Thu, 18 Jan 2024 03:18:52 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel` - unknown; unknown

```console
$ docker pull perl@sha256:15338e684c3d9bd09c2a11863153636f16f1ec43b166b185340f25ac840d4c6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.2 MB (13243230 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfe39898e4a32ee344477fc6f9ce6885dae86eaf531b64cd5f32dfcfbdbe70f7`

```dockerfile
```

-	Layers:
	-	`sha256:b5eefec24d46d6b2cf0e94a928faa4244e36e0bacdb90ecb33b1e178bff32268`  
		Last Modified: Thu, 18 Jan 2024 03:18:52 GMT  
		Size: 13.2 MB (13227165 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:558efb07ca299dff699a17765716c3c5f1698b52dec79dd12e313be8ec20ff3d`  
		Last Modified: Thu, 18 Jan 2024 03:18:52 GMT  
		Size: 16.1 KB (16065 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel` - linux; arm variant v7

```console
$ docker pull perl@sha256:646348d103872b411023094c39fbb0160045dc0b6820c92d37bccbdf4f9db2bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **316.3 MB (316328913 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38dd5c09a1f47c8a5413c6ebafcae5464d0065aa266096b4215ad2e9e6ea23ed`
-	Default Command: `["perl5.39.6","-de0"]`

```dockerfile
# Sun, 31 Dec 2023 10:01:19 GMT
ADD file:781c48325e0a88993e9f749e0cd761de39d671e9a23223797cb25431ac40d39a in / 
# Sun, 31 Dec 2023 10:01:19 GMT
CMD ["bash"]
# Sun, 31 Dec 2023 10:01:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Sun, 31 Dec 2023 10:01:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Sun, 31 Dec 2023 10:01:19 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Sun, 31 Dec 2023 10:01:19 GMT
WORKDIR /usr/src/perl
# Sun, 31 Dec 2023 10:01:19 GMT
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/B/BO/BOOK/perl-5.39.6.tar.gz -o perl-5.39.6.tar.gz     && echo 'cb8715636bc744cca6e8864b6daa16f388d16ca3a134df6e6f35bbbe39dd7f63 *perl-5.39.6.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.39.6.tar.gz -C /usr/src/perl     && rm perl-5.39.6.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997014/cpm -o /usr/local/bin/cpm     && echo 'ee525f2493e36c6f688eddabaf53a51c4d3b2a4ebaa81576ac8b9f78ab57f4a1 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Sun, 31 Dec 2023 10:01:19 GMT
WORKDIR /usr/src/app
# Sun, 31 Dec 2023 10:01:19 GMT
CMD ["perl5.39.6" "-de0"]
```

-	Layers:
	-	`sha256:1d306580a85c9098725ffcffdc42e708e47695a4be4626d1dc152e55ec7f04c2`  
		Last Modified: Thu, 11 Jan 2024 02:48:11 GMT  
		Size: 45.2 MB (45156672 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0f838a77ac7b077a6478dbd3e8ae86811e8e8421b22a470d01688f320c26ea3`  
		Last Modified: Thu, 11 Jan 2024 03:28:50 GMT  
		Size: 21.9 MB (21949911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c77a5ad50b17b550d0d7c458e20b93871af72456b17094173adc0ee560aa0a7`  
		Last Modified: Thu, 11 Jan 2024 03:29:16 GMT  
		Size: 59.2 MB (59212918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ecd8868ebea1b4c1af666b37d45a32f1a4e81b375da02dd00a533b29902c7c6`  
		Last Modified: Thu, 11 Jan 2024 03:30:07 GMT  
		Size: 175.1 MB (175075336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad56473afa65b5d7a9f9ee97a21e1aacb921d8f63c30b036f3c207d8cb36834b`  
		Last Modified: Fri, 12 Jan 2024 19:43:58 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcf5df024446e7a5bfa9ba8b00ea44c67dcc7903c0deb137c55f492da74ada69`  
		Last Modified: Sat, 13 Jan 2024 08:18:34 GMT  
		Size: 14.9 MB (14933809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3de3e55e41ccc4afbc621266bbf9ef55ad3f820bc7e19cebbe6a32d9b8fca5e9`  
		Last Modified: Sat, 13 Jan 2024 08:18:33 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel` - unknown; unknown

```console
$ docker pull perl@sha256:2d0b4d625e7790b7ef1e88073c32e2f01c30f57dd9ed960342e1905ebfec2e15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.2 MB (13248704 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aea3bca3a0461aa998736fbf53f376e7bc580679e6d4f0f1d43a4234428564b8`

```dockerfile
```

-	Layers:
	-	`sha256:dc6299df37de56670374cb25dfedd0355e79c80ba57bec24cedb5fda6b7c94e5`  
		Last Modified: Sat, 13 Jan 2024 08:18:34 GMT  
		Size: 13.2 MB (13232639 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e5f74d804c7399cc26318e47ec7b65b5fdd58015698cc8e3d70a617ed0bb0f1e`  
		Last Modified: Sat, 13 Jan 2024 08:18:33 GMT  
		Size: 16.1 KB (16065 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel` - linux; arm64 variant v8

```console
$ docker pull perl@sha256:b917129382d005f26de3d34fa2fb15dfeaf2f35d2ea4d0148538def4909ae4f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **355.5 MB (355485649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1d3fc6650272f4fc778201e2aa7982552deea12b47449308d8ebecedd7bea1f`
-	Default Command: `["perl5.39.6","-de0"]`

```dockerfile
# Sun, 31 Dec 2023 10:01:19 GMT
ADD file:051a18650d326af1d23e30c93370e647e62f94887ce43b22e1808052bce4f2a6 in / 
# Sun, 31 Dec 2023 10:01:19 GMT
CMD ["bash"]
# Sun, 31 Dec 2023 10:01:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Sun, 31 Dec 2023 10:01:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Sun, 31 Dec 2023 10:01:19 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Sun, 31 Dec 2023 10:01:19 GMT
WORKDIR /usr/src/perl
# Sun, 31 Dec 2023 10:01:19 GMT
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/B/BO/BOOK/perl-5.39.6.tar.gz -o perl-5.39.6.tar.gz     && echo 'cb8715636bc744cca6e8864b6daa16f388d16ca3a134df6e6f35bbbe39dd7f63 *perl-5.39.6.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.39.6.tar.gz -C /usr/src/perl     && rm perl-5.39.6.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997014/cpm -o /usr/local/bin/cpm     && echo 'ee525f2493e36c6f688eddabaf53a51c4d3b2a4ebaa81576ac8b9f78ab57f4a1 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Sun, 31 Dec 2023 10:01:19 GMT
WORKDIR /usr/src/app
# Sun, 31 Dec 2023 10:01:19 GMT
CMD ["perl5.39.6" "-de0"]
```

-	Layers:
	-	`sha256:5665c1f9a9e17acd68ae05b2839df402eac34afdd095f8c115f09886d757840c`  
		Last Modified: Thu, 11 Jan 2024 02:43:41 GMT  
		Size: 49.6 MB (49592247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f419b1a62fc83850ab3cb43274970bb20a18ae6e674535478a48f5bee11559b6`  
		Last Modified: Thu, 11 Jan 2024 09:34:07 GMT  
		Size: 23.6 MB (23582592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:069a35492a4c5b1727f36b1184c413a96ce816d65578adaf3bce2023a1765c0a`  
		Last Modified: Thu, 11 Jan 2024 09:34:23 GMT  
		Size: 64.0 MB (63990799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:599ff0dd2e5531872126111c843bb09b42ae90ff2d37c73e897d9e2e86c995a9`  
		Last Modified: Thu, 11 Jan 2024 09:34:53 GMT  
		Size: 202.5 MB (202501344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf2dd810aaf833bcb67da65925cf6baa78d943c0f3cc239e7aa89f662ec2fcef`  
		Last Modified: Fri, 12 Jan 2024 09:33:24 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d6e96a63fdd68b825bd2e2616e7a1a6c2bb3254b7fd55fe25d0de1228ddc780`  
		Last Modified: Fri, 12 Jan 2024 15:21:58 GMT  
		Size: 15.8 MB (15818400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:666ec2ee0252dea9cb35b53b414230c2c50d514d660e96e669853897f23880df`  
		Last Modified: Fri, 12 Jan 2024 15:21:57 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel` - unknown; unknown

```console
$ docker pull perl@sha256:46700cf3c1e7ff185acbb4770544b4fc01fdf5cc320d333c85f7105a18d8ab45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.4 MB (13443205 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a4e68bf2de20a9562ba158141eeaae9c2207a1aefc9a0e0129340f32d99a73d`

```dockerfile
```

-	Layers:
	-	`sha256:d24a8eae206ebae0d993c7e3eedb84f5e95da954e00f9dce942ca2900a7cfe54`  
		Last Modified: Fri, 12 Jan 2024 15:21:58 GMT  
		Size: 13.4 MB (13427212 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:06c64fe7af476ddea933cfb429812c5537104fcf37e1e18af69e16368b4603f0`  
		Last Modified: Fri, 12 Jan 2024 15:21:57 GMT  
		Size: 16.0 KB (15993 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel` - linux; 386

```console
$ docker pull perl@sha256:3b9131731d71f5ad3f416d7a998afc599ddc51405af43712fb2ec06bebf9ea9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **366.9 MB (366852098 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1ba41b81ffb51410a886adb10d769f8fe38759effcc8f4ace7d303759be5d9f`
-	Default Command: `["perl5.39.6","-de0"]`

```dockerfile
# Sun, 31 Dec 2023 10:01:19 GMT
ADD file:c7cf48f483b7eba0a82956c5ef1a1c78e84c2b91d0b9cf17fdfde5b756fcba9f in / 
# Sun, 31 Dec 2023 10:01:19 GMT
CMD ["bash"]
# Sun, 31 Dec 2023 10:01:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Sun, 31 Dec 2023 10:01:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Sun, 31 Dec 2023 10:01:19 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Sun, 31 Dec 2023 10:01:19 GMT
WORKDIR /usr/src/perl
# Sun, 31 Dec 2023 10:01:19 GMT
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/B/BO/BOOK/perl-5.39.6.tar.gz -o perl-5.39.6.tar.gz     && echo 'cb8715636bc744cca6e8864b6daa16f388d16ca3a134df6e6f35bbbe39dd7f63 *perl-5.39.6.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.39.6.tar.gz -C /usr/src/perl     && rm perl-5.39.6.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997014/cpm -o /usr/local/bin/cpm     && echo 'ee525f2493e36c6f688eddabaf53a51c4d3b2a4ebaa81576ac8b9f78ab57f4a1 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Sun, 31 Dec 2023 10:01:19 GMT
WORKDIR /usr/src/app
# Sun, 31 Dec 2023 10:01:19 GMT
CMD ["perl5.39.6" "-de0"]
```

-	Layers:
	-	`sha256:348e22f3afa19ef4ed67af4c0a3dfafe2c1311e99bde0b9039be46cafd8069f8`  
		Last Modified: Thu, 11 Jan 2024 02:42:53 GMT  
		Size: 50.6 MB (50581977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4abfb5cb040b6af10cb1e9ac26bb34229604ca8c2cd52ef5bf19c4b933dd6600`  
		Last Modified: Thu, 11 Jan 2024 04:41:29 GMT  
		Size: 24.9 MB (24884306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b02d03ac10f8c192e0b06aa689206512609710cce15b14a04e9b07acdfcabed`  
		Last Modified: Wed, 17 Jan 2024 01:50:18 GMT  
		Size: 66.0 MB (65986657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca6edbc2629664e5add77360ae4f09858d24bb963bb6a217cfeaaf1dfb21dcb6`  
		Last Modified: Wed, 17 Jan 2024 01:51:08 GMT  
		Size: 210.0 MB (210036557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed8d7aba2a6dd3f8d96b8df17cf9d48c176a126c44643bb02e59cac0ca563bcd`  
		Last Modified: Wed, 17 Jan 2024 03:58:23 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d144ceb5e3a19df86a6d0d34bc6a2f60114a964ead13d8a0a14888584238dc84`  
		Last Modified: Wed, 17 Jan 2024 03:58:23 GMT  
		Size: 15.4 MB (15362334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b8883ae620306c1c5f122bf7982d087d587e69b8473ef5f19825f017e9dab7e`  
		Last Modified: Wed, 17 Jan 2024 03:58:22 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel` - unknown; unknown

```console
$ docker pull perl@sha256:bed275b612ba6e895bc56a14f185c8041c56e9653888d99c269f4de3389b93bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.4 MB (13399010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f7571631e551caf5fdea53c7f1918f801d7de9926518794234ba8d98081312c`

```dockerfile
```

-	Layers:
	-	`sha256:eeb23d0ba180251556a44f9c0397ac0649b39b10d315ad49f82afcb961da301a`  
		Last Modified: Wed, 17 Jan 2024 03:58:23 GMT  
		Size: 13.4 MB (13382407 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4d503594419b3353cb5d377f3c09a387a867ac94e7878040c525023e0ce4bde2`  
		Last Modified: Wed, 17 Jan 2024 03:58:22 GMT  
		Size: 16.6 KB (16603 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel` - linux; mips64le

```console
$ docker pull perl@sha256:a080cb0266644c8765ce61ed7bcdf42df98f048bbd87155367f7551a680bf041
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **340.9 MB (340914616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25fd91ed2c626b759aa4fbd7b8fad2dfec4c1d5376235d0c99becb8a43807e68`
-	Default Command: `["perl5.39.6","-de0"]`

```dockerfile
# Sun, 31 Dec 2023 10:01:19 GMT
ADD file:e632734e8c2b1e7594b8a79fefe3b2790d6e662e647019a7daa2713f4b1aa7be in / 
# Sun, 31 Dec 2023 10:01:19 GMT
CMD ["bash"]
# Sun, 31 Dec 2023 10:01:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Sun, 31 Dec 2023 10:01:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Sun, 31 Dec 2023 10:01:19 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Sun, 31 Dec 2023 10:01:19 GMT
WORKDIR /usr/src/perl
# Sun, 31 Dec 2023 10:01:19 GMT
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/B/BO/BOOK/perl-5.39.6.tar.gz -o perl-5.39.6.tar.gz     && echo 'cb8715636bc744cca6e8864b6daa16f388d16ca3a134df6e6f35bbbe39dd7f63 *perl-5.39.6.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.39.6.tar.gz -C /usr/src/perl     && rm perl-5.39.6.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997014/cpm -o /usr/local/bin/cpm     && echo 'ee525f2493e36c6f688eddabaf53a51c4d3b2a4ebaa81576ac8b9f78ab57f4a1 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Sun, 31 Dec 2023 10:01:19 GMT
WORKDIR /usr/src/app
# Sun, 31 Dec 2023 10:01:19 GMT
CMD ["perl5.39.6" "-de0"]
```

-	Layers:
	-	`sha256:32de429a78b4633d08d4ddf9cb62b7ff44ee9ed79fafe52b6d33ec4e772c2beb`  
		Last Modified: Thu, 11 Jan 2024 02:21:59 GMT  
		Size: 49.5 MB (49548641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bdc39b4d6447f4b14a9d2668a4ec5e5cf44bb6dd0d7958fc882ba5d7297cd1c`  
		Last Modified: Thu, 11 Jan 2024 03:24:15 GMT  
		Size: 23.6 MB (23630453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1db1512d660252aea394ce778a64b88e7f0b13cc6560953b1615531e4e266d3a`  
		Last Modified: Wed, 17 Jan 2024 02:47:38 GMT  
		Size: 63.0 MB (62965856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee3e4851ee9e93f911d9b949bc1799a9e435ec91bbe77d96918f320eb188bc13`  
		Last Modified: Wed, 17 Jan 2024 02:49:54 GMT  
		Size: 189.7 MB (189696913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a3edd472eba3d90a79c1d237bc1c055ea89ff21a70ffde1bde4ed80c49e40e9`  
		Last Modified: Wed, 17 Jan 2024 07:20:36 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a6ca9579de459305c384d94bdbd1f0f8c2165d96a21a7bd9ed548f355652b34`  
		Last Modified: Wed, 17 Jan 2024 11:57:13 GMT  
		Size: 15.1 MB (15072486 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d55ac1c353c7984f1892d1dac504d36c7ce6399c76fe6fe85f0c4caac267687b`  
		Last Modified: Wed, 17 Jan 2024 11:57:12 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel` - unknown; unknown

```console
$ docker pull perl@sha256:7f517865a434ddf4d756efe0317b41eb99e602f16a01a79c2c37106cd33fb3ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.8 KB (15837 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76a7ee644521b851e6e732936815f3f40930a5bf73ccbddf153495bfb60821ea`

```dockerfile
```

-	Layers:
	-	`sha256:5923db16e67baaa7d4547d8679ce4d35058eed606a3be388640f07278140aa00`  
		Last Modified: Wed, 17 Jan 2024 11:57:11 GMT  
		Size: 15.8 KB (15837 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel` - linux; ppc64le

```console
$ docker pull perl@sha256:fe06ac7e89736db757c4b2891a59ef3d7b474edd7549fa4125028246f04805ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **378.8 MB (378834210 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb511fb7fd366481b5edd5435a20fd8e58dc826d3f8081a4f8bfa26dbd02e940`
-	Default Command: `["perl5.39.6","-de0"]`

```dockerfile
# Sun, 31 Dec 2023 10:01:19 GMT
ADD file:181ff897280683d4e2f512551aa99c5bca9823305859ed4620c8ea3bd4d95cd5 in / 
# Sun, 31 Dec 2023 10:01:19 GMT
CMD ["bash"]
# Sun, 31 Dec 2023 10:01:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Sun, 31 Dec 2023 10:01:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Sun, 31 Dec 2023 10:01:19 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Sun, 31 Dec 2023 10:01:19 GMT
WORKDIR /usr/src/perl
# Sun, 31 Dec 2023 10:01:19 GMT
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/B/BO/BOOK/perl-5.39.6.tar.gz -o perl-5.39.6.tar.gz     && echo 'cb8715636bc744cca6e8864b6daa16f388d16ca3a134df6e6f35bbbe39dd7f63 *perl-5.39.6.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.39.6.tar.gz -C /usr/src/perl     && rm perl-5.39.6.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997014/cpm -o /usr/local/bin/cpm     && echo 'ee525f2493e36c6f688eddabaf53a51c4d3b2a4ebaa81576ac8b9f78ab57f4a1 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Sun, 31 Dec 2023 10:01:19 GMT
WORKDIR /usr/src/app
# Sun, 31 Dec 2023 10:01:19 GMT
CMD ["perl5.39.6" "-de0"]
```

-	Layers:
	-	`sha256:62296c33e75415de6ebf7e20132da876513ede04af94472801e60452c0a295dd`  
		Last Modified: Thu, 11 Jan 2024 02:38:58 GMT  
		Size: 53.6 MB (53557571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef08c7f22c453d0296f7b3aac215dd01664f85d00e83a734e65de9f4669b9b11`  
		Last Modified: Thu, 11 Jan 2024 07:23:16 GMT  
		Size: 25.7 MB (25696347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0b4b3bd26123c050bfca2111b37a82d4c385c67c129372b0688d3bea5051428`  
		Last Modified: Wed, 17 Jan 2024 03:24:46 GMT  
		Size: 69.6 MB (69581529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea6b71c229676130f942ae91085124d04316997b949d1ba7a6500b460e2ce5ef`  
		Last Modified: Wed, 17 Jan 2024 03:25:28 GMT  
		Size: 214.1 MB (214137619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b824a2d88d950a29a9b7634fb30b6d2c1291ac43d6afde65f64039ef61f8bb96`  
		Last Modified: Wed, 17 Jan 2024 18:17:57 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f583281f1e3f9460c900846e94acc42141ac04ff314ddceb5e26738f9cd7ed01`  
		Last Modified: Wed, 17 Jan 2024 19:24:19 GMT  
		Size: 15.9 MB (15860876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ceb9d5d3f21b4de6048dbe46aaa7cbec371b9f146c4d2de6225e877e8b5fedf9`  
		Last Modified: Wed, 17 Jan 2024 19:24:18 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel` - unknown; unknown

```console
$ docker pull perl@sha256:211dbdbf9b67a03e62d70d143821e673eb1c459160ed5e79e206acbe6b4af327
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.4 MB (13399384 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbb69f63d470e6714ef4bdf0aed171360c3da76e616331d9b43ab1b67024d939`

```dockerfile
```

-	Layers:
	-	`sha256:7e389e467d6facff9cf5440336eb8efe734fa795d022efae25a364e282bee78f`  
		Last Modified: Wed, 17 Jan 2024 19:24:18 GMT  
		Size: 13.4 MB (13383355 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c1795de298c853705ce63a70ead297a937738b7da768bedb90055561b3f79ef7`  
		Last Modified: Wed, 17 Jan 2024 19:24:17 GMT  
		Size: 16.0 KB (16029 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel` - linux; s390x

```console
$ docker pull perl@sha256:d2098bb815582d40a796f8d49703aa129278d7f94332388f1efb7566ed25ffc0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **334.4 MB (334435274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae6ae3359b91b82ae8b261af76ec1f6a62ae6f8533832d0a38eeec17ab2cfa4f`
-	Default Command: `["perl5.39.6","-de0"]`

```dockerfile
# Sun, 31 Dec 2023 10:01:19 GMT
ADD file:b52927273f91d79b0b493ff5507714cde656c5d76433c6c5b3dafd358f4ed7cd in / 
# Sun, 31 Dec 2023 10:01:19 GMT
CMD ["bash"]
# Sun, 31 Dec 2023 10:01:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Sun, 31 Dec 2023 10:01:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Sun, 31 Dec 2023 10:01:19 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Sun, 31 Dec 2023 10:01:19 GMT
WORKDIR /usr/src/perl
# Sun, 31 Dec 2023 10:01:19 GMT
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/B/BO/BOOK/perl-5.39.6.tar.gz -o perl-5.39.6.tar.gz     && echo 'cb8715636bc744cca6e8864b6daa16f388d16ca3a134df6e6f35bbbe39dd7f63 *perl-5.39.6.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.39.6.tar.gz -C /usr/src/perl     && rm perl-5.39.6.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997014/cpm -o /usr/local/bin/cpm     && echo 'ee525f2493e36c6f688eddabaf53a51c4d3b2a4ebaa81576ac8b9f78ab57f4a1 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Sun, 31 Dec 2023 10:01:19 GMT
WORKDIR /usr/src/app
# Sun, 31 Dec 2023 10:01:19 GMT
CMD ["perl5.39.6" "-de0"]
```

-	Layers:
	-	`sha256:d28727deb22d156e281ef621e3fd48900f453abc05f099f88bfed20e0f5861b3`  
		Last Modified: Thu, 11 Jan 2024 01:50:35 GMT  
		Size: 47.9 MB (47917872 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdcda5a31401318d38b94cd36426844d1953c0561252561b5205f9b95c442bac`  
		Last Modified: Thu, 11 Jan 2024 02:21:00 GMT  
		Size: 24.0 MB (24043257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aedec06e2299acdad20937d3ac11c81765c143d0fff2fd0ddaff6c61163c7607`  
		Last Modified: Thu, 11 Jan 2024 02:21:18 GMT  
		Size: 63.1 MB (63126669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d20571d211396386902ec075688f72c4477e7e3fa60768de687b2cb055108e30`  
		Last Modified: Thu, 11 Jan 2024 02:21:50 GMT  
		Size: 183.1 MB (183143485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97107e92d4f03e36025d9c410e91f7502c1a995dbeb29e6467ab84cc1c175fa8`  
		Last Modified: Fri, 12 Jan 2024 10:38:29 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c309493851e9217dde6fa42ff76f380366ad0b9753aebe70fafcd401b99c7929`  
		Last Modified: Fri, 12 Jan 2024 13:26:28 GMT  
		Size: 16.2 MB (16203723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b06ca4f9f4b80abd003e60afe0abc0710783f0b0cf4969565b6a391a0bdf9590`  
		Last Modified: Fri, 12 Jan 2024 13:26:27 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel` - unknown; unknown

```console
$ docker pull perl@sha256:c8bee620a23ee36912eaabe79d67c83c3cae19138f921ba96c0b615bfe84b354
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.3 MB (13254062 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2df6f80cd984f9d2f18f7bbe4623e358760c665617e8e525c25d4f33d5653ae1`

```dockerfile
```

-	Layers:
	-	`sha256:71b59b653409877711a70e83fa7ee9f1bd0f5deb53dff8968ae0a479b57578a8`  
		Last Modified: Fri, 12 Jan 2024 13:26:28 GMT  
		Size: 13.2 MB (13238083 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e2cfee92b8ba65a4dfd620361b2bb61500de150613bfa5de6b6f84cb3314217b`  
		Last Modified: Fri, 12 Jan 2024 13:26:27 GMT  
		Size: 16.0 KB (15979 bytes)  
		MIME: application/vnd.in-toto+json
