## `perl:threaded-buster`

```console
$ docker pull perl@sha256:baf9649c953c63d5e52e3800b7ed568d115686c01370830cd388c9477e49326b
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
$ docker pull perl@sha256:941eef46e9e3ef00ba4a413dbda3d92cf57042bf1203f9b6fd0dfd4533374325
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **327.8 MB (327822717 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:934d876e058098f5ca92d2ce32c4838184071ecd66fff91ee2520801cee96225`
-	Default Command: `["perl5.38.2","-de0"]`

```dockerfile
# Mon, 29 Apr 2024 09:51:00 GMT
ADD file:9062f3516bb9d149bc29e8f3ee94806152277d05a3f2ee0ba7bc2040d8bfc8d5 in / 
# Mon, 29 Apr 2024 09:51:00 GMT
CMD ["bash"]
# Mon, 29 Apr 2024 09:51:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 29 Apr 2024 09:51:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 29 Apr 2024 09:51:00 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 29 Apr 2024 09:51:00 GMT
WORKDIR /usr/src/perl
# Mon, 29 Apr 2024 09:51:00 GMT
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/P/PE/PEVANS/perl-5.38.2.tar.gz -o perl-5.38.2.tar.gz     && echo 'a0a31534451eb7b83c7d6594a497543a54d488bc90ca00f5e34762577f40655e *perl-5.38.2.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.38.2.tar.gz -C /usr/src/perl     && rm perl-5.38.2.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997014/cpm -o /usr/local/bin/cpm     && echo 'ee525f2493e36c6f688eddabaf53a51c4d3b2a4ebaa81576ac8b9f78ab57f4a1 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Mon, 29 Apr 2024 09:51:00 GMT
WORKDIR /usr/src/app
# Mon, 29 Apr 2024 09:51:00 GMT
CMD ["perl5.38.2" "-de0"]
```

-	Layers:
	-	`sha256:673c873103ec067ad3ce1763a9ed20efd4591771bc605ceede174e83eb25ee0d`  
		Last Modified: Tue, 14 May 2024 01:33:29 GMT  
		Size: 50.7 MB (50656909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b44f61bacd5268a0f7dbd851e763d6ee101c21d0af21e649584357d4443cd709`  
		Last Modified: Tue, 14 May 2024 03:06:14 GMT  
		Size: 17.6 MB (17586437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3e7d6cb6a5235443faadc8d241ebb270739fd828ca9f0b78c63a1e7f36f8405`  
		Last Modified: Tue, 14 May 2024 03:06:29 GMT  
		Size: 51.9 MB (51894320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79bc40752dd2cf0f18dcf07e73c1c85269734230ce7b22f18f4a4d120f54e608`  
		Last Modified: Tue, 14 May 2024 03:07:00 GMT  
		Size: 192.0 MB (191957446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e896c4ddba18c5913c58c3e9fc7f4181c32c86cadac492822f0e64ebe3ae9ff9`  
		Last Modified: Tue, 14 May 2024 04:04:14 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0816d589c2c44103c1781a40a9a0c7607442c1b6b4fea4c130f11e0d16f6d782`  
		Last Modified: Tue, 14 May 2024 04:05:04 GMT  
		Size: 15.7 MB (15727340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43d2952a7c0ebc85efa99f7bab6c219f7d81b77e5a52dd8cc169aa5018136c68`  
		Last Modified: Tue, 14 May 2024 04:05:04 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:threaded-buster` - unknown; unknown

```console
$ docker pull perl@sha256:736bc6799f51c9690238e9b7865559653333e2976b971f503207beab1de2e673
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.0 MB (15982901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c81b34573f271fc4ee82db8c18dc59bca8a7bc180f288ae46555cd1d55a6cd4`

```dockerfile
```

-	Layers:
	-	`sha256:181b1d067122681d82d53405c0bf503ff832c5817de6c5e28a6ecd9dc347dd2c`  
		Last Modified: Tue, 14 May 2024 04:05:04 GMT  
		Size: 16.0 MB (15966492 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fcc77f9929dc4f826a40a5a58f5c16852d9aebfaade498223b673bfd56e0c62d`  
		Last Modified: Tue, 14 May 2024 04:05:04 GMT  
		Size: 16.4 KB (16409 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:threaded-buster` - linux; arm variant v7

```console
$ docker pull perl@sha256:88c41d2dd024daa40e1b47d897685043f093ab76d733343faf5b98b60b2bad24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.7 MB (292731453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae37dfa228ddfa97ee7bc044026d2f624a5f8d99ec97f5572b3a1eb2f43f3642`
-	Default Command: `["perl5.38.2","-de0"]`

```dockerfile
# Mon, 29 Apr 2024 09:51:00 GMT
ADD file:a05edfdd56e92b1814d8e812ef81e814accd29893888392076dbc26b33b5ae41 in / 
# Mon, 29 Apr 2024 09:51:00 GMT
CMD ["bash"]
# Mon, 29 Apr 2024 09:51:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 29 Apr 2024 09:51:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 29 Apr 2024 09:51:00 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 29 Apr 2024 09:51:00 GMT
WORKDIR /usr/src/perl
# Mon, 29 Apr 2024 09:51:00 GMT
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/P/PE/PEVANS/perl-5.38.2.tar.gz -o perl-5.38.2.tar.gz     && echo 'a0a31534451eb7b83c7d6594a497543a54d488bc90ca00f5e34762577f40655e *perl-5.38.2.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.38.2.tar.gz -C /usr/src/perl     && rm perl-5.38.2.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997014/cpm -o /usr/local/bin/cpm     && echo 'ee525f2493e36c6f688eddabaf53a51c4d3b2a4ebaa81576ac8b9f78ab57f4a1 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Mon, 29 Apr 2024 09:51:00 GMT
WORKDIR /usr/src/app
# Mon, 29 Apr 2024 09:51:00 GMT
CMD ["perl5.38.2" "-de0"]
```

-	Layers:
	-	`sha256:66d6e1b7bddcb1c893c2c3e9b1ac8f5fca7c047037ed836079c97c9a917cd989`  
		Last Modified: Tue, 14 May 2024 01:13:47 GMT  
		Size: 46.1 MB (46129793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16e36c6c43e23d017283e609c78ad3425681f38a7cec50832f329aebf9f45a45`  
		Last Modified: Tue, 14 May 2024 01:49:06 GMT  
		Size: 16.2 MB (16217024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:780d070dbdc44447a3c019b1076d14827afec1e3d9f53f0941c341dde2f5b674`  
		Last Modified: Tue, 14 May 2024 01:49:23 GMT  
		Size: 47.4 MB (47410306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eeab1a68b064abb317c5afc7a68fdc8b46b5c9f37a1fad3e3d9664777a761c11`  
		Last Modified: Tue, 14 May 2024 01:49:55 GMT  
		Size: 168.2 MB (168170028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6881c0064fb53c495eb2113759bb6fb2b200c7f3d3192100e7d556d7a9e75e0d`  
		Last Modified: Wed, 15 May 2024 04:37:50 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a9ba2d6c9969f4b8a7c5d990ac6dda991596a6feba73e2186938657b37f8b1e`  
		Last Modified: Wed, 15 May 2024 05:11:23 GMT  
		Size: 14.8 MB (14804035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11f04a3304b77d985c0740d3ebb4fc06b51f5533cb08613f80b20fa86cebdab3`  
		Last Modified: Wed, 15 May 2024 05:11:22 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:threaded-buster` - unknown; unknown

```console
$ docker pull perl@sha256:0a374d413f00bed12f3110e0e5de45642022ef6e4c40ac8248bb87e2ff50f76f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.8 MB (15784474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2939588709f7967ffa20083ac0d45a65e9bb1418561a775761385336849fc606`

```dockerfile
```

-	Layers:
	-	`sha256:c0976239a79422d43acc142ac466d17cae7b968c044232ed135e01cbc55d7c14`  
		Last Modified: Wed, 15 May 2024 05:11:23 GMT  
		Size: 15.8 MB (15768650 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:743bff1926ca02f4499cc6cdab644dd11c112085c7e20b4bb56a5d8d318ad1c0`  
		Last Modified: Wed, 15 May 2024 05:11:22 GMT  
		Size: 15.8 KB (15824 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:threaded-buster` - linux; arm64 variant v8

```console
$ docker pull perl@sha256:0f124d6386fe2f98de57624a60d590cddce0a6d76d2d2894cd3fe584597ff25e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **318.3 MB (318305024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d307dc48fa2c728bdec2c2412379df547808a39361d9a8b2b3f8d253160fc72a`
-	Default Command: `["perl5.38.2","-de0"]`

```dockerfile
# Thu, 21 Mar 2024 18:18:23 GMT
ADD file:5a7db8f66ffc46a108f386106163b47bdb4a3bcbe5341a94d47988b259039067 in / 
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
	-	`sha256:38adae2f446d050038d7d914eddb5b4a481b4c3e73ec18c36be90c376b639389`  
		Last Modified: Wed, 24 Apr 2024 04:15:06 GMT  
		Size: 49.5 MB (49453161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcc15410e595a34b7a5d9e82b26d580e858211c5947bf56bb293ea57db35185c`  
		Last Modified: Wed, 24 Apr 2024 08:43:19 GMT  
		Size: 17.5 MB (17456193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8513aad98d9a17452335b87f52bab845a7a83392e5ebe6cc99b33a0959cf7a41`  
		Last Modified: Wed, 24 Apr 2024 08:43:33 GMT  
		Size: 52.2 MB (52231381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41858c667c6bef0ef068e6f0f96241c3650c1f4c036818f8797fd044dd3b1233`  
		Last Modified: Wed, 24 Apr 2024 08:43:58 GMT  
		Size: 183.5 MB (183524255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ddbe483d1f94d54a39c56a1498e29920e90c0eabbabd54640a75e241dfd3bc7`  
		Last Modified: Thu, 25 Apr 2024 08:22:59 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb9fdfe7f39e674f92bc77bfd34f18966a39fc5fe58d0400783084844a16dcc5`  
		Last Modified: Thu, 25 Apr 2024 09:20:29 GMT  
		Size: 15.6 MB (15639768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f58deafdc7384e249a7acb59218ddf9f6d758be4b8af2c7f4035c3ff28556f5`  
		Last Modified: Thu, 25 Apr 2024 09:20:27 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:threaded-buster` - unknown; unknown

```console
$ docker pull perl@sha256:d1eb30056bedc1f67ed536174e5d7aff96b05d581b85dc8c96af1318ea89fdff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.0 MB (15973109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a2cc31451ecf60ad0f6316e4c64cac9ebef2bff9daa35faf6695205b82f5fdb`

```dockerfile
```

-	Layers:
	-	`sha256:b59c70eadfb5b0aa57ab67f3c70d34cf81f36c560c0102eb0e739b925b8a97df`  
		Last Modified: Thu, 25 Apr 2024 09:20:28 GMT  
		Size: 16.0 MB (15957351 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:79258b718fe594fa32b68f57304621c5e5e552f9ff953670cb35c5a53d2ddb58`  
		Last Modified: Thu, 25 Apr 2024 09:20:27 GMT  
		Size: 15.8 KB (15758 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:threaded-buster` - linux; 386

```console
$ docker pull perl@sha256:1fd4090e4757d006b91e56e1e60b31f29a1973fa038f79e215dd8476e5d4ba88
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **336.8 MB (336777650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de402b07eb4c855e36a0187ef696c6135b03f07c4867235e3dbb0166d4a1fc09`
-	Default Command: `["perl5.38.2","-de0"]`

```dockerfile
# Mon, 29 Apr 2024 09:51:00 GMT
ADD file:5e59addfe8663b7c16cce40874c2a3c8601e20e80f5a0897c86b64ba463c10e9 in / 
# Mon, 29 Apr 2024 09:51:00 GMT
CMD ["bash"]
# Mon, 29 Apr 2024 09:51:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 29 Apr 2024 09:51:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 29 Apr 2024 09:51:00 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 29 Apr 2024 09:51:00 GMT
WORKDIR /usr/src/perl
# Mon, 29 Apr 2024 09:51:00 GMT
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/P/PE/PEVANS/perl-5.38.2.tar.gz -o perl-5.38.2.tar.gz     && echo 'a0a31534451eb7b83c7d6594a497543a54d488bc90ca00f5e34762577f40655e *perl-5.38.2.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.38.2.tar.gz -C /usr/src/perl     && rm perl-5.38.2.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997014/cpm -o /usr/local/bin/cpm     && echo 'ee525f2493e36c6f688eddabaf53a51c4d3b2a4ebaa81576ac8b9f78ab57f4a1 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Mon, 29 Apr 2024 09:51:00 GMT
WORKDIR /usr/src/app
# Mon, 29 Apr 2024 09:51:00 GMT
CMD ["perl5.38.2" "-de0"]
```

-	Layers:
	-	`sha256:1a892f56e4b10aaecbb51b3219d90bd0d8a1e955acd0624a6ef27ed086ba168c`  
		Last Modified: Tue, 14 May 2024 00:53:06 GMT  
		Size: 51.4 MB (51419713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df672f2f18886bf928d6070d3311b71a33f94ce9708b67ade8e00ea0ec6cf25c`  
		Last Modified: Tue, 14 May 2024 09:15:53 GMT  
		Size: 18.1 MB (18098325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20019971ec9aacb9b7c64eb51f32f35360675176e10007625a27813b8a8cd124`  
		Last Modified: Tue, 14 May 2024 09:16:13 GMT  
		Size: 53.5 MB (53491794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63a3d64f2a6cfb08d0e101f8b79c83a6035104799f3de7058346a363aa6a09f3`  
		Last Modified: Tue, 14 May 2024 09:16:59 GMT  
		Size: 198.5 MB (198492126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09bddb342e35e59844c96deb802ba67b68dc6c78d298a8a52840487ddb2a39c4`  
		Last Modified: Tue, 14 May 2024 10:06:19 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56e38a156758957788fe75aa11f44381085de3864701d197bd2f38327480be7b`  
		Last Modified: Tue, 14 May 2024 10:06:20 GMT  
		Size: 15.3 MB (15275428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d112b8b05996139c062ce94ca9306783879e657f80a70c2ff463a132fc47adc9`  
		Last Modified: Tue, 14 May 2024 10:06:19 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:threaded-buster` - unknown; unknown

```console
$ docker pull perl@sha256:bac15bf33a61e90853b3add387476ec0463e56fdec3a3a0358d230db3657fa68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.0 MB (15988449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97e1e0b0a3d0e605f995478f932a51f6e2476b41f3187fa338683a6eb79b2763`

```dockerfile
```

-	Layers:
	-	`sha256:038bbaf27f7e9d6105454f91d28e20272734971efffa27aead51afaed53c5fde`  
		Last Modified: Tue, 14 May 2024 10:06:20 GMT  
		Size: 16.0 MB (15972074 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3fa2557b1abffe7e6487138748aaca87e3762b90cfdfb1515fc16a060d32c7bf`  
		Last Modified: Tue, 14 May 2024 10:06:19 GMT  
		Size: 16.4 KB (16375 bytes)  
		MIME: application/vnd.in-toto+json
