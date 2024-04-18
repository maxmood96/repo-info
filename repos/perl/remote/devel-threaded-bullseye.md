## `perl:devel-threaded-bullseye`

```console
$ docker pull perl@sha256:5bb101d616b29e95c57b1f6497dfc97132cd9350896cba04dab792c2dc6bd39d
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

### `perl:devel-threaded-bullseye` - linux; amd64

```console
$ docker pull perl@sha256:e99fc0f08a0424009559f647e177260238a18b0ffc765396cc7eafd34c130599
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **338.4 MB (338389331 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a53d8c80543b22ff03847a5c77ac00e18922f5a7ca66af04f6623c51fe3b0ef7`
-	Default Command: `["perl5.39.9","-de0"]`

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
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/P/PE/PEVANS/perl-5.39.9.tar.gz -o perl-5.39.9.tar.gz     && echo 'c589d2e36cbb8db30fb73f661ef2c06ffe9c680f8ebe417169ec259b48ec2119 *perl-5.39.9.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.39.9.tar.gz -C /usr/src/perl     && rm perl-5.39.9.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997014/cpm -o /usr/local/bin/cpm     && echo 'ee525f2493e36c6f688eddabaf53a51c4d3b2a4ebaa81576ac8b9f78ab57f4a1 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Thu, 21 Mar 2024 18:18:23 GMT
WORKDIR /usr/src/app
# Thu, 21 Mar 2024 18:18:23 GMT
CMD ["perl5.39.9" "-de0"]
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
	-	`sha256:4f519f34fe793263925287a7f476cb45ffc7f6c9503014a8ef23053c05d33d3b`  
		Last Modified: Wed, 10 Apr 2024 07:02:20 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78fa431eb605f166584e3edbce20cfd4a010ff0402dfe5088a36c3eae3291909`  
		Last Modified: Wed, 10 Apr 2024 07:02:20 GMT  
		Size: 16.0 MB (15960928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a2908c1883979f290e3421637bc411447e624aff4d0ba96cbd2f5c8df693f57`  
		Last Modified: Wed, 10 Apr 2024 07:02:20 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-threaded-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:82b260135874480fe22ddb8132a3740247acd4046c0d1eb574869d115b3aea99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.0 MB (14989250 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8b5bf713d092c85fd1dcf7e82e8821b622397098fc90df36cb7561afe059e59`

```dockerfile
```

-	Layers:
	-	`sha256:bfe073ec3acec64bf6eaa10a1e164aff8bad280f1c7ef310859e3054a82333e1`  
		Last Modified: Wed, 10 Apr 2024 07:02:20 GMT  
		Size: 15.0 MB (14973378 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:31b4a70ab528a4b1c729d1e899dfd5492a38ca362ca359c550a4da7d2f431ffd`  
		Last Modified: Wed, 10 Apr 2024 07:02:19 GMT  
		Size: 15.9 KB (15872 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-threaded-bullseye` - linux; arm variant v5

```console
$ docker pull perl@sha256:d387221c367e01446f7ebd26a37d291a20b15d32444a70f3b171200b63578626
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **310.7 MB (310674716 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1256acca926f6de5de6416f322db1fa02ae94f557c42a76320881d847e1b4d01`
-	Default Command: `["perl5.39.9","-de0"]`

```dockerfile
# Thu, 21 Mar 2024 18:18:23 GMT
ADD file:1eb31b3bcff4decb2d77374005bc7e0451f76188c3586232986a3f72e069dd04 in / 
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
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/P/PE/PEVANS/perl-5.39.9.tar.gz -o perl-5.39.9.tar.gz     && echo 'c589d2e36cbb8db30fb73f661ef2c06ffe9c680f8ebe417169ec259b48ec2119 *perl-5.39.9.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.39.9.tar.gz -C /usr/src/perl     && rm perl-5.39.9.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997014/cpm -o /usr/local/bin/cpm     && echo 'ee525f2493e36c6f688eddabaf53a51c4d3b2a4ebaa81576ac8b9f78ab57f4a1 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Thu, 21 Mar 2024 18:18:23 GMT
WORKDIR /usr/src/app
# Thu, 21 Mar 2024 18:18:23 GMT
CMD ["perl5.39.9" "-de0"]
```

-	Layers:
	-	`sha256:73e28a24bff6aad570d221d844a24c5be13f1afcd4819e3c4842ae6b4ae928ed`  
		Last Modified: Wed, 10 Apr 2024 00:54:59 GMT  
		Size: 52.6 MB (52591634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4248f04ac8d108861dbe994d7550102128ab72a36f2e74ab8c4831cd3f62d60e`  
		Last Modified: Wed, 10 Apr 2024 04:56:29 GMT  
		Size: 15.4 MB (15374797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1659bd5d3219d4aa530cdde5907a7ec6f956403ff1fdc412cca4f0d6b591c179`  
		Last Modified: Wed, 10 Apr 2024 04:56:46 GMT  
		Size: 52.3 MB (52328994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78adabbe39c0815a36cf1d8811e270a15ac0d9983160eef6eddab0bfca7efabd`  
		Last Modified: Wed, 10 Apr 2024 04:57:22 GMT  
		Size: 175.2 MB (175154967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eba9153d8656c620d8723408d3800f2ba23a64ee3b3316963696a40092e71053`  
		Last Modified: Thu, 11 Apr 2024 08:58:33 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7313dfdd68f741436314531640399579c567cec2ae2c4b623bc3c50887a2fda4`  
		Last Modified: Thu, 11 Apr 2024 11:37:28 GMT  
		Size: 15.2 MB (15224058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f222f8deb686b32f815afc774724655d314948fdc6758b4f2fd5c846ac17225e`  
		Last Modified: Thu, 11 Apr 2024 11:37:27 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-threaded-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:8a60a8a24995a64bfeddb57b1d7749ba92d8e5929e0a0fd5b6e8b4a805c11ebb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 MB (14785157 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15f7463aeae36aab0969b405996271196883f39d7506b5b91035bcb3f62498e8`

```dockerfile
```

-	Layers:
	-	`sha256:c41a2717a0aa94c191c5e6b6f91abcf07312473a1ced2f5320e623e2260124a6`  
		Last Modified: Thu, 11 Apr 2024 11:37:28 GMT  
		Size: 14.8 MB (14769885 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2da049789ef3b283825218b813ca5c28be26331b0efecc5b4730d22921cd7c1a`  
		Last Modified: Thu, 11 Apr 2024 11:37:27 GMT  
		Size: 15.3 KB (15272 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-threaded-bullseye` - linux; arm variant v7

```console
$ docker pull perl@sha256:a3ef331ed710fe37d2a13cbfc516e53e7423b872f6a18d6444d19f4b0e27cfab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.9 MB (297937472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d0c2dafdf0b0ddf788c70c6ab56aeb4ec98506ae1d6df9366937499e4e75c8f`
-	Default Command: `["perl5.39.9","-de0"]`

```dockerfile
# Thu, 21 Mar 2024 18:18:23 GMT
ADD file:eb53aade3ed19f72413045948cad3084902fe630cc20789d2c2b5bc334679575 in / 
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
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/P/PE/PEVANS/perl-5.39.9.tar.gz -o perl-5.39.9.tar.gz     && echo 'c589d2e36cbb8db30fb73f661ef2c06ffe9c680f8ebe417169ec259b48ec2119 *perl-5.39.9.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.39.9.tar.gz -C /usr/src/perl     && rm perl-5.39.9.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997014/cpm -o /usr/local/bin/cpm     && echo 'ee525f2493e36c6f688eddabaf53a51c4d3b2a4ebaa81576ac8b9f78ab57f4a1 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Thu, 21 Mar 2024 18:18:23 GMT
WORKDIR /usr/src/app
# Thu, 21 Mar 2024 18:18:23 GMT
CMD ["perl5.39.9" "-de0"]
```

-	Layers:
	-	`sha256:23ca580217f1a6b17dba868e7ec34ae7fff221e07640fca532510daca8ed46f6`  
		Last Modified: Wed, 10 Apr 2024 01:04:48 GMT  
		Size: 50.2 MB (50246481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab89b030e474718221560707f98fb967bd582bc0f355ca5caf120fc5f25b2d58`  
		Last Modified: Wed, 10 Apr 2024 07:01:21 GMT  
		Size: 14.9 MB (14879245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ef8c5cdb2957e3cc1b26c037acafd549c7286845f8007127da85b383702cee3`  
		Last Modified: Wed, 10 Apr 2024 07:01:40 GMT  
		Size: 50.4 MB (50357907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0c48f55e50a2918f423e3f80c787998eca4a47eec492d7e81553c5a738f095b`  
		Last Modified: Wed, 10 Apr 2024 07:02:17 GMT  
		Size: 167.4 MB (167441750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e432281dc219585e3fabf953ba3d53b6efa29407ca0f3c2e6c8b03bbfba0490`  
		Last Modified: Fri, 12 Apr 2024 07:22:41 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27484412813689f49ec1e1946eb1556cebb3fee7772a705d46cc15e0a3582fd6`  
		Last Modified: Fri, 12 Apr 2024 09:29:01 GMT  
		Size: 15.0 MB (15011822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8aac12313b25e10b8712cdf01536bfcb5caa639bd8d58e5bcdb6c93f57691c4d`  
		Last Modified: Fri, 12 Apr 2024 09:29:00 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-threaded-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:e6afaf2932add70695c57621db586a9ed5f7f44ce37d6f0e1d734df8824c9a49
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 MB (14790531 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c48a3106036757c4aefd699350deb25c7774aff85ac0930fb98db32bd4f68d86`

```dockerfile
```

-	Layers:
	-	`sha256:02a0f8352c8be0eab5246ffe39a78752e9cce1912e98ccecc85729f213ad8ce7`  
		Last Modified: Fri, 12 Apr 2024 09:29:01 GMT  
		Size: 14.8 MB (14775259 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d8f3cd4b798578d8b53e692952fc4ba6901a3bfd4d8d491b73e209f1314368fb`  
		Last Modified: Fri, 12 Apr 2024 09:29:00 GMT  
		Size: 15.3 KB (15272 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-threaded-bullseye` - linux; arm64 variant v8

```console
$ docker pull perl@sha256:45271af8d73d739f4bc4f9c5d15142e6606f40072e5176bccceab8425929bc54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **330.0 MB (329952346 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:855c048a03982376f01c7c93c098836570a4200cd7b953792469707bcde48d33`
-	Default Command: `["perl5.39.9","-de0"]`

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
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/P/PE/PEVANS/perl-5.39.9.tar.gz -o perl-5.39.9.tar.gz     && echo 'c589d2e36cbb8db30fb73f661ef2c06ffe9c680f8ebe417169ec259b48ec2119 *perl-5.39.9.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.39.9.tar.gz -C /usr/src/perl     && rm perl-5.39.9.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997014/cpm -o /usr/local/bin/cpm     && echo 'ee525f2493e36c6f688eddabaf53a51c4d3b2a4ebaa81576ac8b9f78ab57f4a1 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Thu, 21 Mar 2024 18:18:23 GMT
WORKDIR /usr/src/app
# Thu, 21 Mar 2024 18:18:23 GMT
CMD ["perl5.39.9" "-de0"]
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
	-	`sha256:a6f693a84811e1f6df0c681a5c943fed8f319328603b17d5f543a4497ce76909`  
		Last Modified: Thu, 11 Apr 2024 08:23:08 GMT  
		Size: 15.9 MB (15865211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a94b65afd46ad3954bc69c0162027770f7e0a22bc25f791e9f466702913fa4fd`  
		Last Modified: Thu, 11 Apr 2024 08:23:07 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-threaded-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:4ac36df73ceea62a8f2ec9f1238f8d1e285c82e1ebfe88c8eb255e872832c397
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.0 MB (14991060 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ec0183fe0489b9f11401bc4895fd3eb9f9dc2f79864bf754229a4c2960dcf8b`

```dockerfile
```

-	Layers:
	-	`sha256:63b7441967e158e4e439bbbd9861613ab252598a4c36a8937b9fab1fc7923bf6`  
		Last Modified: Thu, 11 Apr 2024 08:23:08 GMT  
		Size: 15.0 MB (14975842 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7099c6916d8fd7b0379213b2e41e0b6ef38d7d22557018b7a704349587ead85c`  
		Last Modified: Thu, 11 Apr 2024 08:23:07 GMT  
		Size: 15.2 KB (15218 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-threaded-bullseye` - linux; 386

```console
$ docker pull perl@sha256:5fc209607b7ff72be1f5f36fa8fe1b6370b79ac231393bc8c9724c01287daad7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **343.7 MB (343651028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcdd4f8e82867ade0307df5cfe6a40600a561a224bf8b219cd52036d5ad1d21e`
-	Default Command: `["perl5.39.9","-de0"]`

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
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/P/PE/PEVANS/perl-5.39.9.tar.gz -o perl-5.39.9.tar.gz     && echo 'c589d2e36cbb8db30fb73f661ef2c06ffe9c680f8ebe417169ec259b48ec2119 *perl-5.39.9.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.39.9.tar.gz -C /usr/src/perl     && rm perl-5.39.9.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997014/cpm -o /usr/local/bin/cpm     && echo 'ee525f2493e36c6f688eddabaf53a51c4d3b2a4ebaa81576ac8b9f78ab57f4a1 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Thu, 21 Mar 2024 18:18:23 GMT
WORKDIR /usr/src/app
# Thu, 21 Mar 2024 18:18:23 GMT
CMD ["perl5.39.9" "-de0"]
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
	-	`sha256:e720bb7d465b648f173926c2f9a6f97b81ed4314401b86f8ad66abcf0bcaedb4`  
		Last Modified: Wed, 10 Apr 2024 09:04:17 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63cb15fcd99c8db31e360e1004355249b39554d7aa07c27d9d28a046789ecd34`  
		Last Modified: Wed, 10 Apr 2024 09:04:17 GMT  
		Size: 15.5 MB (15498357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b094666e043afddbd059734250491ad58c70e1dda54d643b05d19b9b7a66c1e`  
		Last Modified: Wed, 10 Apr 2024 09:04:16 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-threaded-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:688a38441c4ff47c00e61d4b1e302177caf5762cfa630810aec78ed4b7e2305c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.0 MB (14978063 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f07e36019dabe57abb4619ca78832697486ce89bf1cf8245304cf7fea654647a`

```dockerfile
```

-	Layers:
	-	`sha256:da0a4ecaa1800156e819581f23ea936060afc3c32cb66014ccc15be3b95825c8`  
		Last Modified: Wed, 10 Apr 2024 09:04:17 GMT  
		Size: 15.0 MB (14962214 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fb963fa92dec7910494e1103f6ee1df92487bc02d1b8dbc08f92cb9bd4c280ab`  
		Last Modified: Wed, 10 Apr 2024 09:04:16 GMT  
		Size: 15.8 KB (15849 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-threaded-bullseye` - linux; mips64le

```console
$ docker pull perl@sha256:62f649c6df0046331059986a0b652715956997a0dc60918ccfc6ed1418439e52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **316.6 MB (316627633 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8bf13c18f281fa449c848ad80166023606ca710c7306474159fb1d85d58c751`
-	Default Command: `["perl5.39.9","-de0"]`

```dockerfile
# Thu, 21 Mar 2024 18:18:23 GMT
ADD file:b9ae0499407c5db6a4d213452b2b485d2f0c9fae0792c77a629177988969faa3 in / 
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
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/P/PE/PEVANS/perl-5.39.9.tar.gz -o perl-5.39.9.tar.gz     && echo 'c589d2e36cbb8db30fb73f661ef2c06ffe9c680f8ebe417169ec259b48ec2119 *perl-5.39.9.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.39.9.tar.gz -C /usr/src/perl     && rm perl-5.39.9.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997014/cpm -o /usr/local/bin/cpm     && echo 'ee525f2493e36c6f688eddabaf53a51c4d3b2a4ebaa81576ac8b9f78ab57f4a1 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Thu, 21 Mar 2024 18:18:23 GMT
WORKDIR /usr/src/app
# Thu, 21 Mar 2024 18:18:23 GMT
CMD ["perl5.39.9" "-de0"]
```

-	Layers:
	-	`sha256:eade21836c93150a05690be18ba07f9d56297d4f2b59f348647ec05e7c1435cc`  
		Last Modified: Wed, 10 Apr 2024 01:22:42 GMT  
		Size: 53.3 MB (53309804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8bca85f765a047c080d3e09be0e52f8fa2f73c3a685e3fe6eb266733dcea65e`  
		Last Modified: Wed, 10 Apr 2024 15:49:45 GMT  
		Size: 15.7 MB (15734419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06ae3ab149a39251a612af123a349e1dc5fed6c4e6c2fd0dcdd471587d9f3d1d`  
		Last Modified: Wed, 10 Apr 2024 15:50:30 GMT  
		Size: 53.3 MB (53311077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4245946189955b46a9c5b538da5eed5252d87a1fd7f2f33fd5fb3289f5d6cb44`  
		Last Modified: Wed, 10 Apr 2024 15:52:29 GMT  
		Size: 179.1 MB (179097898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:397fafb1841fcd6786ac38db184f61af7dd6296280e138bf1f04f7b10359cb32`  
		Last Modified: Fri, 12 Apr 2024 11:21:17 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8571e457fd5412517b2da25e5adb8f015a86a7d19b50ed5b0dae728e89c89998`  
		Last Modified: Fri, 12 Apr 2024 16:49:34 GMT  
		Size: 15.2 MB (15174168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3b7d1ee2ae92f9d84df7ab1710ccb390128d71d6568f4315aea9b47791baf3a`  
		Last Modified: Fri, 12 Apr 2024 16:48:43 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-threaded-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:7a2f8334630eede730482673db6e45356695dad7d5c3cebf3bc3fc66f5c25037
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.0 KB (15043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:063850e88a98b7de93450293f875b60cfbceebe1b8b31c20927292365d19f891`

```dockerfile
```

-	Layers:
	-	`sha256:28fcebb0c3bdba2fab02d64247ba9f29ec8240f77d37771f1a0c19159e90bd10`  
		Last Modified: Fri, 12 Apr 2024 16:49:32 GMT  
		Size: 15.0 KB (15043 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-threaded-bullseye` - linux; ppc64le

```console
$ docker pull perl@sha256:4cb732d64c88725d3b08de98a95e2cdbf2f95aea3178529f11a26e24d04ed358
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **346.9 MB (346923891 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a9355221e5bce8915fb324107dc927089ad560b8f36cdea2a4b5e4fea18905d`
-	Default Command: `["perl5.39.9","-de0"]`

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
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/P/PE/PEVANS/perl-5.39.9.tar.gz -o perl-5.39.9.tar.gz     && echo 'c589d2e36cbb8db30fb73f661ef2c06ffe9c680f8ebe417169ec259b48ec2119 *perl-5.39.9.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.39.9.tar.gz -C /usr/src/perl     && rm perl-5.39.9.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997014/cpm -o /usr/local/bin/cpm     && echo 'ee525f2493e36c6f688eddabaf53a51c4d3b2a4ebaa81576ac8b9f78ab57f4a1 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Thu, 21 Mar 2024 18:18:23 GMT
WORKDIR /usr/src/app
# Thu, 21 Mar 2024 18:18:23 GMT
CMD ["perl5.39.9" "-de0"]
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
	-	`sha256:5dac92bf6341ccd19d03f8b9ef27ef990247b503894f190afb1d057a38faabf3`  
		Last Modified: Thu, 11 Apr 2024 07:23:02 GMT  
		Size: 16.0 MB (15980797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1917524cf0875eacab6d10c386fad7eeb9af022aca95cea2935599e7baf588b9`  
		Last Modified: Thu, 11 Apr 2024 07:23:01 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-threaded-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:6bd22d1226206ea5b8f86f112a5ef8a216a6cc56224c7f5af23680c3c77e36ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.0 MB (14957919 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a143a0d032475e3ebfaedc270b06e9a49b59a0cd7008d76c4f172bbc03fcbe8`

```dockerfile
```

-	Layers:
	-	`sha256:9e41b93d2d8e637e6dd620fdfc4263a7bb8f1152cfc0301802f1d2ac65ed8039`  
		Last Modified: Thu, 11 Apr 2024 07:23:02 GMT  
		Size: 14.9 MB (14942677 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:92b14c6882e285b5ea006282af912b290bb370befc0e74b9cbe4f0f7f303a67d`  
		Last Modified: Thu, 11 Apr 2024 07:23:01 GMT  
		Size: 15.2 KB (15242 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-threaded-bullseye` - linux; s390x

```console
$ docker pull perl@sha256:f2b191bf4c4dd1ea6990c3e2488fa36d68cae0ba48bb47f529b32161e902f871
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **312.3 MB (312334169 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b4293c87a03fb89c84034b85ab524d9702cfb3c72e3aee7d3e5348677f489a3`
-	Default Command: `["perl5.39.9","-de0"]`

```dockerfile
# Thu, 21 Mar 2024 18:18:23 GMT
ADD file:ca4cd0bb2344426b8777da3ac3278e42efb1e15064ff144111d7ecacdf3cbd4a in / 
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
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/P/PE/PEVANS/perl-5.39.9.tar.gz -o perl-5.39.9.tar.gz     && echo 'c589d2e36cbb8db30fb73f661ef2c06ffe9c680f8ebe417169ec259b48ec2119 *perl-5.39.9.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.39.9.tar.gz -C /usr/src/perl     && rm perl-5.39.9.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997014/cpm -o /usr/local/bin/cpm     && echo 'ee525f2493e36c6f688eddabaf53a51c4d3b2a4ebaa81576ac8b9f78ab57f4a1 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Thu, 21 Mar 2024 18:18:23 GMT
WORKDIR /usr/src/app
# Thu, 21 Mar 2024 18:18:23 GMT
CMD ["perl5.39.9" "-de0"]
```

-	Layers:
	-	`sha256:8d59905935c60c8e62d2bce55ff58a911d9ceda48b95f8209712af92b63b5ceb`  
		Last Modified: Wed, 10 Apr 2024 01:48:44 GMT  
		Size: 53.3 MB (53324935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:389d06a9a1a36eb81d725be8859911dbff14d557f54a14795436ae38ccd42a97`  
		Last Modified: Wed, 10 Apr 2024 07:31:55 GMT  
		Size: 15.6 MB (15641598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4ed65098ad9320ac0b40e4be7ea7a1b7169e2786089554bc580dd22bd53591c`  
		Last Modified: Wed, 10 Apr 2024 07:32:09 GMT  
		Size: 54.1 MB (54075652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ad291048530ded42ea1541cf11a0c743fbc2f8d434ea0ada83f8c96dce458a0`  
		Last Modified: Wed, 10 Apr 2024 07:32:37 GMT  
		Size: 173.0 MB (172991518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1de9f50c3f4c5a67756ef1e1a90f98ab648a8dabd937892e7104144823bf1dd6`  
		Last Modified: Sat, 13 Apr 2024 05:19:09 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fd2173d58f3aa11827d88e3d6172e6b8797567e68f67fa8f98c3ee18d4a956e`  
		Last Modified: Sat, 13 Apr 2024 12:23:27 GMT  
		Size: 16.3 MB (16300199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c39b0b83581c925c2f2609ac380a897aa0fd2d1c32af8130ea5740c140394c4d`  
		Last Modified: Sat, 13 Apr 2024 12:23:25 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-threaded-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:bd182ae260648899587e39f8e17b5c58b71a25f47cc6503502c96c8b29bfbfca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 MB (14810264 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a876ecd78cac3f94b35597ce502348057c886b06f6cc0884a33b89a51a512ee6`

```dockerfile
```

-	Layers:
	-	`sha256:afbfea16a2b5c9eba7d05ccf23509ac29716737f9d6488abc86a73df9fde59d8`  
		Last Modified: Sat, 13 Apr 2024 12:23:26 GMT  
		Size: 14.8 MB (14795054 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a815320684364d2152c3694c590a67d8a880366a32126b7f270949661e783efd`  
		Last Modified: Sat, 13 Apr 2024 12:23:25 GMT  
		Size: 15.2 KB (15210 bytes)  
		MIME: application/vnd.in-toto+json
