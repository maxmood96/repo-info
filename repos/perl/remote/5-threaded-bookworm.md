## `perl:5-threaded-bookworm`

```console
$ docker pull perl@sha256:aa21fa2c573dec889dcfe2c52c6b3c4e87cd07625a1de3419407981e4cc7afd1
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

### `perl:5-threaded-bookworm` - linux; amd64

```console
$ docker pull perl@sha256:1ae7392db5e21db5538e7a3c2511fa1af910d54d4b13817c9537f49c02b4d546
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **364.6 MB (364560560 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:778fd295f0f8537e5ed5237d5014d17f9034e973c54e76544412afd542e69dce`
-	Default Command: `["perl5.38.2","-de0"]`

```dockerfile
# Sun, 31 Dec 2023 10:01:19 GMT
ADD file:077a3156bd8271f26498ae6ac3800e68a42b9277581bc81eea31fec1a123dca5 in / 
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
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/P/PE/PEVANS/perl-5.38.2.tar.gz -o perl-5.38.2.tar.gz     && echo 'a0a31534451eb7b83c7d6594a497543a54d488bc90ca00f5e34762577f40655e *perl-5.38.2.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.38.2.tar.gz -C /usr/src/perl     && rm perl-5.38.2.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997014/cpm -o /usr/local/bin/cpm     && echo 'ee525f2493e36c6f688eddabaf53a51c4d3b2a4ebaa81576ac8b9f78ab57f4a1 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Sun, 31 Dec 2023 10:01:19 GMT
WORKDIR /usr/src/app
# Sun, 31 Dec 2023 10:01:19 GMT
CMD ["perl5.38.2" "-de0"]
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
	-	`sha256:8d55d1cb1ffb0c7e0438b372a96cc0f23a76c21571fa3e7b7b38e3fbc66a8c3a`  
		Last Modified: Thu, 11 Jan 2024 04:44:54 GMT  
		Size: 64.1 MB (64139713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa8e0026efede8b3da7364fd0ec879657b2c9be209b5cc1e2ec83bed6dfcf6a9`  
		Last Modified: Thu, 11 Jan 2024 04:45:29 GMT  
		Size: 211.1 MB (211103479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b303e6ee4568beadaabd5c40a24407672fc108de0fc62bbfd259c91ea145b9e8`  
		Last Modified: Fri, 12 Jan 2024 00:40:58 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:546531e98b14c81b0ad74d532471ab35aaa88d75fbcf789a10bab2f2ef29ae83`  
		Last Modified: Fri, 12 Jan 2024 00:40:58 GMT  
		Size: 15.7 MB (15709116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99c263d99c2207531a683704501f2b7adef82bbe0647f3cafcc8d7bf8a760ba7`  
		Last Modified: Fri, 12 Jan 2024 00:40:58 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:5-threaded-bookworm` - unknown; unknown

```console
$ docker pull perl@sha256:3bc160bf8be637c5d94b2825ef058c54b018d727833dbcecabfe2c5dec96ea78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.4 MB (13421304 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d615c0e51fe276ba9457b1c6ebc3c907ab4c930b405d2744c909ee1a1741ef7`

```dockerfile
```

-	Layers:
	-	`sha256:fa62c89bbddf0ac1e23e5243862bff5f83e44b1952b1fded1410aaf8d30dba31`  
		Last Modified: Fri, 12 Jan 2024 00:40:58 GMT  
		Size: 13.4 MB (13403331 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7257b17d8cf68cae85a5b50db1b7bb11fc1548a130a07ef813925da1711d301f`  
		Last Modified: Fri, 12 Jan 2024 00:40:58 GMT  
		Size: 18.0 KB (17973 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:5-threaded-bookworm` - linux; arm variant v5

```console
$ docker pull perl@sha256:03f787669973a51c1e656bb16ee7dc3ce71588262913371fc1a33116b7765e4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **330.9 MB (330908044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b62d2ed122e3e731112a6659278a7ed9f2d81b39ca01004c3cfa48346f4e9483`
-	Default Command: `["perl5.38.2","-de0"]`

```dockerfile
# Tue, 19 Dec 2023 01:55:14 GMT
ADD file:a6a83a649ad34de44e3b18ac2ef474733028a38445b36395b37a47906a17e460 in / 
# Tue, 19 Dec 2023 01:55:15 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 05:21:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 05:21:59 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 05:23:24 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Sun, 31 Dec 2023 10:01:19 GMT
WORKDIR /usr/src/perl
# Sun, 31 Dec 2023 10:01:19 GMT
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/P/PE/PEVANS/perl-5.38.2.tar.gz -o perl-5.38.2.tar.gz     && echo 'a0a31534451eb7b83c7d6594a497543a54d488bc90ca00f5e34762577f40655e *perl-5.38.2.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.38.2.tar.gz -C /usr/src/perl     && rm perl-5.38.2.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997014/cpm -o /usr/local/bin/cpm     && echo 'ee525f2493e36c6f688eddabaf53a51c4d3b2a4ebaa81576ac8b9f78ab57f4a1 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Sun, 31 Dec 2023 10:01:19 GMT
WORKDIR /usr/src/app
# Sun, 31 Dec 2023 10:01:19 GMT
CMD ["perl5.38.2" "-de0"]
```

-	Layers:
	-	`sha256:f3aac8ada11b4cd51c598b397af8986343d5ffa06ce2a7a7c7c80f4ea6f5e522`  
		Last Modified: Tue, 19 Dec 2023 01:58:07 GMT  
		Size: 47.3 MB (47319238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0fd25a16876a3944cbd080157b9e23fe47b07ccfaa03a3b8075979027a60208`  
		Last Modified: Tue, 19 Dec 2023 05:31:23 GMT  
		Size: 22.7 MB (22724641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6dd8a0a191b42cdb49dcb6ca7c111242e7ef4d447f3b729605f30173433bba2`  
		Last Modified: Tue, 19 Dec 2023 05:31:46 GMT  
		Size: 61.5 MB (61508870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe5ddaed1389aec60f80faad6640540555cb8a57f3acbc1566f210c60f5773d9`  
		Last Modified: Tue, 19 Dec 2023 05:32:27 GMT  
		Size: 184.4 MB (184416924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9eb572e40cc22058b20b4f79a200e14f80a5200853df4aa2bbf0e0cf3a47c7c4`  
		Last Modified: Wed, 20 Dec 2023 20:46:02 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d76564d4338a3858e0c6b2a6afdb267c8b6b1c64ca7da4045e3148fb5839c9e`  
		Last Modified: Mon, 01 Jan 2024 21:58:59 GMT  
		Size: 14.9 MB (14938103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:484434fcbd14b24447616803db442f640868eb123662f5740b648d09422ca289`  
		Last Modified: Mon, 01 Jan 2024 21:58:58 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:5-threaded-bookworm` - unknown; unknown

```console
$ docker pull perl@sha256:894e1b2251072bab5cdd6efad7f3f4bb46bc0a1ccfd491847e225ccb241c3c39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.2 MB (13245973 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6edeaa290bf2472685e6d8d59d4f2980f5184354fc494d782dc4dbb3776dd8ba`

```dockerfile
```

-	Layers:
	-	`sha256:29ac66048cf1abf109b7d7814c1d9d3a28cf36452d52bdf5a3a229787bda337b`  
		Last Modified: Mon, 01 Jan 2024 21:58:59 GMT  
		Size: 13.2 MB (13228545 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ade7b4f993439d2e8bb2994dae910184ebfc8d6def350afec331aae73f3ff50e`  
		Last Modified: Mon, 01 Jan 2024 21:58:58 GMT  
		Size: 17.4 KB (17428 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:5-threaded-bookworm` - linux; arm variant v7

```console
$ docker pull perl@sha256:da319000d8c471d583df6255abe9b1e41e382c1a13bf4c2f5bc2eec40aa5558b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **316.1 MB (316127284 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81ff86b01dd645ce68518f1be7efe1d90262c3342a5f2f6cca59ff5a3ecae22a`
-	Default Command: `["perl5.38.2","-de0"]`

```dockerfile
# Tue, 19 Dec 2023 02:07:39 GMT
ADD file:1633615de1824a95e35747f0133e90ab5ddc138574a83fb9c4f337cf45762574 in / 
# Tue, 19 Dec 2023 02:07:39 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 07:54:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 07:55:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 07:56:32 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Sun, 31 Dec 2023 10:01:19 GMT
WORKDIR /usr/src/perl
# Sun, 31 Dec 2023 10:01:19 GMT
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/P/PE/PEVANS/perl-5.38.2.tar.gz -o perl-5.38.2.tar.gz     && echo 'a0a31534451eb7b83c7d6594a497543a54d488bc90ca00f5e34762577f40655e *perl-5.38.2.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.38.2.tar.gz -C /usr/src/perl     && rm perl-5.38.2.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997014/cpm -o /usr/local/bin/cpm     && echo 'ee525f2493e36c6f688eddabaf53a51c4d3b2a4ebaa81576ac8b9f78ab57f4a1 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Sun, 31 Dec 2023 10:01:19 GMT
WORKDIR /usr/src/app
# Sun, 31 Dec 2023 10:01:19 GMT
CMD ["perl5.38.2" "-de0"]
```

-	Layers:
	-	`sha256:89cc9e7932dc0f797e6c3fc84b4c6868fedaca1b174b38a51e152a23a643be7a`  
		Last Modified: Tue, 19 Dec 2023 02:11:28 GMT  
		Size: 45.2 MB (45156699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d1cce8fac77d35b90037c77fcb46603ed4cdc1388009887c5132cbdf3531132`  
		Last Modified: Tue, 19 Dec 2023 08:06:19 GMT  
		Size: 21.9 MB (21949134 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:258af69dcb8426bcc3ebc63b670048d9d4191fd206986dd72f83a247768f7f65`  
		Last Modified: Tue, 19 Dec 2023 08:06:39 GMT  
		Size: 59.2 MB (59216125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ba6fc4113c5eec43c041f3fe9cca3eae36c8a6cffe2cc7fe2b7089fba2bf7cb`  
		Last Modified: Tue, 19 Dec 2023 08:07:16 GMT  
		Size: 175.1 MB (175078779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6bd9efdfaa3c29d8e1eedd3d71ad1f99b904e058d05774e3c2ffa33fedcdc65`  
		Last Modified: Wed, 20 Dec 2023 23:31:55 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc61144ed3c485d5bb5d6402746c4d03b665929fc59a0b1b27a9549dc7f79408`  
		Last Modified: Mon, 01 Jan 2024 23:00:52 GMT  
		Size: 14.7 MB (14726280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06155cfac2592216fc19609b4ea10cd164c6197727d7e057dc9d8f61a5c80148`  
		Last Modified: Mon, 01 Jan 2024 23:00:51 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:5-threaded-bookworm` - unknown; unknown

```console
$ docker pull perl@sha256:2de295298ea34c37a602b8995d11411281bbddfa09cb8521ccbf76aacb2a0db0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.3 MB (13251447 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6f85cfba21f3ad2ff1472d64c58964317214742a927632707fbe0fa02766e7f`

```dockerfile
```

-	Layers:
	-	`sha256:f1c1060f28361d16fd612b8be14ed818c41fa5e3a948b080b812d0f44d9408c2`  
		Last Modified: Mon, 01 Jan 2024 23:00:52 GMT  
		Size: 13.2 MB (13234019 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4400e8e473d5bb5334e8362ee689d4220cdc6e50aa187b5c4b45bcc63f906a09`  
		Last Modified: Mon, 01 Jan 2024 23:00:51 GMT  
		Size: 17.4 KB (17428 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:5-threaded-bookworm` - linux; arm64 variant v8

```console
$ docker pull perl@sha256:fea3d78c7757ee2f6a0fd192a04aafb56c4f6baca2751d533dfa6b01b1a6b316
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **355.3 MB (355287974 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:119c67789bbeeb44ebf7e4af84e7080067c130b1fe9ebd950a6a39c1fe916875`
-	Default Command: `["perl5.38.2","-de0"]`

```dockerfile
# Tue, 19 Dec 2023 01:41:02 GMT
ADD file:412f80f75ed3e520f767e70b6b27fc81807f62fc5c6e5adf756507e33af9fa6b in / 
# Tue, 19 Dec 2023 01:41:02 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 11:33:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 11:34:00 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 11:34:49 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Sun, 31 Dec 2023 10:01:19 GMT
WORKDIR /usr/src/perl
# Sun, 31 Dec 2023 10:01:19 GMT
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/P/PE/PEVANS/perl-5.38.2.tar.gz -o perl-5.38.2.tar.gz     && echo 'a0a31534451eb7b83c7d6594a497543a54d488bc90ca00f5e34762577f40655e *perl-5.38.2.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.38.2.tar.gz -C /usr/src/perl     && rm perl-5.38.2.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997014/cpm -o /usr/local/bin/cpm     && echo 'ee525f2493e36c6f688eddabaf53a51c4d3b2a4ebaa81576ac8b9f78ab57f4a1 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Sun, 31 Dec 2023 10:01:19 GMT
WORKDIR /usr/src/app
# Sun, 31 Dec 2023 10:01:19 GMT
CMD ["perl5.38.2" "-de0"]
```

-	Layers:
	-	`sha256:b66b4ecd3ecfb67b3b7a2a44b0199cbdfc94965c8bd3fefab75cd2e612799740`  
		Last Modified: Tue, 19 Dec 2023 01:44:14 GMT  
		Size: 49.6 MB (49592259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c641d36985b2db859fc64c43a6dbf7c25cdf73e5d16d107fab1d95a840bb4e1`  
		Last Modified: Tue, 19 Dec 2023 11:42:17 GMT  
		Size: 23.6 MB (23582271 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddd8544b6e15c7a4096b1f48a67fb5bed2efba509fca597f1c164b582ab01c02`  
		Last Modified: Tue, 19 Dec 2023 11:42:35 GMT  
		Size: 64.0 MB (63988289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae58c7c06d64a1a86430205c774637c7615d1365a575b256801bb23390ad5260`  
		Last Modified: Tue, 19 Dec 2023 11:43:05 GMT  
		Size: 202.5 MB (202484237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1769aff3dbf21a4bcca67232b3567c680696a5af89e9dbe0b48f746c33ad4c5a`  
		Last Modified: Wed, 20 Dec 2023 22:42:08 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76bdce1d453ffeed43a5939c6475744b58ed514e16fe76393cceedf98ee1a3d8`  
		Last Modified: Mon, 01 Jan 2024 22:15:05 GMT  
		Size: 15.6 MB (15640650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4661154b063acf8983a9e7528731b59959d9d344fa68cd1073c0787450ac8225`  
		Last Modified: Mon, 01 Jan 2024 22:15:04 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:5-threaded-bookworm` - unknown; unknown

```console
$ docker pull perl@sha256:61915a1009656c5f8ae317593143ed1f719161a36a15c9bc8a35074dce679c51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.4 MB (13445900 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08432422f8c8de0131056094909ad1238dc490a0ba1eee95a08feeff60f7d71d`

```dockerfile
```

-	Layers:
	-	`sha256:a4e4d2adef41b478c8a90f7f049f61b42ce10f5adab713e7aaf4fbf7b98cdca9`  
		Last Modified: Mon, 01 Jan 2024 22:15:05 GMT  
		Size: 13.4 MB (13428568 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ca0234546aa1c39678b015ff1b36189f77d8a8e4104d7c6c50c7026521b7c876`  
		Last Modified: Mon, 01 Jan 2024 22:15:04 GMT  
		Size: 17.3 KB (17332 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:5-threaded-bookworm` - linux; 386

```console
$ docker pull perl@sha256:5330d3a58ae10a386c50a1fb4b160f7c19a6790d87aba95f66596846cd9609a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **366.7 MB (366740307 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8fceca44b2a1a8bd16dea99bd2eecc2cd19e9cef5eebd89e0f2b14b1a65269c`
-	Default Command: `["perl5.38.2","-de0"]`

```dockerfile
# Sun, 31 Dec 2023 10:01:19 GMT
ADD file:c7cf48f483b7eba0a82956c5ef1a1c78e84c2b91d0b9cf17fdfde5b756fcba9f in / 
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
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/P/PE/PEVANS/perl-5.38.2.tar.gz -o perl-5.38.2.tar.gz     && echo 'a0a31534451eb7b83c7d6594a497543a54d488bc90ca00f5e34762577f40655e *perl-5.38.2.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.38.2.tar.gz -C /usr/src/perl     && rm perl-5.38.2.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997014/cpm -o /usr/local/bin/cpm     && echo 'ee525f2493e36c6f688eddabaf53a51c4d3b2a4ebaa81576ac8b9f78ab57f4a1 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Sun, 31 Dec 2023 10:01:19 GMT
WORKDIR /usr/src/app
# Sun, 31 Dec 2023 10:01:19 GMT
CMD ["perl5.38.2" "-de0"]
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
	-	`sha256:5c54028869f774208be77fae1c160385eebefa5743b2d687462a195a10b5ec1b`  
		Last Modified: Thu, 11 Jan 2024 04:41:57 GMT  
		Size: 66.0 MB (65986939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5000f105af4698bd73d613c19498edc90b389261f540f976f31cc1a4f345526f`  
		Last Modified: Thu, 11 Jan 2024 04:42:52 GMT  
		Size: 210.0 MB (210036478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10dd5c668c05b640ee97e09a6679198b2dadd66f08b4413308f65d8314fb2625`  
		Last Modified: Fri, 12 Jan 2024 00:41:52 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8611543825ead35ba8918f10cf4422bc9d838ad7f7fbaf3d7b3fa2702809f637`  
		Last Modified: Fri, 12 Jan 2024 00:41:52 GMT  
		Size: 15.3 MB (15250338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7eb5c03d24d4efadec97ae4caba277d302e3e9908f82cb0c6fbae42926a4039f`  
		Last Modified: Fri, 12 Jan 2024 00:41:51 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:5-threaded-bookworm` - unknown; unknown

```console
$ docker pull perl@sha256:a3cf80253c3cca4e46db4d7b600c54ef4c0f02bb2b0f5db727dc73949ac5ecb7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.4 MB (13401649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ee9e920b65b1336703382293bcc4bbb4281a7d0dba35af788661a48b064c375`

```dockerfile
```

-	Layers:
	-	`sha256:2761aab239aeadf8dccab9900b66bc5e6a171dd67584c7ec6fc4546bac78c00c`  
		Last Modified: Fri, 12 Jan 2024 00:41:52 GMT  
		Size: 13.4 MB (13383735 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a34a49d83b3dccc49f0a0b0fb192a184362d7f2d4db42695267b37a31261b398`  
		Last Modified: Fri, 12 Jan 2024 00:41:52 GMT  
		Size: 17.9 KB (17914 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:5-threaded-bookworm` - linux; mips64le

```console
$ docker pull perl@sha256:7208c9b4dbca70ccc53447fc7bc8a4c6a46be9732674ca8a2fea71af3f88c412
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **340.7 MB (340730253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e90e1f34796c4eccdfefeeb4b49fc55c727c04bb32beab11e69584b43945ef3`
-	Default Command: `["perl5.38.2","-de0"]`

```dockerfile
# Tue, 19 Dec 2023 02:12:55 GMT
ADD file:87d7b313e4309f5e9ad824dfd7dc6f9a85458ccb7056f5001dc6066e964eabcb in / 
# Tue, 19 Dec 2023 02:13:00 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 02:50:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 02:52:06 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 02:57:22 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Sun, 31 Dec 2023 10:01:19 GMT
WORKDIR /usr/src/perl
# Sun, 31 Dec 2023 10:01:19 GMT
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/P/PE/PEVANS/perl-5.38.2.tar.gz -o perl-5.38.2.tar.gz     && echo 'a0a31534451eb7b83c7d6594a497543a54d488bc90ca00f5e34762577f40655e *perl-5.38.2.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.38.2.tar.gz -C /usr/src/perl     && rm perl-5.38.2.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997014/cpm -o /usr/local/bin/cpm     && echo 'ee525f2493e36c6f688eddabaf53a51c4d3b2a4ebaa81576ac8b9f78ab57f4a1 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Sun, 31 Dec 2023 10:01:19 GMT
WORKDIR /usr/src/app
# Sun, 31 Dec 2023 10:01:19 GMT
CMD ["perl5.38.2" "-de0"]
```

-	Layers:
	-	`sha256:659946beb815c8c0157caa0571c5512c4508ff0fe3bbb59e9513e933c7023366`  
		Last Modified: Tue, 19 Dec 2023 02:23:53 GMT  
		Size: 49.5 MB (49548860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65baf0481eb7e4d5215eb36d70ba1c460bd80282806d1e361c83f4c442ed9adf`  
		Last Modified: Tue, 19 Dec 2023 03:18:48 GMT  
		Size: 23.6 MB (23630657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd3c3175afa4d6bd28886bc3fbd23dcc38227468b970b9dc18e6730d47f29cd0`  
		Last Modified: Tue, 19 Dec 2023 03:19:43 GMT  
		Size: 63.0 MB (62963274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d627909a3ff9de03889850fa5e83ecd71d896b3c313a14fb5c6e9915cc9b62e6`  
		Last Modified: Tue, 19 Dec 2023 03:21:51 GMT  
		Size: 189.7 MB (189684223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f653456796c3e032d564413d1e37bb41f2279454ac697cced7b531f14550c45c`  
		Last Modified: Mon, 01 Jan 2024 21:22:46 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5721e8e190810f9da978cbe0398aafc3e637b8981d7e375b21a1c5c65b474d1`  
		Last Modified: Mon, 01 Jan 2024 23:04:45 GMT  
		Size: 14.9 MB (14902969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1639fb214f7b7c27055ed23bdc36510b37d96b04366ed0452a3cbe179ef2521`  
		Last Modified: Mon, 01 Jan 2024 23:04:43 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:5-threaded-bookworm` - unknown; unknown

```console
$ docker pull perl@sha256:07712262ae5ebd673bedf57f157d156b82ca83a7a5db8d685f50ecb95fa557c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.2 KB (17206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0ddf271e04053f0468ac553678c2cbed3447127f0bafdad83e409362885371f`

```dockerfile
```

-	Layers:
	-	`sha256:08a3943b3f0acb58b8d771b4c4ce4a75308d842052150fde18482de97b74c605`  
		Last Modified: Mon, 01 Jan 2024 23:04:43 GMT  
		Size: 17.2 KB (17206 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:5-threaded-bookworm` - linux; ppc64le

```console
$ docker pull perl@sha256:8270c31c750950cd6d30ea9904cfe7181aaefb6532f06274d8f97e2be9a744aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **378.7 MB (378701257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae9336f5dc0bcd4ba03eb267c3fda0b6431bac6389244a3dbbafa81d2eac3df8`
-	Default Command: `["perl5.38.2","-de0"]`

```dockerfile
# Tue, 19 Dec 2023 01:21:31 GMT
ADD file:1728d055717ccd4f036c355a84deb6451942dd6e2c7998ee9d9d4edb3c02f7f4 in / 
# Tue, 19 Dec 2023 01:21:34 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 11:43:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 11:44:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 11:50:16 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Sun, 31 Dec 2023 10:01:19 GMT
WORKDIR /usr/src/perl
# Sun, 31 Dec 2023 10:01:19 GMT
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/P/PE/PEVANS/perl-5.38.2.tar.gz -o perl-5.38.2.tar.gz     && echo 'a0a31534451eb7b83c7d6594a497543a54d488bc90ca00f5e34762577f40655e *perl-5.38.2.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.38.2.tar.gz -C /usr/src/perl     && rm perl-5.38.2.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997014/cpm -o /usr/local/bin/cpm     && echo 'ee525f2493e36c6f688eddabaf53a51c4d3b2a4ebaa81576ac8b9f78ab57f4a1 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Sun, 31 Dec 2023 10:01:19 GMT
WORKDIR /usr/src/app
# Sun, 31 Dec 2023 10:01:19 GMT
CMD ["perl5.38.2" "-de0"]
```

-	Layers:
	-	`sha256:b5382b02d02e48b7676d14a370941b889916302c0c0a4ce6eed6a87ddd65e5a3`  
		Last Modified: Tue, 19 Dec 2023 01:25:50 GMT  
		Size: 53.6 MB (53557744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53bef292d6dca0f2e01dadfb6697f50846fd2abe37345bd28c4b40d155bd3efb`  
		Last Modified: Tue, 19 Dec 2023 12:22:47 GMT  
		Size: 25.7 MB (25696155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:397f3d69bf2380c69602528735990cbdbea6905ab14ff27daaf1ccd8e0599ad3`  
		Last Modified: Tue, 19 Dec 2023 12:23:09 GMT  
		Size: 69.6 MB (69582346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb645d1c095a31790b781022ac255437ab2c1a39357d5785bef239f25436d0d0`  
		Last Modified: Tue, 19 Dec 2023 12:23:51 GMT  
		Size: 214.1 MB (214135090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a107e404797090f23f9a06cad030167ab4a78bcdf8174e8ca6f5708f4225823c`  
		Last Modified: Wed, 20 Dec 2023 21:32:16 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64a42e034389b1ca487aeaa8be1d47892fb7e8055c84c653eb5258cb22e5f7c4`  
		Last Modified: Mon, 01 Jan 2024 21:45:16 GMT  
		Size: 15.7 MB (15729654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7404d87eed4e6682f3c3dffc7f03ccfc3e806262513b20673c12e94ceb16068d`  
		Last Modified: Mon, 01 Jan 2024 21:45:15 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:5-threaded-bookworm` - unknown; unknown

```console
$ docker pull perl@sha256:97450c36108eae572ac4cb00138bc7bce8bb342928a5e0508cbc996bfaf5ad2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.4 MB (13402110 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d281909540a77d02c3a0410db2767db1bdc34d9969dc2853118075faf9cc7f20`

```dockerfile
```

-	Layers:
	-	`sha256:84ebdcd733a3cf5a0bd5d931f9ecfe59f9e2027453338093ae32819f815383fb`  
		Last Modified: Mon, 01 Jan 2024 21:45:16 GMT  
		Size: 13.4 MB (13384727 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bc17337f5e2519ee3b5f647cbd44724ce7ab6209dc5bc192bd4bb61b261119a2`  
		Last Modified: Mon, 01 Jan 2024 21:45:15 GMT  
		Size: 17.4 KB (17383 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:5-threaded-bookworm` - linux; s390x

```console
$ docker pull perl@sha256:30c6970b88bc0cf9ca3a368e778cb2c0af27e0151c21d1d93f702b074eed865b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **334.2 MB (334242776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e7e23b520bc01874aebec7b104f01c77c5e576bedeca17183a97954bd5723bd`
-	Default Command: `["perl5.38.2","-de0"]`

```dockerfile
# Tue, 19 Dec 2023 01:42:12 GMT
ADD file:5e36efc0891837fbd669c10cc5082f41b4ad22190feb2d516f4f0efd4890e772 in / 
# Tue, 19 Dec 2023 01:42:20 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 07:43:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 07:43:56 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 07:44:55 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Sun, 31 Dec 2023 10:01:19 GMT
WORKDIR /usr/src/perl
# Sun, 31 Dec 2023 10:01:19 GMT
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/P/PE/PEVANS/perl-5.38.2.tar.gz -o perl-5.38.2.tar.gz     && echo 'a0a31534451eb7b83c7d6594a497543a54d488bc90ca00f5e34762577f40655e *perl-5.38.2.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.38.2.tar.gz -C /usr/src/perl     && rm perl-5.38.2.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997014/cpm -o /usr/local/bin/cpm     && echo 'ee525f2493e36c6f688eddabaf53a51c4d3b2a4ebaa81576ac8b9f78ab57f4a1 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Sun, 31 Dec 2023 10:01:19 GMT
WORKDIR /usr/src/app
# Sun, 31 Dec 2023 10:01:19 GMT
CMD ["perl5.38.2" "-de0"]
```

-	Layers:
	-	`sha256:9ba06e3db941501f326f297f1b24643ce2b142581fc9f396effcbc7c63df4938`  
		Last Modified: Tue, 19 Dec 2023 01:47:24 GMT  
		Size: 47.9 MB (47917679 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e564b911d9e033f9a67fcf5b0ddaad82153cceb2c4f54b63054a3c41bee756a1`  
		Last Modified: Tue, 19 Dec 2023 07:53:32 GMT  
		Size: 24.0 MB (24042818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ea66ebaf962eb06e4d585525f721841b7431908eb06730bf77ec7484806f571`  
		Last Modified: Tue, 19 Dec 2023 07:53:47 GMT  
		Size: 63.1 MB (63127874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01b9f68d79b5fc3c0f18f46ec4248ca8b98056a74979f1bae5166066dd9f500c`  
		Last Modified: Tue, 19 Dec 2023 07:54:16 GMT  
		Size: 183.1 MB (183128239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d1bf3c27b6914285692e056c03df5a1d9ddfa0685529fe661761fb1d8da51f3`  
		Last Modified: Wed, 20 Dec 2023 21:37:45 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:639f363c40d46954f9ad163b759fe81abb27f09f38ad8ddb87fb6d2c03699922`  
		Last Modified: Mon, 01 Jan 2024 21:50:59 GMT  
		Size: 16.0 MB (16025897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a35ec0829647b74752a8ef5be2d38e0038aca0ac900f42aabd581c26887bd3f`  
		Last Modified: Mon, 01 Jan 2024 21:50:59 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:5-threaded-bookworm` - unknown; unknown

```console
$ docker pull perl@sha256:fc528c0e68b7d702fb5458b5ba4e8205127a83eef2c3ac850c5424f9f66b28ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.3 MB (13256741 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc083670dff32be197c13cc9b2709c9317c602be467db080ebf55e754486152c`

```dockerfile
```

-	Layers:
	-	`sha256:e89fc426450f9e06404eb7846b0edecbcb7bd66d973f067ae1e6448d54f18113`  
		Last Modified: Mon, 01 Jan 2024 21:50:59 GMT  
		Size: 13.2 MB (13239431 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dc9cfb749c86a8fb11e3069721435f1c9b6a5c324c3adf38ecd2a8f83202e37b`  
		Last Modified: Mon, 01 Jan 2024 21:50:59 GMT  
		Size: 17.3 KB (17310 bytes)  
		MIME: application/vnd.in-toto+json
