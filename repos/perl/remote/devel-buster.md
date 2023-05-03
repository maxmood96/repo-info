## `perl:devel-buster`

```console
$ docker pull perl@sha256:d2cc7e5b782c346be35014ad5a24890a0dda735338a74970fac318470099d04c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `perl:devel-buster` - linux; amd64

```console
$ docker pull perl@sha256:e076350f881aea3dc77c8f6e2bc988605a5f31dbef6227b998cca02bdc96ea14
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **327.4 MB (327428315 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c3335fb52d72abd210a87dd486ed638c22026b9f87811d181db08cc1ed4f41d`
-	Default Command: `["perl5.37.11","-de0"]`

```dockerfile
# Wed, 12 Apr 2023 00:20:15 GMT
ADD file:40953ed6e6f96703b2e0c13288437c2aaf8b3df33dbc423686290cbe0e595a5e in / 
# Wed, 12 Apr 2023 00:20:15 GMT
CMD ["bash"]
# Tue, 02 May 2023 23:14:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 May 2023 23:14:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 02 May 2023 23:15:58 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 03 May 2023 13:04:11 GMT
LABEL maintainer=Peter Martini <PeterCMartini@GMail.com>, Zak B. Elep <zakame@cpan.org>
# Wed, 03 May 2023 13:04:11 GMT
WORKDIR /usr/src/perl
# Wed, 03 May 2023 15:23:42 GMT
RUN true     && curl -fL https://www.cpan.org/src/5.0/perl-5.37.11.tar.xz -o perl-5.37.11.tar.xz     && echo '3946b00266595ccc44df28275e2fbb7b86c1482934cbeab2780db304a75ffd58 *perl-5.37.11.tar.xz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.37.11.tar.xz -C /usr/src/perl     && rm perl-5.37.11.tar.xz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7046.tar.gz     && echo '3e8c9d9b44a7348f9acc917163dbfc15bd5ea72501492cea3a35b346440ff862 *App-cpanminus-1.7046.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7046.tar.gz && cd App-cpanminus-1.7046 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997011/cpm -o /usr/local/bin/cpm     && echo '7dee2176a450a8be3a6b9b91dac603a0c3a7e807042626d3fe6c93d843f75610 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7046* /tmp/*     && cpanm --version && cpm --version
# Wed, 03 May 2023 15:23:42 GMT
WORKDIR /
# Wed, 03 May 2023 15:23:42 GMT
CMD ["perl5.37.11" "-de0"]
```

-	Layers:
	-	`sha256:2ff1d7c41c74a25258bfa6f0b8adb0a727f84518f55f65ca845ebc747976c408`  
		Last Modified: Wed, 12 Apr 2023 00:24:01 GMT  
		Size: 50.4 MB (50448726 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b19b5081b1db3d1f9cb6b976463daaf186eb48aa03d63ea69a4b09f3506e6839`  
		Last Modified: Tue, 02 May 2023 23:39:53 GMT  
		Size: 17.6 MB (17580546 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fab42f58c1ef3e6849f7c792aaa60c56b53a70e77977fca6fd201578b6295b1`  
		Last Modified: Tue, 02 May 2023 23:40:08 GMT  
		Size: 51.9 MB (51878611 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30b32f0da361e0e47d8706b2af769c8f4e0f3c3ae6d924174dd1a45bb7cb68c4`  
		Last Modified: Tue, 02 May 2023 23:40:38 GMT  
		Size: 191.9 MB (191872221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e61dc1fb02c02d0d6d99719d0f23502541054f9928b2f41cbd1d67397389a7ee`  
		Last Modified: Wed, 03 May 2023 16:00:48 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4af8fa66cfa5f9af996a46b0c3c0a598679900dbffc472da342a7cb86f5a6465`  
		Last Modified: Wed, 03 May 2023 16:07:18 GMT  
		Size: 15.6 MB (15648042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `perl:devel-buster` - linux; arm variant v7

```console
$ docker pull perl@sha256:ad78d2f32f5b65943e3de6aa8eb5df08ab53880529a04f3af78fab06dd29bd48
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.6 MB (292645822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:369bfa8e6c7fcf76b4d99443587b94517fb2aaabdb06282ef96e4714efddb4fc`
-	Default Command: `["perl5.37.11","-de0"]`

```dockerfile
# Tue, 11 Apr 2023 23:59:53 GMT
ADD file:3f6ca36ec4fbf50ab85c907c089dbb0618c73393c07a5841b922145b17795552 in / 
# Tue, 11 Apr 2023 23:59:54 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 09:37:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 09:37:35 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 12 Apr 2023 09:37:57 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 09:39:43 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 16:55:48 GMT
LABEL maintainer=Peter Martini <PeterCMartini@GMail.com>, Zak B. Elep <zakame@cpan.org>
# Wed, 12 Apr 2023 16:55:49 GMT
WORKDIR /usr/src/perl
# Fri, 21 Apr 2023 19:26:43 GMT
RUN true     && curl -fL https://www.cpan.org/src/5.0/perl-5.37.11.tar.xz -o perl-5.37.11.tar.xz     && echo '3946b00266595ccc44df28275e2fbb7b86c1482934cbeab2780db304a75ffd58 *perl-5.37.11.tar.xz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.37.11.tar.xz -C /usr/src/perl     && rm perl-5.37.11.tar.xz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7046.tar.gz     && echo '3e8c9d9b44a7348f9acc917163dbfc15bd5ea72501492cea3a35b346440ff862 *App-cpanminus-1.7046.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7046.tar.gz && cd App-cpanminus-1.7046 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997011/cpm -o /usr/local/bin/cpm     && echo '7dee2176a450a8be3a6b9b91dac603a0c3a7e807042626d3fe6c93d843f75610 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7046* /tmp/*     && cpanm --version && cpm --version
# Fri, 21 Apr 2023 19:26:43 GMT
WORKDIR /
# Fri, 21 Apr 2023 19:26:44 GMT
CMD ["perl5.37.11" "-de0"]
```

-	Layers:
	-	`sha256:166ef90dbaeab03f451f526d325c57795001e25f10c984c334a82d174b3c554b`  
		Last Modified: Wed, 12 Apr 2023 00:03:36 GMT  
		Size: 45.9 MB (45916201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84460c1688b734c8075a939aae674e32cf7240a0d3a2fa0602a9a9fd472ffe1e`  
		Last Modified: Wed, 12 Apr 2023 09:46:16 GMT  
		Size: 7.2 MB (7153935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ed4779654861d62e5bc31eea7bacd2c7bbfdb617dd9dc01e2afd24a4baedf7f`  
		Last Modified: Wed, 12 Apr 2023 09:46:17 GMT  
		Size: 9.3 MB (9348985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6bfe04b18e678bcacb84dd292223f32a76d4837c22ccd16465318f6c1429f21`  
		Last Modified: Wed, 12 Apr 2023 09:46:34 GMT  
		Size: 47.4 MB (47395508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc69a47db99b12842846092749a24bc3d2701f5e6b46467a6eb56e1d19ed48a3`  
		Last Modified: Wed, 12 Apr 2023 09:47:09 GMT  
		Size: 168.1 MB (168057207 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86eb05016e399483547b514b636debb38599d2ec6b8785b381139e901bb63e71`  
		Last Modified: Wed, 12 Apr 2023 18:17:41 GMT  
		Size: 168.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2808d8a9de463bf2b3d5362bb93864e5e98e996e681e09578c47ba691bf0d7a8`  
		Last Modified: Fri, 21 Apr 2023 20:02:55 GMT  
		Size: 14.8 MB (14773818 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `perl:devel-buster` - linux; arm64 variant v8

```console
$ docker pull perl@sha256:048d74554cd726c52075e60bb6f143b62bb2fba73e1c7372c806b9b410fd4c27
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **317.9 MB (317924875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba4944bfc86ab95cfca1612200db03da184f873d2a487d9ec2ad3d88351d2825`
-	Default Command: `["perl5.37.11","-de0"]`

```dockerfile
# Wed, 12 Apr 2023 00:39:55 GMT
ADD file:93facc669dd63b37fb5dde18f3b3a1cb5621aa396e1960ea85facdd1c619a3f0 in / 
# Wed, 12 Apr 2023 00:39:56 GMT
CMD ["bash"]
# Tue, 02 May 2023 23:43:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 May 2023 23:43:34 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 02 May 2023 23:44:35 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 03 May 2023 14:31:13 GMT
LABEL maintainer=Peter Martini <PeterCMartini@GMail.com>, Zak B. Elep <zakame@cpan.org>
# Wed, 03 May 2023 14:31:13 GMT
WORKDIR /usr/src/perl
# Wed, 03 May 2023 16:25:43 GMT
RUN true     && curl -fL https://www.cpan.org/src/5.0/perl-5.37.11.tar.xz -o perl-5.37.11.tar.xz     && echo '3946b00266595ccc44df28275e2fbb7b86c1482934cbeab2780db304a75ffd58 *perl-5.37.11.tar.xz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.37.11.tar.xz -C /usr/src/perl     && rm perl-5.37.11.tar.xz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7046.tar.gz     && echo '3e8c9d9b44a7348f9acc917163dbfc15bd5ea72501492cea3a35b346440ff862 *App-cpanminus-1.7046.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7046.tar.gz && cd App-cpanminus-1.7046 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997011/cpm -o /usr/local/bin/cpm     && echo '7dee2176a450a8be3a6b9b91dac603a0c3a7e807042626d3fe6c93d843f75610 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7046* /tmp/*     && cpanm --version && cpm --version
# Wed, 03 May 2023 16:25:43 GMT
WORKDIR /
# Wed, 03 May 2023 16:25:43 GMT
CMD ["perl5.37.11" "-de0"]
```

-	Layers:
	-	`sha256:b4910c31031a0301ea4f8b7155269014925aeb17c71b869dea3ff907ba294b55`  
		Last Modified: Wed, 12 Apr 2023 00:42:52 GMT  
		Size: 49.2 MB (49238632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e042bd0c79f2e6cf6975eda3666cdf47590abd026d899660748cbe08726e637`  
		Last Modified: Wed, 03 May 2023 00:12:10 GMT  
		Size: 17.5 MB (17450343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f95dbd7c8c788f8388b151696aa516e98f0a3d0b8d6390f6f5d5a64be53fb135`  
		Last Modified: Wed, 03 May 2023 00:12:24 GMT  
		Size: 52.2 MB (52190952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7ce51d34f86aa68767b4fd179baadbbaa8c48d4aefdaa68df9431bde3d8ab24`  
		Last Modified: Wed, 03 May 2023 00:12:48 GMT  
		Size: 183.5 MB (183455129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6f8a2d9a3ac80be84a238f37ec0f83e8eef21f561326c102895da536bf1aeb7`  
		Last Modified: Wed, 03 May 2023 16:56:17 GMT  
		Size: 168.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b21a96a876210a8fcd69f9ad8a78e11fee6875e7e88433925e0206305d2c2efe`  
		Last Modified: Wed, 03 May 2023 17:02:22 GMT  
		Size: 15.6 MB (15589651 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `perl:devel-buster` - linux; 386

```console
$ docker pull perl@sha256:6348c0bcb2342b647f75efd23c713f4626de570d9b81f6f6bda6476e5ce143ba
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **336.4 MB (336355984 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5449d7c389835e9e57bca6852eaa6db8888a964436ade0dfa4af6156661ca458`
-	Default Command: `["perl5.37.11","-de0"]`

```dockerfile
# Wed, 12 Apr 2023 00:39:11 GMT
ADD file:8299e58c7e43af1f3b9fdb9bd37e3f37cf619a97ef1b87d60ca66860d646d526 in / 
# Wed, 12 Apr 2023 00:39:11 GMT
CMD ["bash"]
# Tue, 02 May 2023 23:44:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 May 2023 23:44:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 02 May 2023 23:46:59 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 03 May 2023 12:53:16 GMT
LABEL maintainer=Peter Martini <PeterCMartini@GMail.com>, Zak B. Elep <zakame@cpan.org>
# Wed, 03 May 2023 12:53:16 GMT
WORKDIR /usr/src/perl
# Wed, 03 May 2023 16:50:58 GMT
RUN true     && curl -fL https://www.cpan.org/src/5.0/perl-5.37.11.tar.xz -o perl-5.37.11.tar.xz     && echo '3946b00266595ccc44df28275e2fbb7b86c1482934cbeab2780db304a75ffd58 *perl-5.37.11.tar.xz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.37.11.tar.xz -C /usr/src/perl     && rm perl-5.37.11.tar.xz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7046.tar.gz     && echo '3e8c9d9b44a7348f9acc917163dbfc15bd5ea72501492cea3a35b346440ff862 *App-cpanminus-1.7046.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7046.tar.gz && cd App-cpanminus-1.7046 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997011/cpm -o /usr/local/bin/cpm     && echo '7dee2176a450a8be3a6b9b91dac603a0c3a7e807042626d3fe6c93d843f75610 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7046* /tmp/*     && cpanm --version && cpm --version
# Wed, 03 May 2023 16:50:58 GMT
WORKDIR /
# Wed, 03 May 2023 16:50:58 GMT
CMD ["perl5.37.11" "-de0"]
```

-	Layers:
	-	`sha256:2d15e1c2a3da7d675c2513d7ceab1d0f33ced9a82bed63d9a11ce71f1218d232`  
		Last Modified: Wed, 12 Apr 2023 00:43:07 GMT  
		Size: 51.2 MB (51206167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bd99c81a486e88f0f0651f64eb17ab23ef66618d2702b301568e0dedde54f37`  
		Last Modified: Tue, 02 May 2023 23:56:17 GMT  
		Size: 18.1 MB (18097666 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7eb713ce4d6df9acc34bad743fb201e85ffd28c4667280dd9af9bdf5f80f2a46`  
		Last Modified: Tue, 02 May 2023 23:56:36 GMT  
		Size: 53.5 MB (53473895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b97e1e4ced90457352bffe63b02b1f7abb90bb492d1d96dbb2f19ddfa467f5d1`  
		Last Modified: Tue, 02 May 2023 23:57:18 GMT  
		Size: 198.4 MB (198424393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:572a9835ba14fc704600b320d955523ab1fecac05c6cae471aefad327af30c4a`  
		Last Modified: Wed, 03 May 2023 17:51:03 GMT  
		Size: 167.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:896cbe3f3e1216211ee93a04a36eb9df266a52593af7cc7a682c810a63f8a16d`  
		Last Modified: Wed, 03 May 2023 17:58:12 GMT  
		Size: 15.2 MB (15153696 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
