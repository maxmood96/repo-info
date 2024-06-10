## `perl:5-threaded-buster`

```console
$ docker pull perl@sha256:c06dae9d921284e6ecd3edace2790f656687ed92a317723f239d7f62b8aac647
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

### `perl:5-threaded-buster` - linux; amd64

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

### `perl:5-threaded-buster` - unknown; unknown

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

### `perl:5-threaded-buster` - linux; arm variant v7

```console
$ docker pull perl@sha256:a90e2c6d4eda1bfcff3382e420723022720976fa60ebef3ef1a182a65b1b91a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **293.0 MB (293023378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:311f9e734e92072ebb53491c1dbda03c216dece3a349a925467238acbc0331e7`
-	Default Command: `["perl5.40.0","-de0"]`

```dockerfile
# Tue, 14 May 2024 01:09:12 GMT
ADD file:a05edfdd56e92b1814d8e812ef81e814accd29893888392076dbc26b33b5ae41 in / 
# Tue, 14 May 2024 01:09:13 GMT
CMD ["bash"]
# Tue, 14 May 2024 01:39:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 14 May 2024 01:39:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 14 May 2024 01:41:03 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 10 Jun 2024 03:33:39 GMT
WORKDIR /usr/src/perl
# Mon, 10 Jun 2024 03:33:39 GMT
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/H/HA/HAARG/perl-5.40.0.tar.gz -o perl-5.40.0.tar.gz     && echo 'c740348f357396327a9795d3e8323bafd0fe8a5c7835fc1cbaba0cc8dfe7161f *perl-5.40.0.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.40.0.tar.gz -C /usr/src/perl     && rm perl-5.40.0.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Mon, 10 Jun 2024 03:33:39 GMT
WORKDIR /usr/src/app
# Mon, 10 Jun 2024 03:33:39 GMT
CMD ["perl5.40.0" "-de0"]
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
	-	`sha256:aac4d78312c91d8822482c2c42f3864f1f9ff99e42a8ff015cc21c64e2788515`  
		Last Modified: Mon, 10 Jun 2024 21:15:29 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60c203fd1f97d80a44795f5d72b84cf50000969c3e12deb19f13653d65c29c44`  
		Last Modified: Mon, 10 Jun 2024 21:57:44 GMT  
		Size: 15.1 MB (15095958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5908080610e380e8671c5fb4b8ba9f6c1160a723dfd667944b6ce7002b3209b5`  
		Last Modified: Mon, 10 Jun 2024 21:57:41 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:5-threaded-buster` - unknown; unknown

```console
$ docker pull perl@sha256:214404691e12cce74556a9242bc755fe7433d5a24c30b3f13a870c5e8ad09df3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.8 MB (15784521 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91605b3e3add312ebb6d80ddbcc89af7841537d2e231b9c4a324893f2bbf7c53`

```dockerfile
```

-	Layers:
	-	`sha256:69583b54f835bd38f78943cbf58cfa655234696a3b1e0bca9ae803e70c1fc57c`  
		Last Modified: Mon, 10 Jun 2024 21:57:41 GMT  
		Size: 15.8 MB (15768649 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:14261c784860ec33a1caac875bc4a3e70696caa27ea990b8685ae4f6ff910db2`  
		Last Modified: Mon, 10 Jun 2024 21:57:40 GMT  
		Size: 15.9 KB (15872 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:5-threaded-buster` - linux; arm64 variant v8

```console
$ docker pull perl@sha256:955eaf6a885b401ecb0ff383e97f72d01cbc0ce21c6418081de39bb1ac5d5874
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **318.3 MB (318314890 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c66e11e8196df356dbfd537215e7ac7e26c9470e6cd918baed0505e7cdaf5a8`
-	Default Command: `["perl5.38.2","-de0"]`

```dockerfile
# Mon, 29 Apr 2024 09:51:00 GMT
ADD file:da8c3a2d966487a4e1bc0646a771d18df585d75dc24f095a1aaa762ce0841747 in / 
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
	-	`sha256:0a8090f4fec79fd213192f5f5c31c70546878a20b6c7ca023ff9001fb788f828`  
		Last Modified: Tue, 14 May 2024 00:43:49 GMT  
		Size: 49.5 MB (49453094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80e540eb6c9fa042a5d3f1166ea6b4d3806d751dcc600baff113c7e2b711719d`  
		Last Modified: Tue, 14 May 2024 01:54:42 GMT  
		Size: 17.5 MB (17456998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:334249e7f4554ad45c3998bd6a23aa8d7ecc535422903784fb251e6345d36f9a`  
		Last Modified: Tue, 14 May 2024 01:54:57 GMT  
		Size: 52.2 MB (52230498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:019b2124bd151541dda5ef935a2883293321b124587270f4c0c28495c25a1ca4`  
		Last Modified: Tue, 14 May 2024 01:55:22 GMT  
		Size: 183.5 MB (183534368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76ff331fd7cb85ed4df9f669857a56694294f4e88dddc2574c76bb5f4ce14b89`  
		Last Modified: Wed, 15 May 2024 11:07:00 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57c240ab149b475e25881cc319f8003b2f707e19bffdafe9a71d35bfada25fc5`  
		Last Modified: Wed, 15 May 2024 11:23:24 GMT  
		Size: 15.6 MB (15639667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3957a3e0fa3c18d66253506570747cdf3b546023ec86e9127b98ec3c2b3ba173`  
		Last Modified: Wed, 15 May 2024 11:23:23 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:5-threaded-buster` - unknown; unknown

```console
$ docker pull perl@sha256:abd4af69d629110b34ceef0ca22ebe51ae7950881028cec5f24b9388b93b8141
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.0 MB (15973109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34eb5e270eab2da1594816fdd5b00d27968614b01ca9e8369b4b4fc2a5532356`

```dockerfile
```

-	Layers:
	-	`sha256:2f43a8b153b738a556b879e9d0c6de4267e412c5b93329db6219766d7730b005`  
		Last Modified: Wed, 15 May 2024 11:23:24 GMT  
		Size: 16.0 MB (15957351 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3372a4e93ea9d239c9eac23d4b6d27b0da914892409cbf8d41b8607d7e89f3a5`  
		Last Modified: Wed, 15 May 2024 11:23:23 GMT  
		Size: 15.8 KB (15758 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:5-threaded-buster` - linux; 386

```console
$ docker pull perl@sha256:17b900e09eab6d4065e124b39b2f09108b6b968432f8a5a292c54985b16f6756
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **337.1 MB (337077229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:171c514586eb769211b681a816dbe7c7ee012b2094eef09acb7d8bd4fd4cf3c9`
-	Default Command: `["perl5.40.0","-de0"]`

```dockerfile
# Tue, 14 May 2024 00:47:45 GMT
ADD file:5e59addfe8663b7c16cce40874c2a3c8601e20e80f5a0897c86b64ba463c10e9 in / 
# Tue, 14 May 2024 00:47:45 GMT
CMD ["bash"]
# Tue, 14 May 2024 09:05:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 14 May 2024 09:05:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 14 May 2024 09:07:14 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 10 Jun 2024 03:33:39 GMT
WORKDIR /usr/src/perl
# Mon, 10 Jun 2024 03:33:39 GMT
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/H/HA/HAARG/perl-5.40.0.tar.gz -o perl-5.40.0.tar.gz     && echo 'c740348f357396327a9795d3e8323bafd0fe8a5c7835fc1cbaba0cc8dfe7161f *perl-5.40.0.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.40.0.tar.gz -C /usr/src/perl     && rm perl-5.40.0.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997017/cpm -o /usr/local/bin/cpm     && echo 'e3931a7d994c96f9c74b97d1b5b75a554fc4f06eadef1eca26ecc0bdcd1f2d11 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Mon, 10 Jun 2024 03:33:39 GMT
WORKDIR /usr/src/app
# Mon, 10 Jun 2024 03:33:39 GMT
CMD ["perl5.40.0" "-de0"]
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
	-	`sha256:32a582385414bc38b45614a81a032b8a6f26bd9db133725355662b4c1a8f69ad`  
		Last Modified: Mon, 10 Jun 2024 21:04:36 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74d8b4e0ddf4d0729363d967f700804d484c9cacf33c3191f0acab5878717157`  
		Last Modified: Mon, 10 Jun 2024 21:04:37 GMT  
		Size: 15.6 MB (15575003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:197aa3bfaa4c25f44cd15f7b55b6a0d3950a61e8f9401125e934bbdfb60dda96`  
		Last Modified: Mon, 10 Jun 2024 21:04:22 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:5-threaded-buster` - unknown; unknown

```console
$ docker pull perl@sha256:29414e4ec04092e929a520234e1cb8e98296949be0ee1d8d78a0ea56e2383e3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.0 MB (15987831 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0163e7e1eb7faeb9b50c44a3e34be2dfc636bd461d4571e3e67df9aaf586af88`

```dockerfile
```

-	Layers:
	-	`sha256:adba1257eb79c2265aec38b7285dcde1f3d63a014c3c195a25ae612e078f86cb`  
		Last Modified: Mon, 10 Jun 2024 21:04:36 GMT  
		Size: 16.0 MB (15972073 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:26853f8667e0a7a0378d698dc91c5081abea5cdf7e645a9798e53caf991e506a`  
		Last Modified: Mon, 10 Jun 2024 21:04:36 GMT  
		Size: 15.8 KB (15758 bytes)  
		MIME: application/vnd.in-toto+json
