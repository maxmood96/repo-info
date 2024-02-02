## `perl:devel-threaded-bullseye`

```console
$ docker pull perl@sha256:e48d2511db82ed47a5e2bd41fe455ba4f016ac25bb88011b62a0d253d831fc0a
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

### `perl:devel-threaded-bullseye` - linux; amd64

```console
$ docker pull perl@sha256:f72e25f9dd69fac3518c8641ea097f479d3c84fa0f770a844437f1f36ec046b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **338.2 MB (338235482 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d56ef34bafee87b177c870f5accb5b2477dca7e3f8724e300dc8cdbe715ae563`
-	Default Command: `["perl5.39.7","-de0"]`

```dockerfile
# Sat, 20 Jan 2024 20:51:34 GMT
ADD file:4fa73c8d113df02c8656b74ab87563432215332f3de78446a02e5ab7d6e2ab7a in / 
# Sat, 20 Jan 2024 20:51:34 GMT
CMD ["bash"]
# Sat, 20 Jan 2024 20:51:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 20 Jan 2024 20:51:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 20 Jan 2024 20:51:34 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 20 Jan 2024 20:51:34 GMT
WORKDIR /usr/src/perl
# Sat, 20 Jan 2024 20:51:34 GMT
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/C/CO/CORION/perl-5.39.7.tar.gz -o perl-5.39.7.tar.gz     && echo 'c85f9ef13fa674839b076d81edb45242a5ddff3df4b111f764a7abe72edd83eb *perl-5.39.7.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.39.7.tar.gz -C /usr/src/perl     && rm perl-5.39.7.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997014/cpm -o /usr/local/bin/cpm     && echo 'ee525f2493e36c6f688eddabaf53a51c4d3b2a4ebaa81576ac8b9f78ab57f4a1 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Sat, 20 Jan 2024 20:51:34 GMT
WORKDIR /usr/src/app
# Sat, 20 Jan 2024 20:51:34 GMT
CMD ["perl5.39.7" "-de0"]
```

-	Layers:
	-	`sha256:7faaa42ac0c18c9baf539c97a5c8f042d02a77b05380cb57759e4407385710dc`  
		Last Modified: Wed, 31 Jan 2024 22:40:15 GMT  
		Size: 55.1 MB (55056963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1efd1e766326156b6d61b11d929f560cb73024ca0ff2a896b23e8bc6e0044244`  
		Last Modified: Wed, 31 Jan 2024 23:33:27 GMT  
		Size: 15.8 MB (15765028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f124d049a72aebbe5ef2fd589921f51fde08aa5b66cfa8cf81748411af8874dc`  
		Last Modified: Wed, 31 Jan 2024 23:33:44 GMT  
		Size: 54.6 MB (54601507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c200adf1811433c67c208599f5f71578e5237cfd9be60d64045c78282562b77`  
		Last Modified: Wed, 31 Jan 2024 23:34:15 GMT  
		Size: 196.9 MB (196898029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a81e50e5cc50502b86a1856d80b2285b3305be45c20569c7669b3b8f8b1c9790`  
		Last Modified: Thu, 01 Feb 2024 00:04:25 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebe0c9cc34d5d47e949843b9f2253174544fe281302d8b59e6adcdc1afef3c45`  
		Last Modified: Thu, 01 Feb 2024 00:04:26 GMT  
		Size: 15.9 MB (15913690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8423e53b640ddc0409e705db7b642a3289210c56edb7f53a293962a2729cf63`  
		Last Modified: Thu, 01 Feb 2024 00:04:25 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-threaded-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:9cfc80960d2991c4b0da7559a08b94b90d36f3536933ab4bfc5e1c3644069cf3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.0 MB (12967977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:283331836f8be196d9934927a5b59be31abb63b1252947d1a58427a50b8f7490`

```dockerfile
```

-	Layers:
	-	`sha256:9374f30862dc33fa28a245dd3817649d1cccb692bbf548feef530469aa2859f4`  
		Last Modified: Thu, 01 Feb 2024 00:04:25 GMT  
		Size: 13.0 MB (12952104 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:14084d7f27030d73b5d9d5e8ad690ae5b0dbc6c13407e45d939647a5e6ca3e20`  
		Last Modified: Thu, 01 Feb 2024 00:04:24 GMT  
		Size: 15.9 KB (15873 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-threaded-bullseye` - linux; arm variant v5

```console
$ docker pull perl@sha256:9d2c900972c6a24933c8ab09c4c7cfa137b0ed264f91f23c70f82c8a893372d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **310.6 MB (310557825 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0558baaaa1e3e59265140c59edd0eb08560d937567c3989dd8e018f715ed2cc`
-	Default Command: `["perl5.39.7","-de0"]`

```dockerfile
# Sat, 20 Jan 2024 20:51:34 GMT
ADD file:b3de5afb7e9c6d6d7f3bca38d87575a8f510b9eb6ee1aca78b37cd5792f6cd3d in / 
# Sat, 20 Jan 2024 20:51:34 GMT
CMD ["bash"]
# Sat, 20 Jan 2024 20:51:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 20 Jan 2024 20:51:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 20 Jan 2024 20:51:34 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 20 Jan 2024 20:51:34 GMT
WORKDIR /usr/src/perl
# Sat, 20 Jan 2024 20:51:34 GMT
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/C/CO/CORION/perl-5.39.7.tar.gz -o perl-5.39.7.tar.gz     && echo 'c85f9ef13fa674839b076d81edb45242a5ddff3df4b111f764a7abe72edd83eb *perl-5.39.7.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.39.7.tar.gz -C /usr/src/perl     && rm perl-5.39.7.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997014/cpm -o /usr/local/bin/cpm     && echo 'ee525f2493e36c6f688eddabaf53a51c4d3b2a4ebaa81576ac8b9f78ab57f4a1 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Sat, 20 Jan 2024 20:51:34 GMT
WORKDIR /usr/src/app
# Sat, 20 Jan 2024 20:51:34 GMT
CMD ["perl5.39.7" "-de0"]
```

-	Layers:
	-	`sha256:3613d41e91f9f86b71a10338dcfe412e314cd29bee2d9674a0b53f59989b5a42`  
		Last Modified: Wed, 31 Jan 2024 22:48:22 GMT  
		Size: 52.6 MB (52560866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:067da67c4d09fae4c4194d0bf830bc5d88e93cc76d61c68ef8b5cc523864e61d`  
		Last Modified: Wed, 31 Jan 2024 23:23:50 GMT  
		Size: 15.4 MB (15376447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:839390782bb735a0c8ac19a96786946523371bf9a989770a9da6c86ca3583548`  
		Last Modified: Wed, 31 Jan 2024 23:24:12 GMT  
		Size: 52.3 MB (52333517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a64c9eccbd5ac6085a2760b6ef04a0140c0bf1633c08d30c4dacf7544003818`  
		Last Modified: Wed, 31 Jan 2024 23:24:46 GMT  
		Size: 175.1 MB (175124271 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58730cd61e689dcade08af20134a8f093b6f2d165f5097a933dfff9913d4e0cc`  
		Last Modified: Thu, 01 Feb 2024 12:25:10 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71bcf4b5ac9b02fa1b7874956e234d4c1bed0f6ccb85d86164b070541423380d`  
		Last Modified: Thu, 01 Feb 2024 15:12:17 GMT  
		Size: 15.2 MB (15162462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:242532c776b2b37eba7c327e47265d7c9140a7bda9ee6bdb9ae7c0646d003949`  
		Last Modified: Thu, 01 Feb 2024 15:12:16 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-threaded-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:becab1370b548d0b488f373d423f99325135e97a90f8c705f696ff96c9edb25b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.8 MB (12789641 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98bbd19248e9bf9211ddd95b3cf4fc954e7fb93363ea8a2b99b34e5600145ee3`

```dockerfile
```

-	Layers:
	-	`sha256:58a65c34cd663e8655138acc594e4ba7382d9bc9e2579c04c17b4c750a0d4235`  
		Last Modified: Thu, 01 Feb 2024 15:12:17 GMT  
		Size: 12.8 MB (12774369 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:58bf48ddd888c1bb2338a94c247a4f1a92dea7058d2123d97f94d5ab095271dc`  
		Last Modified: Thu, 01 Feb 2024 15:12:16 GMT  
		Size: 15.3 KB (15272 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-threaded-bullseye` - linux; arm variant v7

```console
$ docker pull perl@sha256:b23e9f043a2a3daa1a93d136faef021a79fa99ef0be67e17fd278bd02386bff8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.8 MB (297800486 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2da320aef2683d1e7325894722b916934e9416d5cfb3fe26998a0e1fa41be83a`
-	Default Command: `["perl5.39.7","-de0"]`

```dockerfile
# Sat, 20 Jan 2024 20:51:34 GMT
ADD file:7a3ca444fa582cdedade49cd6262ee982b6da86eafe22b1b77326c8eab3f88cf in / 
# Sat, 20 Jan 2024 20:51:34 GMT
CMD ["bash"]
# Sat, 20 Jan 2024 20:51:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 20 Jan 2024 20:51:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 20 Jan 2024 20:51:34 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 20 Jan 2024 20:51:34 GMT
WORKDIR /usr/src/perl
# Sat, 20 Jan 2024 20:51:34 GMT
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/C/CO/CORION/perl-5.39.7.tar.gz -o perl-5.39.7.tar.gz     && echo 'c85f9ef13fa674839b076d81edb45242a5ddff3df4b111f764a7abe72edd83eb *perl-5.39.7.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.39.7.tar.gz -C /usr/src/perl     && rm perl-5.39.7.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997014/cpm -o /usr/local/bin/cpm     && echo 'ee525f2493e36c6f688eddabaf53a51c4d3b2a4ebaa81576ac8b9f78ab57f4a1 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Sat, 20 Jan 2024 20:51:34 GMT
WORKDIR /usr/src/app
# Sat, 20 Jan 2024 20:51:34 GMT
CMD ["perl5.39.7" "-de0"]
```

-	Layers:
	-	`sha256:413453d204f637339c7a4727b614537000709bb2ff00a6307e262cf37237761c`  
		Last Modified: Wed, 31 Jan 2024 22:49:12 GMT  
		Size: 50.2 MB (50216178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b1bf41a938a7614b6b4a47164d8e064bbe0014418bfb366d6fac331d52eb271`  
		Last Modified: Thu, 01 Feb 2024 02:59:37 GMT  
		Size: 14.9 MB (14880646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e95de382e9abef96d20556d56d3fb966963ac36ee44cacf79096d796176232c7`  
		Last Modified: Thu, 01 Feb 2024 02:59:54 GMT  
		Size: 50.4 MB (50361245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90bfc3e692e8ff6873d25f44400c58bd3aa6d14344de87d8ad43f17573aaa0cf`  
		Last Modified: Thu, 01 Feb 2024 03:00:28 GMT  
		Size: 167.4 MB (167381508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f70ea16e0728209c7202fc226759a1b156e7316e9f4728e1ed0160cd57eeb619`  
		Last Modified: Thu, 01 Feb 2024 21:13:06 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5b9e253edce5d9920981b42d285ef2ac3ef3014688288342fae27f4edc41689`  
		Last Modified: Thu, 01 Feb 2024 23:39:10 GMT  
		Size: 15.0 MB (14960645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3339a788c272d03253d28719297eaa888d6a8eab1a6bbd57123fd8c32e2167e3`  
		Last Modified: Thu, 01 Feb 2024 23:39:08 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-threaded-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:b704a37434dce0aef0ed02de8f380e62fb1167e8c0cdde83bb001d1d598a3be3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.8 MB (12795015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4400e6df3a22751c09d7107c4fb748aa7db6f75bb6e083bfbfe34623db7b938f`

```dockerfile
```

-	Layers:
	-	`sha256:b5b137bf8562f0b4529dd9ebde6b07ac2bd75f9928e84a371599e821c2eb0a40`  
		Last Modified: Thu, 01 Feb 2024 23:39:09 GMT  
		Size: 12.8 MB (12779743 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0fd0c9840b62a57dddf9e0bc848746e0ace2bcaaf97bcf7939c0e30911ea557f`  
		Last Modified: Thu, 01 Feb 2024 23:39:08 GMT  
		Size: 15.3 KB (15272 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-threaded-bullseye` - linux; arm64 variant v8

```console
$ docker pull perl@sha256:f1f80374e1a269a2dc8e3227149b869df8fb92b8c5884ed260694c90ad482c01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **329.8 MB (329817169 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8957a31a8611b286fd30c34e47231c89a6e2b62bc26c925b78ad9e90c7cfacf`
-	Default Command: `["perl5.39.7","-de0"]`

```dockerfile
# Thu, 11 Jan 2024 02:40:51 GMT
ADD file:8fb65cadfd211811589ee046d0fbd69d1fe11461b0c0c154a7650bf97307b857 in / 
# Thu, 11 Jan 2024 02:40:51 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 09:26:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Jan 2024 02:25:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Jan 2024 02:25:58 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 20 Jan 2024 20:51:34 GMT
WORKDIR /usr/src/perl
# Sat, 20 Jan 2024 20:51:34 GMT
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/C/CO/CORION/perl-5.39.7.tar.gz -o perl-5.39.7.tar.gz     && echo 'c85f9ef13fa674839b076d81edb45242a5ddff3df4b111f764a7abe72edd83eb *perl-5.39.7.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.39.7.tar.gz -C /usr/src/perl     && rm perl-5.39.7.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997014/cpm -o /usr/local/bin/cpm     && echo 'ee525f2493e36c6f688eddabaf53a51c4d3b2a4ebaa81576ac8b9f78ab57f4a1 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Sat, 20 Jan 2024 20:51:34 GMT
WORKDIR /usr/src/app
# Sat, 20 Jan 2024 20:51:34 GMT
CMD ["perl5.39.7" "-de0"]
```

-	Layers:
	-	`sha256:cf83973c4a096cce9f37c421ad6f19cf1ebf7ae4d8ea98dac4913bd2aef08d1c`  
		Last Modified: Thu, 11 Jan 2024 02:44:25 GMT  
		Size: 53.7 MB (53707847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aebf2a961043d6b9dd703d0a485e216a2e302edf2e2525f7f410987d26905e71`  
		Last Modified: Thu, 11 Jan 2024 09:35:03 GMT  
		Size: 15.8 MB (15750711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:646806c0e22a1bfa60edc42bcc6170f0ccd02431e5871b9cec1962c34d610232`  
		Last Modified: Wed, 17 Jan 2024 02:59:33 GMT  
		Size: 54.7 MB (54699826 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cd94a910a6d687fc7621b3af4657f78c1208a07fa463f30e2ed002dadb7e021`  
		Last Modified: Wed, 17 Jan 2024 03:00:10 GMT  
		Size: 189.8 MB (189834377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a15170ebec76671bc76b4807a56bbb909e2b2128733f5922d8a7d27d0477d070`  
		Last Modified: Thu, 18 Jan 2024 03:50:34 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abb1c41934ad39aad0c7a67691ae3311f59919daab58af2494748b432c5ee946`  
		Last Modified: Mon, 22 Jan 2024 20:49:35 GMT  
		Size: 15.8 MB (15824140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a0f961e5bf07f8ca3eec168b528489b5d6a62e73bb74a4ec17517dca41236aa`  
		Last Modified: Mon, 22 Jan 2024 20:49:33 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-threaded-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:9878ef6d2e62178c0c39019c1a709c0738356c3a5015b8d07efa7283debc8482
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.0 MB (12969680 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57bd4feaccd3645b693a9b811bdc80f86283ca31310f7573e00f30b85af2a352`

```dockerfile
```

-	Layers:
	-	`sha256:17f3704cf588b053c689dca20425651e3ad344988000d23a9e731088e6da6fef`  
		Last Modified: Mon, 22 Jan 2024 20:49:34 GMT  
		Size: 13.0 MB (12954462 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3fc7eae61646f5ad413a436d2d3c2ee2a6f82cbb569fb9f8e8a2547c73444bf4`  
		Last Modified: Mon, 22 Jan 2024 20:49:33 GMT  
		Size: 15.2 KB (15218 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-threaded-bullseye` - linux; 386

```console
$ docker pull perl@sha256:e8ce23c1768218ce3f4b51560a314e12315e5e5ad2119e99e115deb514cdd832
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **343.5 MB (343530462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a08a7274d59691b845addf8a25d7aa02a37f1968908dfd33b71dcefdffb8a9b4`
-	Default Command: `["perl5.39.7","-de0"]`

```dockerfile
# Sat, 20 Jan 2024 20:51:34 GMT
ADD file:52ba8552e4cd0d950c9eb8ab6bf54413f34e4ef697dc4ae766a04f22b7ea1a38 in / 
# Sat, 20 Jan 2024 20:51:34 GMT
CMD ["bash"]
# Sat, 20 Jan 2024 20:51:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 20 Jan 2024 20:51:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 20 Jan 2024 20:51:34 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 20 Jan 2024 20:51:34 GMT
WORKDIR /usr/src/perl
# Sat, 20 Jan 2024 20:51:34 GMT
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/C/CO/CORION/perl-5.39.7.tar.gz -o perl-5.39.7.tar.gz     && echo 'c85f9ef13fa674839b076d81edb45242a5ddff3df4b111f764a7abe72edd83eb *perl-5.39.7.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.39.7.tar.gz -C /usr/src/perl     && rm perl-5.39.7.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997014/cpm -o /usr/local/bin/cpm     && echo 'ee525f2493e36c6f688eddabaf53a51c4d3b2a4ebaa81576ac8b9f78ab57f4a1 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Sat, 20 Jan 2024 20:51:34 GMT
WORKDIR /usr/src/app
# Sat, 20 Jan 2024 20:51:34 GMT
CMD ["perl5.39.7" "-de0"]
```

-	Layers:
	-	`sha256:3f04d4a4d4fa39eba128eb2d49424bb31d43a6258c318d2547e85c723fd692f7`  
		Last Modified: Wed, 31 Jan 2024 22:44:11 GMT  
		Size: 56.0 MB (56046343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f99b6c7685036bde084776c74f9136023dec781b8147da8aeefb0986d4f1c1cf`  
		Last Modified: Wed, 31 Jan 2024 23:46:17 GMT  
		Size: 16.3 MB (16269365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52e6e11307bb0bd3d381c7c9caf2866148b59acb310fab1329102bed20a4e04e`  
		Last Modified: Wed, 31 Jan 2024 23:46:37 GMT  
		Size: 55.9 MB (55939864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b16eaec20d2529e6d6598173a9d9d703f940af73aa52ac269cec733301bc178`  
		Last Modified: Wed, 31 Jan 2024 23:47:23 GMT  
		Size: 199.8 MB (199825679 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab666590d4fb03b2dc91c37d495f1a94e60b254a22773bbf7e97deec20d67c43`  
		Last Modified: Thu, 01 Feb 2024 01:07:08 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b282f59c632b5628505d74e59563ff194c685136a891e918b54e0d1fe4f1ab1f`  
		Last Modified: Thu, 01 Feb 2024 01:07:29 GMT  
		Size: 15.4 MB (15448945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3586c2cc69790d47db08b406c3628de7d88ed2dc7f7daab2bb7e9a11eec9c390`  
		Last Modified: Thu, 01 Feb 2024 01:07:28 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-threaded-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:ca3810ed30cd5030c7dd9c2383a822caed49db433d3ef84790f14bde1654f703
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.0 MB (12956895 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2f947cffc40005e399b525f42246fab0a7bd964da8f2df40d8141dc29e617f6`

```dockerfile
```

-	Layers:
	-	`sha256:14fb14f53056f10048259b9bee2dfef6e8f86f2f61c8a639fb1bea9451b97745`  
		Last Modified: Thu, 01 Feb 2024 01:07:29 GMT  
		Size: 12.9 MB (12941046 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9ee32ba0e53e42dc8b360554ea6f47e2c3f2478bb04e2ee7ab6dc5ffd056f616`  
		Last Modified: Thu, 01 Feb 2024 01:07:28 GMT  
		Size: 15.8 KB (15849 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-threaded-bullseye` - linux; mips64le

```console
$ docker pull perl@sha256:ee5b95cf2012725bfa2559a39d816f6f1ea9e7edf2f4da11daced716b41a3033
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **316.3 MB (316278627 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e11103777a445cf9e3516bae0a394590c3b39a875dcbea92b01ddaa279ba801f`
-	Default Command: `["perl5.39.7","-de0"]`

```dockerfile
# Sat, 20 Jan 2024 20:51:34 GMT
ADD file:646762dde2578506254f2b52895972c76193565971632fabb304bfd0d84e4301 in / 
# Sat, 20 Jan 2024 20:51:34 GMT
CMD ["bash"]
# Sat, 20 Jan 2024 20:51:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 20 Jan 2024 20:51:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 20 Jan 2024 20:51:34 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 20 Jan 2024 20:51:34 GMT
WORKDIR /usr/src/perl
# Sat, 20 Jan 2024 20:51:34 GMT
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/C/CO/CORION/perl-5.39.7.tar.gz -o perl-5.39.7.tar.gz     && echo 'c85f9ef13fa674839b076d81edb45242a5ddff3df4b111f764a7abe72edd83eb *perl-5.39.7.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.39.7.tar.gz -C /usr/src/perl     && rm perl-5.39.7.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997014/cpm -o /usr/local/bin/cpm     && echo 'ee525f2493e36c6f688eddabaf53a51c4d3b2a4ebaa81576ac8b9f78ab57f4a1 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Sat, 20 Jan 2024 20:51:34 GMT
WORKDIR /usr/src/app
# Sat, 20 Jan 2024 20:51:34 GMT
CMD ["perl5.39.7" "-de0"]
```

-	Layers:
	-	`sha256:c1282b8885af09f8f21ef0080afd2b77263b28d997ded5c3e116452fb071674d`  
		Last Modified: Wed, 31 Jan 2024 22:39:06 GMT  
		Size: 53.3 MB (53289105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:540709fc3a1629228a5870109f777c55eca65db59573494afa87e285f8cd276a`  
		Last Modified: Thu, 01 Feb 2024 07:48:49 GMT  
		Size: 15.5 MB (15530667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a4d84da99a70f6525286e6829101a8ec425b5bf8fa809b85cfa4e246e0467d2`  
		Last Modified: Thu, 01 Feb 2024 07:49:34 GMT  
		Size: 53.3 MB (53312108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47251fd4f095a1e69c5e1a5af220fd6f5b6f01fbe471939335aa5d4c348cb1de`  
		Last Modified: Thu, 01 Feb 2024 07:51:31 GMT  
		Size: 179.0 MB (179021258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:191476cb3840ad2106a2962427b13f02f00b01828a3c099c1134dca084605f79`  
		Last Modified: Thu, 01 Feb 2024 21:54:06 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6df40d9d7e38b5961e050867368ad64e87b6262eae03353285e7171f466fdc22`  
		Last Modified: Fri, 02 Feb 2024 09:46:25 GMT  
		Size: 15.1 MB (15125225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3338ca9d1f933fcb609c26660b7e8f510b8825fe7d9ba30bba6335fbd21c6bc3`  
		Last Modified: Fri, 02 Feb 2024 09:46:23 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-threaded-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:c20b41e896552336d5fe210132197a7127873977293bf98220e1479ab56f8eda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.0 KB (15043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ca27711b6c77563d2ce799d227c69f265e3d03e2f39748bee563e6a2debbf01`

```dockerfile
```

-	Layers:
	-	`sha256:0a1bc9a5ded41b7e29e02634bd654aed6cd6d31688649857dfb010fdfa71885f`  
		Last Modified: Fri, 02 Feb 2024 09:46:23 GMT  
		Size: 15.0 KB (15043 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-threaded-bullseye` - linux; ppc64le

```console
$ docker pull perl@sha256:5067a37465668ea2250614606ed5bf4aba0b02099c98712b759e95c4f3ce07fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **346.8 MB (346782244 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ebc70a1c977205b21c0d355e60f93a0fe8bd76a1a47ed5ec044d01bbb0a287e`
-	Default Command: `["perl5.39.7","-de0"]`

```dockerfile
# Sat, 20 Jan 2024 20:51:34 GMT
ADD file:feff7236892a5ed9be64b73bb7748b1b8017599aad443cae41dfdc07dce2bb8e in / 
# Sat, 20 Jan 2024 20:51:34 GMT
CMD ["bash"]
# Sat, 20 Jan 2024 20:51:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 20 Jan 2024 20:51:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 20 Jan 2024 20:51:34 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 20 Jan 2024 20:51:34 GMT
WORKDIR /usr/src/perl
# Sat, 20 Jan 2024 20:51:34 GMT
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/C/CO/CORION/perl-5.39.7.tar.gz -o perl-5.39.7.tar.gz     && echo 'c85f9ef13fa674839b076d81edb45242a5ddff3df4b111f764a7abe72edd83eb *perl-5.39.7.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.39.7.tar.gz -C /usr/src/perl     && rm perl-5.39.7.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997014/cpm -o /usr/local/bin/cpm     && echo 'ee525f2493e36c6f688eddabaf53a51c4d3b2a4ebaa81576ac8b9f78ab57f4a1 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Sat, 20 Jan 2024 20:51:34 GMT
WORKDIR /usr/src/app
# Sat, 20 Jan 2024 20:51:34 GMT
CMD ["perl5.39.7" "-de0"]
```

-	Layers:
	-	`sha256:59e847189f64174916c93398cc517f0b07c2a03b89a56fc88a1216415420047a`  
		Last Modified: Wed, 31 Jan 2024 22:34:47 GMT  
		Size: 58.9 MB (58930288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e97e560f4ccece1914eb3223f7f1dd7f1efb3f797d1cf2f2931b1423428b5668`  
		Last Modified: Wed, 31 Jan 2024 23:48:56 GMT  
		Size: 16.8 MB (16767360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8718270d2cbe623b0cb0056d5d433cf38e8ec5f126002f62f67693ef5edb7456`  
		Last Modified: Wed, 31 Jan 2024 23:49:15 GMT  
		Size: 58.9 MB (58874241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8c8fee1359a50ceab803cfc7fbcbdb50e8cb467db6a3203354529949ebe118e`  
		Last Modified: Wed, 31 Jan 2024 23:49:53 GMT  
		Size: 196.3 MB (196277517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65e147c0a55d5f45f93fd3ec6b3f57cf0c46ed09f606861fafd6ca5dd014dc7f`  
		Last Modified: Fri, 02 Feb 2024 09:38:13 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2245631d8abeb2395749c5794333330eb285b0f45935670eb769ec6529ee6391`  
		Last Modified: Fri, 02 Feb 2024 11:32:10 GMT  
		Size: 15.9 MB (15932570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e65f0979a929380f17e013543aa4eecaaf7f8646c36ae73ab6e6c011e4d1e3e6`  
		Last Modified: Fri, 02 Feb 2024 11:32:09 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-threaded-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:c8739edc47c50196ea89516d00eb15eb8497355d5293e6f3cce2166828293ba7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.9 MB (12942687 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aea76886e7b5f63ea2d7468ec13d43dc1f9e79d66febde1d115a905aa46f99c9`

```dockerfile
```

-	Layers:
	-	`sha256:c87a022a79d96a2c654eff30946f276651c131ec869f052da9ae41cba4f716c6`  
		Last Modified: Fri, 02 Feb 2024 11:32:09 GMT  
		Size: 12.9 MB (12927445 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:01b743e8ef1fc1afb13670350409e4f00a6e19cabb2dae9432dbd7e34d233274`  
		Last Modified: Fri, 02 Feb 2024 11:32:09 GMT  
		Size: 15.2 KB (15242 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-threaded-bullseye` - linux; s390x

```console
$ docker pull perl@sha256:3dc12bd7fd292e560a21cad6715bc47e5835ab12b34d38f83589ef0591035e95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **312.2 MB (312182998 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f11223d78f788f5e002cd383631a3ad5531848c2fa2e0af4557ad88e2a0497e`
-	Default Command: `["perl5.39.7","-de0"]`

```dockerfile
# Thu, 11 Jan 2024 01:45:23 GMT
ADD file:9ddcb5238e539e3b1fd8032aecf5e40f0b8b8162e6d045fcd58520db01e93296 in / 
# Thu, 11 Jan 2024 01:45:28 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 02:11:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Jan 2024 03:17:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Jan 2024 03:19:18 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 20 Jan 2024 20:51:34 GMT
WORKDIR /usr/src/perl
# Sat, 20 Jan 2024 20:51:34 GMT
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/C/CO/CORION/perl-5.39.7.tar.gz -o perl-5.39.7.tar.gz     && echo 'c85f9ef13fa674839b076d81edb45242a5ddff3df4b111f764a7abe72edd83eb *perl-5.39.7.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.39.7.tar.gz -C /usr/src/perl     && rm perl-5.39.7.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997014/cpm -o /usr/local/bin/cpm     && echo 'ee525f2493e36c6f688eddabaf53a51c4d3b2a4ebaa81576ac8b9f78ab57f4a1 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Sat, 20 Jan 2024 20:51:34 GMT
WORKDIR /usr/src/app
# Sat, 20 Jan 2024 20:51:34 GMT
CMD ["perl5.39.7" "-de0"]
```

-	Layers:
	-	`sha256:a1442bb0c8abfd050e8bdb2270126c2f24402a8c57a00f8229c40c2a35253665`  
		Last Modified: Thu, 11 Jan 2024 01:51:04 GMT  
		Size: 53.3 MB (53296125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1d30f97393df8af87413ca6aa015986e13ab489522ffe9a065961b2ed0f9352`  
		Last Modified: Thu, 11 Jan 2024 02:22:01 GMT  
		Size: 15.6 MB (15642723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59822891147cf801aabc1a3824089c8385793e177e1610b0c14dfb8ccafc4934`  
		Last Modified: Wed, 17 Jan 2024 04:04:21 GMT  
		Size: 54.1 MB (54070709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:515d393636eb45ce9c7153873b9a523d1c13aae090017d8089b56b8da8e16645`  
		Last Modified: Wed, 17 Jan 2024 04:04:47 GMT  
		Size: 172.9 MB (172919632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7f890a350a21f7b7870049e0941cf2c5a0f5510c0b17c4b48ef60ad67c7cbcf`  
		Last Modified: Thu, 18 Jan 2024 21:08:30 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2474207742bb64d306158401b31cd4b2f88534d28615363e32b589dba245c681`  
		Last Modified: Mon, 22 Jan 2024 22:47:24 GMT  
		Size: 16.3 MB (16253542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:768c4fe012b9d1c4eefdf61ce1384cc33f114caaef640a54307b0e332261e926`  
		Last Modified: Mon, 22 Jan 2024 22:47:23 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-threaded-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:9e48e36bc07c12408d7396590e3ed97f321697484b6df22adcf04860e0482aea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.8 MB (12810932 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:157e9c47d378d23ee2f9516e84e2158a2106779262d5f87b2485cd0e2888b0d1`

```dockerfile
```

-	Layers:
	-	`sha256:01fe5457387631336d4c6f4a22e767f4d3148ae26c42c84b02d5f412dcd4d74b`  
		Last Modified: Mon, 22 Jan 2024 22:47:23 GMT  
		Size: 12.8 MB (12795722 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:19be10964ce7a93649d2299a2002797a5f8d87d45e5f74e7486981388b3bdd6b`  
		Last Modified: Mon, 22 Jan 2024 22:47:23 GMT  
		Size: 15.2 KB (15210 bytes)  
		MIME: application/vnd.in-toto+json
