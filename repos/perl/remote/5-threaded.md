## `perl:5-threaded`

```console
$ docker pull perl@sha256:4859cff02ccf2ee35738f5f0540e9ab3e2ce036fc8b9326889761d5b3385fabf
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

### `perl:5-threaded` - linux; amd64

```console
$ docker pull perl@sha256:1dde09f93315c779ec9ef2cc37c65ec5e3a176035486c656b4a55df955e174c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **364.6 MB (364575051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b62f97f3d7066b440277d391eebc9278a948194bf41373da68f382b1ad7cde24`
-	Default Command: `["perl5.38.2","-de0"]`

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
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/P/PE/PEVANS/perl-5.38.2.tar.gz -o perl-5.38.2.tar.gz     && echo 'a0a31534451eb7b83c7d6594a497543a54d488bc90ca00f5e34762577f40655e *perl-5.38.2.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.38.2.tar.gz -C /usr/src/perl     && rm perl-5.38.2.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997014/cpm -o /usr/local/bin/cpm     && echo 'ee525f2493e36c6f688eddabaf53a51c4d3b2a4ebaa81576ac8b9f78ab57f4a1 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Sat, 20 Jan 2024 20:51:34 GMT
WORKDIR /usr/src/app
# Sat, 20 Jan 2024 20:51:34 GMT
CMD ["perl5.38.2" "-de0"]
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
	-	`sha256:d488997811b16bbce81b5087a0fc1482b5e0c74eee18b387e7019a816148cf61`  
		Last Modified: Tue, 13 Feb 2024 03:06:15 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaaf36abfb1ddc6e230ce1654b48cc2b8e60946b70e7455d46e00c0ac39c227b`  
		Last Modified: Tue, 13 Feb 2024 03:06:16 GMT  
		Size: 15.7 MB (15714840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:522e442e0466a41ff09a8691e3aeb795815f4e5b5cbc6b53f1041153476ebedf`  
		Last Modified: Tue, 13 Feb 2024 03:06:15 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:5-threaded` - unknown; unknown

```console
$ docker pull perl@sha256:32cfe5141b764444f094fcb773de6cd0e990c60320a0324bd41e3e2342cbd832
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.4 MB (13421360 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e36c5b666336fa248e3b4bbedee93ba3018906c67605cc2076c0981127d5328f`

```dockerfile
```

-	Layers:
	-	`sha256:efa5952e77b5b346bdc5dea0b37a037317a0759d5685fd3765502dbc103f0c08`  
		Last Modified: Tue, 13 Feb 2024 03:06:16 GMT  
		Size: 13.4 MB (13403387 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:92afd62025bd6da39dc2ee1bc30f862785b5de051ae4ceda8ff6d6fa40f1e81d`  
		Last Modified: Tue, 13 Feb 2024 03:06:15 GMT  
		Size: 18.0 KB (17973 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:5-threaded` - linux; arm variant v5

```console
$ docker pull perl@sha256:d76cf1acff2bec745843499d743c26c43ed9e6fb56d98f38229f6b4218692429
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **331.0 MB (330963629 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1bade5bf29df1c609ae5740ceabef1712d2ed0b4e417d3a490bddd76c21ee58`
-	Default Command: `["perl5.38.2","-de0"]`

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
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/P/PE/PEVANS/perl-5.38.2.tar.gz -o perl-5.38.2.tar.gz     && echo 'a0a31534451eb7b83c7d6594a497543a54d488bc90ca00f5e34762577f40655e *perl-5.38.2.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.38.2.tar.gz -C /usr/src/perl     && rm perl-5.38.2.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997014/cpm -o /usr/local/bin/cpm     && echo 'ee525f2493e36c6f688eddabaf53a51c4d3b2a4ebaa81576ac8b9f78ab57f4a1 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Sat, 20 Jan 2024 20:51:34 GMT
WORKDIR /usr/src/app
# Sat, 20 Jan 2024 20:51:34 GMT
CMD ["perl5.38.2" "-de0"]
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
	-	`sha256:e8cddc4a3f048c75b902eb1df30bf33fb0adcdd52d4dee93af5fe5181c98ef03`  
		Last Modified: Wed, 14 Feb 2024 15:47:50 GMT  
		Size: 15.0 MB (14962754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:031d4135e64cd2493f2f39c912dfb9b2f937c40de9250485bf93e3fb3ac6b9cb`  
		Last Modified: Wed, 14 Feb 2024 15:47:49 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:5-threaded` - unknown; unknown

```console
$ docker pull perl@sha256:e103934cd9d9ec8483b20ae28c85f478153a04d58eef3956b921e786b1fecdcc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.2 MB (13246028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa17ede550030f328ead4d90f3df112957b1fc1f0133b8085c22a239d0f14d43`

```dockerfile
```

-	Layers:
	-	`sha256:26a5efd75ecd34acca585893478ceb413e59ba1c48d7130acf90abe6e1283737`  
		Last Modified: Wed, 14 Feb 2024 15:47:50 GMT  
		Size: 13.2 MB (13228601 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3213daa75d8da8d7a98c6a1bae7bf0215d75a3c3f487d27463fa10f81933e331`  
		Last Modified: Wed, 14 Feb 2024 15:47:50 GMT  
		Size: 17.4 KB (17427 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:5-threaded` - linux; arm variant v7

```console
$ docker pull perl@sha256:b85ee107e03460d7904d892220f1234aabf26c9d59ac215cca8d5d760cb5308f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **316.2 MB (316181836 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac6eb6918eb29f8b19040fb7e63f71ac4220cce919456cd5b4425a2c3a33565a`
-	Default Command: `["perl5.38.2","-de0"]`

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
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/P/PE/PEVANS/perl-5.38.2.tar.gz -o perl-5.38.2.tar.gz     && echo 'a0a31534451eb7b83c7d6594a497543a54d488bc90ca00f5e34762577f40655e *perl-5.38.2.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.38.2.tar.gz -C /usr/src/perl     && rm perl-5.38.2.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997014/cpm -o /usr/local/bin/cpm     && echo 'ee525f2493e36c6f688eddabaf53a51c4d3b2a4ebaa81576ac8b9f78ab57f4a1 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Sat, 20 Jan 2024 20:51:34 GMT
WORKDIR /usr/src/app
# Sat, 20 Jan 2024 20:51:34 GMT
CMD ["perl5.38.2" "-de0"]
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
	-	`sha256:ee0eeac784e299f7902e3ca4e4d6b1878868725f53cf4bf6127ef0cae38d0955`  
		Last Modified: Sat, 03 Feb 2024 15:24:24 GMT  
		Size: 14.8 MB (14751317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab9ae5e1c622b7bfcb930d2f39dcc48f179f6094531a11db819fb9666d29f024`  
		Last Modified: Sat, 03 Feb 2024 15:24:23 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:5-threaded` - unknown; unknown

```console
$ docker pull perl@sha256:a5d29aed351051b921d5b4b77a8d84d135c3f0732591a305cb7addb3cf76d06d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.3 MB (13251447 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52b82c29456ac4709e4210e293e3c2b87100080759ac6a145962b5a6a67bdffa`

```dockerfile
```

-	Layers:
	-	`sha256:dfe47026b2d9a090a3cf49dca1ee26f202e6b518059b746f4c3fad4ff01c8e1e`  
		Last Modified: Sat, 03 Feb 2024 15:24:25 GMT  
		Size: 13.2 MB (13234019 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:af17e42c6f7d0160886841171b53c275564d20d0c58b1367dfe8e3a8cf4e5c29`  
		Last Modified: Sat, 03 Feb 2024 15:24:23 GMT  
		Size: 17.4 KB (17428 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:5-threaded` - linux; arm64 variant v8

```console
$ docker pull perl@sha256:185e2886898cdc46a9eee925f0575abd7323000eaaa8e1914dfc9e6f9e67addd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **355.3 MB (355349331 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c867852b0d176b23616ca3b187e72f6100c84f3edd571e112d901601db948f4`
-	Default Command: `["perl5.38.2","-de0"]`

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
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/P/PE/PEVANS/perl-5.38.2.tar.gz -o perl-5.38.2.tar.gz     && echo 'a0a31534451eb7b83c7d6594a497543a54d488bc90ca00f5e34762577f40655e *perl-5.38.2.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.38.2.tar.gz -C /usr/src/perl     && rm perl-5.38.2.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997014/cpm -o /usr/local/bin/cpm     && echo 'ee525f2493e36c6f688eddabaf53a51c4d3b2a4ebaa81576ac8b9f78ab57f4a1 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Sat, 20 Jan 2024 20:51:34 GMT
WORKDIR /usr/src/app
# Sat, 20 Jan 2024 20:51:34 GMT
CMD ["perl5.38.2" "-de0"]
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
	-	`sha256:1f4faa61602c8977e773fbe21fe07ba1475613f6f3d7632bc913a64674470d63`  
		Last Modified: Wed, 14 Feb 2024 03:09:44 GMT  
		Size: 15.7 MB (15664722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8351adddd699323d79fd2823db089bfc32b5e481835f23c31fa1ccada5635df9`  
		Last Modified: Wed, 14 Feb 2024 03:09:43 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:5-threaded` - unknown; unknown

```console
$ docker pull perl@sha256:f846b8abe428a4d0ed53f780cd9899e8115cb7e8b8a4259576e5945c4a2b1c94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.4 MB (13445956 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:736d4c420aa17ee76a7706c7ca953e78fc7cf92b46b0a282d9a968c823234f65`

```dockerfile
```

-	Layers:
	-	`sha256:d363905f8d11c83fff5a23aab0ebc1baf368062c56fa026a0a68d4882b11bb91`  
		Last Modified: Wed, 14 Feb 2024 03:09:44 GMT  
		Size: 13.4 MB (13428624 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:21c028fbb13cb14dc75d19ac538d34261ce785fa900f7c5a240bb363c8e4e534`  
		Last Modified: Wed, 14 Feb 2024 03:09:43 GMT  
		Size: 17.3 KB (17332 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:5-threaded` - linux; 386

```console
$ docker pull perl@sha256:cf3ef8e5fac1db3273d0847ba82d395427498bb2be2bd11b52b517ab4bf8ca14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **366.8 MB (366755074 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bab0c01733c3fcc6b617d735cd67bf987fa501443354d03853d316f42f614a3e`
-	Default Command: `["perl5.38.2","-de0"]`

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
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/P/PE/PEVANS/perl-5.38.2.tar.gz -o perl-5.38.2.tar.gz     && echo 'a0a31534451eb7b83c7d6594a497543a54d488bc90ca00f5e34762577f40655e *perl-5.38.2.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.38.2.tar.gz -C /usr/src/perl     && rm perl-5.38.2.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997014/cpm -o /usr/local/bin/cpm     && echo 'ee525f2493e36c6f688eddabaf53a51c4d3b2a4ebaa81576ac8b9f78ab57f4a1 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Sat, 20 Jan 2024 20:51:34 GMT
WORKDIR /usr/src/app
# Sat, 20 Jan 2024 20:51:34 GMT
CMD ["perl5.38.2" "-de0"]
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
	-	`sha256:6b6a7dffd230416e8de30ad9aeefa8b12bbffba8c403cc066df0a5dcd83b36cc`  
		Last Modified: Tue, 13 Feb 2024 03:05:51 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df26ab3f497b751b3dde592b4e3f21f531bfbdeed8dc30b8616a3ab90f372066`  
		Last Modified: Tue, 13 Feb 2024 03:07:13 GMT  
		Size: 15.3 MB (15254886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:006cdb872079de0750cbfe7c588f23cb3beb449e54341af991747d930277622a`  
		Last Modified: Tue, 13 Feb 2024 03:07:13 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:5-threaded` - unknown; unknown

```console
$ docker pull perl@sha256:ada87935ac8494eba879ee23d6076e32fed967655a15294135eefe67f3cb6350
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.4 MB (13401705 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:965c5d0261ed8ddc6eb9c028886d5a8fe7b76045512428ff945dc3029e5d598d`

```dockerfile
```

-	Layers:
	-	`sha256:12a6543495d371fe5d73c3921f9c659e351f7b83c98581a97f299cfb6c0706d2`  
		Last Modified: Tue, 13 Feb 2024 03:07:13 GMT  
		Size: 13.4 MB (13383791 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:31aabb8aada26c06900ededacc7079f301631fdf864ae042d5b2641144de52e0`  
		Last Modified: Tue, 13 Feb 2024 03:07:12 GMT  
		Size: 17.9 KB (17914 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:5-threaded` - linux; mips64le

```console
$ docker pull perl@sha256:3dd45fab757c466927f39bfb8cb902f79d9bf58856302416089b96bd9d7fa0d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **340.8 MB (340794992 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b4aa90e0aae68a6f704ce0d5d4c638ae5237a6df8c033edea8a7e4097433559`
-	Default Command: `["perl5.38.2","-de0"]`

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
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/P/PE/PEVANS/perl-5.38.2.tar.gz -o perl-5.38.2.tar.gz     && echo 'a0a31534451eb7b83c7d6594a497543a54d488bc90ca00f5e34762577f40655e *perl-5.38.2.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.38.2.tar.gz -C /usr/src/perl     && rm perl-5.38.2.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997014/cpm -o /usr/local/bin/cpm     && echo 'ee525f2493e36c6f688eddabaf53a51c4d3b2a4ebaa81576ac8b9f78ab57f4a1 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Sat, 20 Jan 2024 20:51:34 GMT
WORKDIR /usr/src/app
# Sat, 20 Jan 2024 20:51:34 GMT
CMD ["perl5.38.2" "-de0"]
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
	-	`sha256:d302f33c4307db722bd25d9106e6091743b097915e87e153d64ccd854708d5a3`  
		Last Modified: Wed, 14 Feb 2024 07:16:10 GMT  
		Size: 14.9 MB (14925194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d458bfb07463c4bb6c2a8df935e2f759bee31b1a89114160df449124f9ae0b2a`  
		Last Modified: Wed, 14 Feb 2024 07:16:08 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:5-threaded` - unknown; unknown

```console
$ docker pull perl@sha256:a790e770679ad2de23d33ceffda7010741ec2ef6e8210f960e6c3df05d79ba88
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.2 KB (17204 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9750473fc8c1113f37dfbde8bf7a91bb8868fe90ca35bb9a3a56256a86b5eca`

```dockerfile
```

-	Layers:
	-	`sha256:a6dd2dd3aff4111787a55dc9f6961b2210bf12c00ea1f463c4821af3da31a8ca`  
		Last Modified: Wed, 14 Feb 2024 07:16:07 GMT  
		Size: 17.2 KB (17204 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:5-threaded` - linux; ppc64le

```console
$ docker pull perl@sha256:d753ec155b799e8870782c486835fecdef673d0d0cbb8bff499f053dd7820770
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **378.7 MB (378741787 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06ab74242719b037d776ee535cec6748909e0c72b94d654a35e0e3aaeb73bd4d`
-	Default Command: `["perl5.38.2","-de0"]`

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
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/P/PE/PEVANS/perl-5.38.2.tar.gz -o perl-5.38.2.tar.gz     && echo 'a0a31534451eb7b83c7d6594a497543a54d488bc90ca00f5e34762577f40655e *perl-5.38.2.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.38.2.tar.gz -C /usr/src/perl     && rm perl-5.38.2.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997014/cpm -o /usr/local/bin/cpm     && echo 'ee525f2493e36c6f688eddabaf53a51c4d3b2a4ebaa81576ac8b9f78ab57f4a1 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Sat, 20 Jan 2024 20:51:34 GMT
WORKDIR /usr/src/app
# Sat, 20 Jan 2024 20:51:34 GMT
CMD ["perl5.38.2" "-de0"]
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
	-	`sha256:b55c784ce087e73ae0795be0954540b0a9c58daad93113c4e266af5a76b5f7b9`  
		Last Modified: Tue, 13 Feb 2024 23:22:05 GMT  
		Size: 15.8 MB (15756136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:579aa774a4ec6c5ae4e24861bd117e56e89c9813e502e98b75b901673256042f`  
		Last Modified: Tue, 13 Feb 2024 23:22:04 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:5-threaded` - unknown; unknown

```console
$ docker pull perl@sha256:8dea3912aaaf39b3ecfb1af2b9cac74f180eb4c7073b57ee75fdcf38f188f9b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.4 MB (13402167 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e20b5c51106268c672991f74dbf5537dffb65aae1966d14b77e38492c9f0055`

```dockerfile
```

-	Layers:
	-	`sha256:8fa4434d6c978dc59099429517e859fd5c05f010e6683a2ad172965a2a07932e`  
		Last Modified: Tue, 13 Feb 2024 23:22:05 GMT  
		Size: 13.4 MB (13384783 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5187928b952f9e8ee8e3e273903bfa0d85bef0fd04e7409c4474c1f746c04a26`  
		Last Modified: Tue, 13 Feb 2024 23:22:04 GMT  
		Size: 17.4 KB (17384 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:5-threaded` - linux; s390x

```console
$ docker pull perl@sha256:bb35e81c9ead395d152af9f2dc51422916e9cf1a81c4a03828bb7c77ffb898ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **334.3 MB (334318157 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf7997476460234b7dd3e1a651fd54b255f47ac2b3d83ac38ccda1644433a6f4`
-	Default Command: `["perl5.38.2","-de0"]`

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
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/P/PE/PEVANS/perl-5.38.2.tar.gz -o perl-5.38.2.tar.gz     && echo 'a0a31534451eb7b83c7d6594a497543a54d488bc90ca00f5e34762577f40655e *perl-5.38.2.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.38.2.tar.gz -C /usr/src/perl     && rm perl-5.38.2.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997014/cpm -o /usr/local/bin/cpm     && echo 'ee525f2493e36c6f688eddabaf53a51c4d3b2a4ebaa81576ac8b9f78ab57f4a1 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Sat, 20 Jan 2024 20:51:34 GMT
WORKDIR /usr/src/app
# Sat, 20 Jan 2024 20:51:34 GMT
CMD ["perl5.38.2" "-de0"]
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
	-	`sha256:e069a843f5dface229b8d1bb516429edfc32230bb6803aaa74b6030917f3bff4`  
		Last Modified: Tue, 06 Feb 2024 15:02:32 GMT  
		Size: 16.1 MB (16051949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:617038bb84f46f3e89f59a777cb0798b3f006d263b17a39beb3d8bc9e3bd0470`  
		Last Modified: Tue, 06 Feb 2024 15:02:32 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:5-threaded` - unknown; unknown

```console
$ docker pull perl@sha256:415b366d5f0bf402fa294f9babd49352af16165909d47cc364da177d463c0487
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.3 MB (13256741 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2016d437cd93ef02087211ede5f48fda77b6fc657f42ad23d8824ac5161addd`

```dockerfile
```

-	Layers:
	-	`sha256:d1893f32b2abfb1411e40de949a9ca7a27561fa5a2c7e245cdf8fd0a8f4653bc`  
		Last Modified: Tue, 06 Feb 2024 15:02:32 GMT  
		Size: 13.2 MB (13239431 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:341aad9e4abc0ef01ca47eabd6e8d731676601da2ad9e5a75589fc17d7c58c07`  
		Last Modified: Tue, 06 Feb 2024 15:02:32 GMT  
		Size: 17.3 KB (17310 bytes)  
		MIME: application/vnd.in-toto+json
