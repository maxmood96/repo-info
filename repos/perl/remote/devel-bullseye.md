## `perl:devel-bullseye`

```console
$ docker pull perl@sha256:ea003cd72ec79c957ae6fcf2253c923747dbe179f5515802f61e10e041b0fa93
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

### `perl:devel-bullseye` - linux; amd64

```console
$ docker pull perl@sha256:c0f942e14efa8178a447dad28d573dcc844aa10e5885b942003a1e1fd59bb645
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **338.3 MB (338335352 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:498d5c9532b47ef545859dba3a258e3a32eeb208ba2e0db0c963a4d07c8c44a3`
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
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/P/PE/PEVANS/perl-5.39.9.tar.gz -o perl-5.39.9.tar.gz     && echo 'c589d2e36cbb8db30fb73f661ef2c06ffe9c680f8ebe417169ec259b48ec2119 *perl-5.39.9.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.39.9.tar.gz -C /usr/src/perl     && rm perl-5.39.9.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997014/cpm -o /usr/local/bin/cpm     && echo 'ee525f2493e36c6f688eddabaf53a51c4d3b2a4ebaa81576ac8b9f78ab57f4a1 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
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
	-	`sha256:28c3ee7029392901818ad8c6d3cc2e110661777b3f00ab66fba1c22e14024138`  
		Last Modified: Wed, 10 Apr 2024 07:01:15 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f9f97839d49d009453a95b5ee576777359ba4d526aa34e24fd7828bad6e9306`  
		Last Modified: Wed, 10 Apr 2024 07:01:46 GMT  
		Size: 15.9 MB (15906948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec41c0a9544edfdf4169ccf1c03df889d1e13bad68e3d4f62bd41c8bf2cab722`  
		Last Modified: Wed, 10 Apr 2024 07:01:45 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:5caf63d38b13315c832e47e40205e4aec969abda23b49436fa6b5d7dae56c035
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.0 MB (14989096 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1707c3c069f71e22d8048330596481083b1456c9b56acbfdb960d22e17ff7e44`

```dockerfile
```

-	Layers:
	-	`sha256:a64be1455b8f002c99582f835518fd4c772673d3b32e6a339b5aa08c9d876a08`  
		Last Modified: Wed, 10 Apr 2024 07:01:46 GMT  
		Size: 15.0 MB (14973324 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9990b0c1aa3e9d99612995330f820b3960ac89057ff38ecc74773c1e7dd88f61`  
		Last Modified: Wed, 10 Apr 2024 07:01:45 GMT  
		Size: 15.8 KB (15772 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-bullseye` - linux; arm variant v5

```console
$ docker pull perl@sha256:439284ed6ee7f020c57386c144cba3682857b14f37c464354b86ce496b3ad37c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **310.6 MB (310637949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27511f6f9a615cce9f5baa4708d6da1253c25f9c7d4aa14474c138b5bddba9d8`
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
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/P/PE/PEVANS/perl-5.39.9.tar.gz -o perl-5.39.9.tar.gz     && echo 'c589d2e36cbb8db30fb73f661ef2c06ffe9c680f8ebe417169ec259b48ec2119 *perl-5.39.9.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.39.9.tar.gz -C /usr/src/perl     && rm perl-5.39.9.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997014/cpm -o /usr/local/bin/cpm     && echo 'ee525f2493e36c6f688eddabaf53a51c4d3b2a4ebaa81576ac8b9f78ab57f4a1 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
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
	-	`sha256:80afcf3ea38f499beecb0f37fe3b7de82e4d19d0398c231051f025d6b0d0c747`  
		Last Modified: Thu, 11 Apr 2024 11:14:45 GMT  
		Size: 15.2 MB (15187289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ac898723927bcab5de8965e756650f2b3ef85936300ade6cb91e2085dd6164d`  
		Last Modified: Thu, 11 Apr 2024 11:14:44 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:8e71d28848aebb725ad47d0a83a0bd39aa20edd60b82ee62ca7b65aac912c03a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 MB (14785002 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3eb5a30ac637e942af89e551dfba806fbec5925f253486ef256bba5dfd978ac3`

```dockerfile
```

-	Layers:
	-	`sha256:d1be13c42b444368316119ea08b933072699fedde0c1f1c179ffe8abbb47db00`  
		Last Modified: Thu, 11 Apr 2024 11:14:45 GMT  
		Size: 14.8 MB (14769831 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d521da39c223c785aceadcdba567d43824affcd355dac249f2db1c576792e1fe`  
		Last Modified: Thu, 11 Apr 2024 11:14:44 GMT  
		Size: 15.2 KB (15171 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-bullseye` - linux; arm variant v7

```console
$ docker pull perl@sha256:edcc9a4e0e23f98a81db08ce0eb2c8483c5b0aede1eff6e8ed5e3d8944d4fb21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.9 MB (297914481 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:000b55f7885fc0f3f7e841b7856fc8df64a68eef13d4dfc05770b51e5cb48a7e`
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
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/P/PE/PEVANS/perl-5.39.9.tar.gz -o perl-5.39.9.tar.gz     && echo 'c589d2e36cbb8db30fb73f661ef2c06ffe9c680f8ebe417169ec259b48ec2119 *perl-5.39.9.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.39.9.tar.gz -C /usr/src/perl     && rm perl-5.39.9.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997014/cpm -o /usr/local/bin/cpm     && echo 'ee525f2493e36c6f688eddabaf53a51c4d3b2a4ebaa81576ac8b9f78ab57f4a1 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
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
	-	`sha256:5334ab8d105aadee6440c0dc51502e46540b871643fb8811d8bdd2fb8dfa953a`  
		Last Modified: Fri, 12 Apr 2024 09:16:01 GMT  
		Size: 15.0 MB (14988833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b40d804c7468ef3415ffac4a04b9cddbc232454c026b5b4c8bc3ff929a3bfff`  
		Last Modified: Fri, 12 Apr 2024 09:16:00 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:2285ba09213baa87038bfd82102b797f96f342791cd8c85bfae40fc21b3cb8d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 MB (14790376 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6db4e796baefc840602106a71c5ca378624a5d5be2da704bf5a8d7d4d7180168`

```dockerfile
```

-	Layers:
	-	`sha256:55e2e5d4f1d4e69bbd2d0fa354bfcee6d03af540fcd1eeb0f304ca7c4f3273a9`  
		Last Modified: Fri, 12 Apr 2024 09:16:01 GMT  
		Size: 14.8 MB (14775205 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:242b89a615661f0f42d316874be3fb4a3cd19dfc156d891f3ad842b3878dd913`  
		Last Modified: Fri, 12 Apr 2024 09:16:00 GMT  
		Size: 15.2 KB (15171 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-bullseye` - linux; arm64 variant v8

```console
$ docker pull perl@sha256:531c59faf99b20c9a024dcebf01118eb7e5f163dc1a49af33dbdda9f3df30730
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **329.9 MB (329925634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b36f9d2dcca6fc16411dca79ba1c15917384961b96693a81903a9028b2a7f9e5`
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
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/P/PE/PEVANS/perl-5.39.9.tar.gz -o perl-5.39.9.tar.gz     && echo 'c589d2e36cbb8db30fb73f661ef2c06ffe9c680f8ebe417169ec259b48ec2119 *perl-5.39.9.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.39.9.tar.gz -C /usr/src/perl     && rm perl-5.39.9.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997014/cpm -o /usr/local/bin/cpm     && echo 'ee525f2493e36c6f688eddabaf53a51c4d3b2a4ebaa81576ac8b9f78ab57f4a1 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
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
	-	`sha256:0c07493db6a521b8224568dfbc4191a3c79ba837e82ad9a40f73fa1833bf7ff1`  
		Last Modified: Thu, 11 Apr 2024 08:01:08 GMT  
		Size: 15.8 MB (15838498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8785a8cd230b2baaf3d27ead7385156ac335eee3c62aef6fd7dde359d24589f9`  
		Last Modified: Thu, 11 Apr 2024 08:01:07 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:bd2244bf9afe4d5dd809e8d47b01823becd625cf5968964d56e6fef37115ce27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.0 MB (14990905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81964bba87bf5dee1b2e3a59933ee92e1f9b2805e140e2aaeb9089522e740d75`

```dockerfile
```

-	Layers:
	-	`sha256:e3ca2648e18e01f26b9eac76c4fe7a10ece9944332195cfe989863cfd47d62af`  
		Last Modified: Thu, 11 Apr 2024 08:01:08 GMT  
		Size: 15.0 MB (14975788 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2bae18591b9930f38c18c21fee654189ff9d05a55c67265c4e66cd446261df71`  
		Last Modified: Thu, 11 Apr 2024 08:01:07 GMT  
		Size: 15.1 KB (15117 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-bullseye` - linux; 386

```console
$ docker pull perl@sha256:e9f9789a8d719d1cb8f6e9e55a76dddbb512249b757a9b4b4e701f9769a16f0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **343.6 MB (343554290 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:baf80b56c4989b09c2f09fc7e5b93d5e01569f966628a0a324cd56bd73692302`
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
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/P/PE/PEVANS/perl-5.39.9.tar.gz -o perl-5.39.9.tar.gz     && echo 'c589d2e36cbb8db30fb73f661ef2c06ffe9c680f8ebe417169ec259b48ec2119 *perl-5.39.9.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.39.9.tar.gz -C /usr/src/perl     && rm perl-5.39.9.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997014/cpm -o /usr/local/bin/cpm     && echo 'ee525f2493e36c6f688eddabaf53a51c4d3b2a4ebaa81576ac8b9f78ab57f4a1 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
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
	-	`sha256:603be8a5850f259e1cd3d574c063a066f14e8462cb5c9953ea343210cedeeda0`  
		Last Modified: Wed, 10 Apr 2024 09:03:16 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:534329cc82dfcce6e250479868c9f9f41b2ee60906f1e996e00dbeac9643abcb`  
		Last Modified: Wed, 10 Apr 2024 09:03:17 GMT  
		Size: 15.4 MB (15401618 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1548bf6bfd77eec62807ce9f3d91cfa0a227135a5f0eb64bbadf083ed1d2e216`  
		Last Modified: Wed, 10 Apr 2024 09:03:16 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:ecf2205a73fd0a8d39d6b8e81c74c35095bbae2354cd6f5bde772d46a59ea6f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.0 MB (14977908 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4d24fd4b080ae24e7d3ab9a631d92cf0ef63576f545121ea351f52b04c1c801`

```dockerfile
```

-	Layers:
	-	`sha256:86fd7080e9bd8261837752bfb5ca03e1c886c6fa921afa87bb82b2e02b9bec4c`  
		Last Modified: Wed, 10 Apr 2024 09:03:17 GMT  
		Size: 15.0 MB (14962160 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:12d8d8d168897be1de774f569b70b908ea8f6892ccbf404b31a37213dc2a9923`  
		Last Modified: Wed, 10 Apr 2024 09:03:16 GMT  
		Size: 15.7 KB (15748 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-bullseye` - linux; mips64le

```console
$ docker pull perl@sha256:ad4de363d26243a790c188d9c58e73334532245669277269f16e472835860640
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **316.6 MB (316563128 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db50e66ef0db960aa6bbeea3322a4d23e358823c936c05eb068969fd989dadca`
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
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/P/PE/PEVANS/perl-5.39.9.tar.gz -o perl-5.39.9.tar.gz     && echo 'c589d2e36cbb8db30fb73f661ef2c06ffe9c680f8ebe417169ec259b48ec2119 *perl-5.39.9.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.39.9.tar.gz -C /usr/src/perl     && rm perl-5.39.9.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997014/cpm -o /usr/local/bin/cpm     && echo 'ee525f2493e36c6f688eddabaf53a51c4d3b2a4ebaa81576ac8b9f78ab57f4a1 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
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
	-	`sha256:774fc12541de9945f264e77171b72081efc727e6aad772f0088b6be7876c2b27`  
		Last Modified: Fri, 12 Apr 2024 15:48:33 GMT  
		Size: 15.1 MB (15109664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7d67fed58619d321dd2e61fa9aa151212fc6d73968deae92ffbefd1210ef9f4`  
		Last Modified: Fri, 12 Apr 2024 15:48:31 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:4c05d1cf870283de2ba1015c7a7538c8a34bcaaffbd50f709c64f27fc81e7b36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 KB (14942 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:691724dabdbddeaa0dcf15398b6615d6745ce3da2d8972ab980b5ad8e64c2aef`

```dockerfile
```

-	Layers:
	-	`sha256:1b7142ef115cd053a14ff45b29227069fa7ca10f0336c964a2a63701a74e0083`  
		Last Modified: Fri, 12 Apr 2024 15:48:31 GMT  
		Size: 14.9 KB (14942 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-bullseye` - linux; ppc64le

```console
$ docker pull perl@sha256:8cae956efcab1e1ec37f743c00e220347f7bfc63c0065fe80ada9ecc3ecaad9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **346.8 MB (346842347 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f826bcd4376c61a18c462fc4bb11737fcb2603a077721f6176f1b62b1a4bd11e`
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
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/P/PE/PEVANS/perl-5.39.9.tar.gz -o perl-5.39.9.tar.gz     && echo 'c589d2e36cbb8db30fb73f661ef2c06ffe9c680f8ebe417169ec259b48ec2119 *perl-5.39.9.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.39.9.tar.gz -C /usr/src/perl     && rm perl-5.39.9.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997014/cpm -o /usr/local/bin/cpm     && echo 'ee525f2493e36c6f688eddabaf53a51c4d3b2a4ebaa81576ac8b9f78ab57f4a1 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
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
	-	`sha256:7566cb25d6b452b773ea33a752cec5f2f3dd4ef5d22cea229e7a6baa458126d7`  
		Last Modified: Thu, 11 Apr 2024 06:46:52 GMT  
		Size: 15.9 MB (15899250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cae8e6e4a5bea1fddacd063a8897e09ac666c67f8227141b5f015e039357f980`  
		Last Modified: Thu, 11 Apr 2024 06:46:51 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:b931b28f7f00c23ce9c327c33c76ff94809c36b70beedd8ffdca1a918b1ae68c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.0 MB (14957763 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8382dd16ec87b9fc49dfdee88f141141401f03dae69ff51d89ad9263e7f24086`

```dockerfile
```

-	Layers:
	-	`sha256:2ea2e13d368cae05a89c04b3aa17f87401e9695f40047eff00781f7939970fa6`  
		Last Modified: Thu, 11 Apr 2024 06:46:52 GMT  
		Size: 14.9 MB (14942623 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:96921411d4193a2bf8667dcafa124b401a86889719bd7ed8b24509f689a8ef1e`  
		Last Modified: Thu, 11 Apr 2024 06:46:50 GMT  
		Size: 15.1 KB (15140 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-bullseye` - linux; s390x

```console
$ docker pull perl@sha256:4e230f8a4642ab230851ac66967bcaef73456d65ea28cad6afb86e384695cf2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **312.3 MB (312295271 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd18ac1035a7969b4da85cd48b72e9bba3c7d773b772f30c0549c538b7fb13d2`
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
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/P/PE/PEVANS/perl-5.39.9.tar.gz -o perl-5.39.9.tar.gz     && echo 'c589d2e36cbb8db30fb73f661ef2c06ffe9c680f8ebe417169ec259b48ec2119 *perl-5.39.9.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.39.9.tar.gz -C /usr/src/perl     && rm perl-5.39.9.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997014/cpm -o /usr/local/bin/cpm     && echo 'ee525f2493e36c6f688eddabaf53a51c4d3b2a4ebaa81576ac8b9f78ab57f4a1 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
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
	-	`sha256:6b2ac12edecdb6311e82142ab55e1d3b88769dd2674bdf20e7d777e7a9e57d67`  
		Last Modified: Sat, 13 Apr 2024 11:22:17 GMT  
		Size: 16.3 MB (16261301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ec2eafcc3f750af5db9e5da40fde26ef56de16f90d44945f210dd14de472f2e`  
		Last Modified: Sat, 13 Apr 2024 11:22:16 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-bullseye` - unknown; unknown

```console
$ docker pull perl@sha256:b06251bcff11b57e0e3d9835072ab3923f9b3df892a9d1850ddc2b07e04fb8ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 MB (14810109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3deb09f01ad3b4cda215175878c8892758b7bdc123493462fdb7d08f6f1d43e`

```dockerfile
```

-	Layers:
	-	`sha256:269c98650692b16d2ad6c8ffe8c4a18780883e71a187c403089450fb632982b5`  
		Last Modified: Sat, 13 Apr 2024 11:22:16 GMT  
		Size: 14.8 MB (14795000 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ca73633a06fd953c5fd96345386c13c386eed5eddb26589f4bf37666496f55bf`  
		Last Modified: Sat, 13 Apr 2024 11:22:16 GMT  
		Size: 15.1 KB (15109 bytes)  
		MIME: application/vnd.in-toto+json
