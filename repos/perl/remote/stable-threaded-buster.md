## `perl:stable-threaded-buster`

```console
$ docker pull perl@sha256:c4b91ea13bb5e424faff296f47c19646c7551f48d4b9ecb1d8a47baf1c221174
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

### `perl:stable-threaded-buster` - linux; amd64

```console
$ docker pull perl@sha256:c4009e0139bd47152498952ff492a6588895c9224c5cc5603672921fefeec4d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **327.7 MB (327656827 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eeaabb9dd2534d7eda790344abbc79f87d0b87abe91d4fe1cc7888cc31145bfa`
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
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/P/PE/PEVANS/perl-5.38.2.tar.gz -o perl-5.38.2.tar.gz     && echo 'a0a31534451eb7b83c7d6594a497543a54d488bc90ca00f5e34762577f40655e *perl-5.38.2.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.38.2.tar.gz -C /usr/src/perl     && rm perl-5.38.2.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997014/cpm -o /usr/local/bin/cpm     && echo 'ee525f2493e36c6f688eddabaf53a51c4d3b2a4ebaa81576ac8b9f78ab57f4a1 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
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
	-	`sha256:03ec26d91783451539c5182e0601281b30af464eee6bb78019724fed1d7da0b0`  
		Last Modified: Wed, 10 Apr 2024 07:01:47 GMT  
		Size: 15.7 MB (15727389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68c4d0fb3e38c7f030ffe272488876efdbe7fb02764906041069361f914eb855`  
		Last Modified: Wed, 10 Apr 2024 07:01:46 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:stable-threaded-buster` - unknown; unknown

```console
$ docker pull perl@sha256:69e14cf4595d22de8fb423f2f7f68d7c0de28b0dd9087d5387657abf8f421a44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.6 MB (15626154 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:291a8e583aa92455e86bca5fca531a977646c0a39a96a727a67603b7cabced5a`

```dockerfile
```

-	Layers:
	-	`sha256:8511626161799fa7edb304f1c8f4256942be97f1ae996e8cdacd5dedf3d0a30f`  
		Last Modified: Wed, 10 Apr 2024 07:01:46 GMT  
		Size: 15.6 MB (15609750 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aa4b7497dbac338c1bcb7e2ed08d129648bbb90eec3d83224aec175fc896123f`  
		Last Modified: Wed, 10 Apr 2024 07:01:46 GMT  
		Size: 16.4 KB (16404 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:stable-threaded-buster` - linux; arm variant v7

```console
$ docker pull perl@sha256:a9bf19b4b73f457a93335957b5b7acbe54f16fbdfd266701dd1d7fe7e1d6e1df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.5 MB (292530800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68ba3fbd0dee5447998ff662b86b7a17921e69cb7badbb3e36967656c69362a6`
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
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/P/PE/PEVANS/perl-5.38.2.tar.gz -o perl-5.38.2.tar.gz     && echo 'a0a31534451eb7b83c7d6594a497543a54d488bc90ca00f5e34762577f40655e *perl-5.38.2.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.38.2.tar.gz -C /usr/src/perl     && rm perl-5.38.2.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997014/cpm -o /usr/local/bin/cpm     && echo 'ee525f2493e36c6f688eddabaf53a51c4d3b2a4ebaa81576ac8b9f78ab57f4a1 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
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
	-	`sha256:ca44fa345615936503c437bfad8818fb0b3b70d7a4068093f596f22d0d7d7a9f`  
		Last Modified: Wed, 13 Mar 2024 02:02:42 GMT  
		Size: 14.8 MB (14802086 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:118abb9ca5dcbe6bd8fd1894fc3df4763adf3abe7ed83a14992ae28f7dca272e`  
		Last Modified: Wed, 13 Mar 2024 02:02:41 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:stable-threaded-buster` - unknown; unknown

```console
$ docker pull perl@sha256:fd970e61673231e5584753f145efc5c4e505bc89fb949f5e11dc93e316077071
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 MB (15427536 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14278616e5d8c82cabcac86d76786c0679d2fb51b677ce4a468b3fd9c9e88c25`

```dockerfile
```

-	Layers:
	-	`sha256:a551096db10da84c0a3a0c6ae7d74c2139a5c717bf4a616c2445790408d8fc01`  
		Last Modified: Wed, 13 Mar 2024 02:02:41 GMT  
		Size: 15.4 MB (15411716 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eb99ec8009b73545570e988c9e7c6a61da919e626025165d8e945ec16bdd531e`  
		Last Modified: Wed, 13 Mar 2024 02:02:41 GMT  
		Size: 15.8 KB (15820 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:stable-threaded-buster` - linux; arm64 variant v8

```console
$ docker pull perl@sha256:d1d6db134ecf06f91be6c9ea4c4fc52b6a21ec5c118599f02557e8c60e4b4dbb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **318.1 MB (318127156 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ca380ef4a7c35d6fd6ff00dc2fbc8ba2f7c61c695efd9ab9e92a13a7aaf22cd`
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
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/P/PE/PEVANS/perl-5.38.2.tar.gz -o perl-5.38.2.tar.gz     && echo 'a0a31534451eb7b83c7d6594a497543a54d488bc90ca00f5e34762577f40655e *perl-5.38.2.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.38.2.tar.gz -C /usr/src/perl     && rm perl-5.38.2.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997014/cpm -o /usr/local/bin/cpm     && echo 'ee525f2493e36c6f688eddabaf53a51c4d3b2a4ebaa81576ac8b9f78ab57f4a1 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
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
	-	`sha256:893c5cabb20b5f1cef22fae17511031803ae83aa17bfbbad8856daf662e0f129`  
		Last Modified: Tue, 12 Mar 2024 23:46:04 GMT  
		Size: 15.6 MB (15638755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bf67b40e5e9f2f3ea98623b2215f9e331ecfaa85932b576a5425806829d81e3`  
		Last Modified: Tue, 12 Mar 2024 23:46:03 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:stable-threaded-buster` - unknown; unknown

```console
$ docker pull perl@sha256:7efbed1a00c38fe510e33141f37eb876b48299e25bf8a021e10d0454780bb547
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.6 MB (15616171 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d975b57765683320fa71e72ff40b5b0dd2c5c2853d95e65d85bad10278c0c962`

```dockerfile
```

-	Layers:
	-	`sha256:16c676728cd8c47b432ee19ce5fa5bcec095120aef08be970ae4636c3bf42cc0`  
		Last Modified: Tue, 12 Mar 2024 23:46:04 GMT  
		Size: 15.6 MB (15600417 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:198654a5f24296c7f9da5d4da5770050bc1443ded50fb9cd669845f5024d9f5a`  
		Last Modified: Tue, 12 Mar 2024 23:46:04 GMT  
		Size: 15.8 KB (15754 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:stable-threaded-buster` - linux; 386

```console
$ docker pull perl@sha256:f294e0680ab7265aac9dd1895616b0321c28223f142ed7d057cff49f966d4460
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **336.6 MB (336611418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2f7b693c364359340f459886bb4252d4f4a0cd822bf37725efea3aabf655c7a`
-	Default Command: `["perl5.38.2","-de0"]`

```dockerfile
# Fri, 23 Feb 2024 16:07:57 GMT
ADD file:c816729e048abb40ca265a52e15f687e96a04fac489fca5504d6f1a6c1036f44 in / 
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
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/P/PE/PEVANS/perl-5.38.2.tar.gz -o perl-5.38.2.tar.gz     && echo 'a0a31534451eb7b83c7d6594a497543a54d488bc90ca00f5e34762577f40655e *perl-5.38.2.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.38.2.tar.gz -C /usr/src/perl     && rm perl-5.38.2.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997014/cpm -o /usr/local/bin/cpm     && echo 'ee525f2493e36c6f688eddabaf53a51c4d3b2a4ebaa81576ac8b9f78ab57f4a1 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Fri, 23 Feb 2024 16:07:57 GMT
WORKDIR /usr/src/app
# Fri, 23 Feb 2024 16:07:57 GMT
CMD ["perl5.38.2" "-de0"]
```

-	Layers:
	-	`sha256:738abb02da0a502d42242343d73d542ff3cbebcc7bfda5ae91845cb7a4177497`  
		Last Modified: Tue, 12 Mar 2024 01:03:51 GMT  
		Size: 51.3 MB (51255592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ac5971128c8aa1a16550a107f729e02bba65015ab53141a24c171ec7a05b79a`  
		Last Modified: Tue, 12 Mar 2024 07:56:03 GMT  
		Size: 18.1 MB (18099447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3c4053c8d16e2449fdbac1122e37652f53be8b607a093453ba6bf08e56bd9ba`  
		Last Modified: Tue, 12 Mar 2024 07:56:22 GMT  
		Size: 53.5 MB (53491671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:611538514415c639eba0b1521fa6f33ff37569ea8882616480d31e1051e4242e`  
		Last Modified: Tue, 12 Mar 2024 07:57:06 GMT  
		Size: 198.5 MB (198491053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:843c3d8ad394c4df3370226bc3cb66f10282132630a2be1207c4d12e46573830`  
		Last Modified: Tue, 12 Mar 2024 09:04:51 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d4467358a244b465ff2790c359f63e827963a338654e9c861415449b3ff200a`  
		Last Modified: Tue, 12 Mar 2024 09:04:51 GMT  
		Size: 15.3 MB (15273387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0b1e1b2018ad561602c052568fac72e4176923f404403f14af19819033b4bfd`  
		Last Modified: Tue, 12 Mar 2024 09:04:50 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:stable-threaded-buster` - unknown; unknown

```console
$ docker pull perl@sha256:950cd792c72286d67be63d8b0a8a0a0e207091178ea35b6a9676ce2bbe0fb868
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.6 MB (15631511 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:033baf782b0d60dcde6dc0764e900897d6bf514a1bc513e8dcfd20137dff2ec1`

```dockerfile
```

-	Layers:
	-	`sha256:ef48a62eae8f605906819344688342fe1b58fa2191116881993feb33730dba0f`  
		Last Modified: Tue, 12 Mar 2024 09:04:51 GMT  
		Size: 15.6 MB (15615140 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8c08d5d419a5922ee080e3cf3869815d72752f3cd6596fa87c88500b0933dc4f`  
		Last Modified: Tue, 12 Mar 2024 09:04:50 GMT  
		Size: 16.4 KB (16371 bytes)  
		MIME: application/vnd.in-toto+json
