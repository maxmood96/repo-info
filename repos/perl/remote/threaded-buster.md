## `perl:threaded-buster`

```console
$ docker pull perl@sha256:285dc7bc8c36b7b9bc2b67e26e8002fb9e1d3a66ac721d9e9ae65d4798de3944
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

### `perl:threaded-buster` - linux; amd64

```console
$ docker pull perl@sha256:4b21a72230362cfb1fb8f0e169f8c2ea3d76473ee9b699ce236aa6e8d7262e50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **327.6 MB (327621887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dad783283d18f5f3262d53936c911843cf697b708b66e69ecc8f70a6b1243eae`
-	Default Command: `["perl5.38.2","-de0"]`

```dockerfile
# Sat, 20 Jan 2024 20:51:34 GMT
ADD file:dccb5d0cbcf502fb7c4135575f44ac26d665fc92f50546f3a7f9e4d433726453 in / 
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
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/P/PE/PEVANS/perl-5.38.2.tar.gz -o perl-5.38.2.tar.gz     && echo 'a0a31534451eb7b83c7d6594a497543a54d488bc90ca00f5e34762577f40655e *perl-5.38.2.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.38.2.tar.gz -C /usr/src/perl     && rm perl-5.38.2.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997014/cpm -o /usr/local/bin/cpm     && echo 'ee525f2493e36c6f688eddabaf53a51c4d3b2a4ebaa81576ac8b9f78ab57f4a1 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Sat, 20 Jan 2024 20:51:34 GMT
WORKDIR /usr/src/app
# Sat, 20 Jan 2024 20:51:34 GMT
CMD ["perl5.38.2" "-de0"]
```

-	Layers:
	-	`sha256:544676cb5e57a1ca47f178393253edded2bd54fba92674c7384013b4ddc87226`  
		Last Modified: Tue, 13 Feb 2024 00:43:09 GMT  
		Size: 50.5 MB (50500120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:783b6a2cbfde6d2dad8afded854e09b5b1ebda2fb638638c0f16b27d412ef7e3`  
		Last Modified: Tue, 13 Feb 2024 01:32:48 GMT  
		Size: 17.6 MB (17584782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c92b93a33a64c463f31b9f608a72574ce897c145372a32153f25a2df03b3eed`  
		Last Modified: Tue, 13 Feb 2024 01:33:03 GMT  
		Size: 51.9 MB (51876546 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5506dab13b722a0a2167c56d87ab89be676de83954672d39ea7d159e992a169`  
		Last Modified: Tue, 13 Feb 2024 01:33:34 GMT  
		Size: 191.9 MB (191934438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0fe6632cf596d027fc00ca935611170c30da03e58c1c5d753de78405921fba7`  
		Last Modified: Tue, 13 Feb 2024 03:05:50 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e33629435eb1293bec0a65d6f3861b5dffbdbb91b86b8b16fd67daa6c2dec147`  
		Last Modified: Tue, 13 Feb 2024 03:05:51 GMT  
		Size: 15.7 MB (15725735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a25e47df5cead9165ac33cbe0a66e5962d0e510e8f9636a692a93506d891417`  
		Last Modified: Tue, 13 Feb 2024 03:05:50 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:threaded-buster` - unknown; unknown

```console
$ docker pull perl@sha256:17d6cc2fefb6b6a361d193a592c01ac24a08b6d0fdf68422fa0ef9fcd088bc61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.6 MB (13623182 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86b225d47252ccb74a51e774dacbce3f4247ed2bf06b4e2083b34c4a7583d223`

```dockerfile
```

-	Layers:
	-	`sha256:7a56ad3366e201b4b22444abc97ffd601c75bde3dfb076e7e0ec96ff3fb7cf6b`  
		Last Modified: Tue, 13 Feb 2024 03:05:51 GMT  
		Size: 13.6 MB (13606778 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e5f14a08cf9bf1c3a9b9e6c086c41f13a73ebfdf7b196af08f7f486f57e33583`  
		Last Modified: Tue, 13 Feb 2024 03:05:50 GMT  
		Size: 16.4 KB (16404 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:threaded-buster` - linux; arm variant v7

```console
$ docker pull perl@sha256:e3e3a8de4a528ca452cf7d82997488274ae24a8049d6554f0e4a95d66279064b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.5 MB (292529737 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acb085437ab1d22e775f91463b2ab53a0b321fbaca124afe783d03a982f03ba1`
-	Default Command: `["perl5.38.2","-de0"]`

```dockerfile
# Sat, 20 Jan 2024 20:51:34 GMT
ADD file:f7d675054a4ba85691acd979742ab5f8839e1e198ce8bb7830a06479744db901 in / 
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
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/P/PE/PEVANS/perl-5.38.2.tar.gz -o perl-5.38.2.tar.gz     && echo 'a0a31534451eb7b83c7d6594a497543a54d488bc90ca00f5e34762577f40655e *perl-5.38.2.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.38.2.tar.gz -C /usr/src/perl     && rm perl-5.38.2.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997014/cpm -o /usr/local/bin/cpm     && echo 'ee525f2493e36c6f688eddabaf53a51c4d3b2a4ebaa81576ac8b9f78ab57f4a1 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Sat, 20 Jan 2024 20:51:34 GMT
WORKDIR /usr/src/app
# Sat, 20 Jan 2024 20:51:34 GMT
CMD ["perl5.38.2" "-de0"]
```

-	Layers:
	-	`sha256:d262abdf15e38f7960a48edbd9d8d9de475362307d40e6620e518de8d55b49d6`  
		Last Modified: Wed, 31 Jan 2024 22:49:56 GMT  
		Size: 46.0 MB (45966700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:177171da7d7b3ba27fb8c6a7fcdd2e5b11529c6dacfb38235704dfd2110abc06`  
		Last Modified: Thu, 01 Feb 2024 03:00:39 GMT  
		Size: 16.2 MB (16216433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58a579a1401e8d8e2a5b42e0da1f30d53451c3736d9a0f2bded6153cd62587c1`  
		Last Modified: Thu, 01 Feb 2024 03:00:57 GMT  
		Size: 47.4 MB (47410558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:080b7ee9d0c5269d27372fc7c4591d9dc02f7eb8a92f2d856e16b40b8b59f6fa`  
		Last Modified: Thu, 01 Feb 2024 03:01:32 GMT  
		Size: 168.1 MB (168133549 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c4b8920713dad9ee38a1024a5e09a7d975e1544cb22e1164824648324b66a99`  
		Last Modified: Thu, 01 Feb 2024 21:19:34 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16de1094d0acda6d39a122cc60b469985275df290336de8de80951cbae133254`  
		Last Modified: Sat, 03 Feb 2024 16:23:47 GMT  
		Size: 14.8 MB (14802232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8e09b095e99b2d29426c1a2e2619d6e2ad7114f9f6882565b87fb3f12c3773c`  
		Last Modified: Sat, 03 Feb 2024 16:23:46 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:threaded-buster` - unknown; unknown

```console
$ docker pull perl@sha256:83b6e628972886562a78c52966b5600fea1f025b64c6fe683bf6568bb7e62151
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.5 MB (13450196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d9f1cdb3d87b7c8afc88194dc49e3d8e558cfba392f171ca673b9265b161ee0`

```dockerfile
```

-	Layers:
	-	`sha256:e30d2c355de49861083853731531e27e1630e7f4a1b2b0e8fa278d99dab3e5a8`  
		Last Modified: Sat, 03 Feb 2024 16:23:47 GMT  
		Size: 13.4 MB (13434376 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2d41d70b557e494bb68109da2b9bce128fdf86be6853c6faac9f2bb8fc8385af`  
		Last Modified: Sat, 03 Feb 2024 16:23:46 GMT  
		Size: 15.8 KB (15820 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:threaded-buster` - linux; arm64 variant v8

```console
$ docker pull perl@sha256:8789a414557fc7898a7db4a10550d197af7a8122452c7e6133f00d3e9579bb44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **318.1 MB (318104563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36fdb2ef4093a2e981b0a0f4710452ea412920ec33fc06eb822abc8f014135f8`
-	Default Command: `["perl5.38.2","-de0"]`

```dockerfile
# Sat, 20 Jan 2024 20:51:34 GMT
ADD file:e90b5b9867a710355f422f29d2d58bb702061d4c0d836638a8d2f114407bb59e in / 
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
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/P/PE/PEVANS/perl-5.38.2.tar.gz -o perl-5.38.2.tar.gz     && echo 'a0a31534451eb7b83c7d6594a497543a54d488bc90ca00f5e34762577f40655e *perl-5.38.2.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.38.2.tar.gz -C /usr/src/perl     && rm perl-5.38.2.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997014/cpm -o /usr/local/bin/cpm     && echo 'ee525f2493e36c6f688eddabaf53a51c4d3b2a4ebaa81576ac8b9f78ab57f4a1 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Sat, 20 Jan 2024 20:51:34 GMT
WORKDIR /usr/src/app
# Sat, 20 Jan 2024 20:51:34 GMT
CMD ["perl5.38.2" "-de0"]
```

-	Layers:
	-	`sha256:e1e8121491ed748e37039005619f6a859db4d023c520df7ccac5040bc9ebd266`  
		Last Modified: Wed, 31 Jan 2024 22:49:10 GMT  
		Size: 49.3 MB (49289527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b7fca6cf938062381d3b66b1cde045b81e5061e842ebab5872ecad908abe26d`  
		Last Modified: Wed, 31 Jan 2024 23:53:57 GMT  
		Size: 17.5 MB (17455590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:516414d0ceb2f3d11662b32d4dca67121887880d8412cd692429221ab8231dc9`  
		Last Modified: Wed, 31 Jan 2024 23:54:13 GMT  
		Size: 52.2 MB (52220919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:444d708702c0668e681a5831db2080a8fd839aac855f9d3e3f43562582b0a135`  
		Last Modified: Wed, 31 Jan 2024 23:54:38 GMT  
		Size: 183.5 MB (183499590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:187e18fdfce95d7aee224795538cbae07a7763a5b2efc3a1428e5c7584fbc2df`  
		Last Modified: Fri, 02 Feb 2024 14:31:48 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c61f7766bc118edb48fd22e9c8d1494bcf3794b193f3bc7b6bbbc99ef3ffd3d`  
		Last Modified: Fri, 02 Feb 2024 14:59:52 GMT  
		Size: 15.6 MB (15638671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d4e2bf103cb36e460e34b77f0f68bcc4b65f6af6e3eccef4148966cdb031f7d`  
		Last Modified: Fri, 02 Feb 2024 14:59:51 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:threaded-buster` - unknown; unknown

```console
$ docker pull perl@sha256:399f2ac2a03702839fe43713e8f042c368fa4ef4e59d3385b4422474af70a567
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.6 MB (13614557 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12a76518378d7febf969f76bc206ef1896c1637dce0afa2bbf0f0d87269fdebf`

```dockerfile
```

-	Layers:
	-	`sha256:1525bab7e52cf2ed34372bc88e66e521dadf4d3e45539ff8a154dd28ebb89906`  
		Last Modified: Fri, 02 Feb 2024 14:59:52 GMT  
		Size: 13.6 MB (13598803 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d6f88f047684a7ac01cda802708bc88045309f413eed46f7a063d688585aa0f9`  
		Last Modified: Fri, 02 Feb 2024 14:59:51 GMT  
		Size: 15.8 KB (15754 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:threaded-buster` - linux; 386

```console
$ docker pull perl@sha256:3d7490457fbbcb4980267c8447b0fe067555154530e6bb730184f64014a2d07b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **336.6 MB (336588510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7173f5bd434f30de5b112e78b9bbcc75330cf6cdbe2aeeefd3dfbb45c0cc1431`
-	Default Command: `["perl5.38.2","-de0"]`

```dockerfile
# Sat, 20 Jan 2024 20:51:34 GMT
ADD file:f1db0427c60f5ce5c0fdf61794e7b45091e044f4032ea88ebf7c03ae7a7e4de6 in / 
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
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/P/PE/PEVANS/perl-5.38.2.tar.gz -o perl-5.38.2.tar.gz     && echo 'a0a31534451eb7b83c7d6594a497543a54d488bc90ca00f5e34762577f40655e *perl-5.38.2.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.38.2.tar.gz -C /usr/src/perl     && rm perl-5.38.2.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997014/cpm -o /usr/local/bin/cpm     && echo 'ee525f2493e36c6f688eddabaf53a51c4d3b2a4ebaa81576ac8b9f78ab57f4a1 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Sat, 20 Jan 2024 20:51:34 GMT
WORKDIR /usr/src/app
# Sat, 20 Jan 2024 20:51:34 GMT
CMD ["perl5.38.2" "-de0"]
```

-	Layers:
	-	`sha256:ba068490695163c38116b67ad60e1418ab3585ae8f45a5e4a0d07cbad5406814`  
		Last Modified: Wed, 31 Jan 2024 22:44:59 GMT  
		Size: 51.3 MB (51255213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e81326b8c35782866483ce42b5ecff2eb37cca5b520a6bd7cd1badbd92a48fd9`  
		Last Modified: Wed, 31 Jan 2024 23:47:35 GMT  
		Size: 18.1 MB (18099443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99a451225425a788a1d90696a4da55a7cdfdeea108bbe137d9440aa1b08d6b3a`  
		Last Modified: Wed, 31 Jan 2024 23:47:57 GMT  
		Size: 53.5 MB (53490202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9085c739803b4fdaa9dbd79869da8fb43e2788872b548c5aea23661a2d89192`  
		Last Modified: Wed, 31 Jan 2024 23:48:45 GMT  
		Size: 198.5 MB (198469645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34227f3707963d7842d033447331a87dd90fa1560245a0257d5d4c1222bf1258`  
		Last Modified: Thu, 01 Feb 2024 01:07:08 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:336a2828396c5d5bb7f1f90289dad89e2795535430cb5b3aa05ae732255f34dc`  
		Last Modified: Thu, 01 Feb 2024 01:07:09 GMT  
		Size: 15.3 MB (15273742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c41c5e019123c1291369ae4cf54a3d96b016f102b33e760d8573bd7afc646f4`  
		Last Modified: Thu, 01 Feb 2024 01:07:08 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:threaded-buster` - unknown; unknown

```console
$ docker pull perl@sha256:8866e7a7652675ca2f71affe9de186b53067daeb39d914d267fe6d1a633b6eed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.6 MB (13626611 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2731130a219437be2f90b54885ba185ba8bf8d89392b874635aa5ee63185cd08`

```dockerfile
```

-	Layers:
	-	`sha256:72e5559a1ef0a7025d9ab41b508a05240d8f66b1a2772bef9d129b45300b2bcb`  
		Last Modified: Thu, 01 Feb 2024 01:07:09 GMT  
		Size: 13.6 MB (13610240 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:21e0fedcad012b1475c838adaecb51645877abe6cbc3f588ab3ecc3516c30ed0`  
		Last Modified: Thu, 01 Feb 2024 01:07:08 GMT  
		Size: 16.4 KB (16371 bytes)  
		MIME: application/vnd.in-toto+json
