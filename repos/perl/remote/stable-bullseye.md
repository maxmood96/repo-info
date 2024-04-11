## `perl:stable-bullseye`

```console
$ docker pull perl@sha256:34913fc28febd7dc95cc95c9e2dc3f86fcb2a6f8c7c088bc2d3979a5e3a4f21d
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

### `perl:stable-bullseye` - linux; amd64

```console
$ docker pull perl@sha256:5ae0717d06a15ce609edbb4a1a3b16799b2623246a0107fa52b6dd6cbea54ea2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **338.1 MB (338071751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b449886f14b609f527f0a1ed003de5353aa52c4d123954b4ef2219b5ca4d2699`
-	Default Command: `["perl5.38.2","-de0"]`

```dockerfile
# Thu, 21 Mar 2024 18:18:23 GMT
ADD file:8efdcc3201e79c8a09fc9c1ade08492ea33f838047332a7c61988f6357339dee in / 
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
	-	`sha256:ac323bdaa10f869bd9e7adecd8f5326e44acc4c59168868108b1cdf3891089cc`  
		Last Modified: Wed, 10 Apr 2024 01:55:52 GMT  
		Size: 55.1 MB (55090264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84811b2a563b9003abbd1c06f6e45a857315b931855030bdd0443d13d950a996`  
		Last Modified: Wed, 10 Apr 2024 05:36:00 GMT  
		Size: 15.8 MB (15763518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3ff24b88ad3798f817849ad391d809ece121dc9b7f82f24bb68eed84561f048`  
		Last Modified: Wed, 10 Apr 2024 05:36:15 GMT  
		Size: 54.6 MB (54588743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6f58f24df78e3aabf785017c3197c2a09fd606e7f19a830a1cfde41f681f39e`  
		Last Modified: Wed, 10 Apr 2024 05:36:46 GMT  
		Size: 197.0 MB (196985611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7289597646385d0715e0d2977cefb42f9035ca191576283943f49f230db1b711`  
		Last Modified: Wed, 10 Apr 2024 07:01:10 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d58577b34701b6ae9deeb735a77a795f99c677a9fcb7d2fda38e1843c988538d`  
		Last Modified: Wed, 10 Apr 2024 07:01:10 GMT  
		Size: 15.6 MB (15643349 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f1451a0d5031d3dbcc2063cc7078ba5aea7f1bd68746656fc3c1e570ca4e2e2`  
		Last Modified: Wed, 10 Apr 2024 07:01:09 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:stable-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:4f179f5f498767bbd37596f5df8671b5069fbe3290681c87f88a5ccd13351e9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.0 MB (14990229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6edeaf2266d90ba0d7181f66f09547d524b54383e6bd5c79de14cb24529c610d`

```dockerfile
```

-	Layers:
	-	`sha256:ff79f4c262fcd3d59e9a39539e746f8e793fef409535f7477bec692798cdde7a`  
		Last Modified: Wed, 10 Apr 2024 07:01:09 GMT  
		Size: 15.0 MB (14973926 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e5890078e3339aa80afd9f0ab08ee77b878f77614281c52d556cc902053c0789`  
		Last Modified: Wed, 10 Apr 2024 07:01:09 GMT  
		Size: 16.3 KB (16303 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:stable-bullseye` - linux; arm variant v5

```console
$ docker pull perl@sha256:c8075956e0ce91d1b6c2d91601a0fbeac1026ce8c701738340fdc86734ff33ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **310.4 MB (310375712 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19f3b38af4ec85af4d1c15a8c25eb373ea2cc310c89204c85fbed1124959f416`
-	Default Command: `["perl5.38.2","-de0"]`

```dockerfile
# Fri, 23 Feb 2024 16:07:57 GMT
ADD file:e13a63ed3af4c4dcb74dfa2a2b12a285563b8c905dbac41b538492e1e100f93e in / 
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
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/P/PE/PEVANS/perl-5.38.2.tar.gz -o perl-5.38.2.tar.gz     && echo 'a0a31534451eb7b83c7d6594a497543a54d488bc90ca00f5e34762577f40655e *perl-5.38.2.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.38.2.tar.gz -C /usr/src/perl     && rm perl-5.38.2.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997014/cpm -o /usr/local/bin/cpm     && echo 'ee525f2493e36c6f688eddabaf53a51c4d3b2a4ebaa81576ac8b9f78ab57f4a1 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Fri, 23 Feb 2024 16:07:57 GMT
WORKDIR /usr/src/app
# Fri, 23 Feb 2024 16:07:57 GMT
CMD ["perl5.38.2" "-de0"]
```

-	Layers:
	-	`sha256:57e872a0ca7dbab84f7804705a96154de6b3cffcdb4f8946d4387764bfc1e307`  
		Last Modified: Tue, 12 Mar 2024 00:52:01 GMT  
		Size: 52.6 MB (52586778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d6eec0fce74f09fb69d81e686677faf5c980646b0666d9c658371a380575876`  
		Last Modified: Tue, 12 Mar 2024 01:44:24 GMT  
		Size: 15.4 MB (15374813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c47860a0c6a6b4af8b3bf2ef7b59f064d37fcf25f1ae20363c633b276713acb2`  
		Last Modified: Tue, 12 Mar 2024 01:44:41 GMT  
		Size: 52.3 MB (52328861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a2f143fe44237c686e570db73ca8e79a407a12cd45adcb3067acff6628c74a2`  
		Last Modified: Tue, 12 Mar 2024 01:45:14 GMT  
		Size: 175.2 MB (175154282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d2ebea0b57ec466ede998de13c287ae470fc4671676987ef197503a573a4051`  
		Last Modified: Tue, 12 Mar 2024 15:23:20 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdbe01aba612357627dfd3a9b1c865a7a4b1125ff758e93b3918c3af9297e2c6`  
		Last Modified: Tue, 12 Mar 2024 15:23:21 GMT  
		Size: 14.9 MB (14930712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66af24f0420af16d528a85d0f9eb51b0b32d4b3ad63ff21dbdb0fe40b3a0bdab`  
		Last Modified: Tue, 12 Mar 2024 15:23:20 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:stable-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:cc090f1949b0c59d7ab2aa0e2e7408062f5a55ef5dac01f66bc92dfd7b8521f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 MB (14786168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e51b2aa3b7d7a5892720f7d20146535d7c16729b92b251c19452e06786a997c8`

```dockerfile
```

-	Layers:
	-	`sha256:d97346c3a00f3423d1768b572fa42c4eed111b8e595064ec35c6e82928f01e87`  
		Last Modified: Tue, 12 Mar 2024 15:23:21 GMT  
		Size: 14.8 MB (14770449 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1ef8f659327caffb35d80b0b7074fc456a0703dc3e5bd92af3befb8219fc6942`  
		Last Modified: Tue, 12 Mar 2024 15:23:20 GMT  
		Size: 15.7 KB (15719 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:stable-bullseye` - linux; arm variant v7

```console
$ docker pull perl@sha256:5901987bda9f240eca5f3838b1b34164ecbc8b705db34e5847f8845e2bca59cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.7 MB (297650409 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9121f67daf93a5088de2ba175fa72940f274d7716bdc58b0f5e6ce655e3ddbc4`
-	Default Command: `["perl5.38.2","-de0"]`

```dockerfile
# Fri, 23 Feb 2024 16:07:57 GMT
ADD file:477c339ed6ec658bb1d0025e1568290c3cbbc98d9f973379f3133b83c2de9128 in / 
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
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/P/PE/PEVANS/perl-5.38.2.tar.gz -o perl-5.38.2.tar.gz     && echo 'a0a31534451eb7b83c7d6594a497543a54d488bc90ca00f5e34762577f40655e *perl-5.38.2.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.38.2.tar.gz -C /usr/src/perl     && rm perl-5.38.2.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997014/cpm -o /usr/local/bin/cpm     && echo 'ee525f2493e36c6f688eddabaf53a51c4d3b2a4ebaa81576ac8b9f78ab57f4a1 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Fri, 23 Feb 2024 16:07:57 GMT
WORKDIR /usr/src/app
# Fri, 23 Feb 2024 16:07:57 GMT
CMD ["perl5.38.2" "-de0"]
```

-	Layers:
	-	`sha256:ab40cb80ac5229a1c48dfbfe9aaa04da29109444982d90d4bca2c7b6842beceb`  
		Last Modified: Tue, 12 Mar 2024 01:03:56 GMT  
		Size: 50.2 MB (50241442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a3dae685361a941719b8f1aafa21f93305a1df032b9e9940f90b7dafabb394d`  
		Last Modified: Tue, 12 Mar 2024 02:20:17 GMT  
		Size: 14.9 MB (14878987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a08f233733bf767f50d39c3e0a1ce20900043f44a7e4df655c1c5556a9e2834`  
		Last Modified: Tue, 12 Mar 2024 02:20:36 GMT  
		Size: 50.4 MB (50357621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fea5901896ab9c5ad236e05b73d2065621d4488b4c7d2d61bef4316c3c981b2`  
		Last Modified: Tue, 12 Mar 2024 02:22:12 GMT  
		Size: 167.4 MB (167439330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e6ff466d10aed86bd466164fa892f46fbecfad7f99d4eaa97f70daacc0f4981`  
		Last Modified: Wed, 13 Mar 2024 01:07:50 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cb2f623ad2aebbdde1511f419536affc1337507823a00151266903b0ca6a411`  
		Last Modified: Wed, 13 Mar 2024 01:07:51 GMT  
		Size: 14.7 MB (14732761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18b4949f4dd1354d598729d21ed57fa158eda09c9bdca49811f1353a286c2409`  
		Last Modified: Wed, 13 Mar 2024 01:07:50 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:stable-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:02e64aaa7a9b1dfba3f87daa1fbdb766940c8ca3aca8ba580089c8e14a351d2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 MB (14791542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fa52bbf10a166487fec5dad12eb813c00f56b8df42c7d06655d9a7304b000de`

```dockerfile
```

-	Layers:
	-	`sha256:b882a576fd774285766b834ad1b10179d626c1baf0168f60389677269fb83478`  
		Last Modified: Wed, 13 Mar 2024 01:07:51 GMT  
		Size: 14.8 MB (14775823 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7b691cfe81776de7762495a24976c684d40b63ec02e44aafa6911d41e00a4f54`  
		Last Modified: Wed, 13 Mar 2024 01:07:50 GMT  
		Size: 15.7 KB (15719 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:stable-bullseye` - linux; arm64 variant v8

```console
$ docker pull perl@sha256:6a6eea43345eea8ccda5838d093f47349d55f2dad70e8f08f8c1316613dee2bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **329.7 MB (329666799 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1f333a084a9b97a13e707f66381300433a7bdf0ee1083fccf0512e3fb84fd2d`
-	Default Command: `["perl5.38.2","-de0"]`

```dockerfile
# Thu, 21 Mar 2024 18:18:23 GMT
ADD file:6fedb173fe261ff0e13b004ca692b7edcc74dcc3c4384fee092b96ef9508992c in / 
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
	-	`sha256:197947a07d5f6c6ff020ca65dcea4e52671f85f67bee1b59af46cb0dc36580d9`  
		Last Modified: Wed, 10 Apr 2024 00:44:24 GMT  
		Size: 53.7 MB (53729176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31e3f4a530684a6d51e431d14164bdf20c7ad515e8948ddbfbf5f9c2c3680727`  
		Last Modified: Wed, 10 Apr 2024 04:33:00 GMT  
		Size: 15.7 MB (15749239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27317b8832e116e0457de89bfb9097cbcd3165d6079c38230f3728894dfb3af1`  
		Last Modified: Wed, 10 Apr 2024 04:33:14 GMT  
		Size: 54.7 MB (54694342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:191dceb3c5772a800dd46b1b628a79e2167bd6bb0e9844a04e9ffc8a550a182b`  
		Last Modified: Wed, 10 Apr 2024 04:33:40 GMT  
		Size: 189.9 MB (189914112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2654e961ef31466a705e66d718412f9195d6e192f465efd559ee4f2ae007916d`  
		Last Modified: Thu, 11 Apr 2024 05:24:40 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3f47f5290b6e93c36c639afd852287a8f3ec84ae89f702b5c8312b877ad33c8`  
		Last Modified: Thu, 11 Apr 2024 05:24:41 GMT  
		Size: 15.6 MB (15579664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22af7be71b6789c3f25736e19dac1b789c890ad2eaedea2e8937a37b7517c710`  
		Last Modified: Thu, 11 Apr 2024 05:24:40 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:stable-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:1fae39306f136cd0cbdfcabe9dd67c50a047435b854924d0cb8f5502d6a8d2b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.0 MB (14992047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73a08d969bbaa0796eed8c82418ad99a5814f02f24166c4dfac22632a9985ed1`

```dockerfile
```

-	Layers:
	-	`sha256:c4fc3de7d7aab46d71578c98ba48361f493b044ac5d919d5ef728e7fc5b109cc`  
		Last Modified: Thu, 11 Apr 2024 05:24:41 GMT  
		Size: 15.0 MB (14976394 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8c2499d686f04420c34ccd18d2d4eaddc41380f187efcc5e855f15b0ec25459e`  
		Last Modified: Thu, 11 Apr 2024 05:24:40 GMT  
		Size: 15.7 KB (15653 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:stable-bullseye` - linux; 386

```console
$ docker pull perl@sha256:6e531f8f202a3372a507820a86caf0512d3862b7ba00fa6b954b5383315c49ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **343.3 MB (343289324 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ac3a30611e55b04dc21eda780cd111a292fac08d0b26e8c9407726d2e341c35`
-	Default Command: `["perl5.38.2","-de0"]`

```dockerfile
# Thu, 21 Mar 2024 18:18:23 GMT
ADD file:34b6b0eca66bdded42723d3cb7b488ca726fedb7fd2a42c047e2790ccf93f08b in / 
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
	-	`sha256:1dc10b34406db63eacc8d006ba4d0103014a3a863134cdfe43622d4706753fa7`  
		Last Modified: Wed, 10 Apr 2024 01:02:27 GMT  
		Size: 56.1 MB (56066188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:125c557bd27681f5387605727a1b0d44605793da722ea6f8f66b86df9aa54384`  
		Last Modified: Wed, 10 Apr 2024 08:07:12 GMT  
		Size: 16.3 MB (16267921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13acd7d81d47808020936c58e9842c82c55c0205f369482de2b263fe21ed2dc6`  
		Last Modified: Wed, 10 Apr 2024 08:07:31 GMT  
		Size: 55.9 MB (55927749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed69373b65ed4263cd1d2ead3d6570264c8de6a744aa10974a8266c660515080`  
		Last Modified: Wed, 10 Apr 2024 08:08:16 GMT  
		Size: 199.9 MB (199890546 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2e28faebb11eedf9e4706a39ca93814a647dee694e4757b23163a8cb8983b63`  
		Last Modified: Wed, 10 Apr 2024 09:03:06 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46f63d4a7c75c3f4686210f1d8936dad02df8d3c66ac8f37672fa687f2639435`  
		Last Modified: Wed, 10 Apr 2024 09:03:07 GMT  
		Size: 15.1 MB (15136652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b1374231febf0f842c1593eb8b170db636d82c68db9e7281e0d06d72548e8a1`  
		Last Modified: Wed, 10 Apr 2024 09:03:07 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:stable-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:c4cb773ec6e9a70b84a387ebc1648d79d56b9b4806357adafebefb126bb6a7e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.0 MB (14979022 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19df6db12f6dda92290a4c36d3bf93f00c4e033f281b37be9ea19b22e30a3743`

```dockerfile
```

-	Layers:
	-	`sha256:8bbc4318e29658df1af94022352fbccc74ed7e2a8e506ad06e48879c43d1090b`  
		Last Modified: Wed, 10 Apr 2024 09:03:07 GMT  
		Size: 15.0 MB (14962752 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e943cf48e15e408ac1d82fb65b771a56bada0dd2fb6e27f40345dae58ddb9452`  
		Last Modified: Wed, 10 Apr 2024 09:03:06 GMT  
		Size: 16.3 KB (16270 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:stable-bullseye` - linux; mips64le

```console
$ docker pull perl@sha256:4bd1ea5d8da102e376137e897cc27fd4a4b795921a4d53024d0086d9a77f5a9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **316.3 MB (316294226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b891490e1f92e9425dddd20999f3eb4183af3bc116311a54267259ab6fd8dff`
-	Default Command: `["perl5.38.2","-de0"]`

```dockerfile
# Fri, 23 Feb 2024 16:07:57 GMT
ADD file:ceaac889009e9d867969b5a568939eb0f6e136303e3438d9747193d6ef4755ab in / 
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
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/P/PE/PEVANS/perl-5.38.2.tar.gz -o perl-5.38.2.tar.gz     && echo 'a0a31534451eb7b83c7d6594a497543a54d488bc90ca00f5e34762577f40655e *perl-5.38.2.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.38.2.tar.gz -C /usr/src/perl     && rm perl-5.38.2.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997014/cpm -o /usr/local/bin/cpm     && echo 'ee525f2493e36c6f688eddabaf53a51c4d3b2a4ebaa81576ac8b9f78ab57f4a1 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Fri, 23 Feb 2024 16:07:57 GMT
WORKDIR /usr/src/app
# Fri, 23 Feb 2024 16:07:57 GMT
CMD ["perl5.38.2" "-de0"]
```

-	Layers:
	-	`sha256:3856c0b5cf8a29fd86ef6fe0c2a36a38020518c2e120457769b9044974ec1ca8`  
		Last Modified: Tue, 12 Mar 2024 01:17:56 GMT  
		Size: 53.3 MB (53303519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7acdc20e5c94994c036364331f6d067dbe2215bca100c34dc233aa97abbb88e3`  
		Last Modified: Tue, 12 Mar 2024 02:45:06 GMT  
		Size: 15.7 MB (15734611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e4f183b6f40e96072119ab41213733a9079dd8d43cd4a7c36f9f7e3531dd614`  
		Last Modified: Tue, 12 Mar 2024 02:45:50 GMT  
		Size: 53.3 MB (53310696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa21edf61173913e6f42aa80ddb070961a6780a6703f5e284ec12292d725922b`  
		Last Modified: Tue, 12 Mar 2024 02:47:47 GMT  
		Size: 179.1 MB (179097827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94cdef942a00dcb07f0bdb5ac6ba54449e0f5b296cf1a280b3df9418f0b94d8f`  
		Last Modified: Wed, 13 Mar 2024 04:14:08 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e28b3ebb425834ab700d71211329703598d6e28031bf022e944d3ae777e5193`  
		Last Modified: Wed, 13 Mar 2024 04:14:11 GMT  
		Size: 14.8 MB (14847305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce5efd5232a332ed2a28b0503412cf47fb299897e7c42643975682e89534babc`  
		Last Modified: Wed, 13 Mar 2024 04:14:12 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:stable-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:8b174d7d5dac7b2d967dfc0a83a58bf7247dcc696b64665b2609873f0664dbcc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.2 KB (16155 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ade9cb02ad723887ff5aec208c4a8a04ce43b867803fd4f218fa7adef22fdaed`

```dockerfile
```

-	Layers:
	-	`sha256:75a5957e15145ed3657298cff0638fbb4033b1177017da5503c2f882ba0dbf3e`  
		Last Modified: Wed, 13 Mar 2024 04:14:04 GMT  
		Size: 16.2 KB (16155 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:stable-bullseye` - linux; ppc64le

```console
$ docker pull perl@sha256:c9ed1b02ccc3ae78b56161e8b7b90f61bb2fb8dc09107786fb763f211f2da37c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **346.6 MB (346578016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e09edffe39b29ee8d84dfa07a30b94b2dcd954eb9897f45dcc308f8662f4bfc`
-	Default Command: `["perl5.38.2","-de0"]`

```dockerfile
# Thu, 21 Mar 2024 18:18:23 GMT
ADD file:774dc7f7db45435bfddcc1ff7bb4ae0716252e8f7c3d074ff7611070207b8314 in / 
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
	-	`sha256:eed533dbdbda3df66dcde8a75fb0ab317466f575d116ffa4e053da66ab0dd942`  
		Last Modified: Wed, 10 Apr 2024 01:31:35 GMT  
		Size: 59.0 MB (58959030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e798a4c3c738ae3b2b3ae6f2b6f02c6db9d510fadd63004b60dd8268c907ee34`  
		Last Modified: Wed, 10 Apr 2024 07:17:41 GMT  
		Size: 16.8 MB (16765741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82a0da44da0fa59c2e0283157a263f65dcc5e2b22c7a5515c68bd6d82e305a55`  
		Last Modified: Wed, 10 Apr 2024 07:18:00 GMT  
		Size: 58.9 MB (58873011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:711cc15f136ce528a3936b4864554b8879c5d361f9d968ba9b756dd216f192eb`  
		Last Modified: Wed, 10 Apr 2024 07:18:39 GMT  
		Size: 196.3 MB (196345047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4685bb5a55b13abd964d5e3f531fbc121f816fa4e516bd9c62d43b1cb74774b0`  
		Last Modified: Thu, 11 Apr 2024 05:38:04 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68b3bcf60da3e858f7f01b3fb7a1a7c3a231803dd7c7f974c6790d6f444217a5`  
		Last Modified: Thu, 11 Apr 2024 05:38:05 GMT  
		Size: 15.6 MB (15634919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8208b2bb21444f23fa37c2fe34b009f36252bb1bb69a4a027495839a5c2badeb`  
		Last Modified: Thu, 11 Apr 2024 05:38:04 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:stable-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:e6948cca00bb91f3de90020d4326e2225ef5eae16a2ec87e33193145971b61f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.0 MB (14958922 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45c4560cbb29cb4016c6604b82720712f80992109dff552703744e532c91d823`

```dockerfile
```

-	Layers:
	-	`sha256:1593059226b9847f837aa86c06d46849bfdaa4acb0786d075777dcdb2bd3889c`  
		Last Modified: Thu, 11 Apr 2024 05:38:04 GMT  
		Size: 14.9 MB (14943237 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:10f967807748879a1329ec3fcf0d7bcad60e69cd92b6e8f6e749584fb6c5b0fb`  
		Last Modified: Thu, 11 Apr 2024 05:38:04 GMT  
		Size: 15.7 KB (15685 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:stable-bullseye` - linux; s390x

```console
$ docker pull perl@sha256:00ec7fc28e3262c368caf94c974e311c7b4c34470b6757806a38011463625f53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **312.0 MB (312015814 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d2d76dc2f57c984b676241e9c46b7b6985416937d9835847035cb794223a60f`
-	Default Command: `["perl5.38.2","-de0"]`

```dockerfile
# Fri, 23 Feb 2024 16:07:57 GMT
ADD file:acdf6d23a12147f9c8c6eb2c1074e5f2013daaf2ab667c770659494a89e9c8e3 in / 
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
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/P/PE/PEVANS/perl-5.38.2.tar.gz -o perl-5.38.2.tar.gz     && echo 'a0a31534451eb7b83c7d6594a497543a54d488bc90ca00f5e34762577f40655e *perl-5.38.2.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.38.2.tar.gz -C /usr/src/perl     && rm perl-5.38.2.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997014/cpm -o /usr/local/bin/cpm     && echo 'ee525f2493e36c6f688eddabaf53a51c4d3b2a4ebaa81576ac8b9f78ab57f4a1 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Fri, 23 Feb 2024 16:07:57 GMT
WORKDIR /usr/src/app
# Fri, 23 Feb 2024 16:07:57 GMT
CMD ["perl5.38.2" "-de0"]
```

-	Layers:
	-	`sha256:861d490dd592be84c92fb7027a5967a8a2009c66688194260d1c5a413c8aef48`  
		Last Modified: Tue, 12 Mar 2024 01:21:28 GMT  
		Size: 53.3 MB (53319541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adb2ab3b8920b4d36bbda5b2807296d8b751492cd2709f164bb76692b98f7dae`  
		Last Modified: Tue, 12 Mar 2024 02:48:21 GMT  
		Size: 15.6 MB (15641294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8050bc0c7be4bc967cc1413b9ab67358c6a153789b08c99737f54df7feafc27`  
		Last Modified: Tue, 12 Mar 2024 02:48:34 GMT  
		Size: 54.1 MB (54075731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84dbe74529fc57e85a22f94e3442e33e7b5d04e9a4e5bfef8746df1fd2841eb8`  
		Last Modified: Tue, 12 Mar 2024 02:49:00 GMT  
		Size: 173.0 MB (172991681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e40e7b8b26d2ff496fc83a9961cd3f9f776513c549db88af6ae7c72e9ef03e5e`  
		Last Modified: Wed, 13 Mar 2024 17:06:18 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f75fac7cae0b03aa71ca57f9127c1884e92865a60be28185d26b4c7089407ea9`  
		Last Modified: Wed, 13 Mar 2024 17:06:18 GMT  
		Size: 16.0 MB (15987299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d848e7710eb09e8bbf72e438ebf1f19233b61ed57a55f3a8c00f31b54d8c281`  
		Last Modified: Wed, 13 Mar 2024 17:06:18 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:stable-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:15dba07fceb199c1bf84e28249d38746b24f2bf23908c3140d33d43d2d41a390
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 MB (14811242 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d10727f2aa336b7f481738b56083a92b302bad277c46894f07154a375bb84e9`

```dockerfile
```

-	Layers:
	-	`sha256:7fa6bfa3b1c17284b075b8b15d1968fcd6b6a319b1f48613a5d18b43e065600b`  
		Last Modified: Wed, 13 Mar 2024 17:06:18 GMT  
		Size: 14.8 MB (14795602 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3215c11e9ab7b1d68520e4140aa04eb8a8c313106d7982dea44ba9af195e5e92`  
		Last Modified: Wed, 13 Mar 2024 17:06:17 GMT  
		Size: 15.6 KB (15640 bytes)  
		MIME: application/vnd.in-toto+json
