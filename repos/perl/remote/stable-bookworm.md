## `perl:stable-bookworm`

```console
$ docker pull perl@sha256:cc433d1618890cbee72d1cbb348dc976bcd3ce2ec73dc057c29571d18bf067a6
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

### `perl:stable-bookworm` - linux; amd64

```console
$ docker pull perl@sha256:712e2c8e44dce08d96591fe5b50aff23e4a6f21500c9faf982655ee355683d79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **364.6 MB (364606274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64b5e425befdc0d49afd47b8853e7529cbdb672ed0b45ef8b93171af22c58d0a`
-	Default Command: `["perl5.38.2","-de0"]`

```dockerfile
# Thu, 21 Mar 2024 18:18:23 GMT
ADD file:2cc4cba2834c189d0dc41b5d79e1236770862c38452517fcbbb28015b88ab5cf in / 
# Thu, 21 Mar 2024 18:18:23 GMT
CMD ["bash"]
# Thu, 21 Mar 2024 18:18:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
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
	-	`sha256:1468e7ff95fcb865fbc4dee7094f8b99c4dcddd6eb2180cf044c7396baf6fc2f`  
		Last Modified: Wed, 24 Apr 2024 03:32:18 GMT  
		Size: 49.6 MB (49576283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cf9c2b42f41b1845f3e4421b723d56146db82939dc884555e077768e18132f4`  
		Last Modified: Wed, 24 Apr 2024 04:20:50 GMT  
		Size: 24.1 MB (24050140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4c40c3e3cdf945721f480e1d939aac857876fdb5c33b8fbfcf655c63b0b9428`  
		Last Modified: Wed, 24 Apr 2024 04:21:09 GMT  
		Size: 64.1 MB (64142118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c05cc1123d7e335d59b0f465c23b7ad2ad27f4875b6c3eab41c65a9b50efa382`  
		Last Modified: Wed, 24 Apr 2024 04:21:45 GMT  
		Size: 211.2 MB (211175606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc41c8a224012720385f8a9b08ee5f78caf13f0c934892da7b26a23cb436470b`  
		Last Modified: Wed, 24 Apr 2024 05:05:11 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed75108d9a93ad1b1b1f548e90d4d75d9951e0e2a676598ad15d57b1ee188ca8`  
		Last Modified: Wed, 24 Apr 2024 05:05:41 GMT  
		Size: 15.7 MB (15661862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1a9d57ae45b1b1b8cab6bb50d87a7321b4a6030b0c10c60ed21e0ee324ec1f6`  
		Last Modified: Wed, 24 Apr 2024 05:05:41 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:stable-bookworm` - unknown; unknown

```console
$ docker pull perl@sha256:76b4955aa65f8c7ea10b426fc26d4be7d5089ba8f2efb38e0fc2d4c7215d6802
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 MB (15388130 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8778f2381ed51f98052da88d1e7f4e12edb18000ac2c8f00ac3657dfb97b2fe8`

```dockerfile
```

-	Layers:
	-	`sha256:1a8cb22e91c0ccb1ea0622d05b6f61512e6f499ece158c3185938a77f87f6073`  
		Last Modified: Wed, 24 Apr 2024 05:05:41 GMT  
		Size: 15.4 MB (15370366 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:56c185aa225387a84c12044e503b284d42f61628da3578bc9349f3a3ce5e6b44`  
		Last Modified: Wed, 24 Apr 2024 05:05:41 GMT  
		Size: 17.8 KB (17764 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:stable-bookworm` - linux; arm variant v5

```console
$ docker pull perl@sha256:498266ef5316bc6dd215e8c59b45373a76eca7ee4c669a03d675d18d0fab3ee0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **331.0 MB (331026894 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b77cd6260c582b59c1c87c687b430ea609a7c4615fe90939193e3fb079a6868c`
-	Default Command: `["perl5.38.2","-de0"]`

```dockerfile
# Thu, 21 Mar 2024 18:18:23 GMT
ADD file:458ef8c446d0c1da2aca3270d75aeaf985b33ec7da8acf785930f7c48c85c8ac in / 
# Thu, 21 Mar 2024 18:18:23 GMT
CMD ["bash"]
# Thu, 21 Mar 2024 18:18:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
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
	-	`sha256:cb55d4975809ec76ad68f4174322fed658295a5f59cfef69c5aa183cebddacc9`  
		Last Modified: Wed, 24 Apr 2024 03:56:04 GMT  
		Size: 47.3 MB (47338674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b5ca1e355455209d09fc34a9ddf791d065f602e57edf9994847cb9763f75ddf`  
		Last Modified: Wed, 24 Apr 2024 04:28:20 GMT  
		Size: 22.7 MB (22728573 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea0660e8ec98ea2088b9858a6beb3ad35ea681832f58e7999be624a7771d6a34`  
		Last Modified: Wed, 24 Apr 2024 04:28:42 GMT  
		Size: 61.5 MB (61517814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20ebf214a4e7baa3e52df52da62b2c302118f2f995483ae5a5c081cfb69bd2ea`  
		Last Modified: Wed, 24 Apr 2024 04:29:22 GMT  
		Size: 184.5 MB (184499537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bc46bd8e8cbf63a943339c2a1b407be32aaaba7f6a156765473d738130d220e`  
		Last Modified: Wed, 24 Apr 2024 17:40:12 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:206b35734447d5ef2c3334ae9a861ff6536845789841a9b79e2358f47d5ba98e`  
		Last Modified: Wed, 24 Apr 2024 17:40:13 GMT  
		Size: 14.9 MB (14942029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2efe3efa3fc946361cf5e0ad5a25ee7754b30e1c0cee03bf4fce56ed04fda16`  
		Last Modified: Wed, 24 Apr 2024 17:40:12 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:stable-bookworm` - unknown; unknown

```console
$ docker pull perl@sha256:75e61b7df1dc1eea8fc73d7b08c6c7b810c71b6970f686e0e0a5794a278a9cb9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.2 MB (15187995 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fa40c38c2e7a68487ebe16f39f87ae4dd7d54cf7632064871ed54ed930842b4`

```dockerfile
```

-	Layers:
	-	`sha256:6e10239e738bd59f4505d7b020dde0a0459207c0c4d80b5025c31dc439f42fb7`  
		Last Modified: Wed, 24 Apr 2024 17:40:13 GMT  
		Size: 15.2 MB (15170776 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0525a92cb010deefaaf1270580c5ff62f125a6a87ab4d88eb71e73cbfc0e9f85`  
		Last Modified: Wed, 24 Apr 2024 17:40:12 GMT  
		Size: 17.2 KB (17219 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:stable-bookworm` - linux; arm variant v7

```console
$ docker pull perl@sha256:be1d9155aa20e653286fd9dcfbeddecbb6410bd0351e4619eea7e94cf2cebc62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **316.2 MB (316159769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bfafc6a168da96b43d00f72d5fb021ec17a27322df4478741b5eb334362dd27`
-	Default Command: `["perl5.38.2","-de0"]`

```dockerfile
# Thu, 21 Mar 2024 18:18:23 GMT
ADD file:30e85746fe77290a5de7286ebb7e2484b39554122eadc92de3df4ef4d95de9ff in / 
# Thu, 21 Mar 2024 18:18:23 GMT
CMD ["bash"]
# Thu, 21 Mar 2024 18:18:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
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
	-	`sha256:debd7c42d7ee74277f743dba14187c21ed8be6cf4f57abbaeb7b88c779282f09`  
		Last Modified: Wed, 10 Apr 2024 01:03:59 GMT  
		Size: 45.2 MB (45158610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1564e42498f84ce1d5bb6808049f9c674335b23f95ba63cf15c09549e3990e59`  
		Last Modified: Wed, 10 Apr 2024 06:59:53 GMT  
		Size: 22.0 MB (21950348 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea816b946832e576a6e2cfe5a7a28caeea429092724dc7daabb1e183ddd4817a`  
		Last Modified: Wed, 10 Apr 2024 07:00:21 GMT  
		Size: 59.2 MB (59213244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f06ca0e9dd61a104b8a520d84acce1978bf9c5574bb1c0d9b8cabc3205ce8ec`  
		Last Modified: Wed, 10 Apr 2024 07:01:07 GMT  
		Size: 175.1 MB (175103649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c04ba277342950b666adbd1e2306116843f48615e407107f05b5864cf51ee6c`  
		Last Modified: Fri, 12 Apr 2024 07:16:46 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffba953b433ecd468a02b0fd4bb8cf6f90f61488d14a5ed8f9dd6bb456a4716e`  
		Last Modified: Fri, 12 Apr 2024 07:16:48 GMT  
		Size: 14.7 MB (14733651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dcc931b23e8916cfc7e21d050d8fde0a65f9cad3b0d4b48706a98c9b4eebca4`  
		Last Modified: Fri, 12 Apr 2024 07:16:46 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:stable-bookworm` - unknown; unknown

```console
$ docker pull perl@sha256:12b2bc98be4bbdbaec9b8e05dfabb14136b8fdf9cdfeb482cbdd7fcfdbeccb69
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.2 MB (15193063 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9e98d387a8cb5745b478518def18f5b2b83afd6a9e25e2f4195c4b3865b4db5`

```dockerfile
```

-	Layers:
	-	`sha256:5f5aa5794de521f206f7aadce52cac48dba24ae6afe8f4169cd95c4548ed7f29`  
		Last Modified: Fri, 12 Apr 2024 07:16:47 GMT  
		Size: 15.2 MB (15175848 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3bb3b527b07ce19cf5d26583ad16efc3f754cbb913f693406d799b5dfb7a77b6`  
		Last Modified: Fri, 12 Apr 2024 07:16:46 GMT  
		Size: 17.2 KB (17215 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:stable-bookworm` - linux; arm64 variant v8

```console
$ docker pull perl@sha256:963fd58cd8dc7ee78841bd05acba3c15dfae185c4ab41a4f9de95b8f44faa932
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **355.3 MB (355328624 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8fc66a878a7fc981636304c3c436a3c98637e7326758ea0a762ad02436fa0c53`
-	Default Command: `["perl5.38.2","-de0"]`

```dockerfile
# Thu, 21 Mar 2024 18:18:23 GMT
ADD file:d795219dc83a41b5bb4106e62eebd31ceef0aae1b81541156eae5fe98e89337c in / 
# Thu, 21 Mar 2024 18:18:23 GMT
CMD ["bash"]
# Thu, 21 Mar 2024 18:18:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
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
	-	`sha256:1e92f3a395ff98a929e797a3c392bb6d0f05531068d34b81d3cd41ed6ce82ca4`  
		Last Modified: Wed, 10 Apr 2024 00:43:42 GMT  
		Size: 49.6 MB (49596265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:374850c6db1702573c7004d630027931be318b2d71cb28e890e2fcd0f0730712`  
		Last Modified: Wed, 10 Apr 2024 04:31:58 GMT  
		Size: 23.6 MB (23582868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:421c44fab18bc9f4c62ca481e074d50b3a036e7c95c7607b6d036c34d67c5264`  
		Last Modified: Wed, 10 Apr 2024 04:32:17 GMT  
		Size: 64.0 MB (63990996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9717a38adec9939307bba3151627c24c2bbac069b221c2fcb0500a40f2736ec`  
		Last Modified: Wed, 10 Apr 2024 04:32:48 GMT  
		Size: 202.5 MB (202538376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d72a55f2216a4688fb0356d9ac2dfb86dcb32ee896883e3d3ff1813a3e223643`  
		Last Modified: Thu, 11 Apr 2024 05:19:49 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6af09ef775f647445a68ee227b68b22c5cda2247f77ac554ab503e7ed8fd4c03`  
		Last Modified: Thu, 11 Apr 2024 05:19:49 GMT  
		Size: 15.6 MB (15619852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ccfcbec9c8d8faabb477ef02816c5652454fd8dc04167377fdc1aae67dfb888`  
		Last Modified: Thu, 11 Apr 2024 05:19:49 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:stable-bookworm` - unknown; unknown

```console
$ docker pull perl@sha256:29c173ef7580a3a0a519ada8065e2955480656b02935bb3a9067a2f4e9939248
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 MB (15415606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0601d95ecb9678af3ced5b005eac509bcaa0ce71812b25cff3576c201e2e80d0`

```dockerfile
```

-	Layers:
	-	`sha256:d9e9a155461938c401bb71195a92d89b54cc1e57fa761b531034dd9fcd15bc1a`  
		Last Modified: Thu, 11 Apr 2024 05:19:49 GMT  
		Size: 15.4 MB (15398487 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0f069d512df78fb5008e742fd0a2663c9706704c45ff97fd312c69feaa1c2673`  
		Last Modified: Thu, 11 Apr 2024 05:19:48 GMT  
		Size: 17.1 KB (17119 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:stable-bookworm` - linux; 386

```console
$ docker pull perl@sha256:2a17eaf31421469df4e4b56f05219fd512cfed48326901a6e815451a4a84e2be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **366.7 MB (366732664 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ef5b530816ff7ff02602b6310f052e0a8da2be4f14243aef8ea3476a41efb4d`
-	Default Command: `["perl5.38.2","-de0"]`

```dockerfile
# Thu, 21 Mar 2024 18:18:23 GMT
ADD file:f9a006425066d79ec04210dee08da23c9a68df2b7ea7e47b41cbc9d8b7545361 in / 
# Thu, 21 Mar 2024 18:18:23 GMT
CMD ["bash"]
# Thu, 21 Mar 2024 18:18:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
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
	-	`sha256:c7b4c0568972903287c2ba295779f478db7fc45d1844ec5d10e22332f4cd1d84`  
		Last Modified: Wed, 24 Apr 2024 03:43:10 GMT  
		Size: 50.6 MB (50602565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdba4056eb3a537ebb74fd333c27daceac5385bc3101b6029e706a51de775f00`  
		Last Modified: Wed, 24 Apr 2024 04:41:08 GMT  
		Size: 24.9 MB (24888940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1aa0583cb1d092e1ca2b9a9e9ad274c286cbda7804622a36572a00c3440b4d88`  
		Last Modified: Wed, 24 Apr 2024 04:41:36 GMT  
		Size: 66.0 MB (65989175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d4346162f795b064031764e3d351299d91568e9a1cb9ff0ae23d323d99339d1`  
		Last Modified: Wed, 24 Apr 2024 04:42:27 GMT  
		Size: 210.1 MB (210101062 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b3bebde3e672a46587e4fab5c65fb15087ffd827df3db469fc8cbdd84221f4d`  
		Last Modified: Wed, 24 Apr 2024 05:06:31 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e61cb72be621ee294dede4e32e7293becbb2476a01c7f5f75d3a40e42f1bb74`  
		Last Modified: Wed, 24 Apr 2024 05:06:31 GMT  
		Size: 15.2 MB (15150655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:413eac1eef3d9a067ce0d4459322cfd1f38701ee389a77bc76353e92e79c5137`  
		Last Modified: Wed, 24 Apr 2024 05:06:31 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:stable-bookworm` - unknown; unknown

```console
$ docker pull perl@sha256:1810c9fc3f820b99843cfb5630b226285d92e28ff9af3f65c477c01aaf246512
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 MB (15367108 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ed259a60070e405074e662355333ef19c057b440acce9acac1b50566d36d80c`

```dockerfile
```

-	Layers:
	-	`sha256:e44cdedcb49a35775a479f4143d9320e85b9ff1d9677c0fb891d489885e56af9`  
		Last Modified: Wed, 24 Apr 2024 05:06:31 GMT  
		Size: 15.3 MB (15349403 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d016a7140af4d4b9596788326aa967fa0a87d97cb56adcde7a3265e4a1720013`  
		Last Modified: Wed, 24 Apr 2024 05:06:31 GMT  
		Size: 17.7 KB (17705 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:stable-bookworm` - linux; mips64le

```console
$ docker pull perl@sha256:7624986a3498ef68e4c180fa44eca7dcdf24bd90ba7346b426ae3fc36ffd977c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **340.7 MB (340731086 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3350ef9604edc7508f00413b8c0f88ed01ddd1099940795cd0959bac471bf15`
-	Default Command: `["perl5.38.2","-de0"]`

```dockerfile
# Thu, 21 Mar 2024 18:18:23 GMT
ADD file:236d3683476bb8b0b7aeab0fd57eb85cfd2718deaba78d6113f3cfd93778c6ae in / 
# Thu, 21 Mar 2024 18:18:23 GMT
CMD ["bash"]
# Thu, 21 Mar 2024 18:18:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
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
	-	`sha256:8d3071232c2d967757129e1e890a482a53bf14992ca2a151a61f4661b0ac445c`  
		Last Modified: Wed, 10 Apr 2024 01:21:15 GMT  
		Size: 49.6 MB (49567247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af6c10adc206ee143e79f0f22af100821851954909d39ecb2784d730c08e7d42`  
		Last Modified: Wed, 10 Apr 2024 15:46:22 GMT  
		Size: 23.6 MB (23630649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59038da844051badb769294af562fc6d5228b2a6133802cc157f8ba7e99b38a6`  
		Last Modified: Wed, 10 Apr 2024 15:47:16 GMT  
		Size: 63.0 MB (62965809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bff48902465690b5e1c724ab386f90544f73ef8d3af2c1cdab1d946569082db6`  
		Last Modified: Wed, 10 Apr 2024 15:49:25 GMT  
		Size: 189.7 MB (189698924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb5067040c294c6c04b2ae69e5400cba1f4c2d1e53b29457da5c7665556fcce2`  
		Last Modified: Fri, 12 Apr 2024 10:55:34 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36fdf06800726a12a2d6fa7027dfed88e889a41f5a4253aebd6a4eb370e768fb`  
		Last Modified: Fri, 12 Apr 2024 10:55:37 GMT  
		Size: 14.9 MB (14868189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3db823b33524b146bb4f83f239f477ab141126fd9d611b62c0197018cd8ba90`  
		Last Modified: Fri, 12 Apr 2024 10:55:36 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:stable-bookworm` - unknown; unknown

```console
$ docker pull perl@sha256:9b394ec5209c35819522fee79434cdd10826ae4d76a07a450b396fb495298e3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.7 KB (17656 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba9f370a155b6b0a35c8b751b00be8cbb5ac570d6d1df9dcf637a27e0c1627df`

```dockerfile
```

-	Layers:
	-	`sha256:5717c1a6233e5f26f8c9af1ca09d8f3ea9ea881f790eaec7bc2f56e0f43ccb35`  
		Last Modified: Fri, 12 Apr 2024 10:55:30 GMT  
		Size: 17.7 KB (17656 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:stable-bookworm` - linux; ppc64le

```console
$ docker pull perl@sha256:06ddf660d9afb37ad14d12b6ed68358ad69ecbae5d9643c0df145e2907b8838c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **378.7 MB (378671140 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61eb2e4cd53379f3c6084e3a4282c6cc948dd09d3af7eccd15c2df880cc945c9`
-	Default Command: `["perl5.38.2","-de0"]`

```dockerfile
# Thu, 21 Mar 2024 18:18:23 GMT
ADD file:12519205a7ecc1a9b92b9b26c967bf9f7204f2e0b9c81cb9a147b10a29b0715c in / 
# Thu, 21 Mar 2024 18:18:23 GMT
CMD ["bash"]
# Thu, 21 Mar 2024 18:18:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
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
	-	`sha256:e6dcf23c0df5604eb9aa3050ab9c36d44dec4ab1448d2c229f4beaaf0f7fa503`  
		Last Modified: Wed, 10 Apr 2024 01:30:37 GMT  
		Size: 53.6 MB (53562477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e9a49dc2918c681cd1306002e0306d198b0ab9f74366235b251cb85c930eaaa`  
		Last Modified: Wed, 10 Apr 2024 07:16:20 GMT  
		Size: 25.7 MB (25696598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7558a95a0d29869e7f316194c1d23abcbbe4d8c3340f4d3103f670b9d4af3eef`  
		Last Modified: Wed, 10 Apr 2024 07:16:43 GMT  
		Size: 69.6 MB (69581154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aab0dede385435598179e3ab86d7c4094cf59880d986b82c837b42b0649d5afa`  
		Last Modified: Wed, 10 Apr 2024 07:17:27 GMT  
		Size: 214.2 MB (214172353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d82b24b282bb2e235e4b3a377597eecd2e62269be1584ff5a61e734001e23412`  
		Last Modified: Thu, 11 Apr 2024 05:31:47 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65dd346169943a73c1e4931b9cb8d42caf2fe0a6bb8231b82d6f73c559c4167d`  
		Last Modified: Thu, 11 Apr 2024 05:31:48 GMT  
		Size: 15.7 MB (15658290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:709575525371eb081a73f05f67ebd677f08e9507abaef0917038dc8b5e8cd149`  
		Last Modified: Thu, 11 Apr 2024 05:31:47 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:stable-bookworm` - unknown; unknown

```console
$ docker pull perl@sha256:81dd0d57e2701ac86f0aaa28cfa8929193e88fd58b0d80cfde257ece791a3f43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 MB (15363845 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44b3bbe5acf9924d24bf38234e7809bd4b65ac058395201d69e819a83022c34b`

```dockerfile
```

-	Layers:
	-	`sha256:9c58afb936de0ab309635cf71e11e015c0d301547bc993b413b75398078a8442`  
		Last Modified: Thu, 11 Apr 2024 05:31:48 GMT  
		Size: 15.3 MB (15346674 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5c2d1fe70be88544b477542829555eb930bbbbc8e45eb2f27c2c75574c05f04f`  
		Last Modified: Thu, 11 Apr 2024 05:31:47 GMT  
		Size: 17.2 KB (17171 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:stable-bookworm` - linux; s390x

```console
$ docker pull perl@sha256:cd78873837f80677f0ce13045a1b0caad9bf7d4dd35b4753c52a20eea73d1bb1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **334.3 MB (334255831 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21af60e86ac35a113186a778a73a8ac724ff4451126c66b645533ac599ecf551`
-	Default Command: `["perl5.38.2","-de0"]`

```dockerfile
# Thu, 21 Mar 2024 18:18:23 GMT
ADD file:4b6b256d3328c1d19403b3eb0f375b5d33724b65f790edd27be4adca49c66e4b in / 
# Thu, 21 Mar 2024 18:18:23 GMT
CMD ["bash"]
# Thu, 21 Mar 2024 18:18:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
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
	-	`sha256:17f5c0a7be3d447b0aca6569b534fabcb69c578072a0cdb81f078fd4872eba70`  
		Last Modified: Wed, 10 Apr 2024 01:48:11 GMT  
		Size: 47.9 MB (47922706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5a94fdcea32a650c77c01028838d670a5840f3ead5a1cf5526e922967f0df66`  
		Last Modified: Wed, 10 Apr 2024 07:30:52 GMT  
		Size: 24.0 MB (24043531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdaec0019454e24574ad418259f50f0d68508dcf92f31f05ca5d5ad33dcf43bb`  
		Last Modified: Wed, 10 Apr 2024 07:31:10 GMT  
		Size: 63.1 MB (63126889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfce7e73c441e81b6b2408dea6732c47c87f4c633b91c6d77faf8891b50ab262`  
		Last Modified: Wed, 10 Apr 2024 07:31:45 GMT  
		Size: 183.2 MB (183165967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9f35a2ff4d86badf7ed41d0e401c93fd00fc3f0ef265aaf9113d50f7f81e115`  
		Last Modified: Sat, 13 Apr 2024 04:57:16 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c057c10dfb2c9e11a6078ebffed11c24749753120ed86558eccdc6f377930bcb`  
		Last Modified: Sat, 13 Apr 2024 04:57:16 GMT  
		Size: 16.0 MB (15996471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1be6d3b62e01ed36fc5513651556059135b05df41026d97b3e35e41f95518d7`  
		Last Modified: Sat, 13 Apr 2024 04:57:15 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:stable-bookworm` - unknown; unknown

```console
$ docker pull perl@sha256:8a152974f4d635996acbaec034f4246cb42ab3bca099cd5287d830d5e9d7bfa9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.2 MB (15201748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44497e5b8da19add001a970a8f1e252e7cb36d075ca5a89a0fe1860d188919dd`

```dockerfile
```

-	Layers:
	-	`sha256:fcd1a741543e663f3183913ce1e6e89e7bc6922cf4ee9ec186656abe96aa13f5`  
		Last Modified: Sat, 13 Apr 2024 04:57:16 GMT  
		Size: 15.2 MB (15184652 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:024109ac225466c66de8a6eb864be72196c39afa7577517eebb5a6fd52a90cd4`  
		Last Modified: Sat, 13 Apr 2024 04:57:15 GMT  
		Size: 17.1 KB (17096 bytes)  
		MIME: application/vnd.in-toto+json
