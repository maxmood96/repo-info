## `perl:latest`

```console
$ docker pull perl@sha256:02f5dc9d5f8068b0d4de915d7a564940076c92a773d7077ec75139becc248ec6
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

### `perl:latest` - linux; amd64

```console
$ docker pull perl@sha256:cd3f11aa87cca43c1c5e41bc5d84d13854d1c4506fd000dbe35063319d8a2e67
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **337.8 MB (337771071 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a6d16b694f35b16a4dd459ade58891b59d4d8a5bda8c405667d496fe0f8bf11`
-	Default Command: `["perl5.36.0","-de0"]`

```dockerfile
# Tue, 06 Dec 2022 01:20:41 GMT
ADD file:553d20b03d45305e58cde07e0c259421bba044155ac90b4559e5cc0b69093347 in / 
# Tue, 06 Dec 2022 01:20:41 GMT
CMD ["bash"]
# Tue, 06 Dec 2022 02:13:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 06 Dec 2022 02:13:31 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 06 Dec 2022 02:13:49 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 06 Dec 2022 02:14:50 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 06 Dec 2022 09:21:16 GMT
LABEL maintainer=Peter Martini <PeterCMartini@GMail.com>, Zak B. Elep <zakame@cpan.org>
# Tue, 06 Dec 2022 09:21:16 GMT
COPY file:3744c5cc39cdbdcae10db09a1f0f399005a79f93c237b387a72ff5710cdd458c in /usr/src/perl/ 
# Tue, 06 Dec 2022 09:21:16 GMT
WORKDIR /usr/src/perl
# Tue, 06 Dec 2022 09:26:41 GMT
RUN true     && curl -fL https://www.cpan.org/src/5.0/perl-5.36.0.tar.xz -o perl-5.36.0.tar.xz     && echo '0f386dccbee8e26286404b2cca144e1005be65477979beb9b1ba272d4819bcf0 *perl-5.36.0.tar.xz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.36.0.tar.xz -C /usr/src/perl     && rm perl-5.36.0.tar.xz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7046.tar.gz     && echo '3e8c9d9b44a7348f9acc917163dbfc15bd5ea72501492cea3a35b346440ff862 *App-cpanminus-1.7046.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7046.tar.gz && cd App-cpanminus-1.7046 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997011/cpm -o /usr/local/bin/cpm     && echo '7dee2176a450a8be3a6b9b91dac603a0c3a7e807042626d3fe6c93d843f75610 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7046* /tmp/*     && cpanm --version && cpm --version
# Tue, 06 Dec 2022 09:26:42 GMT
WORKDIR /
# Tue, 06 Dec 2022 09:26:42 GMT
CMD ["perl5.36.0" "-de0"]
```

-	Layers:
	-	`sha256:f2f58072e9ed1aa1b0143341c5ee83815c00ce47548309fa240155067ab0e698`  
		Last Modified: Tue, 06 Dec 2022 01:24:48 GMT  
		Size: 55.0 MB (55041342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c8cfbf51e6e6869f1af2a1e7067b07fd6733036a333c9d29f743b0285e26037`  
		Last Modified: Tue, 06 Dec 2022 02:21:44 GMT  
		Size: 5.2 MB (5164910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa3a609d15798d35c1484072876b7d22a316e98de6a097de33b9dade6a689cd1`  
		Last Modified: Tue, 06 Dec 2022 02:21:44 GMT  
		Size: 10.9 MB (10877423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:094e7d9bb04ebf214ea8dc5a488995449684104ae8ad9603bf061cac0d18eb54`  
		Last Modified: Tue, 06 Dec 2022 02:22:02 GMT  
		Size: 54.6 MB (54587090 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cbfd734f3824a4390fe4be45f6a11a5543bca1023e4814d72460eaebc2eef89`  
		Last Modified: Tue, 06 Dec 2022 02:22:38 GMT  
		Size: 196.9 MB (196869178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0930c93ecd0d3585870483335b4019211c9c78805b39be93874689100bcc6a78`  
		Last Modified: Tue, 06 Dec 2022 11:41:05 GMT  
		Size: 200.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d547cd8cc2c7ebc267dc76de06f68e4d982f385536067079f0f72a188d52d4f7`  
		Last Modified: Tue, 06 Dec 2022 11:41:08 GMT  
		Size: 15.2 MB (15230928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `perl:latest` - linux; arm variant v5

```console
$ docker pull perl@sha256:e6d5c3da8915823d74eedae6fbb16304bd96f1ddef429dd7ded80e39eb41ede7
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **310.1 MB (310078867 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44a798004c5816bf5cf7cc96e2d2ace6596ff2b554f60e40944cc896918a820f`
-	Default Command: `["perl5.36.0","-de0"]`

```dockerfile
# Tue, 06 Dec 2022 01:49:07 GMT
ADD file:92bc802977fb4abf65d3a11a702509aece192d088d815bf79a0e6bdb5a8b57c8 in / 
# Tue, 06 Dec 2022 01:49:08 GMT
CMD ["bash"]
# Tue, 06 Dec 2022 02:16:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 06 Dec 2022 02:16:59 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 06 Dec 2022 02:17:27 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 06 Dec 2022 02:18:28 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 06 Dec 2022 08:49:33 GMT
LABEL maintainer=Peter Martini <PeterCMartini@GMail.com>, Zak B. Elep <zakame@cpan.org>
# Tue, 06 Dec 2022 08:49:33 GMT
COPY file:3744c5cc39cdbdcae10db09a1f0f399005a79f93c237b387a72ff5710cdd458c in /usr/src/perl/ 
# Tue, 06 Dec 2022 08:49:33 GMT
WORKDIR /usr/src/perl
# Tue, 06 Dec 2022 08:55:41 GMT
RUN true     && curl -fL https://www.cpan.org/src/5.0/perl-5.36.0.tar.xz -o perl-5.36.0.tar.xz     && echo '0f386dccbee8e26286404b2cca144e1005be65477979beb9b1ba272d4819bcf0 *perl-5.36.0.tar.xz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.36.0.tar.xz -C /usr/src/perl     && rm perl-5.36.0.tar.xz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7046.tar.gz     && echo '3e8c9d9b44a7348f9acc917163dbfc15bd5ea72501492cea3a35b346440ff862 *App-cpanminus-1.7046.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7046.tar.gz && cd App-cpanminus-1.7046 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997011/cpm -o /usr/local/bin/cpm     && echo '7dee2176a450a8be3a6b9b91dac603a0c3a7e807042626d3fe6c93d843f75610 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7046* /tmp/*     && cpanm --version && cpm --version
# Tue, 06 Dec 2022 08:55:41 GMT
WORKDIR /
# Tue, 06 Dec 2022 08:55:42 GMT
CMD ["perl5.36.0" "-de0"]
```

-	Layers:
	-	`sha256:0eeca4d47a0d9a966ac355f8eb8d728ca02c90f2db97fac6164fb9dd7eee639f`  
		Last Modified: Tue, 06 Dec 2022 01:54:02 GMT  
		Size: 52.5 MB (52544799 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c330e998bf60345da71330a458334a9904ec525dcfd0b830b9ff405076e5e9f`  
		Last Modified: Tue, 06 Dec 2022 02:23:07 GMT  
		Size: 5.1 MB (5072274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a963630613496775b31748fdc26130adc20eebd435f6c83acf2d9901566ec2f5`  
		Last Modified: Tue, 06 Dec 2022 02:23:07 GMT  
		Size: 10.6 MB (10574287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e44d8829d6a73032763e8aefb6237c9972206128230789679a163bc113c6fbc`  
		Last Modified: Tue, 06 Dec 2022 02:23:32 GMT  
		Size: 52.3 MB (52322314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8be2b372bdbc9c1a8b0e596c98992c98c67ccb38fd56fceaf2a27e9dbfb4ff1b`  
		Last Modified: Tue, 06 Dec 2022 02:24:14 GMT  
		Size: 175.0 MB (175043908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcae88c91308ae808b011fc2c1467c36b12cf7c07317a5a6cc1b71a0ba74980f`  
		Last Modified: Tue, 06 Dec 2022 10:11:01 GMT  
		Size: 179.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efdd880680ad0f309804d74428cf7856f1e14a0c7352d4637d617b9f054f5fd3`  
		Last Modified: Tue, 06 Dec 2022 10:11:05 GMT  
		Size: 14.5 MB (14521106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `perl:latest` - linux; arm variant v7

```console
$ docker pull perl@sha256:5fdca1cec0cce204413364bc918453279e827ab0dbac4c529d292bc469039340
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.4 MB (297364425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f742cfd8907c4a5392e77cabcf2352914c7027953604cdcf7019d093206e0468`
-	Default Command: `["perl5.36.0","-de0"]`

```dockerfile
# Wed, 21 Dec 2022 01:58:09 GMT
ADD file:4b6f71680de34554595f062f9e52037b48edf19ca8f34c75877caa85c42caad3 in / 
# Wed, 21 Dec 2022 01:58:10 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 02:27:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 02:27:49 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 21 Dec 2022 02:28:11 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 02:29:03 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 03:14:38 GMT
LABEL maintainer=Peter Martini <PeterCMartini@GMail.com>, Zak B. Elep <zakame@cpan.org>
# Wed, 21 Dec 2022 03:14:39 GMT
COPY file:3744c5cc39cdbdcae10db09a1f0f399005a79f93c237b387a72ff5710cdd458c in /usr/src/perl/ 
# Wed, 21 Dec 2022 03:14:39 GMT
WORKDIR /usr/src/perl
# Wed, 21 Dec 2022 03:20:53 GMT
RUN true     && curl -fL https://www.cpan.org/src/5.0/perl-5.36.0.tar.xz -o perl-5.36.0.tar.xz     && echo '0f386dccbee8e26286404b2cca144e1005be65477979beb9b1ba272d4819bcf0 *perl-5.36.0.tar.xz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.36.0.tar.xz -C /usr/src/perl     && rm perl-5.36.0.tar.xz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7046.tar.gz     && echo '3e8c9d9b44a7348f9acc917163dbfc15bd5ea72501492cea3a35b346440ff862 *App-cpanminus-1.7046.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7046.tar.gz && cd App-cpanminus-1.7046 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997011/cpm -o /usr/local/bin/cpm     && echo '7dee2176a450a8be3a6b9b91dac603a0c3a7e807042626d3fe6c93d843f75610 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7046* /tmp/*     && cpanm --version && cpm --version
# Wed, 21 Dec 2022 03:20:53 GMT
WORKDIR /
# Wed, 21 Dec 2022 03:20:53 GMT
CMD ["perl5.36.0" "-de0"]
```

-	Layers:
	-	`sha256:706bb1d74512e1fb9ba97aa9212a32d07726fbfe77e4c7e609406d2065418f57`  
		Last Modified: Wed, 21 Dec 2022 02:04:37 GMT  
		Size: 50.2 MB (50190771 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6680cc86b286376b17781e60087f333900d6195e47181a19cc371bdfcabcaa81`  
		Last Modified: Wed, 21 Dec 2022 02:37:59 GMT  
		Size: 4.9 MB (4931334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7be4d1bc2e6499ce625dcdda5acd93b321c54ee260c695d77c968071e871021d`  
		Last Modified: Wed, 21 Dec 2022 02:37:59 GMT  
		Size: 10.2 MB (10217819 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a65a60d98682702b4ca7c54d1b60f35f73d52dc11af8d26f125673a5962046e`  
		Last Modified: Wed, 21 Dec 2022 02:38:23 GMT  
		Size: 50.3 MB (50342949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:863fbc7dd41ea590ace5d8dcbe391137f9b8170091ef531834d3f20d63f10cf1`  
		Last Modified: Wed, 21 Dec 2022 02:39:06 GMT  
		Size: 167.4 MB (167354881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:728346feafecf3fd463a033b9449233b30b6ec897c9889ae38688ad8d2d72757`  
		Last Modified: Wed, 21 Dec 2022 05:48:19 GMT  
		Size: 179.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36e1054fe4de1e073b902b6da6b9ca210b72c16778a404cc864d3d3cd911aaba`  
		Last Modified: Wed, 21 Dec 2022 05:48:19 GMT  
		Size: 14.3 MB (14326492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `perl:latest` - linux; arm64 variant v8

```console
$ docker pull perl@sha256:278a6b30c6eda98bfb43a8e6eaa536a6ed6180bc09f96cca5a037fa0c3fac310
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **329.4 MB (329370061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f656d5dd12eed2e335eece3ef6b48edaf0606cb97ddb0dbe8792d2d0a2694a5`
-	Default Command: `["perl5.36.0","-de0"]`

```dockerfile
# Wed, 21 Dec 2022 01:39:40 GMT
ADD file:5bbdc914ec8ed60ac85293e88ee1aafc3f0290762e320fc86dc9d79fa201834e in / 
# Wed, 21 Dec 2022 01:39:41 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 02:05:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 02:06:04 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 21 Dec 2022 02:06:20 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 02:07:15 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 04:07:17 GMT
LABEL maintainer=Peter Martini <PeterCMartini@GMail.com>, Zak B. Elep <zakame@cpan.org>
# Wed, 21 Dec 2022 04:07:17 GMT
COPY file:3744c5cc39cdbdcae10db09a1f0f399005a79f93c237b387a72ff5710cdd458c in /usr/src/perl/ 
# Wed, 21 Dec 2022 04:07:17 GMT
WORKDIR /usr/src/perl
# Wed, 21 Dec 2022 04:11:32 GMT
RUN true     && curl -fL https://www.cpan.org/src/5.0/perl-5.36.0.tar.xz -o perl-5.36.0.tar.xz     && echo '0f386dccbee8e26286404b2cca144e1005be65477979beb9b1ba272d4819bcf0 *perl-5.36.0.tar.xz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.36.0.tar.xz -C /usr/src/perl     && rm perl-5.36.0.tar.xz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7046.tar.gz     && echo '3e8c9d9b44a7348f9acc917163dbfc15bd5ea72501492cea3a35b346440ff862 *App-cpanminus-1.7046.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7046.tar.gz && cd App-cpanminus-1.7046 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997011/cpm -o /usr/local/bin/cpm     && echo '7dee2176a450a8be3a6b9b91dac603a0c3a7e807042626d3fe6c93d843f75610 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7046* /tmp/*     && cpanm --version && cpm --version
# Wed, 21 Dec 2022 04:11:32 GMT
WORKDIR /
# Wed, 21 Dec 2022 04:11:32 GMT
CMD ["perl5.36.0" "-de0"]
```

-	Layers:
	-	`sha256:c3e6129b48b69d14c5e7a5605e2b94003fb71aac82eac46b8689f5b8007af2c5`  
		Last Modified: Wed, 21 Dec 2022 01:42:49 GMT  
		Size: 53.7 MB (53681797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef0470f9572d03767b054118fe19e60a9c7e2510168b3a0868d9ac2953d2def5`  
		Last Modified: Wed, 21 Dec 2022 02:12:40 GMT  
		Size: 5.1 MB (5149770 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99dfcef0545e5bca269c65c0208385c886321a1e0212977299827be5346dfea5`  
		Last Modified: Wed, 21 Dec 2022 02:12:40 GMT  
		Size: 10.9 MB (10873505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:940d63caabf45c64562daab3c243c8724dd47bf45054d902ef3cb6206fc9c3f6`  
		Last Modified: Wed, 21 Dec 2022 02:12:57 GMT  
		Size: 54.7 MB (54682464 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f50438bf9d47df748db3fa6d353315cfa3b13c62806c353d37018d50cfa03d9`  
		Last Modified: Wed, 21 Dec 2022 02:13:26 GMT  
		Size: 189.8 MB (189803168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b0279f69163c5398147cb35f4392ca0f75e232708305d95d5269b97d7704fa5`  
		Last Modified: Wed, 21 Dec 2022 05:59:26 GMT  
		Size: 205.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a08bf77e39c4919e9cf8ef6bd9332ab9f2aeed664f24e5f5d295f4085e1eae2`  
		Last Modified: Wed, 21 Dec 2022 05:59:28 GMT  
		Size: 15.2 MB (15179152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `perl:latest` - linux; 386

```console
$ docker pull perl@sha256:7ab813a6b13d18178b0e2d8e8d3b5687626f94bb0c8a15309372690383a10b51
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **342.6 MB (342560093 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45d541d9245f5a1ff3dc85e526cc7f2d9848f4d86efb0829bf4f56b2b86b3c23`
-	Default Command: `["perl5.36.0","-de0"]`

```dockerfile
# Tue, 06 Dec 2022 01:39:34 GMT
ADD file:f84226ae95254e2a6a67086b709477f04fcf4d6c3a6ed05dd9cabcda0156ec04 in / 
# Tue, 06 Dec 2022 01:39:35 GMT
CMD ["bash"]
# Tue, 06 Dec 2022 02:07:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 06 Dec 2022 02:07:27 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 06 Dec 2022 02:07:49 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 06 Dec 2022 02:08:41 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 06 Dec 2022 04:14:45 GMT
LABEL maintainer=Peter Martini <PeterCMartini@GMail.com>, Zak B. Elep <zakame@cpan.org>
# Tue, 06 Dec 2022 04:14:46 GMT
COPY file:3744c5cc39cdbdcae10db09a1f0f399005a79f93c237b387a72ff5710cdd458c in /usr/src/perl/ 
# Tue, 06 Dec 2022 04:14:47 GMT
WORKDIR /usr/src/perl
# Tue, 06 Dec 2022 04:20:56 GMT
RUN true     && curl -fL https://www.cpan.org/src/5.0/perl-5.36.0.tar.xz -o perl-5.36.0.tar.xz     && echo '0f386dccbee8e26286404b2cca144e1005be65477979beb9b1ba272d4819bcf0 *perl-5.36.0.tar.xz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.36.0.tar.xz -C /usr/src/perl     && rm perl-5.36.0.tar.xz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7046.tar.gz     && echo '3e8c9d9b44a7348f9acc917163dbfc15bd5ea72501492cea3a35b346440ff862 *App-cpanminus-1.7046.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7046.tar.gz && cd App-cpanminus-1.7046 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997011/cpm -o /usr/local/bin/cpm     && echo '7dee2176a450a8be3a6b9b91dac603a0c3a7e807042626d3fe6c93d843f75610 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7046* /tmp/*     && cpanm --version && cpm --version
# Tue, 06 Dec 2022 04:20:57 GMT
WORKDIR /
# Tue, 06 Dec 2022 04:20:58 GMT
CMD ["perl5.36.0" "-de0"]
```

-	Layers:
	-	`sha256:a9be27fc8e6e19a1a3d5f3a8805c7b1a4c21e2db96b34ed6fd26bb06b286b67f`  
		Last Modified: Tue, 06 Dec 2022 01:45:14 GMT  
		Size: 56.0 MB (56022389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdeaec533b8156939ec8efa8656d8e265815f8ff149d6e08269eb479f2cd727e`  
		Last Modified: Tue, 06 Dec 2022 02:15:16 GMT  
		Size: 5.1 MB (5086953 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbe9a9bc77fb252ac70f975f35cdebf672b81d5e45817cff584306bc1f7be395`  
		Last Modified: Tue, 06 Dec 2022 02:15:16 GMT  
		Size: 11.0 MB (11032586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a46762e3a77ee43666072e46a63adfa4169382825df90ef576d25a952a7f4a9`  
		Last Modified: Tue, 06 Dec 2022 02:15:37 GMT  
		Size: 55.9 MB (55924390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f7a3820cd92329345116b9528b2651e6ed8776b06f176429968547d5d46dd92`  
		Last Modified: Tue, 06 Dec 2022 02:16:19 GMT  
		Size: 199.8 MB (199769362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:169a9e9d1404dc6b16968c276aecec768d8382b752a0dc74103020f7bf484a54`  
		Last Modified: Tue, 06 Dec 2022 06:53:03 GMT  
		Size: 178.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e906104903113918a4633ed25748eafa7b0479a7e401fd91dd0e0a75f60fbd7c`  
		Last Modified: Tue, 06 Dec 2022 06:53:06 GMT  
		Size: 14.7 MB (14724235 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `perl:latest` - linux; mips64le

```console
$ docker pull perl@sha256:8505e0ce6be80a3ff52ddefe7fe0f5bf1ced0b5bba5d9b7965479e932ea6cd63
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **315.6 MB (315576117 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2cd6396936b202a4450bc4b38e9a59a604866818009bebf0bb0a263b8196e020`
-	Default Command: `["perl5.36.0","-de0"]`

```dockerfile
# Tue, 06 Dec 2022 01:54:55 GMT
ADD file:09d48994a41c54566f7123db033773e6246c0703a518af76843198196cd39645 in / 
# Tue, 06 Dec 2022 01:55:00 GMT
CMD ["bash"]
# Tue, 06 Dec 2022 17:16:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 06 Dec 2022 17:16:47 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 06 Dec 2022 17:18:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 06 Dec 2022 17:23:43 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 07 Dec 2022 03:40:50 GMT
LABEL maintainer=Peter Martini <PeterCMartini@GMail.com>, Zak B. Elep <zakame@cpan.org>
# Wed, 07 Dec 2022 03:40:55 GMT
COPY file:3744c5cc39cdbdcae10db09a1f0f399005a79f93c237b387a72ff5710cdd458c in /usr/src/perl/ 
# Wed, 07 Dec 2022 03:41:01 GMT
WORKDIR /usr/src/perl
# Wed, 07 Dec 2022 04:03:09 GMT
RUN true     && curl -fL https://www.cpan.org/src/5.0/perl-5.36.0.tar.xz -o perl-5.36.0.tar.xz     && echo '0f386dccbee8e26286404b2cca144e1005be65477979beb9b1ba272d4819bcf0 *perl-5.36.0.tar.xz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.36.0.tar.xz -C /usr/src/perl     && rm perl-5.36.0.tar.xz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7046.tar.gz     && echo '3e8c9d9b44a7348f9acc917163dbfc15bd5ea72501492cea3a35b346440ff862 *App-cpanminus-1.7046.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7046.tar.gz && cd App-cpanminus-1.7046 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997011/cpm -o /usr/local/bin/cpm     && echo '7dee2176a450a8be3a6b9b91dac603a0c3a7e807042626d3fe6c93d843f75610 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7046* /tmp/*     && cpanm --version && cpm --version
# Wed, 07 Dec 2022 04:03:16 GMT
WORKDIR /
# Wed, 07 Dec 2022 04:03:22 GMT
CMD ["perl5.36.0" "-de0"]
```

-	Layers:
	-	`sha256:acb57a81743c28ead1a32571c107ac15cd970593fea4f2954b57f22e6bbad1d0`  
		Last Modified: Tue, 06 Dec 2022 02:02:59 GMT  
		Size: 53.3 MB (53260631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3775e3b48d5b75d557cd315824f4c6f06a699ddbda90085efdafca39708308cb`  
		Last Modified: Tue, 06 Dec 2022 17:36:12 GMT  
		Size: 4.9 MB (4919540 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:226edb4ba5e4851b2344de27abb2912005f2259d9a16819ef66c22ca5eff8c4d`  
		Last Modified: Tue, 06 Dec 2022 17:36:14 GMT  
		Size: 10.7 MB (10661692 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:983b5b89a87657fcfac5cae3540e343a9cf77d6e10cf3eb736a4e46608390212`  
		Last Modified: Tue, 06 Dec 2022 17:37:02 GMT  
		Size: 53.3 MB (53306766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:005791f776c3cbe2a6500e8c8e134cfb1061735ab9cc82bbda48536dc55c0840`  
		Last Modified: Tue, 06 Dec 2022 17:39:05 GMT  
		Size: 179.0 MB (178979694 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe96d7b0f8dba2070c5569b7008d644b52d82e6b8bfe5d9ee45852271c28f477`  
		Last Modified: Wed, 07 Dec 2022 05:59:36 GMT  
		Size: 180.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fc03bf72f041ed99c17641318bc7712fb15cfbb955cb4e187a42b82ade89fdc`  
		Last Modified: Wed, 07 Dec 2022 05:59:48 GMT  
		Size: 14.4 MB (14447614 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `perl:latest` - linux; ppc64le

```console
$ docker pull perl@sha256:e28c5d7e0926e705ca6368861412db3a94dc2dd88b57263cd7a5db4c939f7205
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **346.3 MB (346277403 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85862c291d04def3ef68b4ea4f83c0da68c4f979048cc7e402c340231d253dc1`
-	Default Command: `["perl5.36.0","-de0"]`

```dockerfile
# Wed, 21 Dec 2022 01:17:21 GMT
ADD file:c95bdb0df70fa9ce48b31a7ceb8a7be0c5b925efcf01c43595868b86994dc192 in / 
# Wed, 21 Dec 2022 01:17:25 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 04:54:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 04:54:49 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 21 Dec 2022 04:55:32 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 04:57:30 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 05:26:03 GMT
LABEL maintainer=Peter Martini <PeterCMartini@GMail.com>, Zak B. Elep <zakame@cpan.org>
# Wed, 21 Dec 2022 05:26:03 GMT
COPY file:3744c5cc39cdbdcae10db09a1f0f399005a79f93c237b387a72ff5710cdd458c in /usr/src/perl/ 
# Wed, 21 Dec 2022 05:26:03 GMT
WORKDIR /usr/src/perl
# Wed, 21 Dec 2022 05:33:52 GMT
RUN true     && curl -fL https://www.cpan.org/src/5.0/perl-5.36.0.tar.xz -o perl-5.36.0.tar.xz     && echo '0f386dccbee8e26286404b2cca144e1005be65477979beb9b1ba272d4819bcf0 *perl-5.36.0.tar.xz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.36.0.tar.xz -C /usr/src/perl     && rm perl-5.36.0.tar.xz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7046.tar.gz     && echo '3e8c9d9b44a7348f9acc917163dbfc15bd5ea72501492cea3a35b346440ff862 *App-cpanminus-1.7046.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7046.tar.gz && cd App-cpanminus-1.7046 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997011/cpm -o /usr/local/bin/cpm     && echo '7dee2176a450a8be3a6b9b91dac603a0c3a7e807042626d3fe6c93d843f75610 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7046* /tmp/*     && cpanm --version && cpm --version
# Wed, 21 Dec 2022 05:33:53 GMT
WORKDIR /
# Wed, 21 Dec 2022 05:33:53 GMT
CMD ["perl5.36.0" "-de0"]
```

-	Layers:
	-	`sha256:542880f4d15404af17d342ecbb76bb92724fc7cb8a91a5e18f26bd8f8811a38a`  
		Last Modified: Wed, 21 Dec 2022 01:22:46 GMT  
		Size: 58.9 MB (58897040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9b0d1697a3bff7991f1c96b22ffd254326c700694ddcf45ba42cd27f8a9cb94`  
		Last Modified: Wed, 21 Dec 2022 05:06:06 GMT  
		Size: 5.4 MB (5413147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5363f0c14d79c77678586642d6ff9ef822416864a8358da267bef743bb215907`  
		Last Modified: Wed, 21 Dec 2022 05:06:07 GMT  
		Size: 11.6 MB (11629527 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ec399ef8d37e347a1f93e54dd49428d1cec8a8926b5b48c5823c1e9813d561a`  
		Last Modified: Wed, 21 Dec 2022 05:06:38 GMT  
		Size: 58.9 MB (58866093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebe8cb6c21b75ae2fbcc74642a4953de0fae1083c05384c2ee8e1152859f1384`  
		Last Modified: Wed, 21 Dec 2022 05:07:40 GMT  
		Size: 196.2 MB (196229879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a32a6572de312c305c89d009b04110e03dfa48881a7248ed7c67672335b88b7`  
		Last Modified: Wed, 21 Dec 2022 07:10:32 GMT  
		Size: 202.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f592eb05a71ba2a87e1d9552634ae8c96e9d5f88e95b1ce61e4dd27061e684ba`  
		Last Modified: Wed, 21 Dec 2022 07:10:38 GMT  
		Size: 15.2 MB (15241515 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `perl:latest` - linux; s390x

```console
$ docker pull perl@sha256:96ab2786379eda899efc974f7368369b1cd6bf03f167ffc9c78b88160d7bf768
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **311.7 MB (311688205 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a355ba225fa09c18dca14306de7327300c730dd9b6ebc71bd0db2e8b58a703e`
-	Default Command: `["perl5.36.0","-de0"]`

```dockerfile
# Wed, 21 Dec 2022 01:42:51 GMT
ADD file:22c4f2d41083ce4433bec4a71e7e6ddc5bec8e44e9cf2c9f93d0874b5b4de7c3 in / 
# Wed, 21 Dec 2022 01:42:54 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 05:28:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 05:28:19 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 21 Dec 2022 05:29:12 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 05:31:22 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 06:00:04 GMT
LABEL maintainer=Peter Martini <PeterCMartini@GMail.com>, Zak B. Elep <zakame@cpan.org>
# Wed, 21 Dec 2022 06:00:04 GMT
COPY file:3744c5cc39cdbdcae10db09a1f0f399005a79f93c237b387a72ff5710cdd458c in /usr/src/perl/ 
# Wed, 21 Dec 2022 06:00:05 GMT
WORKDIR /usr/src/perl
# Wed, 21 Dec 2022 06:07:24 GMT
RUN true     && curl -fL https://www.cpan.org/src/5.0/perl-5.36.0.tar.xz -o perl-5.36.0.tar.xz     && echo '0f386dccbee8e26286404b2cca144e1005be65477979beb9b1ba272d4819bcf0 *perl-5.36.0.tar.xz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.36.0.tar.xz -C /usr/src/perl     && rm perl-5.36.0.tar.xz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7046.tar.gz     && echo '3e8c9d9b44a7348f9acc917163dbfc15bd5ea72501492cea3a35b346440ff862 *App-cpanminus-1.7046.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7046.tar.gz && cd App-cpanminus-1.7046 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997011/cpm -o /usr/local/bin/cpm     && echo '7dee2176a450a8be3a6b9b91dac603a0c3a7e807042626d3fe6c93d843f75610 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7046* /tmp/*     && cpanm --version && cpm --version
# Wed, 21 Dec 2022 06:07:28 GMT
WORKDIR /
# Wed, 21 Dec 2022 06:07:29 GMT
CMD ["perl5.36.0" "-de0"]
```

-	Layers:
	-	`sha256:7f45294776f4c97d23f8dbfca98d4b57701b478eedfcb154a7e7dc6d6954ba44`  
		Last Modified: Wed, 21 Dec 2022 01:48:50 GMT  
		Size: 53.3 MB (53258472 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33059268c0ceb39818d5991d1a0e968b0ac63a17cd965fc4a7094dae7b286bff`  
		Last Modified: Wed, 21 Dec 2022 05:41:10 GMT  
		Size: 5.1 MB (5147132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adad3194d340e6c5e79c1917e144d792bb5073c3e126f969f1695bc449822315`  
		Last Modified: Wed, 21 Dec 2022 05:41:11 GMT  
		Size: 10.8 MB (10766081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a479ec115bd827027c66c90c65bac92d04e338c0cc00025b35dbfc756f4fbbd9`  
		Last Modified: Wed, 21 Dec 2022 05:41:30 GMT  
		Size: 54.1 MB (54054846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1be60c4ac9a8d51fbb8d4c3843e2016173124b685f731ad093fb907b8b208ea7`  
		Last Modified: Wed, 21 Dec 2022 05:41:58 GMT  
		Size: 172.9 MB (172868922 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e5749158b3c28465615cf15dcc1a9465e97d77720758571d6d465daa6aef8b8`  
		Last Modified: Wed, 21 Dec 2022 07:45:54 GMT  
		Size: 203.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ca720990847a7b655f81a922b59204d7653dc666580a9b29f009a352e0d33e8`  
		Last Modified: Wed, 21 Dec 2022 07:45:57 GMT  
		Size: 15.6 MB (15592549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
