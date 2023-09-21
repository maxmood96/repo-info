## `perl:devel-threaded-bullseye`

```console
$ docker pull perl@sha256:bd8b7f456535bf2dae9559384ef401f6eaeef8127f123d952fddcd99c97b1f4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 8
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; s390x

### `perl:devel-threaded-bullseye` - linux; amd64

```console
$ docker pull perl@sha256:02d2f985e3fd17a18a8e2e7b6252fc72fa0853e05675d304304ae3f33e0cbad6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **337.9 MB (337922791 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0e38fa05ff885a725c00e2440b0e91f0c44820617235f9b1ce1a3849ec11b80`
-	Default Command: `["perl5.39.2","-de0"]`

```dockerfile
# Wed, 20 Sep 2023 04:55:51 GMT
ADD file:85db4f4c5016f51f7112a5d09cb7d4620f565a1379ae4b8a03c5ffc23886a876 in / 
# Wed, 20 Sep 2023 04:55:51 GMT
CMD ["bash"]
# Wed, 20 Sep 2023 09:22:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 20 Sep 2023 09:22:32 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 20 Sep 2023 09:23:31 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 20 Sep 2023 12:31:20 GMT
LABEL maintainer=Peter Martini <PeterCMartini@GMail.com>, Zak B. Elep <zakame@cpan.org>
# Wed, 20 Sep 2023 12:31:20 GMT
WORKDIR /usr/src/perl
# Wed, 20 Sep 2023 16:10:37 GMT
RUN true     && curl -fL https://www.cpan.org/src/5.0/perl-5.39.2.tar.xz -o perl-5.39.2.tar.xz     && echo 'b7ae33d3c6ff80107d14c92dfb3d8d4944fec926b11bcc40c8764b73c710694f *perl-5.39.2.tar.xz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.39.2.tar.xz -C /usr/src/perl     && rm perl-5.39.2.tar.xz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997011/cpm -o /usr/local/bin/cpm     && echo '7dee2176a450a8be3a6b9b91dac603a0c3a7e807042626d3fe6c93d843f75610 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version
# Wed, 20 Sep 2023 16:10:37 GMT
WORKDIR /usr/src/app
# Wed, 20 Sep 2023 16:10:38 GMT
CMD ["perl5.39.2" "-de0"]
```

-	Layers:
	-	`sha256:ddf874abf16cc990e0fd75a154a34ca0a03ee310ad895a18fb62ae15bf4171fb`  
		Last Modified: Wed, 20 Sep 2023 05:00:41 GMT  
		Size: 55.1 MB (55056714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c1459d3ab8b5e46ac1a0a00134fe2f7b693474eb6d75ace97ecbe811a6f5b0e`  
		Last Modified: Wed, 20 Sep 2023 09:31:06 GMT  
		Size: 15.8 MB (15760408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29ab00e7798a04602c3f6e2dc445a994d75e96c45533cd44701f58509982a8c5`  
		Last Modified: Wed, 20 Sep 2023 09:31:23 GMT  
		Size: 54.6 MB (54584790 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7883a473306cf6632abe7e913e0f1a21ac2fed038a4116473b25738b8b88b294`  
		Last Modified: Wed, 20 Sep 2023 09:31:55 GMT  
		Size: 196.8 MB (196842512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b52b3edeb95fa7a0041689ffc83f83c850c381908d41acdd82e901f87878cdfd`  
		Last Modified: Wed, 20 Sep 2023 16:26:00 GMT  
		Size: 166.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:800b1193fed3c7e60e3546d1ae49e09bd14f18e6d3df4f2bfccc66912c2cd923`  
		Last Modified: Wed, 20 Sep 2023 16:35:57 GMT  
		Size: 15.7 MB (15678037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:700f76d91bbed00cdaaab4f99bab1fa2f54348d106602a44e6cd9f2965e42357`  
		Last Modified: Wed, 20 Sep 2023 16:35:54 GMT  
		Size: 164.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `perl:devel-threaded-bullseye` - linux; arm variant v5

```console
$ docker pull perl@sha256:141696bd6215cdb6ee41c9f1b62096eae1e6b624873eca969def699d5504176c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **310.3 MB (310265117 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5753530b0c8e7c842cfc970dc01a917408cb8befa95cb40b018628280e79287`
-	Default Command: `["perl5.39.2","-de0"]`

```dockerfile
# Wed, 20 Sep 2023 00:50:08 GMT
ADD file:36b8026af7713ecb15198f7cb7beff053db2fb1d0cdbba2e05ede6d2067120be in / 
# Wed, 20 Sep 2023 00:50:08 GMT
CMD ["bash"]
# Wed, 20 Sep 2023 09:57:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 20 Sep 2023 09:57:43 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 20 Sep 2023 09:59:16 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 20 Sep 2023 13:33:51 GMT
LABEL maintainer=Peter Martini <PeterCMartini@GMail.com>, Zak B. Elep <zakame@cpan.org>
# Wed, 20 Sep 2023 13:33:51 GMT
WORKDIR /usr/src/perl
# Wed, 20 Sep 2023 15:03:23 GMT
RUN true     && curl -fL https://www.cpan.org/src/5.0/perl-5.39.2.tar.xz -o perl-5.39.2.tar.xz     && echo 'b7ae33d3c6ff80107d14c92dfb3d8d4944fec926b11bcc40c8764b73c710694f *perl-5.39.2.tar.xz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.39.2.tar.xz -C /usr/src/perl     && rm perl-5.39.2.tar.xz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997011/cpm -o /usr/local/bin/cpm     && echo '7dee2176a450a8be3a6b9b91dac603a0c3a7e807042626d3fe6c93d843f75610 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version
# Wed, 20 Sep 2023 15:03:23 GMT
WORKDIR /usr/src/app
# Wed, 20 Sep 2023 15:03:23 GMT
CMD ["perl5.39.2" "-de0"]
```

-	Layers:
	-	`sha256:791ab9666f498037db4451bb82dd3cb63afd5ef69c2068959d5516a7832d373b`  
		Last Modified: Wed, 20 Sep 2023 00:55:10 GMT  
		Size: 52.6 MB (52558199 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37002420bf0e3d73b89ed87c7e321032a64691875353cde3cc0370cc78f07f50`  
		Last Modified: Wed, 20 Sep 2023 10:06:18 GMT  
		Size: 15.4 MB (15369135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b43ccaa88e1d24c47bf1c55018f8d61128185b8b108f3c5c1d641a7f96a0fea0`  
		Last Modified: Wed, 20 Sep 2023 10:06:36 GMT  
		Size: 52.3 MB (52340617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d334d3272118e82d2944c89ec38c02adf4d2140b4b133805f538ad58e6449e9d`  
		Last Modified: Wed, 20 Sep 2023 10:07:22 GMT  
		Size: 175.1 MB (175056831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e9593005fb4011362fc25e6666a5242fc03a6ed144d8fe97e1329537aa522bc`  
		Last Modified: Wed, 20 Sep 2023 15:11:17 GMT  
		Size: 167.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f971f6bf99092eebbc2064845e9f4cc3b1636856c1b0a898d4b246b61b720817`  
		Last Modified: Wed, 20 Sep 2023 15:15:18 GMT  
		Size: 14.9 MB (14940003 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a85c0c319a4a332c7e0d5a20ede9653d48767d37c98718796caaa952e2fb7285`  
		Last Modified: Wed, 20 Sep 2023 15:15:15 GMT  
		Size: 165.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `perl:devel-threaded-bullseye` - linux; arm variant v7

```console
$ docker pull perl@sha256:0fbd69b386a8a2669d0edd5d8fcbedca20d0290dac22a2748962be1f82ea0501
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.5 MB (297501996 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e7204da5c88eb1dbb2dbb31aa4e47e7bf7058657b23c6420aa1a40158d77084`
-	Default Command: `["perl5.39.2","-de0"]`

```dockerfile
# Wed, 20 Sep 2023 04:57:26 GMT
ADD file:3bf3380482840b3a4166e82c3f951812076851ba1527261fdd1da780662b2de1 in / 
# Wed, 20 Sep 2023 04:57:26 GMT
CMD ["bash"]
# Wed, 20 Sep 2023 15:26:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 20 Sep 2023 15:26:57 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 20 Sep 2023 15:28:04 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 20 Sep 2023 17:08:11 GMT
LABEL maintainer=Peter Martini <PeterCMartini@GMail.com>, Zak B. Elep <zakame@cpan.org>
# Wed, 20 Sep 2023 17:08:11 GMT
WORKDIR /usr/src/perl
# Wed, 20 Sep 2023 21:06:31 GMT
RUN true     && curl -fL https://www.cpan.org/src/5.0/perl-5.39.2.tar.xz -o perl-5.39.2.tar.xz     && echo 'b7ae33d3c6ff80107d14c92dfb3d8d4944fec926b11bcc40c8764b73c710694f *perl-5.39.2.tar.xz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.39.2.tar.xz -C /usr/src/perl     && rm perl-5.39.2.tar.xz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997011/cpm -o /usr/local/bin/cpm     && echo '7dee2176a450a8be3a6b9b91dac603a0c3a7e807042626d3fe6c93d843f75610 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version
# Wed, 20 Sep 2023 21:06:31 GMT
WORKDIR /usr/src/app
# Wed, 20 Sep 2023 21:06:31 GMT
CMD ["perl5.39.2" "-de0"]
```

-	Layers:
	-	`sha256:1d4e041d2204b383d6d6893cfcf5b852394f34744a85cea9ec0b3fb65cbc6143`  
		Last Modified: Wed, 20 Sep 2023 05:01:34 GMT  
		Size: 50.2 MB (50219551 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2dbd770246538a809113f7f8fd84fedf3bd2bee5ed2f4fad2ab81cca9a78580d`  
		Last Modified: Wed, 20 Sep 2023 15:36:25 GMT  
		Size: 14.9 MB (14868646 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:145367a45c553b855c9dec20850966d6ec435636dba00c32133a9181c6f0b3e9`  
		Last Modified: Wed, 20 Sep 2023 15:36:43 GMT  
		Size: 50.4 MB (50355432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:733e5937f159c4788716aa1891265686c96fd934eeccd3bbf46f01ea4bf34b5e`  
		Last Modified: Wed, 20 Sep 2023 15:37:14 GMT  
		Size: 167.3 MB (167322461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9a4eefac99ecab3d08e3423a9068da1a56190345657fd930cb09711ccd4b24f`  
		Last Modified: Wed, 20 Sep 2023 21:28:54 GMT  
		Size: 167.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89f9151e82dfa7c03d7ce9805418242321bff90c84826147c98f46c8be17840f`  
		Last Modified: Wed, 20 Sep 2023 21:40:43 GMT  
		Size: 14.7 MB (14735574 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa47d59361d7a68dffbd7b247f78cc5f17a64185776e43e10571d2d45c516911`  
		Last Modified: Wed, 20 Sep 2023 21:40:38 GMT  
		Size: 165.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `perl:devel-threaded-bullseye` - linux; arm64 variant v8

```console
$ docker pull perl@sha256:54fb2c19b74149eea8879629c2a838b66f2dabfd2c3df1f6b0d2d811d47aee39
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **329.5 MB (329500252 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe0835988e1e50fb66a0c167d323d677c226fedb10401d45b0ff334378e668c0`
-	Default Command: `["perl5.39.2","-de0"]`

```dockerfile
# Wed, 20 Sep 2023 02:44:20 GMT
ADD file:46dcdcde338d2c01fed5db3fac9041736d9305145d8fc2039dd5b3714d38ede8 in / 
# Wed, 20 Sep 2023 02:44:21 GMT
CMD ["bash"]
# Wed, 20 Sep 2023 09:24:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 20 Sep 2023 09:25:09 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 20 Sep 2023 09:26:03 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 20 Sep 2023 12:49:59 GMT
LABEL maintainer=Peter Martini <PeterCMartini@GMail.com>, Zak B. Elep <zakame@cpan.org>
# Wed, 20 Sep 2023 12:49:59 GMT
WORKDIR /usr/src/perl
# Wed, 20 Sep 2023 15:45:26 GMT
RUN true     && curl -fL https://www.cpan.org/src/5.0/perl-5.39.2.tar.xz -o perl-5.39.2.tar.xz     && echo 'b7ae33d3c6ff80107d14c92dfb3d8d4944fec926b11bcc40c8764b73c710694f *perl-5.39.2.tar.xz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.39.2.tar.xz -C /usr/src/perl     && rm perl-5.39.2.tar.xz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997011/cpm -o /usr/local/bin/cpm     && echo '7dee2176a450a8be3a6b9b91dac603a0c3a7e807042626d3fe6c93d843f75610 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version
# Wed, 20 Sep 2023 15:45:26 GMT
WORKDIR /usr/src/app
# Wed, 20 Sep 2023 15:45:27 GMT
CMD ["perl5.39.2" "-de0"]
```

-	Layers:
	-	`sha256:31f5dc1f52c865588c43d8ec718f14d430e149b28f0b28232da825da7ae28f76`  
		Last Modified: Wed, 20 Sep 2023 02:47:53 GMT  
		Size: 53.7 MB (53704892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb60045eb75c62e890b95d28e4893132a6c7d61ec9979104ee4ff6e86c4badee`  
		Last Modified: Wed, 20 Sep 2023 09:33:11 GMT  
		Size: 15.7 MB (15746671 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:292737ab468ef80c6f78bdde4896157b8953d1e5556e1e526f40aeadcb547573`  
		Last Modified: Wed, 20 Sep 2023 09:33:26 GMT  
		Size: 54.7 MB (54676309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d93979d624211374be152eee1c99ed4ca9e6bae68694135fc440ab6c8fd2044`  
		Last Modified: Wed, 20 Sep 2023 09:33:51 GMT  
		Size: 189.8 MB (189778334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1117f9029f2f12e3c0ea1a49d453513b6d3c4ec5a2cf433fd56be576e3c53290`  
		Last Modified: Wed, 20 Sep 2023 15:58:14 GMT  
		Size: 168.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21f372b1a5c0cb7391d3c34daf37d1f1ecebeefe5e3bc686093914fc997f6bba`  
		Last Modified: Wed, 20 Sep 2023 16:08:09 GMT  
		Size: 15.6 MB (15593714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d302821773d483201d84bff193a17e8336eeb2d9f6eb1f38474a7237c5aa831`  
		Last Modified: Wed, 20 Sep 2023 16:08:06 GMT  
		Size: 164.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `perl:devel-threaded-bullseye` - linux; 386

```console
$ docker pull perl@sha256:7ab6b2680e9ce15b0144dbbde85cf480f6f5ea6327390323140b198830dd151a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **343.2 MB (343205475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3582173b2526a86cf82d72a5eb07847df4070178718af46bd9bb66110bcea49a`
-	Default Command: `["perl5.39.2","-de0"]`

```dockerfile
# Wed, 20 Sep 2023 00:42:07 GMT
ADD file:342c36522089238a534c0912491a4cf64b89133969e051cdad2e694ec761142c in / 
# Wed, 20 Sep 2023 00:42:07 GMT
CMD ["bash"]
# Wed, 20 Sep 2023 11:27:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 20 Sep 2023 11:27:45 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 20 Sep 2023 11:29:02 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 20 Sep 2023 17:56:41 GMT
LABEL maintainer=Peter Martini <PeterCMartini@GMail.com>, Zak B. Elep <zakame@cpan.org>
# Wed, 20 Sep 2023 17:56:42 GMT
WORKDIR /usr/src/perl
# Thu, 21 Sep 2023 00:22:16 GMT
RUN true     && curl -fL https://www.cpan.org/src/5.0/perl-5.39.2.tar.xz -o perl-5.39.2.tar.xz     && echo 'b7ae33d3c6ff80107d14c92dfb3d8d4944fec926b11bcc40c8764b73c710694f *perl-5.39.2.tar.xz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.39.2.tar.xz -C /usr/src/perl     && rm perl-5.39.2.tar.xz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997011/cpm -o /usr/local/bin/cpm     && echo '7dee2176a450a8be3a6b9b91dac603a0c3a7e807042626d3fe6c93d843f75610 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version
# Thu, 21 Sep 2023 00:22:17 GMT
WORKDIR /usr/src/app
# Thu, 21 Sep 2023 00:22:17 GMT
CMD ["perl5.39.2" "-de0"]
```

-	Layers:
	-	`sha256:00121bf241b18e981bcc804f905be7b34f95cce415db622599e21dc1a496ee8d`  
		Last Modified: Wed, 20 Sep 2023 00:47:11 GMT  
		Size: 56.0 MB (56040498 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:656938def9400b0af510c0a87c5dd1a6daf011fd1270e3c56c71d6ec54b5ab1b`  
		Last Modified: Wed, 20 Sep 2023 11:38:25 GMT  
		Size: 16.3 MB (16263804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d08fdcc11a9302a19159b5ae4e19e22d42c914e371c0d7a532d73d7d45d3aed`  
		Last Modified: Wed, 20 Sep 2023 11:38:47 GMT  
		Size: 55.9 MB (55922986 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3eabd2ad72b1eaa8ae1de02f17e175b40c5e4605b70269e10ad0283db90d6ac`  
		Last Modified: Wed, 20 Sep 2023 11:39:33 GMT  
		Size: 199.8 MB (199763042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f668da9214843ad6056e9e105b863ab71207238514ff5139841abff5acfb1342`  
		Last Modified: Thu, 21 Sep 2023 00:46:49 GMT  
		Size: 167.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caf8d2736882baf001d061d0379d29a5c297d2964e3f9ed78a9751c37343219e`  
		Last Modified: Thu, 21 Sep 2023 00:58:09 GMT  
		Size: 15.2 MB (15214814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19f5fe7426f881977755b5037408f314e8b69490fc739787809799991d752544`  
		Last Modified: Thu, 21 Sep 2023 00:58:04 GMT  
		Size: 164.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `perl:devel-threaded-bullseye` - linux; mips64le

```console
$ docker pull perl@sha256:d487aea894bb9e16b941b2423e4680e925eac37d0a2ae97d93afb8bca722b401
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **316.0 MB (315968050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb0bcdcf3625049ab05416ef31e6ebcec555078b87108b5ba8023119cc58491d`
-	Default Command: `["perl5.39.2","-de0"]`

```dockerfile
# Thu, 07 Sep 2023 01:09:47 GMT
ADD file:fdd438b39f1dce564715691d2a092378f02bc722e29cb80216efcbaf71cff0b8 in / 
# Thu, 07 Sep 2023 01:09:53 GMT
CMD ["bash"]
# Thu, 07 Sep 2023 03:52:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 07 Sep 2023 03:54:17 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 07 Sep 2023 04:00:09 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 07 Sep 2023 04:34:04 GMT
LABEL maintainer=Peter Martini <PeterCMartini@GMail.com>, Zak B. Elep <zakame@cpan.org>
# Thu, 07 Sep 2023 04:34:09 GMT
WORKDIR /usr/src/perl
# Thu, 07 Sep 2023 10:30:47 GMT
RUN true     && curl -fL https://www.cpan.org/src/5.0/perl-5.39.2.tar.xz -o perl-5.39.2.tar.xz     && echo 'b7ae33d3c6ff80107d14c92dfb3d8d4944fec926b11bcc40c8764b73c710694f *perl-5.39.2.tar.xz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.39.2.tar.xz -C /usr/src/perl     && rm perl-5.39.2.tar.xz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997011/cpm -o /usr/local/bin/cpm     && echo '7dee2176a450a8be3a6b9b91dac603a0c3a7e807042626d3fe6c93d843f75610 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version
# Thu, 07 Sep 2023 10:30:53 GMT
WORKDIR /usr/src/app
# Thu, 07 Sep 2023 10:30:59 GMT
CMD ["perl5.39.2" "-de0"]
```

-	Layers:
	-	`sha256:0d1f1f4ccb1e0da4313c3ebcd521e7fa8073526c6f64ca7214ed31ae9bd0788e`  
		Last Modified: Thu, 07 Sep 2023 01:21:00 GMT  
		Size: 53.3 MB (53271469 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b80fcec80ebe264db68a3623aea9c7b0061e84f5d1badc96d9af8660a8643cb`  
		Last Modified: Thu, 07 Sep 2023 04:23:17 GMT  
		Size: 15.5 MB (15520537 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18e60242b89f56e84024b48424b36403c5ed51b10293ee206a3058817baef6e4`  
		Last Modified: Thu, 07 Sep 2023 04:24:04 GMT  
		Size: 53.3 MB (53306675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1dd0df6bf1b0768a46f3fb43fb69160771edacabdaceaa0ddb050c8b36f31730`  
		Last Modified: Thu, 07 Sep 2023 04:26:01 GMT  
		Size: 179.0 MB (178968417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49eee037eb42eb68488000955a95dc021d3547df0ac554ba9b1c1a6362dd7c7a`  
		Last Modified: Thu, 07 Sep 2023 10:57:28 GMT  
		Size: 133.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aaa9e76757a9f9dbb052a77e1470f569d049c8c2752282126c68e73f532b8540`  
		Last Modified: Thu, 07 Sep 2023 11:04:18 GMT  
		Size: 14.9 MB (14900689 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b6359a61d5535c7faa8e84e408688cb53ba8897168862b84cf3ff1b4d93f013`  
		Last Modified: Thu, 07 Sep 2023 11:04:05 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `perl:devel-threaded-bullseye` - linux; ppc64le

```console
$ docker pull perl@sha256:ba3f6b8b14e6e13ebfc8592f6fbbf2731cfbe0e1b9d536c59210c89e03065925
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **346.5 MB (346476991 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a12a7b862a4dd6fd531164ee34c30eecc27b92f085f167aaf248015567185a00`
-	Default Command: `["perl5.39.2","-de0"]`

```dockerfile
# Wed, 20 Sep 2023 07:53:09 GMT
ADD file:c12b11abfba27478510c84d05abdd8fec539db9ec30af6d042671f4d5bf793e5 in / 
# Wed, 20 Sep 2023 07:53:12 GMT
CMD ["bash"]
# Wed, 20 Sep 2023 09:53:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 20 Sep 2023 09:54:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 20 Sep 2023 09:59:08 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 20 Sep 2023 18:37:52 GMT
LABEL maintainer=Peter Martini <PeterCMartini@GMail.com>, Zak B. Elep <zakame@cpan.org>
# Wed, 20 Sep 2023 18:37:53 GMT
WORKDIR /usr/src/perl
# Wed, 20 Sep 2023 20:43:38 GMT
RUN true     && curl -fL https://www.cpan.org/src/5.0/perl-5.39.2.tar.xz -o perl-5.39.2.tar.xz     && echo 'b7ae33d3c6ff80107d14c92dfb3d8d4944fec926b11bcc40c8764b73c710694f *perl-5.39.2.tar.xz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.39.2.tar.xz -C /usr/src/perl     && rm perl-5.39.2.tar.xz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997011/cpm -o /usr/local/bin/cpm     && echo '7dee2176a450a8be3a6b9b91dac603a0c3a7e807042626d3fe6c93d843f75610 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version
# Wed, 20 Sep 2023 20:43:40 GMT
WORKDIR /usr/src/app
# Wed, 20 Sep 2023 20:43:40 GMT
CMD ["perl5.39.2" "-de0"]
```

-	Layers:
	-	`sha256:9f3507d882ae95f06b3672497cdd3317bd4f8e0255e73d10f1f263e5d780f102`  
		Last Modified: Wed, 20 Sep 2023 08:50:16 GMT  
		Size: 58.9 MB (58928499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04a84a3dd07e7f4a4117efeb4dfb2cd5752a6495b332adc44482bd2964626ce9`  
		Last Modified: Wed, 20 Sep 2023 10:22:16 GMT  
		Size: 16.8 MB (16752924 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fca2a058b7253284355cf28252852be40a5207eb0fd8a7a9cbc7e2b0dd48e61e`  
		Last Modified: Wed, 20 Sep 2023 10:22:39 GMT  
		Size: 58.9 MB (58865110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22fa6f995be18d5920224ffc49bfb41e404969a3667799383a06921bd5d2ee3f`  
		Last Modified: Wed, 20 Sep 2023 10:23:33 GMT  
		Size: 196.2 MB (196219105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47a390c85f40b92dcbe3893e7ad6e637ebfc32d7c7c783941d22945b0b9ec02d`  
		Last Modified: Wed, 20 Sep 2023 20:53:09 GMT  
		Size: 166.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56dc21917a5f273d8c35468510e9eb1192e860dd73c959f95972eb296597b5a1`  
		Last Modified: Wed, 20 Sep 2023 20:57:43 GMT  
		Size: 15.7 MB (15711023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e936e490663df45307287f59b9a8933819104d3edfe3c03ff2a9318a0d486676`  
		Last Modified: Wed, 20 Sep 2023 20:57:38 GMT  
		Size: 164.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `perl:devel-threaded-bullseye` - linux; s390x

```console
$ docker pull perl@sha256:5f11eed5ca014c36155b98516a13cec79a363e7f91e24aa256281a94623901ad
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **311.9 MB (311886223 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb3e4b494031e7ff365fd9fde900e17eda00bb8c5ef2723bc9c7b2e2e59fd3ff`
-	Default Command: `["perl5.39.2","-de0"]`

```dockerfile
# Wed, 20 Sep 2023 02:54:37 GMT
ADD file:eedfa120b98e158d4eeb9ecad39e28c5715c44bddec3545f61b78ecebd01cc11 in / 
# Wed, 20 Sep 2023 02:54:41 GMT
CMD ["bash"]
# Wed, 20 Sep 2023 09:51:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 20 Sep 2023 09:51:32 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 20 Sep 2023 09:52:23 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 20 Sep 2023 10:51:57 GMT
LABEL maintainer=Peter Martini <PeterCMartini@GMail.com>, Zak B. Elep <zakame@cpan.org>
# Wed, 20 Sep 2023 10:51:58 GMT
WORKDIR /usr/src/perl
# Wed, 20 Sep 2023 12:23:18 GMT
RUN true     && curl -fL https://www.cpan.org/src/5.0/perl-5.39.2.tar.xz -o perl-5.39.2.tar.xz     && echo 'b7ae33d3c6ff80107d14c92dfb3d8d4944fec926b11bcc40c8764b73c710694f *perl-5.39.2.tar.xz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.39.2.tar.xz -C /usr/src/perl     && rm perl-5.39.2.tar.xz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997011/cpm -o /usr/local/bin/cpm     && echo '7dee2176a450a8be3a6b9b91dac603a0c3a7e807042626d3fe6c93d843f75610 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version
# Wed, 20 Sep 2023 12:23:20 GMT
WORKDIR /usr/src/app
# Wed, 20 Sep 2023 12:23:20 GMT
CMD ["perl5.39.2" "-de0"]
```

-	Layers:
	-	`sha256:d0496e15eebca8286145e6a2cb12c47bb17a28a89cc286a0f7a94763f7713716`  
		Last Modified: Wed, 20 Sep 2023 03:00:01 GMT  
		Size: 53.3 MB (53290747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ffb65667eeb2d3b6696a39c6bee7f8e530b0ca44e4ffdce5129fae1417349ab`  
		Last Modified: Wed, 20 Sep 2023 09:59:26 GMT  
		Size: 15.6 MB (15631894 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd7bdcba55b78b8074e079cbf178f213bba5f35b2e940b37ef069b50b092ef5f`  
		Last Modified: Wed, 20 Sep 2023 09:59:39 GMT  
		Size: 54.1 MB (54061720 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b281045931687b0edd0ac8da65d377622620e8468caf6cc573c45dbbf7611951`  
		Last Modified: Wed, 20 Sep 2023 10:00:06 GMT  
		Size: 172.9 MB (172874403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15b6e23b4762781e09acfe749b4c9e2aec50b0d43b1af223af370c5217a7680a`  
		Last Modified: Wed, 20 Sep 2023 12:30:42 GMT  
		Size: 167.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:872f98b1e0554d7892279939c2bddacb054b6ade2ea14a3230eb0e3e384e8700`  
		Last Modified: Wed, 20 Sep 2023 12:33:33 GMT  
		Size: 16.0 MB (16027129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf0d91592194921d775fc6b2807c8d0c9383d5199819aad6416a92509e3b2d52`  
		Last Modified: Wed, 20 Sep 2023 12:33:30 GMT  
		Size: 163.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
