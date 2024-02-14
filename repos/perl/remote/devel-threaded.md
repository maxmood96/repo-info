## `perl:devel-threaded`

```console
$ docker pull perl@sha256:8851692ba057f175dbffaddefb1465c041c723c55a228d88b282e69eca1b6db1
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
$ docker pull perl@sha256:e04732b315d5ce3862358963dae1d3f5be87bc1adf8c354adf28235ee91db7b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **364.8 MB (364785905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64fdd7bfc55251673c648160062a34e3757fdddaf04bfb4ff103338863dba09e`
-	Default Command: `["perl5.39.7","-de0"]`

```dockerfile
# Sat, 20 Jan 2024 20:51:34 GMT
ADD file:333b899a197a48b3333115a3b59efed559494808873943f606a9bc2b6e242c49 in / 
# Sat, 20 Jan 2024 20:51:34 GMT
CMD ["bash"]
# Sat, 20 Jan 2024 20:51:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
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
	-	`sha256:7bb465c2914923b08ae03b7fc67b92a1ef9b09c4c1eb9d6711b22ee6bbb46a00`  
		Last Modified: Tue, 13 Feb 2024 00:41:39 GMT  
		Size: 49.6 MB (49552605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b9b41aaa3c52ab268b47da303015b94ced04a1eb02e58860e58b283404974f4`  
		Last Modified: Tue, 13 Feb 2024 01:30:39 GMT  
		Size: 24.0 MB (24046577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49b40be4436eff6fe463f6977159dc727df37cabe65ade75c75c1caa3cb0a234`  
		Last Modified: Tue, 13 Feb 2024 01:30:58 GMT  
		Size: 64.1 MB (64140328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c558fac597f8ecbb7a66712e14912ce1d83b23a92ca8b6ff14eef209ab01aff2`  
		Last Modified: Tue, 13 Feb 2024 01:31:35 GMT  
		Size: 211.1 MB (211120435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58d0f76cef60e92138a495e9ff58b28107e6204aba97a9deaec21019186456c5`  
		Last Modified: Tue, 13 Feb 2024 03:06:41 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c70bb5e869b95ef5c60fea0968d585b47491c012577c4527dfc94affb8d26e1`  
		Last Modified: Tue, 13 Feb 2024 03:06:55 GMT  
		Size: 15.9 MB (15925697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:435995a712a7465ad7e44fe845700131bb5a14fda5058f00c37522f7bd0f46b1`  
		Last Modified: Tue, 13 Feb 2024 03:06:55 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-threaded` - unknown; unknown

```console
$ docker pull perl@sha256:e9a18bde464373989e7367fbb9485938323dea33f39f292787a64c3e2cdd2f37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.4 MB (13418950 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1542a305f1a2b007116bd54ed1a6e2f801f4deca4b44e232435c2539720b6827`

```dockerfile
```

-	Layers:
	-	`sha256:21c2ad9e1ea6655f67f9a2c30b07cb61c63e12d2f28e86e75fc8e49780388c3f`  
		Last Modified: Tue, 13 Feb 2024 03:06:55 GMT  
		Size: 13.4 MB (13402147 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e22ebf19a5fce1480dec348ae9f40cf20a92d9fb7690c9c87e95c54d2f4dc882`  
		Last Modified: Tue, 13 Feb 2024 03:06:55 GMT  
		Size: 16.8 KB (16803 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-threaded` - linux; arm variant v5

```console
$ docker pull perl@sha256:059e4de9c2f38b3ba58b476bd2fd3178d894d1a77dc7ebdd170a0d2c979878a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **331.2 MB (331186868 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc0828223cab573bec69c767512b8e48e755fd53993597a196003879b20cca64`
-	Default Command: `["perl5.39.7","-de0"]`

```dockerfile
# Sat, 20 Jan 2024 20:51:34 GMT
ADD file:32a9c7aaf2ccd1a1e30b6cad6aff8691eb3b1405483450a082bc84962be78652 in / 
# Sat, 20 Jan 2024 20:51:34 GMT
CMD ["bash"]
# Sat, 20 Jan 2024 20:51:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
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
	-	`sha256:96cfcfafa452979ace6d9825bfc1192c702df30f7cecf2ea7f7041de5d705416`  
		Last Modified: Tue, 13 Feb 2024 01:13:03 GMT  
		Size: 47.3 MB (47311769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6afa8b078d49474b25b523639beeefec0c79e8cadd718cc322dcb26c6311ed72`  
		Last Modified: Tue, 13 Feb 2024 01:53:42 GMT  
		Size: 22.7 MB (22724953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffe00269555fa07180f949e687ed0dcb155e1271595d70130de36c79b029d21e`  
		Last Modified: Tue, 13 Feb 2024 01:54:10 GMT  
		Size: 61.5 MB (61515806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f4f2c673dee7c01dead9d002b58f94f192dedcd8cb540af771a3e99076df2ae`  
		Last Modified: Tue, 13 Feb 2024 01:54:59 GMT  
		Size: 184.4 MB (184448080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12943da3ee160c194703143cc6ce40e31a520787c0dbc5ff396ec29da57d159c`  
		Last Modified: Wed, 14 Feb 2024 14:43:39 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8415ee3ee8b5dd9d80f11ac7abd8bfea430194df138dcc8f4f603cc6d475dfed`  
		Last Modified: Wed, 14 Feb 2024 18:36:49 GMT  
		Size: 15.2 MB (15185995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a385191817f5a54d19cbdb27986c9c38af8b91a60f715bd7ffcff9980995ef67`  
		Last Modified: Wed, 14 Feb 2024 18:36:48 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-threaded` - unknown; unknown

```console
$ docker pull perl@sha256:e18382dbdc9dcd6443572922c98646da9e1eaf8a5916f28e1b829d153aa72700
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.2 MB (13243555 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8687841ec84d0a56140572dc05190208aff016f606d8cb53ba30ccbb85fc7fca`

```dockerfile
```

-	Layers:
	-	`sha256:576976e6f0acdb33f9adffe32437f00fd5381f7c392f3ffbfeba420faf2430c8`  
		Last Modified: Wed, 14 Feb 2024 18:36:49 GMT  
		Size: 13.2 MB (13227329 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:70b314d1583a18496325d2e3d5d87094696333583a8162c461b640dc12ff99f8`  
		Last Modified: Wed, 14 Feb 2024 18:36:48 GMT  
		Size: 16.2 KB (16226 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-threaded` - linux; arm variant v7

```console
$ docker pull perl@sha256:88197a1526f6765dfa09677868393b0444f534489cd189b648d01de26868c7f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **316.4 MB (316402971 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9c98fe98c9e64ed6164a903639a536ee9d4f1dcbbf794e2cbcd059740da9a25`
-	Default Command: `["perl5.39.7","-de0"]`

```dockerfile
# Sat, 20 Jan 2024 20:51:34 GMT
ADD file:24186d75daba80fe802230517bbb6b4e9d6c695398d1db98108b4487d27ebb43 in / 
# Sat, 20 Jan 2024 20:51:34 GMT
CMD ["bash"]
# Sat, 20 Jan 2024 20:51:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
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
	-	`sha256:af02191d26cb0ab470ac42e81c677a72e87ee39e67a36576e102fffc8b1de4a7`  
		Last Modified: Wed, 31 Jan 2024 22:48:27 GMT  
		Size: 45.2 MB (45177992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f5dbfdb18fe3f9c4fd9d347eb380df7b3080c079f6bffef53d6d588fa3b49bf`  
		Last Modified: Thu, 01 Feb 2024 02:58:27 GMT  
		Size: 22.0 MB (21953682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2114ad3bcb8a20c51922836cabcbf31c1cc36bf285577a204f4dac5b756e1cc`  
		Last Modified: Thu, 01 Feb 2024 02:58:49 GMT  
		Size: 59.2 MB (59216669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d88bc19189eb4f1105881142f65d20f20c62599e816c26cb5fab6c266f89b80`  
		Last Modified: Thu, 01 Feb 2024 02:59:25 GMT  
		Size: 175.1 MB (175081910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aed9d64fb77e11b7c626d9032c20fa0c8d0f5b9faad0805bd6cd7e941a91846c`  
		Last Modified: Thu, 01 Feb 2024 20:58:54 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99898aff552634502ad7b878eafdfbb5ddd833944b163b697c86dcfca15ca407`  
		Last Modified: Thu, 01 Feb 2024 23:15:22 GMT  
		Size: 15.0 MB (14972453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29335c50b521a9f8ad21269b8e6caf04e5a110a22aaaa675292a13d9ccfd4b5a`  
		Last Modified: Thu, 01 Feb 2024 23:15:20 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-threaded` - unknown; unknown

```console
$ docker pull perl@sha256:53979e5a9d0c7d498de1344abec4ee07cd58642bb4a36c63cc69081c6c0b0261
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.2 MB (13248973 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa96a246bb6b388101919df17ab0a54d62dc31f1a43038028f0be1646105cad2`

```dockerfile
```

-	Layers:
	-	`sha256:2c0377b03a6132b34e36ea6243c34e8d111221a721399a614f1f032b51068dae`  
		Last Modified: Thu, 01 Feb 2024 23:15:21 GMT  
		Size: 13.2 MB (13232747 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4f7a5c2ffa87a9bf5bf956493fca4a7e871079ec54d14197b1c8f152c8114c5c`  
		Last Modified: Thu, 01 Feb 2024 23:15:20 GMT  
		Size: 16.2 KB (16226 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-threaded` - linux; arm64 variant v8

```console
$ docker pull perl@sha256:7c44196ce0cb99f72a08183726c5bfb79a34b594822146d5bb765b40e0cbbdd8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **355.6 MB (355553723 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b5084d33512d7e220f894cdd168875c6295560115c64dc720020ba71beb3125`
-	Default Command: `["perl5.39.7","-de0"]`

```dockerfile
# Sat, 20 Jan 2024 20:51:34 GMT
ADD file:73b36e8089732e9bb253d9a9db76cc1cf5c430bd49647849b77924cd5fdaf8ae in / 
# Sat, 20 Jan 2024 20:51:34 GMT
CMD ["bash"]
# Sat, 20 Jan 2024 20:51:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
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
	-	`sha256:c2964e85ea54bbef26d274e85fa0a3fde68f074e0774d0729e6ebe341e24eee1`  
		Last Modified: Tue, 13 Feb 2024 00:44:29 GMT  
		Size: 49.6 MB (49590965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3436c315a5dcd9b17acc96236fdf378dcf2deb72fe9dafb42d894a3c362ac75`  
		Last Modified: Tue, 13 Feb 2024 01:46:27 GMT  
		Size: 23.6 MB (23582766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:603ae72c83b17aae41ce6857f0063bfd35b5f00dc5d7e1ad47fa18debb28b2c7`  
		Last Modified: Tue, 13 Feb 2024 01:46:49 GMT  
		Size: 64.0 MB (63990920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcabfc6c415bdafce0fb78b78afe51a8be789b05c4c3f5ccf5f1046bb5d32776`  
		Last Modified: Tue, 13 Feb 2024 01:47:24 GMT  
		Size: 202.5 MB (202519692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ed5b3a97590258739513ce09b05522a7ef85d4bb25db4f546682d388618a5cf`  
		Last Modified: Wed, 14 Feb 2024 01:30:38 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba18f3135b317b61479299e9e332c929e54ce2971f651a43a9437db1b4ce2c8a`  
		Last Modified: Wed, 14 Feb 2024 07:02:45 GMT  
		Size: 15.9 MB (15869115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b113627f75d01267e7b318914c9e6bef02e644cd84c2695697cbcebd0683735f`  
		Last Modified: Wed, 14 Feb 2024 07:02:44 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-threaded` - unknown; unknown

```console
$ docker pull perl@sha256:c00fd4f5a055ff5f563403313aebca4db0d2f252c1aab6d15bfe7adbcab05a42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.4 MB (13443530 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e44b152983b316ea961e26c8867fc9b87fe1befc17253680bc2a83bb98b6321`

```dockerfile
```

-	Layers:
	-	`sha256:8af1faafe38e635b8d6b0f274dba0bbd801102941e44b9821e0f1847b34a2530`  
		Last Modified: Wed, 14 Feb 2024 07:02:45 GMT  
		Size: 13.4 MB (13427376 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1816da0e37b17d3c8903780e4c67db5f50b06ce74c4604c5872b61d9ed70a600`  
		Last Modified: Wed, 14 Feb 2024 07:02:44 GMT  
		Size: 16.2 KB (16154 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-threaded` - linux; 386

```console
$ docker pull perl@sha256:e479e5932ae8c4cf8a6d81efc547f432b1d5e2c8e5356cc5a5a28d8945bf0a05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **367.0 MB (366972021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ace71fe9c784ec7cc287246cd77d513869152146d949d49fe9f1c0eb7ac15605`
-	Default Command: `["perl5.39.7","-de0"]`

```dockerfile
# Sat, 20 Jan 2024 20:51:34 GMT
ADD file:e12b4798eb856f517a57dfe550811e57903589ffa74a09d47f7c0261e23ca645 in / 
# Sat, 20 Jan 2024 20:51:34 GMT
CMD ["bash"]
# Sat, 20 Jan 2024 20:51:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
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
	-	`sha256:911275c2fc723590176bf48d32222d2b1299cd1a17294bdc4cebd96e25742b27`  
		Last Modified: Tue, 13 Feb 2024 00:43:21 GMT  
		Size: 50.6 MB (50581925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a04ecbcf46d4507b6a8970b941f809a05d49cd1ac9402f7495e0cfbeac9fd1c9`  
		Last Modified: Tue, 13 Feb 2024 01:29:22 GMT  
		Size: 24.9 MB (24884414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84d2a319089434096accd3face0ee4bb9f2e02eb5571f7d983c3c48579df902f`  
		Last Modified: Tue, 13 Feb 2024 01:29:47 GMT  
		Size: 66.0 MB (65986836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa04ac89e98e423a77743b83b547bbfed238c3f5c7c341959541005af241df49`  
		Last Modified: Tue, 13 Feb 2024 01:30:38 GMT  
		Size: 210.0 MB (210046749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cfd008d65f669214a96c39b28fe5196643d6c8068da323bc26bddc6579ee5a0`  
		Last Modified: Tue, 13 Feb 2024 03:08:42 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:770d25605f48453bd473053d12e0849815d4581654f54905e42279208a7130b6`  
		Last Modified: Tue, 13 Feb 2024 03:08:42 GMT  
		Size: 15.5 MB (15471834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b49662a4bc0ddac2e2ba3540bea587006a2c6529a35dae8e1a2ee317e339eec9`  
		Last Modified: Tue, 13 Feb 2024 03:08:42 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-threaded` - unknown; unknown

```console
$ docker pull perl@sha256:b24fb4159367b25df09e252fb1c3b86b82c1bc38f9ae18399f408ef555db6ab3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.4 MB (13399333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f2802039829b880a2fbbc6d7ebd79c70bb35bcf15afd2159d4e61114a1ce441`

```dockerfile
```

-	Layers:
	-	`sha256:b87836f4b28df3aed826056a40c1132c4e936818858d49543d094ec592fa51d1`  
		Last Modified: Tue, 13 Feb 2024 03:08:42 GMT  
		Size: 13.4 MB (13382571 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:253a131d0c637890e84761a068177a976246b492e2b3664e31b3c12177b8831f`  
		Last Modified: Tue, 13 Feb 2024 03:08:41 GMT  
		Size: 16.8 KB (16762 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-threaded` - linux; mips64le

```console
$ docker pull perl@sha256:7c6af3c858b14f191ca04cc3c960ee319f1338eea22e53c9e35b2c151399ed54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **341.0 MB (341014904 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8fcf16d38ee9e844ca24d0c1f908ee721dd7b18160b9df3fee6736fd3a36d74d`
-	Default Command: `["perl5.39.7","-de0"]`

```dockerfile
# Sat, 20 Jan 2024 20:51:34 GMT
ADD file:fb8895339019f207ef48174cf1263bc0d0c200e8ff5100bd033fa9f04719a0ab in / 
# Sat, 20 Jan 2024 20:51:34 GMT
CMD ["bash"]
# Sat, 20 Jan 2024 20:51:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
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
	-	`sha256:e79c0a3a7155a4df44e64f72b3886978fe62771937c5515432ff2dbd7eb44ae2`  
		Last Modified: Tue, 13 Feb 2024 02:14:26 GMT  
		Size: 49.6 MB (49563166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6c104a14c05b649f6cf44b231609cb7fd64237e83ca7b8eb07b2a5029fb7481`  
		Last Modified: Tue, 13 Feb 2024 04:20:33 GMT  
		Size: 23.6 MB (23630739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51b7aae7f397e2eb111826952978a14b68b4e05e905f004686ce9a46b279ffd8`  
		Last Modified: Tue, 13 Feb 2024 04:21:26 GMT  
		Size: 63.0 MB (62965953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44cedb7a3137759e51142758f8b7029dc78e57a3033813443144502d7ef4c020`  
		Last Modified: Tue, 13 Feb 2024 04:23:34 GMT  
		Size: 189.7 MB (189709673 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33b3e71460aab7560532c6c2653ddadcbe6f40d9565115a778794f3db242668f`  
		Last Modified: Wed, 14 Feb 2024 05:29:00 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:451f28da8533a8f0640eb58a4b6381ffb48ef80a7a958e4bbf7f8bcd182cf4d1`  
		Last Modified: Wed, 14 Feb 2024 16:14:18 GMT  
		Size: 15.1 MB (15145106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:637162aa3cfc7acc70217c241b4ceb94c92fa98eb2239e2ce1d5cd9617837e86`  
		Last Modified: Wed, 14 Feb 2024 16:14:16 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-threaded` - unknown; unknown

```console
$ docker pull perl@sha256:db58ddbe21811066d3ff29d2ef90f938cd35b20154627212aefbb131dbb6a0b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.0 KB (15998 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed47cc7c32b7397dd4173189e0c1c0ceabeea4998a764be8f131e0a1dc1850ae`

```dockerfile
```

-	Layers:
	-	`sha256:5d304c5651f05a515e7b09b5757338706370ec247a8bd0acf3f0dec0f1d9826d`  
		Last Modified: Wed, 14 Feb 2024 16:14:16 GMT  
		Size: 16.0 KB (15998 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-threaded` - linux; ppc64le

```console
$ docker pull perl@sha256:32e320a298423faa8ec44eb7436d711e0b60367e41edf576a31c67edd7f708df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **379.0 MB (378950612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:070e3547edd24f3cd3f5add566090c0883d1d37dca49c85434ebcddb4c8fe053`
-	Default Command: `["perl5.39.7","-de0"]`

```dockerfile
# Sat, 20 Jan 2024 20:51:34 GMT
ADD file:83b2c138b49e79b23d3462cb4b39f3f6f151b690a83c7b1ff169ae4590fa0b43 in / 
# Sat, 20 Jan 2024 20:51:34 GMT
CMD ["bash"]
# Sat, 20 Jan 2024 20:51:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
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
	-	`sha256:79696cca44e9751723104a8e361568bddd373ed772da9f88250ba2947fbc6043`  
		Last Modified: Tue, 13 Feb 2024 00:43:22 GMT  
		Size: 53.6 MB (53556530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7e1eedad062cc55ed99a98d52f8d5ad41e90a0d0e6e0f6d078e28affbcc296f`  
		Last Modified: Tue, 13 Feb 2024 07:36:09 GMT  
		Size: 25.7 MB (25696437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3aa5d5534722f047808ec018306e8774ac9f7fe290d7e48b9d2979085bbfd0bb`  
		Last Modified: Tue, 13 Feb 2024 07:36:31 GMT  
		Size: 69.6 MB (69581064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4766a6e0e49a985c19ff5bed265467d9f1f6eada575066cf5a142c50bd88a57d`  
		Last Modified: Tue, 13 Feb 2024 07:37:13 GMT  
		Size: 214.2 MB (214151358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9970551fdc0ebf932e5625d4d46b2af8d54a304080bc0cc90b139517cecc7bf`  
		Last Modified: Tue, 13 Feb 2024 22:37:31 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9591d303189c65877b1b76ee06adfd1bdcfe9d82d92c55231a4c0dedc3da39aa`  
		Last Modified: Wed, 14 Feb 2024 03:10:48 GMT  
		Size: 16.0 MB (15964957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d0aa56c089ec014a7e8c73c79ad29dfad10560118503c5e22f5cc54ab6ddae0`  
		Last Modified: Wed, 14 Feb 2024 03:10:47 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-threaded` - unknown; unknown

```console
$ docker pull perl@sha256:b7e0187e55bfdcd3599f045e9937bae6e814cac2bd764be6812e2af08112ded3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.4 MB (13399709 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb7583e5ad9e38e2348514ea12795924b6f4faf7eecf355042972d89db1a957f`

```dockerfile
```

-	Layers:
	-	`sha256:53a48eb21bdf580f7d417e941d22b7a91d7fba9b0e2d29cdd04d6e6eacf081db`  
		Last Modified: Wed, 14 Feb 2024 03:10:47 GMT  
		Size: 13.4 MB (13383519 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:158d8ce06dd99e402900688add08c16a695e5385f390c6ff107e22e90927c94a`  
		Last Modified: Wed, 14 Feb 2024 03:10:46 GMT  
		Size: 16.2 KB (16190 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-threaded` - linux; s390x

```console
$ docker pull perl@sha256:a39194631ae8f1be8e1109dd13954590c6184ac0c206ecd9f3b49443dbee4379
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **334.5 MB (334524658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78cda1cf712c7fd60bd7430a646fe3a0eb1728fc6c636691e2193e8d51db0ab2`
-	Default Command: `["perl5.39.7","-de0"]`

```dockerfile
# Sat, 20 Jan 2024 20:51:34 GMT
ADD file:b1c0200d0f8b6070dfcbbadb831cbd04bd8d1b15c3c1f8e6e13c467f6c3f2879 in / 
# Sat, 20 Jan 2024 20:51:34 GMT
CMD ["bash"]
# Sat, 20 Jan 2024 20:51:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
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
	-	`sha256:0241650ae38ec8570f9718818b3b516c90697c5cd5686d5dd89306ae5f8e4657`  
		Last Modified: Wed, 31 Jan 2024 23:28:45 GMT  
		Size: 47.9 MB (47940767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1461a92bfa612443d019b6fc535db5abfd3639e66c1c5f41a511bdb1a782f00`  
		Last Modified: Thu, 01 Feb 2024 08:18:52 GMT  
		Size: 24.0 MB (24046914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05bc22d156c3113277b2a400b2b60e0ea00f6f62f339de493144008d5cc58796`  
		Last Modified: Thu, 01 Feb 2024 08:19:08 GMT  
		Size: 63.1 MB (63130267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25e9ee69e7f405307aed24012667e5bb90820e6d392951de2b5b22485ac9567c`  
		Last Modified: Thu, 01 Feb 2024 08:19:38 GMT  
		Size: 183.1 MB (183147992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f976dca31793a6a81bc9d112b432a54f457d3d1001eaaae31e1f4a24ab6cf730`  
		Last Modified: Tue, 06 Feb 2024 13:02:57 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1339c0fca380827e71743b3488719e8de594f3cb947ffd423bc7d40bbd07697`  
		Last Modified: Wed, 07 Feb 2024 05:25:19 GMT  
		Size: 16.3 MB (16258451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be1b218afbada658ca843e9dc6e83b2c227a9ff862ce4f0b60c72dddf4f9070f`  
		Last Modified: Wed, 07 Feb 2024 05:25:19 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-threaded` - unknown; unknown

```console
$ docker pull perl@sha256:3229ebc70a15fc682d80eadcd1df50a27b2e09340d16aa6718a713781a7d75d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.3 MB (13254331 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e6c2b3dddcbe98bcf51c28787bfdcd6ecaa3bdf57b5808eb2af38ea01ba9b7c`

```dockerfile
```

-	Layers:
	-	`sha256:4d8552ccfba23c922b2775f4365a03040c1c5f3c8290a7d5723e17cf4c830eb3`  
		Last Modified: Wed, 07 Feb 2024 05:25:19 GMT  
		Size: 13.2 MB (13238191 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4226a7c69984c12b1c353beb59c0f014772d3ea887beedad25b81070d5dfc44a`  
		Last Modified: Wed, 07 Feb 2024 05:25:19 GMT  
		Size: 16.1 KB (16140 bytes)  
		MIME: application/vnd.in-toto+json
