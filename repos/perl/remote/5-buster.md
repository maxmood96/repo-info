## `perl:5-buster`

```console
$ docker pull perl@sha256:e4efab880776bbfcdcd2a7545b8e092b2a62c3065831a17f5b1fcc361e48a433
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

### `perl:5-buster` - linux; amd64

```console
$ docker pull perl@sha256:2c8a0f50f0bf634726ae9463a1618732928d54417af7b7a074fe116c1d0d4a84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **327.6 MB (327563836 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ee9b45607e6e99c0fb89f153708000c4bb03081344b81b2dbea7fb77ff927f1`
-	Default Command: `["perl5.38.2","-de0"]`

```dockerfile
# Sat, 20 Jan 2024 20:51:34 GMT
ADD file:b60b9a116275a2d143473d643b907c76618f91fa8455daedbf3cb3c3dcc769d7 in / 
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
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/P/PE/PEVANS/perl-5.38.2.tar.gz -o perl-5.38.2.tar.gz     && echo 'a0a31534451eb7b83c7d6594a497543a54d488bc90ca00f5e34762577f40655e *perl-5.38.2.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.38.2.tar.gz -C /usr/src/perl     && rm perl-5.38.2.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997014/cpm -o /usr/local/bin/cpm     && echo 'ee525f2493e36c6f688eddabaf53a51c4d3b2a4ebaa81576ac8b9f78ab57f4a1 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Sat, 20 Jan 2024 20:51:34 GMT
WORKDIR /usr/src/app
# Sat, 20 Jan 2024 20:51:34 GMT
CMD ["perl5.38.2" "-de0"]
```

-	Layers:
	-	`sha256:286a4b9eefae02fec0ae760a2d7c4124f44aa719d5b50e69c401aaa6dcdae50a`  
		Last Modified: Wed, 31 Jan 2024 22:41:07 GMT  
		Size: 50.5 MB (50500710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e596689f03daed190c8e7db6f0a6e6869bf97e67ed7114bb84c8e3daa9b648d8`  
		Last Modified: Wed, 31 Jan 2024 23:34:26 GMT  
		Size: 17.6 MB (17584819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c933d55a84b39f50891da1a3d93708a40af88018898950d1c1d45287cbceead`  
		Last Modified: Wed, 31 Jan 2024 23:34:41 GMT  
		Size: 51.9 MB (51877396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aec1650ec847faff4a08d29f1974f9dfb31d13d19f2e8c9f6007fdcb96385356`  
		Last Modified: Wed, 31 Jan 2024 23:35:12 GMT  
		Size: 191.9 MB (191933959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73fad6d3fd16e9a650f9a09c7bd0d1d98832d80ec814d98d205e3e28e1556251`  
		Last Modified: Thu, 01 Feb 2024 00:04:51 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82678b9184a95a6ba443ed8d6604efa2087c33b8803dd6f16250de864ad073df`  
		Last Modified: Thu, 01 Feb 2024 00:04:52 GMT  
		Size: 15.7 MB (15666689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55d412614764f9699552de47454501ef825b8a394fe6003da714b359b00a171a`  
		Last Modified: Thu, 01 Feb 2024 00:04:52 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:5-buster` - unknown; unknown

```console
$ docker pull perl@sha256:43c13b68880ea5d2cf666f4d8e067253ff51af458756846f5d5cfad0bc977872
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.6 MB (13622956 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad1277475f9356263a51aa6be4d0203a85db813bde422e6ada9326900bf46c5b`

```dockerfile
```

-	Layers:
	-	`sha256:fa8a212616436851067a0394dc68730f546d3d7aa59e337323814bfbc71b890b`  
		Last Modified: Thu, 01 Feb 2024 00:04:50 GMT  
		Size: 13.6 MB (13606688 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7cc925330237e65e5978b16fbd8317db85253d925acc9d0bb7e1a862e01b3a88`  
		Last Modified: Thu, 01 Feb 2024 00:04:50 GMT  
		Size: 16.3 KB (16268 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:5-buster` - linux; arm variant v7

```console
$ docker pull perl@sha256:0d121fab83fd5054d316b89c6172628c0fe4bcc1e5baab4138f4b927cd83bf14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.5 MB (292508023 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82763b4a7ae592a8df9acb4a5dcb3d48d7144e2e92fbc97dbd8347e430541a82`
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
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/P/PE/PEVANS/perl-5.38.2.tar.gz -o perl-5.38.2.tar.gz     && echo 'a0a31534451eb7b83c7d6594a497543a54d488bc90ca00f5e34762577f40655e *perl-5.38.2.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.38.2.tar.gz -C /usr/src/perl     && rm perl-5.38.2.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997014/cpm -o /usr/local/bin/cpm     && echo 'ee525f2493e36c6f688eddabaf53a51c4d3b2a4ebaa81576ac8b9f78ab57f4a1 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
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
	-	`sha256:3ebda397af796b6e0449600156c74a452be4eccc692553df17393fe79bfc8443`  
		Last Modified: Sat, 03 Feb 2024 13:45:25 GMT  
		Size: 14.8 MB (14780518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:416956224ed9cb94105f96390dd4bad2e6e0caaae97df1f4f49014697426d2f1`  
		Last Modified: Sat, 03 Feb 2024 13:45:24 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:5-buster` - unknown; unknown

```console
$ docker pull perl@sha256:bd060af01d067df99361ec4f2cdfbb1bd9466be237b5340e2f2439816098e298
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.4 MB (13449969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c4d5988931c1da69ef88ecf52fa94b44ca7daf259753d9831289ecb1eff1a24`

```dockerfile
```

-	Layers:
	-	`sha256:6945120b8dba9c6247cba21c9fc9e1a16ceffb4404aa1b774d39b5e4e05e0272`  
		Last Modified: Sat, 03 Feb 2024 13:45:25 GMT  
		Size: 13.4 MB (13434286 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6dc4835931eca4520958fd16744442473bfeb2cfb80f7b22530dadf700f03d59`  
		Last Modified: Sat, 03 Feb 2024 13:45:24 GMT  
		Size: 15.7 KB (15683 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:5-buster` - linux; arm64 variant v8

```console
$ docker pull perl@sha256:3574e3be71e3b7cf5f5addc382196411e794e016c2b2869a3b64b7f8f875fa30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **318.1 MB (318072952 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa0c6be743e4dc65f9c0d25cb24c05424d059e24d3fe9f3f09b3a26783a94ce2`
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
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/P/PE/PEVANS/perl-5.38.2.tar.gz -o perl-5.38.2.tar.gz     && echo 'a0a31534451eb7b83c7d6594a497543a54d488bc90ca00f5e34762577f40655e *perl-5.38.2.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.38.2.tar.gz -C /usr/src/perl     && rm perl-5.38.2.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997014/cpm -o /usr/local/bin/cpm     && echo 'ee525f2493e36c6f688eddabaf53a51c4d3b2a4ebaa81576ac8b9f78ab57f4a1 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
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
	-	`sha256:cc1aef75fe2813476e8a3ed2a3938baa9f95b4f33b737b73fb7ab23089d30762`  
		Last Modified: Fri, 02 Feb 2024 14:31:50 GMT  
		Size: 15.6 MB (15607061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2a5c19cc63c5cb089031bd5f31bd694a06dc17a2650c31f6802e5d92c26ea0e`  
		Last Modified: Fri, 02 Feb 2024 14:31:50 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:5-buster` - unknown; unknown

```console
$ docker pull perl@sha256:707b9d47e33fa705a7ed510d61430313f381e6940fc5c0c132d5d21d3b6efc50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.6 MB (13614993 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24bacaa724a09ed07728e761144cf5f6f6507f3b74dba82bb7e5c262324a25b5`

```dockerfile
```

-	Layers:
	-	`sha256:8fc40c058d30871b3ad2264708d63f0dc28bbf2b3c65d2003af867a1cd1bd197`  
		Last Modified: Fri, 02 Feb 2024 14:31:48 GMT  
		Size: 13.6 MB (13598713 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:42c36e125cff21ca77cee5043e4079959ebad9d1ceb3b1221488491e043d4db2`  
		Last Modified: Fri, 02 Feb 2024 14:31:48 GMT  
		Size: 16.3 KB (16280 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:5-buster` - linux; 386

```console
$ docker pull perl@sha256:9fd46505246b768d15ecb8d3654ab9b0ee94c6a8e50d53949903a30a3fa623c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **336.5 MB (336488749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3c7c34b0d65d3cb6a058f5af6dc32925875edfc57da4ae7cf85264308ddc072`
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
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/P/PE/PEVANS/perl-5.38.2.tar.gz -o perl-5.38.2.tar.gz     && echo 'a0a31534451eb7b83c7d6594a497543a54d488bc90ca00f5e34762577f40655e *perl-5.38.2.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.38.2.tar.gz -C /usr/src/perl     && rm perl-5.38.2.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997014/cpm -o /usr/local/bin/cpm     && echo 'ee525f2493e36c6f688eddabaf53a51c4d3b2a4ebaa81576ac8b9f78ab57f4a1 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
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
	-	`sha256:79995d5c483973ea26b5d393bc0b763b4c1f6fa843aad0eb102cc3ad4e4dcf66`  
		Last Modified: Thu, 01 Feb 2024 01:06:11 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccfe7cb1851ab98b49da1b8fe06e1bc4c95d7e85f10fd785888df94726cc5b6f`  
		Last Modified: Thu, 01 Feb 2024 01:06:20 GMT  
		Size: 15.2 MB (15173982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b846a7631c362a07cfe71e2f51b78477ef1febae68cef3283acfd97e6874ec9c`  
		Last Modified: Thu, 01 Feb 2024 01:06:20 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:5-buster` - unknown; unknown

```console
$ docker pull perl@sha256:7287a1523e59d6d4b4b6b32a1fcaa29945a7d503d91e7a80d7242370b721bf5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.6 MB (13626384 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9699b807a912217ed00138cb566e152c9621e4436e002b0d7d4020370bd9915f`

```dockerfile
```

-	Layers:
	-	`sha256:09a1ca40f0f521e09480a1f63eb5fdac8d46dd9badfca8c94ec5bc0d048c6d90`  
		Last Modified: Thu, 01 Feb 2024 01:06:20 GMT  
		Size: 13.6 MB (13610150 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:25dbe4f080d1da665d5f1b33575cf723dfd4604aa01d6d0e66d79d455071e36f`  
		Last Modified: Thu, 01 Feb 2024 01:06:20 GMT  
		Size: 16.2 KB (16234 bytes)  
		MIME: application/vnd.in-toto+json
