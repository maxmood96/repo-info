## `perl:5-buster`

```console
$ docker pull perl@sha256:7abfa89f9f3807a12a5ead234a0394692594cc862ad98c544f8b76f79bb1c7ec
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
$ docker pull perl@sha256:07c1d90caf772f828a8be788fd459ed1b99353cf12e5ab926d5128a6876251d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **327.8 MB (327763679 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96733cd90a5c71f31428f2955c787f08e0172a1b707f739050ac466e21fb8f91`
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
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/P/PE/PEVANS/perl-5.38.2.tar.gz -o perl-5.38.2.tar.gz     && echo 'a0a31534451eb7b83c7d6594a497543a54d488bc90ca00f5e34762577f40655e *perl-5.38.2.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.38.2.tar.gz -C /usr/src/perl     && rm perl-5.38.2.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997014/cpm -o /usr/local/bin/cpm     && echo 'ee525f2493e36c6f688eddabaf53a51c4d3b2a4ebaa81576ac8b9f78ab57f4a1 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
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
	-	`sha256:ea33eba33a9d9286dc6569e7b2421b91133c199a90593603ecfee71f1ed9c411`  
		Last Modified: Tue, 14 May 2024 04:04:22 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecbf5108fda89fdb08157aeff1cde1d99fde2141cc536f62b78566da9e4ec9db`  
		Last Modified: Tue, 14 May 2024 04:04:23 GMT  
		Size: 15.7 MB (15668301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09b8a848acf06343dca9f5766f3fa6476774a23a4e3f65c5d6696c639d167b0b`  
		Last Modified: Tue, 14 May 2024 04:04:22 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:5-buster` - unknown; unknown

```console
$ docker pull perl@sha256:f526b2797937e3b3c1368635c0cd77c587787e86b5a213336dbc02bb299ce9d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.0 MB (15982674 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e401859c72175cc5b4b87da9bf1da5d5a6f31f8e5b5d1fcf952858a26d2de90d`

```dockerfile
```

-	Layers:
	-	`sha256:ad52fe0883b59059210e364bd227cbd895196db0b47437e9973389752e30622c`  
		Last Modified: Tue, 14 May 2024 04:04:23 GMT  
		Size: 16.0 MB (15966402 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:32efa45ee6062c4a9b05ba1a339e9fb8a1caee6850f94f0db61fdd123322c109`  
		Last Modified: Tue, 14 May 2024 04:04:22 GMT  
		Size: 16.3 KB (16272 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:5-buster` - linux; arm variant v7

```console
$ docker pull perl@sha256:16d5b1371e27825d77657250f1af34d3938174d81428a1fe28cac4d4e3b61d1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.7 MB (292709722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ec0a5c1d730ad2b59ad2e8b0932ad6ae541b0bcf5559ed88edccf5bd2f9a284`
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
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/P/PE/PEVANS/perl-5.38.2.tar.gz -o perl-5.38.2.tar.gz     && echo 'a0a31534451eb7b83c7d6594a497543a54d488bc90ca00f5e34762577f40655e *perl-5.38.2.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.38.2.tar.gz -C /usr/src/perl     && rm perl-5.38.2.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997014/cpm -o /usr/local/bin/cpm     && echo 'ee525f2493e36c6f688eddabaf53a51c4d3b2a4ebaa81576ac8b9f78ab57f4a1 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
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
	-	`sha256:6bb157af0a38c662ef343236b0249ee3a881fd9d49068c6eba2a6e62e6ac1307`  
		Last Modified: Wed, 15 May 2024 04:37:53 GMT  
		Size: 14.8 MB (14782305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4afa775895895e3d9fafdf356e89703c7a131fc6afffe12e5348a76b732407b`  
		Last Modified: Wed, 15 May 2024 04:37:52 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:5-buster` - unknown; unknown

```console
$ docker pull perl@sha256:80ba53cb98dea9f6d87a5d3216261141e04cc0d6fc5235a24829963935c47af3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.8 MB (15784909 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aefb7548a48ea74bcc11ec334be4a03c57ba4ba7e845e1b495b0b3ca1d70e7d2`

```dockerfile
```

-	Layers:
	-	`sha256:add478fb8eddce64fe41b9471bc0b4e56f6d6caf7755d0336cfad9f1b239a502`  
		Last Modified: Wed, 15 May 2024 04:37:51 GMT  
		Size: 15.8 MB (15768560 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:97ccf7e0e24c1b518f8e4cfa5934df1cddf936a0f2cbc2a2eea3ff18134a92e6`  
		Last Modified: Wed, 15 May 2024 04:37:50 GMT  
		Size: 16.3 KB (16349 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:5-buster` - linux; arm64 variant v8

```console
$ docker pull perl@sha256:fb2b6ec6c1695a6ed39e5ff86fce09dd6ef664b4b7204fef30be0adc73d0a79a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **318.3 MB (318273908 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9072f0cfa57af00da8a90461bcbee53e9198e4f3841a41a4553a7a82f977c021`
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
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/P/PE/PEVANS/perl-5.38.2.tar.gz -o perl-5.38.2.tar.gz     && echo 'a0a31534451eb7b83c7d6594a497543a54d488bc90ca00f5e34762577f40655e *perl-5.38.2.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.38.2.tar.gz -C /usr/src/perl     && rm perl-5.38.2.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997014/cpm -o /usr/local/bin/cpm     && echo 'ee525f2493e36c6f688eddabaf53a51c4d3b2a4ebaa81576ac8b9f78ab57f4a1 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
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
	-	`sha256:638e9ed0ad70e6d38e7d508188f86446e532c2a96c173968397ac9ec36b03fba`  
		Last Modified: Thu, 25 Apr 2024 08:23:01 GMT  
		Size: 15.6 MB (15608652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecbad134d56e838d269cb85f298ac33882f77645970e1ffeb6bb26aa826149f8`  
		Last Modified: Thu, 25 Apr 2024 08:23:01 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:5-buster` - unknown; unknown

```console
$ docker pull perl@sha256:9747658b4cc327b515a95fad129bd0e4c1e1e5c2250e3fd9738a6b62d31aead2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.0 MB (15973545 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ecc99f3121ca42e327dd2ce60b62ca3b4050c32894253f05a5922fc9327bc942`

```dockerfile
```

-	Layers:
	-	`sha256:6987ece7d62dc680988122e97ad36becd127ad2df7a8c07e121c6301a6b4982f`  
		Last Modified: Thu, 25 Apr 2024 08:23:00 GMT  
		Size: 16.0 MB (15957261 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e74b9a0022e506589fbf35548ff88b22145dfd08822e5668f8400417e3170719`  
		Last Modified: Thu, 25 Apr 2024 08:22:58 GMT  
		Size: 16.3 KB (16284 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:5-buster` - linux; 386

```console
$ docker pull perl@sha256:b27ce405c37bdd280c0ccd94f68dc96203885fddd67984bb198fffaa62190807
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **336.7 MB (336676991 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fc1d354d2523a48da159ff8654ca6f51217b7b3e2efa08faec6a2b04d1d96d0`
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
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/P/PE/PEVANS/perl-5.38.2.tar.gz -o perl-5.38.2.tar.gz     && echo 'a0a31534451eb7b83c7d6594a497543a54d488bc90ca00f5e34762577f40655e *perl-5.38.2.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.38.2.tar.gz -C /usr/src/perl     && rm perl-5.38.2.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997014/cpm -o /usr/local/bin/cpm     && echo 'ee525f2493e36c6f688eddabaf53a51c4d3b2a4ebaa81576ac8b9f78ab57f4a1 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
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
	-	`sha256:865551133bdca991791bbe6d7a19885e0e509ffccb7d82481cd1275602354381`  
		Last Modified: Tue, 14 May 2024 10:05:29 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f99e73fef21ac50e88550a0d241f2bc16c889e7549cd0835f6dd4c3f540149a`  
		Last Modified: Tue, 14 May 2024 10:05:29 GMT  
		Size: 15.2 MB (15174768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb4091973b8539fe89ea48893fef8290f043565103e1a12b2ecddf160a3c963a`  
		Last Modified: Tue, 14 May 2024 10:05:29 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:5-buster` - unknown; unknown

```console
$ docker pull perl@sha256:ae364b6e81c169ba46b4b0d20ab9cb3743b4ef7ac81772f10593dfbf850bb81c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.0 MB (15988222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f8af13d900a270da4c722020c363b04992ae739d3dbe6d6a61fb1d7dde6f541`

```dockerfile
```

-	Layers:
	-	`sha256:a89c7d42e118a561aa54ef5bbd646f5f49ac2447f6220cc984421de17a998261`  
		Last Modified: Tue, 14 May 2024 10:05:29 GMT  
		Size: 16.0 MB (15971984 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4a50e749e9a04a75b7d3f785064027808f2df49ffa0195350ddc1be4dd0b19be`  
		Last Modified: Tue, 14 May 2024 10:05:28 GMT  
		Size: 16.2 KB (16238 bytes)  
		MIME: application/vnd.in-toto+json
