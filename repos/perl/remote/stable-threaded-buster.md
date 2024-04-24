## `perl:stable-threaded-buster`

```console
$ docker pull perl@sha256:f71eda1c54bbc32e9b78712ae4ac797b56e5cd50567960ddf8c664d188f57370
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
$ docker pull perl@sha256:c38dd68df99bd4821bc01951cfee5b3bd91f323c5864191f4f009630c2389858
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **327.8 MB (327811280 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9520ef0d37d97905254957ffad3b9949082120b421c94f3652d81c2ae3edf61a`
-	Default Command: `["perl5.38.2","-de0"]`

```dockerfile
# Thu, 21 Mar 2024 18:18:23 GMT
ADD file:b604b7bddfed00352fcc1abb8f44014438aca55d833109520e80b61c5fb207a1 in / 
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
	-	`sha256:dbd6422b1b97494149e51bbd6c24d444b4a8794d2702d105efce98c44de9ad50`  
		Last Modified: Wed, 24 Apr 2024 03:33:41 GMT  
		Size: 50.7 MB (50657502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da3eeb481764e6e279258aa837b781d2473689eb7a7d79fc80fc0f4ea11407d3`  
		Last Modified: Wed, 24 Apr 2024 04:22:58 GMT  
		Size: 17.6 MB (17585553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1322649fbe6339542d838841a0f72dea49bb02186f02026edbca0748db168c1`  
		Last Modified: Wed, 24 Apr 2024 04:23:13 GMT  
		Size: 51.9 MB (51895971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bf9ee9914dd7dd8911e1dfbcda44d2309024daab6b2d3a0cf1789cc5f01f9c5`  
		Last Modified: Wed, 24 Apr 2024 04:23:43 GMT  
		Size: 191.9 MB (191944705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8433ae06620951dbaa69ceafcf1089b8cc170ffaa86433e54a575b5372370dc2`  
		Last Modified: Wed, 24 Apr 2024 05:06:40 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1e1cab2143cb9576b1feb03d38a989f3079346a4f5fa6ffe52ac82e2f1475c1`  
		Last Modified: Wed, 24 Apr 2024 05:06:40 GMT  
		Size: 15.7 MB (15727283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0602701e95c46a20f1752e25f41727240a09cbcab693f16a2f4174979e8aa805`  
		Last Modified: Wed, 24 Apr 2024 05:06:40 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:stable-threaded-buster` - unknown; unknown

```console
$ docker pull perl@sha256:26f16919826bc78c5cf3ed59a13f0599a8ed45adbb63df93712adb31255e4562
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.0 MB (15982900 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28079652bc42838b4d0efd6676f71f10126c06dbfcbb0f9a10172165d3edc75c`

```dockerfile
```

-	Layers:
	-	`sha256:0c88d6800198534d612dfcacb599ca78e18730de69cfce2fe9f1cb1031ec39a7`  
		Last Modified: Wed, 24 Apr 2024 05:06:40 GMT  
		Size: 16.0 MB (15966492 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:688b5a40ab474efc6e904b1d0a33c816c1940ca787ae885e88187e0a0a783d59`  
		Last Modified: Wed, 24 Apr 2024 05:06:40 GMT  
		Size: 16.4 KB (16408 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:stable-threaded-buster` - linux; arm variant v7

```console
$ docker pull perl@sha256:10db852624389785ff52a119ffdfa42108f4f75a41deae749eb5403a610d96cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.5 MB (292530979 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69f237036b5f28772d5233cb7051f677527c8ed425058cf2f87a91dca7dcbe7f`
-	Default Command: `["perl5.38.2","-de0"]`

```dockerfile
# Thu, 21 Mar 2024 18:18:23 GMT
ADD file:56eb0c1e9a01d2e3320b2f3d897736bfe09ccb53ef1ae8bfea2b9d4099bc1d6b in / 
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
	-	`sha256:300908ef79221077165ff78ff105758d14dd67c42610c4e0aafdd731a920a871`  
		Last Modified: Wed, 10 Apr 2024 01:05:35 GMT  
		Size: 46.0 MB (45962444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a28291d070880fd3bc1d1083c0a3dfd62197b6f8f9b8f0222bebfb7abc3998c`  
		Last Modified: Wed, 10 Apr 2024 07:02:28 GMT  
		Size: 16.2 MB (16217560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df332bea5b985c1c2dd5d35090367d1eeb17f766d81c69c6484a9dbdfb6a2a19`  
		Last Modified: Wed, 10 Apr 2024 07:02:46 GMT  
		Size: 47.4 MB (47411064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50c429ea890a21b115686f06bcd8e64b77317af15fee22637d21494c7f7e8763`  
		Last Modified: Wed, 10 Apr 2024 07:03:24 GMT  
		Size: 168.1 MB (168135545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abb6fde524734c99a9ef73f6d32a075a3571b2c98655e9f6da7efa8be371067c`  
		Last Modified: Fri, 12 Apr 2024 07:29:03 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4908b769d985e14c68fb0ee6f5aff4cb9937133b329149ffa1d0ce82b159080`  
		Last Modified: Fri, 12 Apr 2024 08:01:27 GMT  
		Size: 14.8 MB (14804102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abb319202a48440acbeb914e3e168fa54770d79b2cd953a2c3dbf8f28c332138`  
		Last Modified: Fri, 12 Apr 2024 08:01:26 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:stable-threaded-buster` - unknown; unknown

```console
$ docker pull perl@sha256:8f66261a90a763eccf3d061947eb5f08dd0a14cb984c4281cfe89100321b84c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 MB (15427728 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0f95d1b956f49cbe61682c2c7bf6748686178a10980871efa514ce3f7cf126e`

```dockerfile
```

-	Layers:
	-	`sha256:7e7b21203211f670596cb173a69efc9a0c66ba4897e2a9b37063a7c05d4d3cda`  
		Last Modified: Fri, 12 Apr 2024 08:01:27 GMT  
		Size: 15.4 MB (15411908 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c60f76fe35f751237b6b7be85b3d72b84a59eda09fbe41f94587de36c433f2e4`  
		Last Modified: Fri, 12 Apr 2024 08:01:26 GMT  
		Size: 15.8 KB (15820 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:stable-threaded-buster` - linux; arm64 variant v8

```console
$ docker pull perl@sha256:0b71446c790d0839f00b2ef6a61f327961ace95d8677f793bf596e404d68dc46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **318.1 MB (318143982 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5cf6cd6b179a26d617d703bcc5acc3829045f19f569acc0bac55964a32b7204d`
-	Default Command: `["perl5.38.2","-de0"]`

```dockerfile
# Thu, 21 Mar 2024 18:18:23 GMT
ADD file:9b995c280b9e45d7ee0b5a7151b97767f47960ed492e35fd55c5eec6917bde2c in / 
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
	-	`sha256:5173f9984b20306181404de41336884e6153c70a737a933879b7878563fc5bad`  
		Last Modified: Wed, 10 Apr 2024 00:45:06 GMT  
		Size: 49.3 MB (49290826 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5a2fef8d22586d8b400820a7eb103890ffb31484294a394d9d1f6c707a2bb9c`  
		Last Modified: Wed, 10 Apr 2024 04:33:49 GMT  
		Size: 17.5 MB (17456523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13f4463add27d4c2d315ca63e2d49c8bfb34a4fdd9015ea40d66f773285375d7`  
		Last Modified: Wed, 10 Apr 2024 04:34:03 GMT  
		Size: 52.2 MB (52231857 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a8636ccf677873adfe47bae13204f2fe3222b5c3d17e9cad47a51e6e6c67116`  
		Last Modified: Wed, 10 Apr 2024 04:34:28 GMT  
		Size: 183.5 MB (183524834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a1409dd3778ff2c3113bb58886f75004dc4ed421c6223f74386a28702a97a43`  
		Last Modified: Thu, 11 Apr 2024 05:53:26 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b6b7e69a20ff446955e99a1885a2c86e6b2c9b8760b7b4302390667a265cd9b`  
		Last Modified: Thu, 11 Apr 2024 06:21:07 GMT  
		Size: 15.6 MB (15639675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2ec3167adcae77bb978cf330c66214a34d30174c1d79ad811872cf6e2536601`  
		Last Modified: Thu, 11 Apr 2024 06:21:06 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:stable-threaded-buster` - unknown; unknown

```console
$ docker pull perl@sha256:89477d99615d1f36113569e036c98922d868e8eea261fafd2f4d94dc76b8b2ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.6 MB (15616363 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de4d57ecfcdb2159947e38a306bd2f76b3ab287bb672d2410e20c1083b9a9bf7`

```dockerfile
```

-	Layers:
	-	`sha256:ba7ee81618d83239e637ed96dfdee5e379166803eb53c3a917be0247f642c305`  
		Last Modified: Thu, 11 Apr 2024 06:21:07 GMT  
		Size: 15.6 MB (15600609 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:de007d4da3c45ad2910ddd6299a650d32d3f00fcf98cc56aaf8772d6199a5641`  
		Last Modified: Thu, 11 Apr 2024 06:21:06 GMT  
		Size: 15.8 KB (15754 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:stable-threaded-buster` - linux; 386

```console
$ docker pull perl@sha256:580f1c7e9d6bb43a8ce2643f7c6f2f78cfd8b67034018a2729813de78f25db2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **336.6 MB (336621561 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce32ecb565fc14bf95bbeaff8ce4f00bffe5371ed7af0b5198e3f6fe4264f6ad`
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
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/P/PE/PEVANS/perl-5.38.2.tar.gz -o perl-5.38.2.tar.gz     && echo 'a0a31534451eb7b83c7d6594a497543a54d488bc90ca00f5e34762577f40655e *perl-5.38.2.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.38.2.tar.gz -C /usr/src/perl     && rm perl-5.38.2.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997014/cpm -o /usr/local/bin/cpm     && echo 'ee525f2493e36c6f688eddabaf53a51c4d3b2a4ebaa81576ac8b9f78ab57f4a1 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
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
	-	`sha256:1e126bce55f4b580bc9425f77fdd1f6f5b7945f1f6dabf08fb85aac20d887e9b`  
		Last Modified: Wed, 10 Apr 2024 09:04:26 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:672cbff355187326072650e412b9e372ac1ae05aa53500b029491dec97461e15`  
		Last Modified: Wed, 10 Apr 2024 09:04:27 GMT  
		Size: 15.3 MB (15275429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:587d7abf702fc3df28d73333fae3be00045d50b247dcc2ab231c0e185f8f46a1`  
		Last Modified: Wed, 10 Apr 2024 09:04:26 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:stable-threaded-buster` - unknown; unknown

```console
$ docker pull perl@sha256:573498cdfdbdc2b47a4c2c25af47c5c81c7f690e30b9a9902b9d857108e3e90c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.6 MB (15631703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20507951211dec4ba51d08423323e25847aee0115eb6a08a4463deb02753a52d`

```dockerfile
```

-	Layers:
	-	`sha256:770f445c50b00ad1d89dfdcab293113f231c3e1f6a3b3356eab1dccb77e610d1`  
		Last Modified: Wed, 10 Apr 2024 09:04:27 GMT  
		Size: 15.6 MB (15615332 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d64eb57ce26626e6e1db61da0af55282db730dc4868f715a83f2964e09433b11`  
		Last Modified: Wed, 10 Apr 2024 09:04:26 GMT  
		Size: 16.4 KB (16371 bytes)  
		MIME: application/vnd.in-toto+json
