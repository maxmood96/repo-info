## `perl:threaded-buster`

```console
$ docker pull perl@sha256:54eb2cc807491a63fcfba263996ec38df0578be605d2e60f5509ba8e29ffc9ba
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

### `perl:threaded-buster` - linux; amd64

```console
$ docker pull perl@sha256:872c2d96a1c50d878d9183cfe41ee5f0b7f920498f6f2dd134b11b65a1574d9d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **326.9 MB (326907164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73f34f6dfa7dc1ae81300aaf959e7890b479164c9c4e12b20ec63b1f32b56cd7`
-	Default Command: `["perl5.34.0","-de0"]`

```dockerfile
# Tue, 01 Mar 2022 02:13:41 GMT
ADD file:e8b516b464e535b435a6ed8609bac98acc90ee30e2a0667f68932f0d924f6e49 in / 
# Tue, 01 Mar 2022 02:13:42 GMT
CMD ["bash"]
# Tue, 01 Mar 2022 06:27:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 06:28:02 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 01 Mar 2022 06:28:26 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 06:29:28 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 15:05:19 GMT
LABEL maintainer=Peter Martini <PeterCMartini@GMail.com>, Zak B. Elep <zakame@cpan.org>
# Tue, 01 Mar 2022 15:05:20 GMT
COPY file:3744c5cc39cdbdcae10db09a1f0f399005a79f93c237b387a72ff5710cdd458c in /usr/src/perl/ 
# Tue, 01 Mar 2022 15:05:20 GMT
WORKDIR /usr/src/perl
# Tue, 01 Mar 2022 15:56:41 GMT
RUN true     && curl -SL https://www.cpan.org/src/5.0/perl-5.34.0.tar.xz -o perl-5.34.0.tar.xz     && echo '82c2e5e5c71b0e10487a80d79140469ab1f8056349ca8545140a224dbbed7ded *perl-5.34.0.tar.xz' | sha256sum -c -     && tar --strip-components=1 -xaf perl-5.34.0.tar.xz -C /usr/src/perl     && rm perl-5.34.0.tar.xz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -LO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7044.tar.gz     && echo '9b60767fe40752ef7a9d3f13f19060a63389a5c23acc3e9827e19b75500f81f3 *App-cpanminus-1.7044.tar.gz' | sha256sum -c -     && tar -xzf App-cpanminus-1.7044.tar.gz && cd App-cpanminus-1.7044 && perl bin/cpanm . && cd /root     && true     && rm -fr ./cpanm /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7044* /tmp/*
# Tue, 01 Mar 2022 15:56:41 GMT
WORKDIR /
# Tue, 01 Mar 2022 15:56:41 GMT
CMD ["perl5.34.0" "-de0"]
```

-	Layers:
	-	`sha256:1c9a8b42b5780ac49c71f392c9512c0167ecc23de9b30b1b5f38747b73097d1a`  
		Last Modified: Tue, 01 Mar 2022 02:19:43 GMT  
		Size: 50.4 MB (50437046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:163066942b43a00ba7f4674c4c1ca90eccc8d99366a3dc47cb64e06ad79c36e5`  
		Last Modified: Tue, 01 Mar 2022 06:37:36 GMT  
		Size: 7.8 MB (7834052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf70e03a8272d87e65c7b1592f97f6e739cf1f5d13cc536670f41c28b086b4cb`  
		Last Modified: Tue, 01 Mar 2022 06:37:37 GMT  
		Size: 10.0 MB (9997298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86c5ff33549498a7154441116b5843e184c1f4441df2eab519ad2c498cb8a716`  
		Last Modified: Tue, 01 Mar 2022 06:37:56 GMT  
		Size: 51.8 MB (51843267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c03e72651e6b47f74f08da02f8570740d842273289cac86572b8eca1712e9ee`  
		Last Modified: Tue, 01 Mar 2022 06:38:38 GMT  
		Size: 192.4 MB (192423535 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c74941317e0c613c95bf4aa373e3ee85119e6d29072ce1db14608445ae265007`  
		Last Modified: Tue, 01 Mar 2022 19:05:58 GMT  
		Size: 200.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76c3fa9c8bc6f4253d5358b7102fb5a345be07b72690882ebc0db6948d676ec2`  
		Last Modified: Tue, 01 Mar 2022 19:07:43 GMT  
		Size: 14.4 MB (14371766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `perl:threaded-buster` - linux; arm variant v5

```console
$ docker pull perl@sha256:32a45b4c46d1e1585426f0d765110ce13835e3318978ab4c6e9d35fdaf3c80b2
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **299.8 MB (299827592 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb16f8a8a1f1ef7651b455d14eb7015441d3c6728678a8e10c2a9bb2ef4c8b47`
-	Default Command: `["perl5.34.0","-de0"]`

```dockerfile
# Tue, 01 Mar 2022 02:03:21 GMT
ADD file:67f3f7e89901c5f16436fda6f05f959b01ce2654ab6b4cd9d53b597d1a30a97d in / 
# Tue, 01 Mar 2022 02:03:23 GMT
CMD ["bash"]
# Tue, 01 Mar 2022 03:05:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 03:06:12 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 01 Mar 2022 03:07:09 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 03:09:39 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 04:25:01 GMT
LABEL maintainer=Peter Martini <PeterCMartini@GMail.com>, Zak B. Elep <zakame@cpan.org>
# Tue, 01 Mar 2022 04:25:01 GMT
COPY file:3744c5cc39cdbdcae10db09a1f0f399005a79f93c237b387a72ff5710cdd458c in /usr/src/perl/ 
# Tue, 01 Mar 2022 04:25:02 GMT
WORKDIR /usr/src/perl
# Tue, 01 Mar 2022 05:25:28 GMT
RUN true     && curl -SL https://www.cpan.org/src/5.0/perl-5.34.0.tar.xz -o perl-5.34.0.tar.xz     && echo '82c2e5e5c71b0e10487a80d79140469ab1f8056349ca8545140a224dbbed7ded *perl-5.34.0.tar.xz' | sha256sum -c -     && tar --strip-components=1 -xaf perl-5.34.0.tar.xz -C /usr/src/perl     && rm perl-5.34.0.tar.xz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -LO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7044.tar.gz     && echo '9b60767fe40752ef7a9d3f13f19060a63389a5c23acc3e9827e19b75500f81f3 *App-cpanminus-1.7044.tar.gz' | sha256sum -c -     && tar -xzf App-cpanminus-1.7044.tar.gz && cd App-cpanminus-1.7044 && perl bin/cpanm . && cd /root     && true     && rm -fr ./cpanm /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7044* /tmp/*
# Tue, 01 Mar 2022 05:25:29 GMT
WORKDIR /
# Tue, 01 Mar 2022 05:25:29 GMT
CMD ["perl5.34.0" "-de0"]
```

-	Layers:
	-	`sha256:cce169e928830f476b72f6fb2bd7ce1b80e59d3bd3d24202f5fbd7a9535fd48c`  
		Last Modified: Tue, 01 Mar 2022 02:19:20 GMT  
		Size: 48.2 MB (48154229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4d57d0b9b76245f122bedc54cfb401efe4ae73525e3e5096c640b38010ce60e`  
		Last Modified: Tue, 01 Mar 2022 03:27:49 GMT  
		Size: 7.4 MB (7377224 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a657cd7a4baa440bfbce8ec469123713e5b5d23c6629f9fa5b6dd0e75ce50d3a`  
		Last Modified: Tue, 01 Mar 2022 03:27:49 GMT  
		Size: 9.7 MB (9687611 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9dc7ca897fec0f5641e72195c9642b35a822abea245e98700f0e566cb0196407`  
		Last Modified: Tue, 01 Mar 2022 03:28:37 GMT  
		Size: 49.6 MB (49578751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb1d56c43a7774500c3528199e955ee9dee66be059673845da5bb32049f8a855`  
		Last Modified: Tue, 01 Mar 2022 03:30:32 GMT  
		Size: 171.4 MB (171363080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8331517aee9fe64ed742d64955d3d256f51849ff56f49d90b9365b8df19b83f2`  
		Last Modified: Tue, 01 Mar 2022 09:09:29 GMT  
		Size: 204.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:139d3e8bd3e7d968afb48c2f28a847b543fe9bc373b66764e452b5cd53ac0fad`  
		Last Modified: Tue, 01 Mar 2022 09:12:20 GMT  
		Size: 13.7 MB (13666493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `perl:threaded-buster` - linux; arm variant v7

```console
$ docker pull perl@sha256:1c6dcd0c7c753c4d71a791e6a3a2122f043117333cd1467e157f0e006e352b90
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.8 MB (291847513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e88caba0a21ed6f098c1dcfd6c8c3f1784e7dd46e82c9fb539857902f33ff6ed`
-	Default Command: `["perl5.34.0","-de0"]`

```dockerfile
# Tue, 01 Mar 2022 02:03:29 GMT
ADD file:49ab7c627696d55c8512392867bee4593a377d34c5c4f75aac1eb176a56b672c in / 
# Tue, 01 Mar 2022 02:03:30 GMT
CMD ["bash"]
# Tue, 01 Mar 2022 09:29:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 09:30:08 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 01 Mar 2022 09:30:54 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 09:33:14 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 16:36:10 GMT
LABEL maintainer=Peter Martini <PeterCMartini@GMail.com>, Zak B. Elep <zakame@cpan.org>
# Tue, 01 Mar 2022 16:36:10 GMT
COPY file:3744c5cc39cdbdcae10db09a1f0f399005a79f93c237b387a72ff5710cdd458c in /usr/src/perl/ 
# Tue, 01 Mar 2022 16:36:11 GMT
WORKDIR /usr/src/perl
# Tue, 01 Mar 2022 17:32:26 GMT
RUN true     && curl -SL https://www.cpan.org/src/5.0/perl-5.34.0.tar.xz -o perl-5.34.0.tar.xz     && echo '82c2e5e5c71b0e10487a80d79140469ab1f8056349ca8545140a224dbbed7ded *perl-5.34.0.tar.xz' | sha256sum -c -     && tar --strip-components=1 -xaf perl-5.34.0.tar.xz -C /usr/src/perl     && rm perl-5.34.0.tar.xz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -LO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7044.tar.gz     && echo '9b60767fe40752ef7a9d3f13f19060a63389a5c23acc3e9827e19b75500f81f3 *App-cpanminus-1.7044.tar.gz' | sha256sum -c -     && tar -xzf App-cpanminus-1.7044.tar.gz && cd App-cpanminus-1.7044 && perl bin/cpanm . && cd /root     && true     && rm -fr ./cpanm /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7044* /tmp/*
# Tue, 01 Mar 2022 17:32:27 GMT
WORKDIR /
# Tue, 01 Mar 2022 17:32:27 GMT
CMD ["perl5.34.0" "-de0"]
```

-	Layers:
	-	`sha256:5e77565ce5247d53df5dcb65e54c6d6e73e60996d11fbc1ce5ee34bf80dfa1f2`  
		Last Modified: Tue, 01 Mar 2022 02:19:53 GMT  
		Size: 45.9 MB (45918104 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b40356d157bf4856aec771f3f51360d39ebb8715ba13f6f19d8153416eced08`  
		Last Modified: Tue, 01 Mar 2022 09:53:58 GMT  
		Size: 7.1 MB (7125246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e02534a5c6a025b55da20b42dc333e67684e4ef06a3b2d46d0b0f00543548e29`  
		Last Modified: Tue, 01 Mar 2022 09:53:59 GMT  
		Size: 9.3 MB (9343821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee494db552973674b15404f408d37e26afac1a9202a409e16f59441f0ccaa6c2`  
		Last Modified: Tue, 01 Mar 2022 09:54:42 GMT  
		Size: 47.4 MB (47357696 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0af9e9486892bd2f95c6d1d261190476cefd457e617950ba150ca2d5a36e43be`  
		Last Modified: Tue, 01 Mar 2022 09:56:27 GMT  
		Size: 168.6 MB (168628818 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5964291c5164e84379f18c04c12e0e8dbbfb1144ef09aaf21adaea99b5158c5`  
		Last Modified: Tue, 01 Mar 2022 21:02:19 GMT  
		Size: 201.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eff6f0b71bf07c455aa886ce56752c527bb7c72239daa52d190d29770e5c434f`  
		Last Modified: Tue, 01 Mar 2022 21:05:08 GMT  
		Size: 13.5 MB (13473627 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `perl:threaded-buster` - linux; arm64 variant v8

```console
$ docker pull perl@sha256:036d54dd338149206ba08dc23cfeec3ba641e5051bfe2ed0598098e53d3e6481
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **317.2 MB (317201342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fff28bb75b4e059ffb9c968e2138422ca7a0a7538f931e44760b22ebba901445`
-	Default Command: `["perl5.34.0","-de0"]`

```dockerfile
# Thu, 17 Mar 2022 03:22:08 GMT
ADD file:37cabd1fec04269c22fc158f62ce5bc655934f2e58fb1ff3a1e366a33ba9bc18 in / 
# Thu, 17 Mar 2022 03:22:09 GMT
CMD ["bash"]
# Thu, 17 Mar 2022 22:12:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 17 Mar 2022 22:12:25 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 17 Mar 2022 22:12:41 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 17 Mar 2022 22:13:28 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Mar 2022 02:09:15 GMT
LABEL maintainer=Peter Martini <PeterCMartini@GMail.com>, Zak B. Elep <zakame@cpan.org>
# Fri, 18 Mar 2022 02:09:16 GMT
COPY file:3744c5cc39cdbdcae10db09a1f0f399005a79f93c237b387a72ff5710cdd458c in /usr/src/perl/ 
# Fri, 18 Mar 2022 02:09:17 GMT
WORKDIR /usr/src/perl
# Fri, 18 Mar 2022 02:29:56 GMT
RUN true     && curl -SL https://www.cpan.org/src/5.0/perl-5.34.0.tar.xz -o perl-5.34.0.tar.xz     && echo '82c2e5e5c71b0e10487a80d79140469ab1f8056349ca8545140a224dbbed7ded *perl-5.34.0.tar.xz' | sha256sum -c -     && tar --strip-components=1 -xaf perl-5.34.0.tar.xz -C /usr/src/perl     && rm perl-5.34.0.tar.xz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -LO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7044.tar.gz     && echo '9b60767fe40752ef7a9d3f13f19060a63389a5c23acc3e9827e19b75500f81f3 *App-cpanminus-1.7044.tar.gz' | sha256sum -c -     && tar -xzf App-cpanminus-1.7044.tar.gz && cd App-cpanminus-1.7044 && perl bin/cpanm . && cd /root     && true     && rm -fr ./cpanm /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7044* /tmp/*
# Fri, 18 Mar 2022 02:29:57 GMT
WORKDIR /
# Fri, 18 Mar 2022 02:29:58 GMT
CMD ["perl5.34.0" "-de0"]
```

-	Layers:
	-	`sha256:3996f04b7c6c17d8b25c04c7287353b896b4a0b10ab440f47d00573a7d5c3e17`  
		Last Modified: Thu, 17 Mar 2022 03:28:59 GMT  
		Size: 49.2 MB (49222993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80907b498681187ef4aa817ec6f39ba351e376afbb4fcf4415841ab9015cfc59`  
		Last Modified: Thu, 17 Mar 2022 22:22:15 GMT  
		Size: 7.7 MB (7695349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8327dc7899c1a628cf11f95bb594fca3c86e45d1f4f0eb73d2ba9058eba5927`  
		Last Modified: Thu, 17 Mar 2022 22:22:15 GMT  
		Size: 9.8 MB (9767203 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1431347b40fe69ed685917a6ef1b8c28d5de6147f3c62ea11a1951ead75ccdd`  
		Last Modified: Thu, 17 Mar 2022 22:22:34 GMT  
		Size: 52.2 MB (52174886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6df5b0cd9b56b640f0f401d463c7ef2450f177165445568d3a4644f629b1708`  
		Last Modified: Thu, 17 Mar 2022 22:23:08 GMT  
		Size: 184.0 MB (184035372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48d9780a15305ee35cea065cfaa9e80088d16b065efecaeff5c66c9c3685a093`  
		Last Modified: Fri, 18 Mar 2022 03:48:48 GMT  
		Size: 179.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80bbd3cb6a28913c0fc4016596ae2f75f801534e3b1c35eb87db8ef30ee6dede`  
		Last Modified: Fri, 18 Mar 2022 03:50:38 GMT  
		Size: 14.3 MB (14305360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `perl:threaded-buster` - linux; 386

```console
$ docker pull perl@sha256:77892549012bf0a62f8b509bf1222899b4dfd9d4b9a258239861c02303d630f0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **335.9 MB (335878197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:926372fc7c4c1f4c2822e471e6e9efd128f0e949259dc9ac7e15130e85d65935`
-	Default Command: `["perl5.34.0","-de0"]`

```dockerfile
# Tue, 01 Mar 2022 02:07:47 GMT
ADD file:bdcedc0826a512fa5720a5481555b67977a75cc3a2c76cf5525f4067f6e30f78 in / 
# Tue, 01 Mar 2022 02:07:47 GMT
CMD ["bash"]
# Tue, 01 Mar 2022 05:42:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 05:42:42 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 01 Mar 2022 05:43:05 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 05:44:14 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 10:55:35 GMT
LABEL maintainer=Peter Martini <PeterCMartini@GMail.com>, Zak B. Elep <zakame@cpan.org>
# Tue, 01 Mar 2022 10:55:36 GMT
COPY file:3744c5cc39cdbdcae10db09a1f0f399005a79f93c237b387a72ff5710cdd458c in /usr/src/perl/ 
# Tue, 01 Mar 2022 10:55:36 GMT
WORKDIR /usr/src/perl
# Tue, 01 Mar 2022 12:03:59 GMT
RUN true     && curl -SL https://www.cpan.org/src/5.0/perl-5.34.0.tar.xz -o perl-5.34.0.tar.xz     && echo '82c2e5e5c71b0e10487a80d79140469ab1f8056349ca8545140a224dbbed7ded *perl-5.34.0.tar.xz' | sha256sum -c -     && tar --strip-components=1 -xaf perl-5.34.0.tar.xz -C /usr/src/perl     && rm perl-5.34.0.tar.xz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -LO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7044.tar.gz     && echo '9b60767fe40752ef7a9d3f13f19060a63389a5c23acc3e9827e19b75500f81f3 *App-cpanminus-1.7044.tar.gz' | sha256sum -c -     && tar -xzf App-cpanminus-1.7044.tar.gz && cd App-cpanminus-1.7044 && perl bin/cpanm . && cd /root     && true     && rm -fr ./cpanm /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7044* /tmp/*
# Tue, 01 Mar 2022 12:04:00 GMT
WORKDIR /
# Tue, 01 Mar 2022 12:04:00 GMT
CMD ["perl5.34.0" "-de0"]
```

-	Layers:
	-	`sha256:476db560471d1237921e304e3ff8f4080b6678e161577b3284ac8cc10eeacb64`  
		Last Modified: Tue, 01 Mar 2022 02:16:20 GMT  
		Size: 51.2 MB (51207695 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5c26a779ac27dbfd1d496436ab636b45a1a0157570daf0fe074b2b128251084`  
		Last Modified: Tue, 01 Mar 2022 05:53:41 GMT  
		Size: 8.0 MB (8000492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5f554cfd6e25d31263311f533991fee169f308525eac5bfd2a37a744aca5580`  
		Last Modified: Tue, 01 Mar 2022 05:53:41 GMT  
		Size: 10.3 MB (10340017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97a9779cb01b98555fd465f4f1e10c4a014e406cf5e9f662ca5522c871ae253d`  
		Last Modified: Tue, 01 Mar 2022 05:54:05 GMT  
		Size: 53.4 MB (53439729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:810b7691d877f19f715660a9aa2b87c8434c2f52ccbfc77c4da2262237fc81cb`  
		Last Modified: Tue, 01 Mar 2022 05:54:58 GMT  
		Size: 199.0 MB (198978965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:843a44d35e9e1698c512db7f4f1812d92be7df2c5f075e1d5b7c141a4e6232ec`  
		Last Modified: Tue, 01 Mar 2022 15:00:05 GMT  
		Size: 202.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:201093609ffebdc4781999c80dde6367b70dc74b24e6c0560b3eed4ddb15d67f`  
		Last Modified: Tue, 01 Mar 2022 15:02:24 GMT  
		Size: 13.9 MB (13911097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `perl:threaded-buster` - linux; mips64le

```console
$ docker pull perl@sha256:6e8a0e194389b052490229aa06bd23dfd023dcc056639ae12abc8f9145d0fa94
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **310.6 MB (310604586 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c0ff444f55afb0e48e8e640d01e7d5a70150e7bddec37dec36fc28ab2130b4a`
-	Default Command: `["perl5.34.0","-de0"]`

```dockerfile
# Thu, 17 Mar 2022 08:53:34 GMT
ADD file:a0b3ac9e4bfb39c253a8a7a55fb55d0b908af833cdcc9931837698ec5f55b989 in / 
# Thu, 17 Mar 2022 08:53:39 GMT
CMD ["bash"]
# Thu, 17 Mar 2022 19:29:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 17 Mar 2022 19:29:59 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 17 Mar 2022 19:31:36 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 17 Mar 2022 19:37:57 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 17 Mar 2022 22:16:32 GMT
LABEL maintainer=Peter Martini <PeterCMartini@GMail.com>, Zak B. Elep <zakame@cpan.org>
# Thu, 17 Mar 2022 22:16:38 GMT
COPY file:3744c5cc39cdbdcae10db09a1f0f399005a79f93c237b387a72ff5710cdd458c in /usr/src/perl/ 
# Thu, 17 Mar 2022 22:16:44 GMT
WORKDIR /usr/src/perl
# Thu, 17 Mar 2022 23:58:40 GMT
RUN true     && curl -SL https://www.cpan.org/src/5.0/perl-5.34.0.tar.xz -o perl-5.34.0.tar.xz     && echo '82c2e5e5c71b0e10487a80d79140469ab1f8056349ca8545140a224dbbed7ded *perl-5.34.0.tar.xz' | sha256sum -c -     && tar --strip-components=1 -xaf perl-5.34.0.tar.xz -C /usr/src/perl     && rm perl-5.34.0.tar.xz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -LO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7044.tar.gz     && echo '9b60767fe40752ef7a9d3f13f19060a63389a5c23acc3e9827e19b75500f81f3 *App-cpanminus-1.7044.tar.gz' | sha256sum -c -     && tar -xzf App-cpanminus-1.7044.tar.gz && cd App-cpanminus-1.7044 && perl bin/cpanm . && cd /root     && true     && rm -fr ./cpanm /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7044* /tmp/*
# Thu, 17 Mar 2022 23:58:47 GMT
WORKDIR /
# Thu, 17 Mar 2022 23:58:53 GMT
CMD ["perl5.34.0" "-de0"]
```

-	Layers:
	-	`sha256:047b7fb675b6ff99fd7dedbd4d0b0a3242855acbf0be0e3a69b39ea19852bf7f`  
		Last Modified: Thu, 17 Mar 2022 10:44:02 GMT  
		Size: 49.1 MB (49079461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55203676937c9ec933fb27d1c8139cf1a83a5d5d392495e941a0824319a07428`  
		Last Modified: Thu, 17 Mar 2022 19:54:04 GMT  
		Size: 7.3 MB (7253901 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5af9a4d78faa84f9b4e38f2bd9489ea3e3fb4b460d64cc87d7a259fab08daa46`  
		Last Modified: Thu, 17 Mar 2022 19:54:04 GMT  
		Size: 9.8 MB (9800271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e21ca836913dcc7e4e29f2dc0605b4d1702ff89e56fe9cef67e16c75dca5e8e`  
		Last Modified: Thu, 17 Mar 2022 19:54:50 GMT  
		Size: 50.9 MB (50859572 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e7329720af3f37ce1c4429d92cb1f2e87eacface8ef8c5f2ba96c2403f4d1e1`  
		Last Modified: Thu, 17 Mar 2022 19:56:54 GMT  
		Size: 180.0 MB (179987188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41c33d3c9863c2e28bf3b019d5a357b41853a5ec8645abf921ec7a67f8cee812`  
		Last Modified: Fri, 18 Mar 2022 06:06:26 GMT  
		Size: 179.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0f8984c9c16bc792195bf5328296968f402f8aa8106cb7f1cee355b3962b866`  
		Last Modified: Fri, 18 Mar 2022 06:08:45 GMT  
		Size: 13.6 MB (13624014 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `perl:threaded-buster` - linux; ppc64le

```console
$ docker pull perl@sha256:d238bb0f5b2a9d9d173d7df941a8f85c5568da755adfbe3dc25d08bafcc57802
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **348.4 MB (348409470 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3154902c63ecee5ea089565dfb32ebc582f662ac9b06731b2ed7a45d7d5eca7`
-	Default Command: `["perl5.34.0","-de0"]`

```dockerfile
# Tue, 01 Mar 2022 02:05:31 GMT
ADD file:b0fccd713cf7d422b1caea3a5d8c8bc230da590e6004fb58a27f2e53589bb87e in / 
# Tue, 01 Mar 2022 02:05:38 GMT
CMD ["bash"]
# Tue, 01 Mar 2022 07:18:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 07:18:57 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 01 Mar 2022 07:21:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 07:28:57 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Mar 2022 01:51:50 GMT
LABEL maintainer=Peter Martini <PeterCMartini@GMail.com>, Zak B. Elep <zakame@cpan.org>
# Wed, 02 Mar 2022 01:51:52 GMT
COPY file:3744c5cc39cdbdcae10db09a1f0f399005a79f93c237b387a72ff5710cdd458c in /usr/src/perl/ 
# Wed, 02 Mar 2022 01:51:54 GMT
WORKDIR /usr/src/perl
# Wed, 02 Mar 2022 02:29:58 GMT
RUN true     && curl -SL https://www.cpan.org/src/5.0/perl-5.34.0.tar.xz -o perl-5.34.0.tar.xz     && echo '82c2e5e5c71b0e10487a80d79140469ab1f8056349ca8545140a224dbbed7ded *perl-5.34.0.tar.xz' | sha256sum -c -     && tar --strip-components=1 -xaf perl-5.34.0.tar.xz -C /usr/src/perl     && rm perl-5.34.0.tar.xz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -LO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7044.tar.gz     && echo '9b60767fe40752ef7a9d3f13f19060a63389a5c23acc3e9827e19b75500f81f3 *App-cpanminus-1.7044.tar.gz' | sha256sum -c -     && tar -xzf App-cpanminus-1.7044.tar.gz && cd App-cpanminus-1.7044 && perl bin/cpanm . && cd /root     && true     && rm -fr ./cpanm /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7044* /tmp/*
# Wed, 02 Mar 2022 02:30:06 GMT
WORKDIR /
# Wed, 02 Mar 2022 02:30:14 GMT
CMD ["perl5.34.0" "-de0"]
```

-	Layers:
	-	`sha256:3af27652881c17f6980cd7f32718c45cc6047a3391b74b55f499341c8efb5ec5`  
		Last Modified: Tue, 01 Mar 2022 02:15:48 GMT  
		Size: 54.2 MB (54183617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2afaad5be738f67c67e6b3d540b5a3dcad788dcd8f5180f494ca1465ac0c03f`  
		Last Modified: Tue, 01 Mar 2022 07:43:43 GMT  
		Size: 8.3 MB (8273085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdd41299687186ba7a9a5ca4d29f672f8a2ef6047cbb81a80e5c8b78fd082580`  
		Last Modified: Tue, 01 Mar 2022 07:43:43 GMT  
		Size: 10.7 MB (10727782 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba7ff69cbc600643af29c318ec272c395ba5acdb3ec94fbf3ee6222336909324`  
		Last Modified: Tue, 01 Mar 2022 07:44:06 GMT  
		Size: 57.5 MB (57458037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:deeb3fba2a0d7a6b9c6fd1d05d43a2dbade16c20f6df8d31244446ecfe2663ee`  
		Last Modified: Tue, 01 Mar 2022 07:44:50 GMT  
		Size: 203.3 MB (203329202 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f08bcd87553153c485f286c2ca8087f8547edde8a0f55c383bbfa284658af91`  
		Last Modified: Wed, 02 Mar 2022 05:06:06 GMT  
		Size: 202.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6fb5687bd226525d24a99777ac251893e45bb358cf3eb6c9df29048036f71f8`  
		Last Modified: Wed, 02 Mar 2022 05:08:53 GMT  
		Size: 14.4 MB (14437545 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `perl:threaded-buster` - linux; s390x

```console
$ docker pull perl@sha256:e3cd45d9e148f4541c1a2eecf41043ed44a77b5b1389c8acf4af75f911004d4a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **309.3 MB (309289537 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36c75c2bf617bfe203980cc6abeb151f1505a24fd6de7879809016cb2684856c`
-	Default Command: `["perl5.34.0","-de0"]`

```dockerfile
# Tue, 01 Mar 2022 02:02:09 GMT
ADD file:d42860e0eaa59b8efe33f2b9046be595efe776263ed470e4020317e451efbc47 in / 
# Tue, 01 Mar 2022 02:02:11 GMT
CMD ["bash"]
# Tue, 01 Mar 2022 03:52:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 03:52:57 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 01 Mar 2022 03:53:17 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 03:54:16 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 07:27:01 GMT
LABEL maintainer=Peter Martini <PeterCMartini@GMail.com>, Zak B. Elep <zakame@cpan.org>
# Tue, 01 Mar 2022 07:27:01 GMT
COPY file:3744c5cc39cdbdcae10db09a1f0f399005a79f93c237b387a72ff5710cdd458c in /usr/src/perl/ 
# Tue, 01 Mar 2022 07:27:01 GMT
WORKDIR /usr/src/perl
# Tue, 01 Mar 2022 07:51:01 GMT
RUN true     && curl -SL https://www.cpan.org/src/5.0/perl-5.34.0.tar.xz -o perl-5.34.0.tar.xz     && echo '82c2e5e5c71b0e10487a80d79140469ab1f8056349ca8545140a224dbbed7ded *perl-5.34.0.tar.xz' | sha256sum -c -     && tar --strip-components=1 -xaf perl-5.34.0.tar.xz -C /usr/src/perl     && rm perl-5.34.0.tar.xz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -LO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7044.tar.gz     && echo '9b60767fe40752ef7a9d3f13f19060a63389a5c23acc3e9827e19b75500f81f3 *App-cpanminus-1.7044.tar.gz' | sha256sum -c -     && tar -xzf App-cpanminus-1.7044.tar.gz && cd App-cpanminus-1.7044 && perl bin/cpanm . && cd /root     && true     && rm -fr ./cpanm /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7044* /tmp/*
# Tue, 01 Mar 2022 07:51:03 GMT
WORKDIR /
# Tue, 01 Mar 2022 07:51:03 GMT
CMD ["perl5.34.0" "-de0"]
```

-	Layers:
	-	`sha256:05bdf937590b731e3ffabc77f5871a8a9c7e597b417485eb87bc8541e791026b`  
		Last Modified: Tue, 01 Mar 2022 02:07:47 GMT  
		Size: 49.0 MB (49005374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdb8877d9e145f9b36d4b6ce925bfba017d214117b3a9ffdded7895c9e5f07ad`  
		Last Modified: Tue, 01 Mar 2022 04:00:50 GMT  
		Size: 7.4 MB (7401505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f39f0fcec69d1c8fe79f586cfff15fbfb251a666eb3bd6f16ec55c24d4392017`  
		Last Modified: Tue, 01 Mar 2022 04:00:50 GMT  
		Size: 9.9 MB (9883076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:712b9a603e5ec96f647d7c70f8627b53e05bdb787d56a8cd518f70181b04ca3e`  
		Last Modified: Tue, 01 Mar 2022 04:01:04 GMT  
		Size: 51.4 MB (51381386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09d0f13163ac43db084ed13d3b1f8efa441073c91a0850e97abfa7df8fbf2cb0`  
		Last Modified: Tue, 01 Mar 2022 04:01:29 GMT  
		Size: 176.9 MB (176903278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70800bf86472b3fff084680e40b5fc121e346281f838bbfb5c8ff0f3c09413e8`  
		Last Modified: Tue, 01 Mar 2022 09:23:15 GMT  
		Size: 201.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d3812721ef978e9c25d7b92479b36df1234bf4973a21c3b52c0c19da33098de`  
		Last Modified: Tue, 01 Mar 2022 09:24:25 GMT  
		Size: 14.7 MB (14714717 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
