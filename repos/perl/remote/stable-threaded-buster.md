## `perl:stable-threaded-buster`

```console
$ docker pull perl@sha256:3a83a08c36660ea9cd45f79193b58a0db8064acc41331a9c572223db89d4fd6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `perl:stable-threaded-buster` - linux; amd64

```console
$ docker pull perl@sha256:1f9a834c8f664aa448bad3e14c844a7880c3ae425ca2a51c39c3fd6ad0f5ee92
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **327.6 MB (327581372 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db36d48bdfdd0e56f1c9d1df3120e40cc5f8ee551bb21759adb590693eaf8e9b`
-	Default Command: `["perl5.38.0","-de0"]`

```dockerfile
# Thu, 07 Sep 2023 00:21:23 GMT
ADD file:d9c3e291731c1f06d615709ebc665a41f6d6355607d87ae00768e3be4b330bed in / 
# Thu, 07 Sep 2023 00:21:24 GMT
CMD ["bash"]
# Thu, 07 Sep 2023 02:59:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 07 Sep 2023 02:59:28 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 07 Sep 2023 03:00:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 07 Sep 2023 07:42:57 GMT
LABEL maintainer=Peter Martini <PeterCMartini@GMail.com>, Zak B. Elep <zakame@cpan.org>
# Thu, 07 Sep 2023 07:42:57 GMT
WORKDIR /usr/src/perl
# Thu, 07 Sep 2023 08:24:19 GMT
RUN true     && curl -fL https://www.cpan.org/src/5.0/perl-5.38.0.tar.xz -o perl-5.38.0.tar.xz     && echo 'eca551caec3bc549a4e590c0015003790bdd1a604ffe19cc78ee631d51f7072e *perl-5.38.0.tar.xz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.38.0.tar.xz -C /usr/src/perl     && rm perl-5.38.0.tar.xz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997011/cpm -o /usr/local/bin/cpm     && echo '7dee2176a450a8be3a6b9b91dac603a0c3a7e807042626d3fe6c93d843f75610 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version
# Thu, 07 Sep 2023 08:24:19 GMT
WORKDIR /usr/src/app
# Thu, 07 Sep 2023 08:24:19 GMT
CMD ["perl5.38.0" "-de0"]
```

-	Layers:
	-	`sha256:311da6c465ea1576925360eba391bcd32dece9be95960a0bc9ffcb25fe712017`  
		Last Modified: Thu, 07 Sep 2023 00:26:22 GMT  
		Size: 50.5 MB (50497598 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e9bf114588c05b2df612b083b96582f3b8dbf51647aa6138a50d09d42df2454`  
		Last Modified: Thu, 07 Sep 2023 03:06:52 GMT  
		Size: 17.6 MB (17579550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffd9397e94b74abcb54e514f1430e00f604328d1f895eadbd482f08cc02444e5`  
		Last Modified: Thu, 07 Sep 2023 03:07:09 GMT  
		Size: 51.9 MB (51887218 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:513d779256048c961239af5f500589330546b072775217272e19ffae1635e98e`  
		Last Modified: Thu, 07 Sep 2023 03:07:41 GMT  
		Size: 191.9 MB (191897265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43716e59bb0f38d3abaf05476f673412c8a30d658aa83b14d22a1fe5e9ed01a2`  
		Last Modified: Thu, 07 Sep 2023 11:31:15 GMT  
		Size: 166.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7912d18293654643bdba698f170415359e9389768e8f5dbbca2eeaba38e6d04d`  
		Last Modified: Thu, 07 Sep 2023 11:33:27 GMT  
		Size: 15.7 MB (15719411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4f940ebd970d04e87d4fbe6a5830a8b65d0ef2a3db19653178eeb1a3bda0f74`  
		Last Modified: Thu, 07 Sep 2023 11:33:24 GMT  
		Size: 164.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `perl:stable-threaded-buster` - linux; arm variant v7

```console
$ docker pull perl@sha256:5d38e0edd900cd1d826f4c1371d684bf43d4f05e5922554d45c97c6793b309fd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.5 MB (292454136 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a13acb83724865d1b4072ec873c42d3629a7e49385a47372ab6b57b7510ddae2`
-	Default Command: `["perl5.38.0","-de0"]`

```dockerfile
# Thu, 07 Sep 2023 00:58:19 GMT
ADD file:7ec242a3962c31a67f54c602b7f422709b35916aa381a646dc41202360549761 in / 
# Thu, 07 Sep 2023 00:58:21 GMT
CMD ["bash"]
# Thu, 07 Sep 2023 01:37:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 07 Sep 2023 01:37:49 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 07 Sep 2023 01:39:26 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 07 Sep 2023 07:13:26 GMT
LABEL maintainer=Peter Martini <PeterCMartini@GMail.com>, Zak B. Elep <zakame@cpan.org>
# Thu, 07 Sep 2023 07:13:27 GMT
WORKDIR /usr/src/perl
# Thu, 07 Sep 2023 07:55:46 GMT
RUN true     && curl -fL https://www.cpan.org/src/5.0/perl-5.38.0.tar.xz -o perl-5.38.0.tar.xz     && echo 'eca551caec3bc549a4e590c0015003790bdd1a604ffe19cc78ee631d51f7072e *perl-5.38.0.tar.xz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.38.0.tar.xz -C /usr/src/perl     && rm perl-5.38.0.tar.xz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997011/cpm -o /usr/local/bin/cpm     && echo '7dee2176a450a8be3a6b9b91dac603a0c3a7e807042626d3fe6c93d843f75610 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version
# Thu, 07 Sep 2023 07:55:46 GMT
WORKDIR /usr/src/app
# Thu, 07 Sep 2023 07:55:46 GMT
CMD ["perl5.38.0" "-de0"]
```

-	Layers:
	-	`sha256:719d9383401f642312dab568888c86aa5069040b61dbe32fb40d5a7bc5fd5c02`  
		Last Modified: Thu, 07 Sep 2023 01:03:31 GMT  
		Size: 46.0 MB (45966117 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e2da04a998e4694d1b45ec9b56798040834751f733528e18fb5bffc24059f83`  
		Last Modified: Thu, 07 Sep 2023 01:47:14 GMT  
		Size: 16.2 MB (16211872 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f37b051fc63e1403e73c08f53e28d73136050d2f4e34fcfef866fee0ecca0609`  
		Last Modified: Thu, 07 Sep 2023 01:47:32 GMT  
		Size: 47.4 MB (47376593 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b934173fbca67d2ffd70b07905e1c9102337868264ff33f45b18962566594fa0`  
		Last Modified: Thu, 07 Sep 2023 01:48:08 GMT  
		Size: 168.1 MB (168100292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9dd1464c2827f9aab6697899e05db7de2d138242977260d480c4700b5f6d6e4b`  
		Last Modified: Thu, 07 Sep 2023 11:13:12 GMT  
		Size: 167.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4524ebf4fb1af4ffd9b0d2002198c9081f114275e55391921d8e6b2a22273b89`  
		Last Modified: Thu, 07 Sep 2023 11:15:41 GMT  
		Size: 14.8 MB (14798931 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30e8ee5cdbca4784172eeec1d5e30c9367b1fd183604cfc0f8337c3293dc5f7e`  
		Last Modified: Thu, 07 Sep 2023 11:15:37 GMT  
		Size: 164.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `perl:stable-threaded-buster` - linux; arm64 variant v8

```console
$ docker pull perl@sha256:2faa6518e0bb714b26d527d4578fa9b7fa117ed2244343d191aad93745b90187
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **318.1 MB (318061928 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a34dcddf67418f55ac4194c1a6bd3b1691b77b166d95601e7efa9e2f5cdaba49`
-	Default Command: `["perl5.38.0","-de0"]`

```dockerfile
# Thu, 07 Sep 2023 00:40:00 GMT
ADD file:d9e56538de5f967fc9a8327ecb4e67562f6f95e56b455b9494e35d3b57c89332 in / 
# Thu, 07 Sep 2023 00:40:00 GMT
CMD ["bash"]
# Thu, 07 Sep 2023 06:53:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 07 Sep 2023 06:54:08 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 07 Sep 2023 06:55:02 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 07 Sep 2023 11:34:16 GMT
LABEL maintainer=Peter Martini <PeterCMartini@GMail.com>, Zak B. Elep <zakame@cpan.org>
# Thu, 07 Sep 2023 11:34:16 GMT
WORKDIR /usr/src/perl
# Thu, 07 Sep 2023 11:53:06 GMT
RUN true     && curl -fL https://www.cpan.org/src/5.0/perl-5.38.0.tar.xz -o perl-5.38.0.tar.xz     && echo 'eca551caec3bc549a4e590c0015003790bdd1a604ffe19cc78ee631d51f7072e *perl-5.38.0.tar.xz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.38.0.tar.xz -C /usr/src/perl     && rm perl-5.38.0.tar.xz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997011/cpm -o /usr/local/bin/cpm     && echo '7dee2176a450a8be3a6b9b91dac603a0c3a7e807042626d3fe6c93d843f75610 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version
# Thu, 07 Sep 2023 11:53:06 GMT
WORKDIR /usr/src/app
# Thu, 07 Sep 2023 11:53:07 GMT
CMD ["perl5.38.0" "-de0"]
```

-	Layers:
	-	`sha256:26ee4ff96582b6c5e191414a6b74b283e3039e003d1b6f546cc00d6b14ff8abb`  
		Last Modified: Thu, 07 Sep 2023 00:43:57 GMT  
		Size: 49.3 MB (49290609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:446eab4103f443744320bea51eafbe02912e638811b0190923d9143775a66f02`  
		Last Modified: Thu, 07 Sep 2023 07:01:09 GMT  
		Size: 17.5 MB (17451009 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e3c22a0f840b20987055dd0b4baf221ec226cfb650ade4cab8d23f35193fbe4`  
		Last Modified: Thu, 07 Sep 2023 07:01:24 GMT  
		Size: 52.2 MB (52227154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7ab8ad9b40817ba00da4027aa19faa2d94c8b338c3a7bd50e41c8f7d8537192`  
		Last Modified: Thu, 07 Sep 2023 07:01:48 GMT  
		Size: 183.5 MB (183463074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa3be97e839528cbe6a2e0140ada3b5d240b84ab957e291897d0eed58a33fb58`  
		Last Modified: Thu, 07 Sep 2023 13:00:17 GMT  
		Size: 168.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a51a46a4784e611592df8f9e9576085a2f4fcc730970251d080acc6d99c86f7`  
		Last Modified: Thu, 07 Sep 2023 13:01:27 GMT  
		Size: 15.6 MB (15629749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a115771b7db1b8fa0233f53083b35bab5d5a84a3b5ac613c7a4fb18b49bd36c9`  
		Last Modified: Thu, 07 Sep 2023 13:01:25 GMT  
		Size: 165.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `perl:stable-threaded-buster` - linux; 386

```console
$ docker pull perl@sha256:95b5984bb9107e84100afd102e99c01f2faa60d56167b39a2c02f47d9a3717a4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **336.5 MB (336542529 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f122081dd012e446c4176ae6faf38519f656b3593106343e3e78f7eae836c894`
-	Default Command: `["perl5.38.0","-de0"]`

```dockerfile
# Tue, 15 Aug 2023 23:39:33 GMT
ADD file:f985eed393788dbeb3e4d9ab7f77d632d72f60bc5da30c59bb7de8fa3de0681c in / 
# Tue, 15 Aug 2023 23:39:33 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 00:29:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 16 Aug 2023 00:30:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 16 Aug 2023 00:31:43 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 16 Aug 2023 10:06:05 GMT
LABEL maintainer=Peter Martini <PeterCMartini@GMail.com>, Zak B. Elep <zakame@cpan.org>
# Wed, 16 Aug 2023 10:06:05 GMT
WORKDIR /usr/src/perl
# Wed, 16 Aug 2023 11:14:49 GMT
RUN true     && curl -fL https://www.cpan.org/src/5.0/perl-5.38.0.tar.xz -o perl-5.38.0.tar.xz     && echo 'eca551caec3bc549a4e590c0015003790bdd1a604ffe19cc78ee631d51f7072e *perl-5.38.0.tar.xz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.38.0.tar.xz -C /usr/src/perl     && rm perl-5.38.0.tar.xz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997011/cpm -o /usr/local/bin/cpm     && echo '7dee2176a450a8be3a6b9b91dac603a0c3a7e807042626d3fe6c93d843f75610 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version
# Wed, 16 Aug 2023 11:14:50 GMT
WORKDIR /usr/src/app
# Wed, 16 Aug 2023 11:14:50 GMT
CMD ["perl5.38.0" "-de0"]
```

-	Layers:
	-	`sha256:ce293edb9c35c6521b0a7d87a0d8e0252e4b0cab665a3103cb6d06e3e37cf414`  
		Last Modified: Tue, 15 Aug 2023 23:44:33 GMT  
		Size: 51.3 MB (51255460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30d7c3776eae51e29722c4381d59391e00b49339c7298dcbef6adffe94829182`  
		Last Modified: Wed, 16 Aug 2023 00:37:17 GMT  
		Size: 18.1 MB (18095956 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:377913e8bda7ade79ce7bc10aab7401851a4cb9565903c8bca5b0360b4fab3bd`  
		Last Modified: Wed, 16 Aug 2023 00:37:36 GMT  
		Size: 53.5 MB (53486191 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:772141f0f201b519ab5689ccf41e7601936a21705c554b9ee73448eb217def09`  
		Last Modified: Wed, 16 Aug 2023 00:38:19 GMT  
		Size: 198.4 MB (198441615 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0672b71f5bc4e8c14f90a3278596c55f4acb1ceb0ed01d463a2e118b29b57d5f`  
		Last Modified: Wed, 16 Aug 2023 16:29:10 GMT  
		Size: 167.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8378e1d72a8c97560b6f6d2d6ed2327ed526e3de994fe20e49634971a773ada3`  
		Last Modified: Wed, 16 Aug 2023 16:31:36 GMT  
		Size: 15.3 MB (15262974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:168e3bba372bd4c9e23ec200853b369ecaf1c39d3975ec6417579a8084066ef1`  
		Last Modified: Wed, 16 Aug 2023 16:31:31 GMT  
		Size: 166.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
