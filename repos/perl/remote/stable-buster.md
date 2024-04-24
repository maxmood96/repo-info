## `perl:stable-buster`

```console
$ docker pull perl@sha256:0b9cb9af75fbd66906326f780cf31a9116c903b4f8924888fa44e0d0bf6c2b96
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

### `perl:stable-buster` - linux; amd64

```console
$ docker pull perl@sha256:2816786f8d4987ef2f8476ab7fd7b4f017371d2f3b025190e05fba15f0cca273
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **327.8 MB (327752283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8763bd858badf369db18ca42cbd658f37f7065ba5d7f7464c05a42148299c0aa`
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
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/P/PE/PEVANS/perl-5.38.2.tar.gz -o perl-5.38.2.tar.gz     && echo 'a0a31534451eb7b83c7d6594a497543a54d488bc90ca00f5e34762577f40655e *perl-5.38.2.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.38.2.tar.gz -C /usr/src/perl     && rm perl-5.38.2.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997014/cpm -o /usr/local/bin/cpm     && echo 'ee525f2493e36c6f688eddabaf53a51c4d3b2a4ebaa81576ac8b9f78ab57f4a1 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
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
	-	`sha256:a81741cd904f936402f070f46b414a7421b73c7f78ada740d3f5c3fb9671d4d5`  
		Last Modified: Wed, 24 Apr 2024 05:05:37 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d377a1bfe519ef106226e3b3468f33ff51a103646fcd22351dce52349f925bb`  
		Last Modified: Wed, 24 Apr 2024 05:05:41 GMT  
		Size: 15.7 MB (15668285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:171be2a4242c0f5e947a0e3aeb15ff33416075758234b0ab8d29520a80d23b00`  
		Last Modified: Wed, 24 Apr 2024 05:05:37 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:stable-buster` - unknown; unknown

```console
$ docker pull perl@sha256:f7e25907b92c56bbc4315c3e3a13e0ca89bb1403adfedaff9724a92c7f4a0773
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.0 MB (15982674 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9d03fccf785abc21bbadfa7a494b52891beed78d41720b79f299143cce1e588`

```dockerfile
```

-	Layers:
	-	`sha256:f7fd229e1c3360e82cc9f016588412618c551b695e1b586ca768d1cc8979fc8a`  
		Last Modified: Wed, 24 Apr 2024 05:05:38 GMT  
		Size: 16.0 MB (15966402 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5bc24748f88944b8efd463602d02bdd03ea0dbd1eaeca80c95aecced58be3dab`  
		Last Modified: Wed, 24 Apr 2024 05:05:37 GMT  
		Size: 16.3 KB (16272 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:stable-buster` - linux; arm variant v7

```console
$ docker pull perl@sha256:ee1fa44be68adfd357743cecd0bbc046f1f3538839941ca971b21957febe9a2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.5 MB (292509093 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95b2cf92f1d78648d9a72c4aed11ffd8b03a614c83574f020cb6774a79cde61e`
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
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/P/PE/PEVANS/perl-5.38.2.tar.gz -o perl-5.38.2.tar.gz     && echo 'a0a31534451eb7b83c7d6594a497543a54d488bc90ca00f5e34762577f40655e *perl-5.38.2.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.38.2.tar.gz -C /usr/src/perl     && rm perl-5.38.2.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997014/cpm -o /usr/local/bin/cpm     && echo 'ee525f2493e36c6f688eddabaf53a51c4d3b2a4ebaa81576ac8b9f78ab57f4a1 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
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
	-	`sha256:61e0159266c5f4078da420b3304060ea9e31386d58cb0cdadffb0f6123a1cd4e`  
		Last Modified: Fri, 12 Apr 2024 07:29:05 GMT  
		Size: 14.8 MB (14782212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:583ea47d33b491af1cfcb324493b347148a2ffcd4603fcd4a6360464e0738d78`  
		Last Modified: Fri, 12 Apr 2024 07:29:05 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:stable-buster` - unknown; unknown

```console
$ docker pull perl@sha256:80ab0344f8a0b1c335ed6780ff4a7f39b4717ff0b7c653aa096a138c7e86c8e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 MB (15428163 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8c391c197257a8cb9f7720c8ee4330f38e902c57ad72ee993e52e107fb932c4`

```dockerfile
```

-	Layers:
	-	`sha256:dcfade45a2a918a474ae721d64e890f3fc6118541ac887c06b5dd6c05c43bd6a`  
		Last Modified: Fri, 12 Apr 2024 07:29:04 GMT  
		Size: 15.4 MB (15411818 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6a4a8504eb2094a3ba7e3c9e5924ae6d109c854f4699196641a65894139236bd`  
		Last Modified: Fri, 12 Apr 2024 07:29:03 GMT  
		Size: 16.3 KB (16345 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:stable-buster` - linux; arm64 variant v8

```console
$ docker pull perl@sha256:cf549c48ac6c18f165a3a4af83a7f7e4f99d29c302b524bf58b5ee488a5de24c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **318.1 MB (318113178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:812ba17bdedfdf376591e1ade7d171728ab29f636600c8a5653b816a4fb9fc5f`
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
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/P/PE/PEVANS/perl-5.38.2.tar.gz -o perl-5.38.2.tar.gz     && echo 'a0a31534451eb7b83c7d6594a497543a54d488bc90ca00f5e34762577f40655e *perl-5.38.2.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.38.2.tar.gz -C /usr/src/perl     && rm perl-5.38.2.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997014/cpm -o /usr/local/bin/cpm     && echo 'ee525f2493e36c6f688eddabaf53a51c4d3b2a4ebaa81576ac8b9f78ab57f4a1 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
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
	-	`sha256:0a9c342df092910043fa7f267b7c0b10672e8279bd6eb90b7b90676a249d0d71`  
		Last Modified: Thu, 11 Apr 2024 05:53:28 GMT  
		Size: 15.6 MB (15608870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fd61cf114b7f11dedb7e11d31d16bb641d086ee7fa7b3fcc62010f77f0db7b0`  
		Last Modified: Thu, 11 Apr 2024 05:53:27 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:stable-buster` - unknown; unknown

```console
$ docker pull perl@sha256:1bb5679b1fa4c3c9a08de7497fb73da5a1597155338c4f74334c0d1467977275
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.6 MB (15616799 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7bcb6720835211456f2ffea0831784f21056f96ad46d378ad78d599d2c4f6724`

```dockerfile
```

-	Layers:
	-	`sha256:b2d8d01087c326f542d4885f4e32636f33755709c5384af4e70bd56ebcf997cf`  
		Last Modified: Thu, 11 Apr 2024 05:53:27 GMT  
		Size: 15.6 MB (15600519 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b560009352b90084b05d47240de3dea65d1f143b6e018f5db3d253b4eea9ae99`  
		Last Modified: Thu, 11 Apr 2024 05:53:26 GMT  
		Size: 16.3 KB (16280 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:stable-buster` - linux; 386

```console
$ docker pull perl@sha256:f044746504b96b2edd45020618a15cf3ced08861c51a24f4aa46f03fc7b2356f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **336.7 MB (336684374 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:760b741ca8be1127e7e5535faaaf33b6ec79031ac056c63850a602bb2f7d9e5c`
-	Default Command: `["perl5.38.2","-de0"]`

```dockerfile
# Thu, 21 Mar 2024 18:18:23 GMT
ADD file:5f943bcdbbb65accdf0b3bc452a1d4fafd2c64a9c6f6b3010b2a7ca20bedef36 in / 
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
	-	`sha256:a3113a911224f7223aa235bbc20dff34c7d1419374b2180cf17ec274239d63d4`  
		Last Modified: Wed, 24 Apr 2024 03:44:44 GMT  
		Size: 51.4 MB (51420054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1354eeaeda7eb3c61cf02dbb765bed988acda27118f144f40318507dd7934295`  
		Last Modified: Wed, 24 Apr 2024 04:44:02 GMT  
		Size: 18.1 MB (18099027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3055ae20eecf0d5388e9ed336426983b625a70d36236930785aac17415cfcf3`  
		Last Modified: Wed, 24 Apr 2024 04:44:23 GMT  
		Size: 53.5 MB (53491779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:761a4fb01a05271ea38a1437f27706939e45c0f2ea11a0b93f7920952ab0334a`  
		Last Modified: Wed, 24 Apr 2024 04:45:06 GMT  
		Size: 198.5 MB (198498122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee4acd57c0ab2013b687310adaa134ea727491022811060c9cada13a9c8cbf4c`  
		Last Modified: Wed, 24 Apr 2024 06:06:19 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b4a3e9a0bf85586a609788c9f149908e682b9c9c293bb3726c50c9a50c57dc1`  
		Last Modified: Wed, 24 Apr 2024 06:06:19 GMT  
		Size: 15.2 MB (15175127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ff40bbaa602540511d034819dace27ad35c19bf9d9a02988ea3a21b8ff3f441`  
		Last Modified: Wed, 24 Apr 2024 06:06:19 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:stable-buster` - unknown; unknown

```console
$ docker pull perl@sha256:9dd2c4baea4e2a92a8d38c1ca0e54d711eb106dbe82e349304326da3ab7c3a90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.0 MB (15988222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1dfa3a53a2b855aca234c849b8f0fd1cad54e87915214973e5d5c7feed2a6ce2`

```dockerfile
```

-	Layers:
	-	`sha256:e6a46f656fb94805545de5eb67be669f9bd72dcab299d74606d3e71b0f0678b9`  
		Last Modified: Wed, 24 Apr 2024 06:06:19 GMT  
		Size: 16.0 MB (15971984 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6cb099ca47373036249e7cce7427c7aa6fb6246fe5077c8d8a08929a0a43f9e3`  
		Last Modified: Wed, 24 Apr 2024 06:06:19 GMT  
		Size: 16.2 KB (16238 bytes)  
		MIME: application/vnd.in-toto+json
