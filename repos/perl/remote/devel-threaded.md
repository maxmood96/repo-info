## `perl:devel-threaded`

```console
$ docker pull perl@sha256:08510e909e4896a1714871d72bb405b5e2e925af685f65c9693ca81f009ece9b
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

### `perl:devel-threaded` - linux; amd64

```console
$ docker pull perl@sha256:9c34d50e3d40dc81875d5e58c3702cd38840cf87757952fb728acdfe3342d47a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **364.8 MB (364764841 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0bb0afd6fae87b26f14ec6b46e9cda2db92a36efe5ea226598f036401e0685a`
-	Default Command: `["perl5.39.6","-de0"]`

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
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/B/BO/BOOK/perl-5.39.6.tar.gz -o perl-5.39.6.tar.gz     && echo 'cb8715636bc744cca6e8864b6daa16f388d16ca3a134df6e6f35bbbe39dd7f63 *perl-5.39.6.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.39.6.tar.gz -C /usr/src/perl     && rm perl-5.39.6.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997014/cpm -o /usr/local/bin/cpm     && echo 'ee525f2493e36c6f688eddabaf53a51c4d3b2a4ebaa81576ac8b9f78ab57f4a1 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
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
	-	`sha256:8d55d1cb1ffb0c7e0438b372a96cc0f23a76c21571fa3e7b7b38e3fbc66a8c3a`  
		Last Modified: Thu, 11 Jan 2024 04:44:54 GMT  
		Size: 64.1 MB (64139713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa8e0026efede8b3da7364fd0ec879657b2c9be209b5cc1e2ec83bed6dfcf6a9`  
		Last Modified: Thu, 11 Jan 2024 04:45:29 GMT  
		Size: 211.1 MB (211103479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6faa5828c73025ed2ba43e387404f5185ac8a2e739c04b73f1c45e6b3bfc74ff`  
		Last Modified: Fri, 12 Jan 2024 00:31:57 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9d21aa8025cd342acc6e8a81ff973ac35349d077db7018c55e4ff43006dfe10`  
		Last Modified: Fri, 12 Jan 2024 00:31:58 GMT  
		Size: 15.9 MB (15913400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d5a150ff2f1bf5e862b209c10ca64ed1b087f4817ac3b15d0545342b292edea`  
		Last Modified: Fri, 12 Jan 2024 00:31:57 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-threaded` - unknown; unknown

```console
$ docker pull perl@sha256:a03226a06c0c9ab5b6c00c0adae2ab06ba37f4a13022d6482a8bea64392b04d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.4 MB (13418888 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c9a3748e5328a859bce75e565ae77f52f34dce22420916901bf735f0bb5590f`

```dockerfile
```

-	Layers:
	-	`sha256:5c9828a78b61a5ce4e489b840fde32d4ae8e7281de983a5d3f1ba3d334f86c8c`  
		Last Modified: Fri, 12 Jan 2024 00:31:58 GMT  
		Size: 13.4 MB (13402091 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2e5d1eedf46d57927bb3c4f91a30379ea8aff1767a358bf580113532da16749f`  
		Last Modified: Fri, 12 Jan 2024 00:31:57 GMT  
		Size: 16.8 KB (16797 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-threaded` - linux; arm variant v5

```console
$ docker pull perl@sha256:a03d0691413690d0844c872be2bcb6317244443c46eb28622ae54cf36ff25f9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **331.1 MB (331129111 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5682a5d43c21197ecb0c62847a45ebe09d3ce2792d13f0c6cef3e93511f365dd`
-	Default Command: `["perl5.39.6","-de0"]`

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
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/B/BO/BOOK/perl-5.39.6.tar.gz -o perl-5.39.6.tar.gz     && echo 'cb8715636bc744cca6e8864b6daa16f388d16ca3a134df6e6f35bbbe39dd7f63 *perl-5.39.6.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.39.6.tar.gz -C /usr/src/perl     && rm perl-5.39.6.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997014/cpm -o /usr/local/bin/cpm     && echo 'ee525f2493e36c6f688eddabaf53a51c4d3b2a4ebaa81576ac8b9f78ab57f4a1 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Sun, 31 Dec 2023 10:01:19 GMT
WORKDIR /usr/src/app
# Sun, 31 Dec 2023 10:01:19 GMT
CMD ["perl5.39.6" "-de0"]
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
	-	`sha256:ff2d50bd2d72558cfe433b746275bb9744fdb947d8a6b0a226107e813b4ec362`  
		Last Modified: Tue, 02 Jan 2024 02:21:52 GMT  
		Size: 15.2 MB (15159171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0de82e85f9ef3aee0685d01aa46f4d631d83e214b3455c3b328e2b14c81e7b0c`  
		Last Modified: Tue, 02 Jan 2024 02:21:51 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-threaded` - unknown; unknown

```console
$ docker pull perl@sha256:f5eeaaf996b3f27e22cc4b9c155790ba4ac5e228e1d154d6a6370ab6545d0851
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.2 MB (13243493 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3fe792867dff25ff97a6b476c781ee3a56511a11210ab7fcd71cd8925d5312e`

```dockerfile
```

-	Layers:
	-	`sha256:a430dbb5c6a95e01a0f531b85a95505e4004dec216d04bfd831b4947b2d2081f`  
		Last Modified: Tue, 02 Jan 2024 02:21:52 GMT  
		Size: 13.2 MB (13227273 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c7797edc4f6dafa653df8dde5f2299dbd19581fe27429cc457839b53f5acbbc9`  
		Last Modified: Tue, 02 Jan 2024 02:21:51 GMT  
		Size: 16.2 KB (16220 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-threaded` - linux; arm variant v7

```console
$ docker pull perl@sha256:cf3bbf90a048dbb113ca0e6314d2f8aeeb068185ba56de134f8ed32ead87eb5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **316.3 MB (316334225 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fdf1d7f069be9a07168d69ef8d5ada5dec3cf67eb898c8468ae9ef2c54101bb5`
-	Default Command: `["perl5.39.6","-de0"]`

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
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/B/BO/BOOK/perl-5.39.6.tar.gz -o perl-5.39.6.tar.gz     && echo 'cb8715636bc744cca6e8864b6daa16f388d16ca3a134df6e6f35bbbe39dd7f63 *perl-5.39.6.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.39.6.tar.gz -C /usr/src/perl     && rm perl-5.39.6.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997014/cpm -o /usr/local/bin/cpm     && echo 'ee525f2493e36c6f688eddabaf53a51c4d3b2a4ebaa81576ac8b9f78ab57f4a1 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Sun, 31 Dec 2023 10:01:19 GMT
WORKDIR /usr/src/app
# Sun, 31 Dec 2023 10:01:19 GMT
CMD ["perl5.39.6" "-de0"]
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
	-	`sha256:a5c7e92f27aed4fbf83752563858f34d8b088fa1c39fbefb3e0f73aca56223f4`  
		Last Modified: Tue, 02 Jan 2024 06:35:29 GMT  
		Size: 14.9 MB (14933218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70605d3d747fe6d41b85b63f6ae449488115165a676864dac4e16c0fe0dc874f`  
		Last Modified: Tue, 02 Jan 2024 06:35:28 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-threaded` - unknown; unknown

```console
$ docker pull perl@sha256:3474545c180eaaaa892e075fa4de0c362c5dca223785ad02711c63292c8bc36c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.2 MB (13248966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9a4f178b3509661c7d99c08bc68a85f56ba1e62f577a9442b38c74327da19ab`

```dockerfile
```

-	Layers:
	-	`sha256:0766a16117ef0b5ffb4e11f2d28ed6828b0bd3e72c6a88dfdad4bbcd2cda9e63`  
		Last Modified: Tue, 02 Jan 2024 06:35:29 GMT  
		Size: 13.2 MB (13232747 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b547454cdc23c40f5f1b292dc6cbb13d4f3763984c0a39025e9685b45b594a2b`  
		Last Modified: Tue, 02 Jan 2024 06:35:28 GMT  
		Size: 16.2 KB (16219 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-threaded` - linux; arm64 variant v8

```console
$ docker pull perl@sha256:61d0dd80ad71c648dbcbf08925864024ca8a5dcfd61fad8a804f0be3ed0bed13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **355.5 MB (355526945 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ed335a2e36ae982a01561a9441f78976bbe022fdaa3ae7e607b8fd3f4af8eb1`
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
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/B/BO/BOOK/perl-5.39.6.tar.gz -o perl-5.39.6.tar.gz     && echo 'cb8715636bc744cca6e8864b6daa16f388d16ca3a134df6e6f35bbbe39dd7f63 *perl-5.39.6.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.39.6.tar.gz -C /usr/src/perl     && rm perl-5.39.6.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997014/cpm -o /usr/local/bin/cpm     && echo 'ee525f2493e36c6f688eddabaf53a51c4d3b2a4ebaa81576ac8b9f78ab57f4a1 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
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
	-	`sha256:c79343d4bf3b2fb0f5aa25fe8b5ff4363aeaa14b3f1fee622fa5976558a834df`  
		Last Modified: Fri, 12 Jan 2024 15:43:56 GMT  
		Size: 15.9 MB (15859696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68f30c40933f7d96e185cb1899c29743f146cb840888e044911c37c8f19f7975`  
		Last Modified: Fri, 12 Jan 2024 15:43:55 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-threaded` - unknown; unknown

```console
$ docker pull perl@sha256:cc36833e028ce40c06fcba4ec62ff0382bc91d9332c9c052de5659fe23fa0988
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.4 MB (13443468 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31dc24767fe4e3d66a5433ab9085b892c222794885cb726e5388512ec87854fb`

```dockerfile
```

-	Layers:
	-	`sha256:5c94829dfa6520c2bb25b23cf814af3f94eeb2d884dd95da7811ab4b28cfea08`  
		Last Modified: Fri, 12 Jan 2024 15:43:55 GMT  
		Size: 13.4 MB (13427320 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6d8ec00d06efd76fedd79f94102310aaee5b223dabeaf7fb4f7ba0a2d51d0c22`  
		Last Modified: Fri, 12 Jan 2024 15:43:54 GMT  
		Size: 16.1 KB (16148 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-threaded` - linux; 386

```console
$ docker pull perl@sha256:c438ed52a7e8b497de3d39cfa3d8420a0c6a47fcf4613d43aca66bccc398e6ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **367.0 MB (366953010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a599956edf3a18283dc3c0e58ce061cc6c86c1e0f98b0508f7d778065c00872`
-	Default Command: `["perl5.39.6","-de0"]`

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
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/B/BO/BOOK/perl-5.39.6.tar.gz -o perl-5.39.6.tar.gz     && echo 'cb8715636bc744cca6e8864b6daa16f388d16ca3a134df6e6f35bbbe39dd7f63 *perl-5.39.6.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.39.6.tar.gz -C /usr/src/perl     && rm perl-5.39.6.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997014/cpm -o /usr/local/bin/cpm     && echo 'ee525f2493e36c6f688eddabaf53a51c4d3b2a4ebaa81576ac8b9f78ab57f4a1 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
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
	-	`sha256:5c54028869f774208be77fae1c160385eebefa5743b2d687462a195a10b5ec1b`  
		Last Modified: Thu, 11 Jan 2024 04:41:57 GMT  
		Size: 66.0 MB (65986939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5000f105af4698bd73d613c19498edc90b389261f540f976f31cc1a4f345526f`  
		Last Modified: Thu, 11 Jan 2024 04:42:52 GMT  
		Size: 210.0 MB (210036478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ad4700c45bc61893971e1814d0da689150c442b545098e6944486955e913c1b`  
		Last Modified: Fri, 12 Jan 2024 00:32:48 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c03289ee20771e32f568dff2ae10ba19cc1e21dc576a270fa68ae8a110816e2e`  
		Last Modified: Fri, 12 Jan 2024 00:32:49 GMT  
		Size: 15.5 MB (15463042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0f409ef3a2e3d077733bfd36c34858d91ab6b5848ea6da5ff44019bfe71790d`  
		Last Modified: Fri, 12 Jan 2024 00:32:48 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-threaded` - unknown; unknown

```console
$ docker pull perl@sha256:6a4ea57f00dcb2e7b5f18d1ccc17bd6fc74ed73cc606bf80bab57b58f2d7c9fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.4 MB (13399273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7f1bdeeadce19369d19f8d244388a960486dcf7f54054f544e532aeb08d2773`

```dockerfile
```

-	Layers:
	-	`sha256:f1f6f6f3fbb39f66500dae7897efe1db5179e928f6dd7c581454543979eb214b`  
		Last Modified: Fri, 12 Jan 2024 00:32:48 GMT  
		Size: 13.4 MB (13382515 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1df0be6c77dee77ecf775ede51edb8e3d4716ef866e704da1a93995dd8b71c08`  
		Last Modified: Fri, 12 Jan 2024 00:32:48 GMT  
		Size: 16.8 KB (16758 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-threaded` - linux; mips64le

```console
$ docker pull perl@sha256:826f269714c76c3b66ae4d97dd9d8eb33733d7b5fcce8087921d823ee1270df3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **341.0 MB (340971113 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ca1ed2cd805c8a9b63dd42d5b70819fbbf073da81deadd582e0d8ca46517212`
-	Default Command: `["perl5.39.6","-de0"]`

```dockerfile
# Sun, 31 Dec 2023 10:01:19 GMT
ADD file:e632734e8c2b1e7594b8a79fefe3b2790d6e662e647019a7daa2713f4b1aa7be in / 
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
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/B/BO/BOOK/perl-5.39.6.tar.gz -o perl-5.39.6.tar.gz     && echo 'cb8715636bc744cca6e8864b6daa16f388d16ca3a134df6e6f35bbbe39dd7f63 *perl-5.39.6.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.39.6.tar.gz -C /usr/src/perl     && rm perl-5.39.6.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997014/cpm -o /usr/local/bin/cpm     && echo 'ee525f2493e36c6f688eddabaf53a51c4d3b2a4ebaa81576ac8b9f78ab57f4a1 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
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
	-	`sha256:ec9fe3d753531dacf4e8585a7a9b9201236938acff15c0cbbcc1dac8d260ba5d`  
		Last Modified: Thu, 11 Jan 2024 03:25:09 GMT  
		Size: 63.0 MB (62965807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b493a406f39a1f0332e388a3aa3550325dde35f0ec7faa0550d92515456cec42`  
		Last Modified: Thu, 11 Jan 2024 03:27:18 GMT  
		Size: 189.7 MB (189696507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6176861c86b31b6a472b0c8e8cdfdfbce980713e2adac9907fbcbc50800377a`  
		Last Modified: Fri, 12 Jan 2024 05:01:59 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:625d22aaaa5fe75b226ce8282edeb12697e019baca616b55828fa9c1a736cecd`  
		Last Modified: Fri, 12 Jan 2024 16:05:37 GMT  
		Size: 15.1 MB (15129438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17cb2199d7b7a6cf4930a1ded39a3678b1427ae2b1dbd3e7e77e91a730b973af`  
		Last Modified: Fri, 12 Jan 2024 16:05:36 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-threaded` - unknown; unknown

```console
$ docker pull perl@sha256:42d8d0046f690da2b06d4d973f0e7a332103fe07c2457eb9f3daf1c9ac31407b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.0 KB (15994 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd5f7cf512e5e975a5b84e27fddfe021d54f55e5ae130c03efd20965e3364026`

```dockerfile
```

-	Layers:
	-	`sha256:09ba7bb9428e547d242db8ae995a8356f149a25261dba694dc304e07cbc5ac8e`  
		Last Modified: Fri, 12 Jan 2024 16:05:35 GMT  
		Size: 16.0 KB (15994 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-threaded` - linux; ppc64le

```console
$ docker pull perl@sha256:46f4cd822833b677332ff9f37cf006be1edc5c519fdd55154e38e123353471df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **378.9 MB (378924595 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b55ea1fe8b5d5a0dd53b5e2c34355cd942d31675cb55e2b5ae9622a6b6ac24d4`
-	Default Command: `["perl5.39.6","-de0"]`

```dockerfile
# Sun, 31 Dec 2023 10:01:19 GMT
ADD file:181ff897280683d4e2f512551aa99c5bca9823305859ed4620c8ea3bd4d95cd5 in / 
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
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/B/BO/BOOK/perl-5.39.6.tar.gz -o perl-5.39.6.tar.gz     && echo 'cb8715636bc744cca6e8864b6daa16f388d16ca3a134df6e6f35bbbe39dd7f63 *perl-5.39.6.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.39.6.tar.gz -C /usr/src/perl     && rm perl-5.39.6.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997014/cpm -o /usr/local/bin/cpm     && echo 'ee525f2493e36c6f688eddabaf53a51c4d3b2a4ebaa81576ac8b9f78ab57f4a1 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
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
	-	`sha256:d7111430dcc903e7bfff6d90c34c09c7269ae6d852479c032f3e738a4d2f8d19`  
		Last Modified: Thu, 11 Jan 2024 07:23:38 GMT  
		Size: 69.6 MB (69581348 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81a36685a0b4a75b89c0305b54821a88557fb6728e1de0ca5cb2b71f68c0a742`  
		Last Modified: Thu, 11 Jan 2024 07:24:20 GMT  
		Size: 214.1 MB (214137303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3b83a120fd64f10fa7c51c2ed129f7df674a71af6f86517e78867cc6faf7d6d`  
		Last Modified: Fri, 12 Jan 2024 09:43:28 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:179f91267aab199dcffacb067c26803382a93133a435029c6853e8f35a946bca`  
		Last Modified: Fri, 12 Jan 2024 13:29:19 GMT  
		Size: 16.0 MB (15951758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d076a4a779500f99b77b7c7eb793649ea38d54ca1df4bff244c537aa92e1fe8`  
		Last Modified: Fri, 12 Jan 2024 13:29:18 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-threaded` - unknown; unknown

```console
$ docker pull perl@sha256:e813fc30da3a35b6cbef250bc5eaeab59c6f8401a30bf66112d502c09976aec3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.4 MB (13399647 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bb4871f292a7b0edfa6f84fda19aa97a239d538f3b9abd2bdb746aa73ae7158`

```dockerfile
```

-	Layers:
	-	`sha256:3139c569ed6d29e7850545391a5c726b82e0996cd68ed481c36fb9b693851084`  
		Last Modified: Fri, 12 Jan 2024 13:29:19 GMT  
		Size: 13.4 MB (13383463 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1fe431c9b4a3e92c1297c998e2575ea49d01484cf7a5b9cd34edd4cf132195e3`  
		Last Modified: Fri, 12 Jan 2024 13:29:18 GMT  
		Size: 16.2 KB (16184 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-threaded` - linux; s390x

```console
$ docker pull perl@sha256:4a17171548acabc6023e5f936b35dd49dd95421ddb3887d8260c537f0e2b5f01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **334.5 MB (334475513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58f265725981e78a0e2addd54bf598a45660da8635ba3fd4d76bcb4f82fefdf4`
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
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/B/BO/BOOK/perl-5.39.6.tar.gz -o perl-5.39.6.tar.gz     && echo 'cb8715636bc744cca6e8864b6daa16f388d16ca3a134df6e6f35bbbe39dd7f63 *perl-5.39.6.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.39.6.tar.gz -C /usr/src/perl     && rm perl-5.39.6.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997014/cpm -o /usr/local/bin/cpm     && echo 'ee525f2493e36c6f688eddabaf53a51c4d3b2a4ebaa81576ac8b9f78ab57f4a1 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
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
	-	`sha256:68fb5e5700a2871eb6660a30183799ab101364edef79446ea26d3dd08ae23c07`  
		Last Modified: Fri, 12 Jan 2024 13:54:19 GMT  
		Size: 16.2 MB (16243962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6f16152e0c76433998af9ec77f8d18196d1da9e8e60191cc3398b7a843d36d0`  
		Last Modified: Fri, 12 Jan 2024 13:54:19 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-threaded` - unknown; unknown

```console
$ docker pull perl@sha256:648eee9c23400e17f436fcdf72132b7c7070694905b67c5a0ce384053b503234
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.3 MB (13254325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:452baf3adf6e00463814d1c5f747ad47ded59ebe5cb31fb671b39a0035bacf42`

```dockerfile
```

-	Layers:
	-	`sha256:14dcec5b8c065368d67af0dabd22264dc0ae22a885cee3f61540b0e27c6b5fb2`  
		Last Modified: Fri, 12 Jan 2024 13:54:19 GMT  
		Size: 13.2 MB (13238191 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:46ddbf0036edd975ca056ec44d03f4c37be84c35792f2c8e45f6f914411c028c`  
		Last Modified: Fri, 12 Jan 2024 13:54:19 GMT  
		Size: 16.1 KB (16134 bytes)  
		MIME: application/vnd.in-toto+json
