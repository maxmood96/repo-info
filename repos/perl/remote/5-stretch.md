## `perl:5-stretch`

```console
$ docker pull perl@sha256:cf1bf3ffd3f484e3514d7a42a71d7e29049bd816d38fb6213096061ad2b16f4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `perl:5-stretch` - linux; amd64

```console
$ docker pull perl@sha256:d7145f6820c2fe132398632e59c9dd872a98b1096b82c02cdc32d350df46ee17
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **339.3 MB (339309493 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5a349da73ff768bbfd7f0ae9b3f32dddd4c482cbcf5af8bd40f84583c9df96f`
-	Default Command: `["perl5.30.2","-de0"]`

```dockerfile
# Tue, 31 Mar 2020 01:23:50 GMT
ADD file:774b5e2033bb42ad97daa64267a5f041124cc0b05ec0198f1b5578ceea5a48e4 in / 
# Tue, 31 Mar 2020 01:23:51 GMT
CMD ["bash"]
# Tue, 31 Mar 2020 02:06:41 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 02:06:47 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 31 Mar 2020 02:07:10 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 02:08:07 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 08:53:26 GMT
LABEL maintainer=Peter Martini <PeterCMartini@GMail.com>, Zak B. Elep <zakame@cpan.org>
# Tue, 31 Mar 2020 08:53:27 GMT
COPY file:15650064fd29deac721f0aa084ddb3d41db77b78e2907775e257bd67e116ade4 in /usr/src/perl/ 
# Tue, 31 Mar 2020 08:53:27 GMT
WORKDIR /usr/src/perl
# Tue, 31 Mar 2020 09:06:20 GMT
RUN true     && curl -SL https://www.cpan.org/src/5.0/perl-5.30.2.tar.xz -o perl-5.30.2.tar.xz     && echo 'a1aa88bd6fbbdc2e82938afbb76c408b0ea847317737b712dc196cc7907a5259 *perl-5.30.2.tar.xz' | sha256sum -c -     && tar --strip-components=1 -xaf perl-5.30.2.tar.xz -C /usr/src/perl     && rm perl-5.30.2.tar.xz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -LO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7044.tar.gz     && echo '9b60767fe40752ef7a9d3f13f19060a63389a5c23acc3e9827e19b75500f81f3 *App-cpanminus-1.7044.tar.gz' | sha256sum -c -     && tar -xzf App-cpanminus-1.7044.tar.gz && cd App-cpanminus-1.7044 && perl bin/cpanm . && cd /root     && true     && rm -fr ./cpanm /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7044* /tmp/*
# Tue, 31 Mar 2020 09:06:21 GMT
WORKDIR /
# Tue, 31 Mar 2020 09:06:21 GMT
CMD ["perl5.30.2" "-de0"]
```

-	Layers:
	-	`sha256:56da78ce36e97a8ba1f860575bb1422d1cb6ab4dade70b06ddf1651302dde955`  
		Last Modified: Tue, 31 Mar 2020 01:29:15 GMT  
		Size: 45.4 MB (45375928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbfe0f13ac4531fb6d077fda0e94ced4b9ed8a354c54b4efced9b7755d3f39d1`  
		Last Modified: Tue, 31 Mar 2020 02:12:44 GMT  
		Size: 10.8 MB (10797329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6254ff6d0e6052b7bead70e37703002eda28ac40f9a1167ea9bf813bf9c17d7f`  
		Last Modified: Tue, 31 Mar 2020 02:12:43 GMT  
		Size: 4.3 MB (4340113 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0e1e13bd9f6c381f158a5366b3eff242e8b4a4decfa940e915b1d5705ef4a28`  
		Last Modified: Tue, 31 Mar 2020 02:12:58 GMT  
		Size: 50.1 MB (50071604 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b86b38b40a24c042077b816eebfc5356bf938c6aed3069e102175ef1720416b8`  
		Last Modified: Tue, 31 Mar 2020 02:13:37 GMT  
		Size: 214.9 MB (214906068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f53e6370ec49bdbaa334892ec53ccccea0a1de71707fb2974fde3a9185ed8d4`  
		Last Modified: Tue, 31 Mar 2020 13:16:39 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0c49b88026c6307dd6b0703278faa50c21a9781d2bfb6b382301366e25f13e3`  
		Last Modified: Tue, 31 Mar 2020 13:16:43 GMT  
		Size: 13.8 MB (13818036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `perl:5-stretch` - linux; arm variant v7

```console
$ docker pull perl@sha256:9ddb4140675242f63a2fc1d399be04fd599060ebb0c76943b5410d83a87a963a
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **310.5 MB (310483513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54b071b3536704defcf492f28ad16c0b1d6be29bc33b9d658d7e269b24e0a683`
-	Default Command: `["perl5.30.2","-de0"]`

```dockerfile
# Thu, 16 Apr 2020 01:04:37 GMT
ADD file:b83ed4f9f7c8b10eba728f85030722a771b39336afd7ff9eef2eb6b94791533e in / 
# Thu, 16 Apr 2020 01:04:40 GMT
CMD ["bash"]
# Thu, 16 Apr 2020 01:50:11 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Thu, 16 Apr 2020 01:50:28 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 16 Apr 2020 01:51:15 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 16 Apr 2020 01:53:53 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 16 Apr 2020 05:36:12 GMT
LABEL maintainer=Peter Martini <PeterCMartini@GMail.com>, Zak B. Elep <zakame@cpan.org>
# Thu, 16 Apr 2020 05:36:12 GMT
COPY file:15650064fd29deac721f0aa084ddb3d41db77b78e2907775e257bd67e116ade4 in /usr/src/perl/ 
# Thu, 16 Apr 2020 05:36:13 GMT
WORKDIR /usr/src/perl
# Thu, 16 Apr 2020 05:46:04 GMT
RUN true     && curl -SL https://www.cpan.org/src/5.0/perl-5.30.2.tar.xz -o perl-5.30.2.tar.xz     && echo 'a1aa88bd6fbbdc2e82938afbb76c408b0ea847317737b712dc196cc7907a5259 *perl-5.30.2.tar.xz' | sha256sum -c -     && tar --strip-components=1 -xaf perl-5.30.2.tar.xz -C /usr/src/perl     && rm perl-5.30.2.tar.xz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -LO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7044.tar.gz     && echo '9b60767fe40752ef7a9d3f13f19060a63389a5c23acc3e9827e19b75500f81f3 *App-cpanminus-1.7044.tar.gz' | sha256sum -c -     && tar -xzf App-cpanminus-1.7044.tar.gz && cd App-cpanminus-1.7044 && perl bin/cpanm . && cd /root     && true     && rm -fr ./cpanm /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7044* /tmp/*
# Thu, 16 Apr 2020 05:46:06 GMT
WORKDIR /
# Thu, 16 Apr 2020 05:46:07 GMT
CMD ["perl5.30.2" "-de0"]
```

-	Layers:
	-	`sha256:37d8a5aac9ec54f7757e1243cff051c8372be0cf907e086fba2607e08d2a4135`  
		Last Modified: Thu, 16 Apr 2020 01:12:16 GMT  
		Size: 42.1 MB (42101227 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3f4f4abba4245745ee86a35473696f5ecbe961a03af35bd6f07b2253c3bedba`  
		Last Modified: Thu, 16 Apr 2020 01:59:44 GMT  
		Size: 9.5 MB (9498336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3accf104e4ac412a36f3c1fc31fb94722661bf356ac878a4b502dc20086c8d2f`  
		Last Modified: Thu, 16 Apr 2020 01:59:42 GMT  
		Size: 3.9 MB (3918841 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b661b06bea35fef2d1bfd84e8d9bb0f243557b3d08139187ad1d0956db6fccc0`  
		Last Modified: Thu, 16 Apr 2020 02:00:05 GMT  
		Size: 46.4 MB (46410934 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bfd73fcb2a87267ab0f0d969574064aa6b804681b72b3642486b35336335d3e`  
		Last Modified: Thu, 16 Apr 2020 02:01:03 GMT  
		Size: 195.6 MB (195565244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9094588a67f2567b2988727ade552537b7023cae340f827b08b52f5763c1c189`  
		Last Modified: Thu, 16 Apr 2020 09:46:27 GMT  
		Size: 441.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37d6524c0a7e6ef233d78aee96ca29d8903000285291bde1f09521e664ceafa0`  
		Last Modified: Thu, 16 Apr 2020 09:46:33 GMT  
		Size: 13.0 MB (12988490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `perl:5-stretch` - linux; arm64 variant v8

```console
$ docker pull perl@sha256:900013e643733a861ef6f43dac164adddee0e21381c42a8095999c034fe05913
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **321.0 MB (320963666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:081fedff13006e43b0f5deb8b3462b6366438194f4774c2dea0a0aa78fd66f24`
-	Default Command: `["perl5.30.2","-de0"]`

```dockerfile
# Thu, 16 Apr 2020 02:44:49 GMT
ADD file:6d09304a2db2752e78b9ce9610594102dc756aa4cd210f85bbfa21105c7dd88f in / 
# Thu, 16 Apr 2020 02:44:52 GMT
CMD ["bash"]
# Thu, 16 Apr 2020 03:21:36 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Thu, 16 Apr 2020 03:21:48 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 16 Apr 2020 03:22:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 16 Apr 2020 03:25:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 16 Apr 2020 07:47:33 GMT
LABEL maintainer=Peter Martini <PeterCMartini@GMail.com>, Zak B. Elep <zakame@cpan.org>
# Thu, 16 Apr 2020 07:47:34 GMT
COPY file:15650064fd29deac721f0aa084ddb3d41db77b78e2907775e257bd67e116ade4 in /usr/src/perl/ 
# Thu, 16 Apr 2020 07:47:34 GMT
WORKDIR /usr/src/perl
# Thu, 16 Apr 2020 07:57:55 GMT
RUN true     && curl -SL https://www.cpan.org/src/5.0/perl-5.30.2.tar.xz -o perl-5.30.2.tar.xz     && echo 'a1aa88bd6fbbdc2e82938afbb76c408b0ea847317737b712dc196cc7907a5259 *perl-5.30.2.tar.xz' | sha256sum -c -     && tar --strip-components=1 -xaf perl-5.30.2.tar.xz -C /usr/src/perl     && rm perl-5.30.2.tar.xz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -LO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7044.tar.gz     && echo '9b60767fe40752ef7a9d3f13f19060a63389a5c23acc3e9827e19b75500f81f3 *App-cpanminus-1.7044.tar.gz' | sha256sum -c -     && tar -xzf App-cpanminus-1.7044.tar.gz && cd App-cpanminus-1.7044 && perl bin/cpanm . && cd /root     && true     && rm -fr ./cpanm /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7044* /tmp/*
# Thu, 16 Apr 2020 07:57:58 GMT
WORKDIR /
# Thu, 16 Apr 2020 07:58:00 GMT
CMD ["perl5.30.2" "-de0"]
```

-	Layers:
	-	`sha256:65d54b492d599e7c785a582a0f70195e1f09f0886e54cb7788f1021f383eb4ed`  
		Last Modified: Thu, 16 Apr 2020 02:51:10 GMT  
		Size: 43.2 MB (43159230 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7be35cdee43e0bbb89c0867d201ff274ba25b6ea9bfe7f8f0c1d1d6de36ab08a`  
		Last Modified: Thu, 16 Apr 2020 03:30:52 GMT  
		Size: 9.7 MB (9748442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b803ac2c0e69edab9b8db20bee0f9dfc0191a7975c94d4d2ea0088d5a1759be8`  
		Last Modified: Thu, 16 Apr 2020 03:30:51 GMT  
		Size: 4.1 MB (4094379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f56b7aa1f85cab0d60a62bc0cefa5ec56563f6681054c670ba97d559b4e7ba34`  
		Last Modified: Thu, 16 Apr 2020 03:31:12 GMT  
		Size: 48.0 MB (48027596 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4ea2e3cd35d1d26927d79d0dcd2866f7425d626b5dbc2237a51e25b533d3ae0`  
		Last Modified: Thu, 16 Apr 2020 03:32:10 GMT  
		Size: 202.3 MB (202282533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:235eb484701c05658cbe6bb373508f767c419b6579250c7e7a1b4d8826ecd3b0`  
		Last Modified: Thu, 16 Apr 2020 11:55:55 GMT  
		Size: 441.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e8bbe9d88b889163bd9b9ff7b97236b13d87ab30aa134f53ef579ff138cc6d6`  
		Last Modified: Thu, 16 Apr 2020 11:56:03 GMT  
		Size: 13.7 MB (13651045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `perl:5-stretch` - linux; 386

```console
$ docker pull perl@sha256:4eee805ece46c68d28e95ae48f29774899af2a91119631df507a00a5009c1b5e
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **346.4 MB (346354171 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8b58a9b0fdc0723beb1d2b37adcc1f03fb4a2b27e98b20f8c4e9f04d93d8307`
-	Default Command: `["perl5.30.2","-de0"]`

```dockerfile
# Thu, 16 Apr 2020 01:43:06 GMT
ADD file:298a4dfec0058f9502705ebab6ca3787b1bcb5845d21ecfcd1771505b061b061 in / 
# Thu, 16 Apr 2020 01:43:06 GMT
CMD ["bash"]
# Thu, 16 Apr 2020 02:33:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Thu, 16 Apr 2020 02:33:08 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 16 Apr 2020 02:33:36 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 16 Apr 2020 02:35:01 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 16 Apr 2020 06:55:58 GMT
LABEL maintainer=Peter Martini <PeterCMartini@GMail.com>, Zak B. Elep <zakame@cpan.org>
# Thu, 16 Apr 2020 06:55:58 GMT
COPY file:15650064fd29deac721f0aa084ddb3d41db77b78e2907775e257bd67e116ade4 in /usr/src/perl/ 
# Thu, 16 Apr 2020 06:55:59 GMT
WORKDIR /usr/src/perl
# Thu, 16 Apr 2020 07:10:29 GMT
RUN true     && curl -SL https://www.cpan.org/src/5.0/perl-5.30.2.tar.xz -o perl-5.30.2.tar.xz     && echo 'a1aa88bd6fbbdc2e82938afbb76c408b0ea847317737b712dc196cc7907a5259 *perl-5.30.2.tar.xz' | sha256sum -c -     && tar --strip-components=1 -xaf perl-5.30.2.tar.xz -C /usr/src/perl     && rm perl-5.30.2.tar.xz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -LO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7044.tar.gz     && echo '9b60767fe40752ef7a9d3f13f19060a63389a5c23acc3e9827e19b75500f81f3 *App-cpanminus-1.7044.tar.gz' | sha256sum -c -     && tar -xzf App-cpanminus-1.7044.tar.gz && cd App-cpanminus-1.7044 && perl bin/cpanm . && cd /root     && true     && rm -fr ./cpanm /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7044* /tmp/*
# Thu, 16 Apr 2020 07:10:29 GMT
WORKDIR /
# Thu, 16 Apr 2020 07:10:30 GMT
CMD ["perl5.30.2" "-de0"]
```

-	Layers:
	-	`sha256:aedad1667b3098c616b8251fdfca8170596731152b6043a01601df826b79b4e0`  
		Last Modified: Thu, 16 Apr 2020 01:49:17 GMT  
		Size: 46.1 MB (46094897 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5a13ff1ee1a9968ed086324092c33ec123f94ecb99ccede500342483418d840`  
		Last Modified: Thu, 16 Apr 2020 02:40:58 GMT  
		Size: 10.8 MB (10818136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6cdc434eb33063a8439a59c1a179e4fa3c9d968ee9a3ad4e2ff12714e1b77b1`  
		Last Modified: Thu, 16 Apr 2020 02:40:57 GMT  
		Size: 4.6 MB (4561464 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f2fcb87ea1dc9422e771e3534fe181a7836d49701ee9061b31b09a1a00c9f44`  
		Last Modified: Thu, 16 Apr 2020 02:41:16 GMT  
		Size: 51.6 MB (51613902 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a2599ad162f6a3d5888ba12dadbc993699533ebe3fa5834083bbcefd7267612`  
		Last Modified: Thu, 16 Apr 2020 02:42:05 GMT  
		Size: 220.0 MB (219957415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4bdd182e363b205b7fa00aee06e745414b2fd0db914c605e44a4a413d841f85`  
		Last Modified: Thu, 16 Apr 2020 11:36:30 GMT  
		Size: 412.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:910962309454f76f66dd00d9f5489d10daf741b9ef3e9023c06895e5ef796eb3`  
		Last Modified: Thu, 16 Apr 2020 11:36:36 GMT  
		Size: 13.3 MB (13307945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `perl:5-stretch` - linux; ppc64le

```console
$ docker pull perl@sha256:801743bedf3bf11f8f253c76cc12826511fe4ce15d8dd5c10397d6772b0d8c07
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **334.2 MB (334231394 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f7d9d0ccc67cea102efc6c9708eaa9b5f3615d217ef1e5379a064b8454cdfda`
-	Default Command: `["perl5.30.2","-de0"]`

```dockerfile
# Tue, 31 Mar 2020 01:36:08 GMT
ADD file:88dd9829c8f6a5ba7164ab347e4b14c986122f77fa3881b5b5f9bd34f8e0a794 in / 
# Tue, 31 Mar 2020 01:36:13 GMT
CMD ["bash"]
# Tue, 31 Mar 2020 03:46:28 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 03:46:53 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 31 Mar 2020 03:48:27 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 03:56:58 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 07:47:09 GMT
LABEL maintainer=Peter Martini <PeterCMartini@GMail.com>, Zak B. Elep <zakame@cpan.org>
# Tue, 31 Mar 2020 07:47:10 GMT
COPY file:15650064fd29deac721f0aa084ddb3d41db77b78e2907775e257bd67e116ade4 in /usr/src/perl/ 
# Tue, 31 Mar 2020 07:47:12 GMT
WORKDIR /usr/src/perl
# Tue, 31 Mar 2020 07:53:42 GMT
RUN true     && curl -SL https://www.cpan.org/src/5.0/perl-5.30.2.tar.xz -o perl-5.30.2.tar.xz     && echo 'a1aa88bd6fbbdc2e82938afbb76c408b0ea847317737b712dc196cc7907a5259 *perl-5.30.2.tar.xz' | sha256sum -c -     && tar --strip-components=1 -xaf perl-5.30.2.tar.xz -C /usr/src/perl     && rm perl-5.30.2.tar.xz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -LO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7044.tar.gz     && echo '9b60767fe40752ef7a9d3f13f19060a63389a5c23acc3e9827e19b75500f81f3 *App-cpanminus-1.7044.tar.gz' | sha256sum -c -     && tar -xzf App-cpanminus-1.7044.tar.gz && cd App-cpanminus-1.7044 && perl bin/cpanm . && cd /root     && true     && rm -fr ./cpanm /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7044* /tmp/*
# Tue, 31 Mar 2020 07:53:46 GMT
WORKDIR /
# Tue, 31 Mar 2020 07:53:49 GMT
CMD ["perl5.30.2" "-de0"]
```

-	Layers:
	-	`sha256:a7f28865f7aedbe572d508cc57c37cad5f147864f7c67c67a38458e070687420`  
		Last Modified: Tue, 31 Mar 2020 01:52:56 GMT  
		Size: 45.6 MB (45647140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b575341a09a9b1fed08dca01f194be6db272e3f2d161ea2edf0db64d8e706213`  
		Last Modified: Tue, 31 Mar 2020 04:07:20 GMT  
		Size: 10.0 MB (10002319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28423de192fc0e4ecfc04a57e531587e8876d098a124122748a8f55a842f3213`  
		Last Modified: Tue, 31 Mar 2020 04:07:19 GMT  
		Size: 4.3 MB (4296673 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cccdb86da25ba4684a518e5fe94d237bd1d84392cdee077d26f6aed0520237e`  
		Last Modified: Tue, 31 Mar 2020 04:08:09 GMT  
		Size: 50.1 MB (50085204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfe17ae7a3b975904e86d12aae11a52d1775c818c61d0513cbfaa36fa3ad4352`  
		Last Modified: Tue, 31 Mar 2020 04:09:18 GMT  
		Size: 210.5 MB (210525053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66a28a55ab968e10a98494850d9a9d360a3bb0902deb99aa3628f425161bfb72`  
		Last Modified: Tue, 31 Mar 2020 10:48:08 GMT  
		Size: 443.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0520e175f24ef51139e446df839cf001e492c3796c4c15ad9369931f44042690`  
		Last Modified: Tue, 31 Mar 2020 10:48:18 GMT  
		Size: 13.7 MB (13674562 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `perl:5-stretch` - linux; s390x

```console
$ docker pull perl@sha256:1ae1173246f21c801d60e83c1dc8b71716dcb4c1a2d6cf17172574cfca06b623
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **331.7 MB (331652513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c4ec3d3dafc9c1b68156fb112e1a6fc9d185f4c43f5353e6f0696e75f7c836a`
-	Default Command: `["perl5.30.2","-de0"]`

```dockerfile
# Thu, 16 Apr 2020 00:43:47 GMT
ADD file:bf54e49d85edbe8d61bd9e868d71faf0f26b4474f23eda7b692abfaf7aea50a4 in / 
# Thu, 16 Apr 2020 00:43:49 GMT
CMD ["bash"]
# Thu, 16 Apr 2020 02:02:42 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Thu, 16 Apr 2020 02:02:47 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 16 Apr 2020 02:03:12 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 16 Apr 2020 02:04:47 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 16 Apr 2020 03:35:43 GMT
LABEL maintainer=Peter Martini <PeterCMartini@GMail.com>, Zak B. Elep <zakame@cpan.org>
# Thu, 16 Apr 2020 03:35:43 GMT
COPY file:15650064fd29deac721f0aa084ddb3d41db77b78e2907775e257bd67e116ade4 in /usr/src/perl/ 
# Thu, 16 Apr 2020 03:35:43 GMT
WORKDIR /usr/src/perl
# Thu, 16 Apr 2020 03:40:01 GMT
RUN true     && curl -SL https://www.cpan.org/src/5.0/perl-5.30.2.tar.xz -o perl-5.30.2.tar.xz     && echo 'a1aa88bd6fbbdc2e82938afbb76c408b0ea847317737b712dc196cc7907a5259 *perl-5.30.2.tar.xz' | sha256sum -c -     && tar --strip-components=1 -xaf perl-5.30.2.tar.xz -C /usr/src/perl     && rm perl-5.30.2.tar.xz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -LO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7044.tar.gz     && echo '9b60767fe40752ef7a9d3f13f19060a63389a5c23acc3e9827e19b75500f81f3 *App-cpanminus-1.7044.tar.gz' | sha256sum -c -     && tar -xzf App-cpanminus-1.7044.tar.gz && cd App-cpanminus-1.7044 && perl bin/cpanm . && cd /root     && true     && rm -fr ./cpanm /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7044* /tmp/*
# Thu, 16 Apr 2020 03:40:02 GMT
WORKDIR /
# Thu, 16 Apr 2020 03:40:02 GMT
CMD ["perl5.30.2" "-de0"]
```

-	Layers:
	-	`sha256:b4e6598a8ad88c3d661d89d6fda41ee33a54f3c6f16c4988cceaa6fd0afd04bb`  
		Last Modified: Thu, 16 Apr 2020 00:48:18 GMT  
		Size: 45.2 MB (45232626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9cb98b0a4ec56e95b4ba3f3261ba975cd69e2a0240149eb53e4bbff9739e272`  
		Last Modified: Thu, 16 Apr 2020 02:08:04 GMT  
		Size: 10.3 MB (10325610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06c82c0f221bc14891b71387b7587fd4f2a615d339ecf0afadce350f82b3e098`  
		Last Modified: Thu, 16 Apr 2020 02:08:03 GMT  
		Size: 4.4 MB (4372651 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3d17818ca9e172b803a01ef9860f9b1c67b359a6d75c51e65a63c0448b3816d`  
		Last Modified: Thu, 16 Apr 2020 02:08:18 GMT  
		Size: 50.5 MB (50513161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2557aea605e0656c02d9c1b5edabffb8913484720675da14238c640088e5999`  
		Last Modified: Thu, 16 Apr 2020 02:08:56 GMT  
		Size: 206.9 MB (206917991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21003175356a3d83c170d92cd0049cd7768b36cc178dea3254d08fe227e8b8f8`  
		Last Modified: Thu, 16 Apr 2020 05:23:15 GMT  
		Size: 439.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27c3c2f5f9c8d3d650b8106e560c60a1aabb726ffe2fe5ce2e2d489940724bbb`  
		Last Modified: Thu, 16 Apr 2020 05:23:18 GMT  
		Size: 14.3 MB (14290035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
