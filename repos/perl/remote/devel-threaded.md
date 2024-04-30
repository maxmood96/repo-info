## `perl:devel-threaded`

```console
$ docker pull perl@sha256:32d0c985dd7b9557c26d3d4006037681a13124021a11ec4b2c25c083c0441d04
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

### `perl:devel-threaded` - linux; amd64

```console
$ docker pull perl@sha256:c9513d2b505679749eecb0b23cdba6f59a6640b6844de7dc5b1a8bfa7a7fd572
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **364.9 MB (364931059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db134ed5c520e46f6aa072bb83af27ae3396fe014c790e592f1a47b25e04aba6`
-	Default Command: `["perl5.39.10","-de0"]`

```dockerfile
# Wed, 24 Apr 2024 03:27:57 GMT
ADD file:2cc4cba2834c189d0dc41b5d79e1236770862c38452517fcbbb28015b88ab5cf in / 
# Wed, 24 Apr 2024 03:27:57 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 04:10:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 04:10:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 04:11:52 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 29 Apr 2024 09:51:00 GMT
WORKDIR /usr/src/perl
# Mon, 29 Apr 2024 09:51:00 GMT
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/P/PE/PEVANS/perl-5.39.10.tar.gz -o perl-5.39.10.tar.gz     && echo '4b7ffb3e068583fa5c8413390c998b2c15214f205ce737acc485b40932b9f419 *perl-5.39.10.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.39.10.tar.gz -C /usr/src/perl     && rm perl-5.39.10.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997014/cpm -o /usr/local/bin/cpm     && echo 'ee525f2493e36c6f688eddabaf53a51c4d3b2a4ebaa81576ac8b9f78ab57f4a1 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Mon, 29 Apr 2024 09:51:00 GMT
WORKDIR /usr/src/app
# Mon, 29 Apr 2024 09:51:00 GMT
CMD ["perl5.39.10" "-de0"]
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
	-	`sha256:1f54735751e055ba0ce76fb6b2694c81df5148e0fbac272b89f505529fb10a4e`  
		Last Modified: Mon, 29 Apr 2024 18:20:00 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae054d0488c57da9e47cc0106592b4595c5a4038971e463319bd34051ad60753`  
		Last Modified: Mon, 29 Apr 2024 18:20:00 GMT  
		Size: 16.0 MB (15986645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f882ceb7138f77a78baf3e2a7ceaa3e93c06f856bcf1ce3205002403baf9e0c9`  
		Last Modified: Mon, 29 Apr 2024 18:20:00 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-threaded` - unknown; unknown

```console
$ docker pull perl@sha256:9b32a71b3aaa350841004438a80e4c7d7783cbb3f9c640f6796f66b20cba906a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 MB (15386122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d79fd8b1f3414e24093fe0f48030fdc735174d8fb58f5f1e6c078f14bfcf42a`

```dockerfile
```

-	Layers:
	-	`sha256:298caa65eb928c1eb4ba8f774923add1652e7f12f567c245f32a6c79234a6ea9`  
		Last Modified: Mon, 29 Apr 2024 18:20:00 GMT  
		Size: 15.4 MB (15369298 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:144b3ed25978250554184f67bed1bea1b764118da272076c73ba9f8a3a74785c`  
		Last Modified: Mon, 29 Apr 2024 18:20:00 GMT  
		Size: 16.8 KB (16824 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-threaded` - linux; arm variant v5

```console
$ docker pull perl@sha256:af417140e6a698c3cc7cb8a65a937aa591d69d3386e69c60d484260895885ee6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **331.3 MB (331329305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27afdb33e08757bb4ebe7e9228b6fc4fe57038aa5a4b6cff42429fffdc9edbae`
-	Default Command: `["perl5.39.10","-de0"]`

```dockerfile
# Wed, 24 Apr 2024 03:53:02 GMT
ADD file:458ef8c446d0c1da2aca3270d75aeaf985b33ec7da8acf785930f7c48c85c8ac in / 
# Wed, 24 Apr 2024 03:53:03 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 04:16:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 04:16:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 04:17:59 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 29 Apr 2024 09:51:00 GMT
WORKDIR /usr/src/perl
# Mon, 29 Apr 2024 09:51:00 GMT
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/P/PE/PEVANS/perl-5.39.10.tar.gz -o perl-5.39.10.tar.gz     && echo '4b7ffb3e068583fa5c8413390c998b2c15214f205ce737acc485b40932b9f419 *perl-5.39.10.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.39.10.tar.gz -C /usr/src/perl     && rm perl-5.39.10.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997014/cpm -o /usr/local/bin/cpm     && echo 'ee525f2493e36c6f688eddabaf53a51c4d3b2a4ebaa81576ac8b9f78ab57f4a1 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Mon, 29 Apr 2024 09:51:00 GMT
WORKDIR /usr/src/app
# Mon, 29 Apr 2024 09:51:00 GMT
CMD ["perl5.39.10" "-de0"]
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
	-	`sha256:4488a927ea6171a17555bf6b40a7fb8348ee527664af5f9c13ae3faf37c7165a`  
		Last Modified: Mon, 29 Apr 2024 19:04:17 GMT  
		Size: 15.2 MB (15244441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35915d479e0398c36a904d48486686d5717dc15f30b0285070018befe60024fc`  
		Last Modified: Mon, 29 Apr 2024 19:04:17 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-threaded` - unknown; unknown

```console
$ docker pull perl@sha256:948dfabb91b23cfc6a378363a44f6ef3c673f9848447b0b1c55a4a8014e4221f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.2 MB (15185923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5aa069dea68db7bb980e00d6e96d16138fc67c2eb4de0f939b9402a0ffea8820`

```dockerfile
```

-	Layers:
	-	`sha256:bb18b2e4f31c3af26f9a256d1b2f199d4d7751fec10f15ebd82a4bfb07ef9b0d`  
		Last Modified: Mon, 29 Apr 2024 19:04:17 GMT  
		Size: 15.2 MB (15169676 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:095f4abc03f5cba6b9196ef45b2bbf637e2c6f25c7af8d800c01f0af496ba7d6`  
		Last Modified: Mon, 29 Apr 2024 19:04:16 GMT  
		Size: 16.2 KB (16247 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-threaded` - linux; arm variant v7

```console
$ docker pull perl@sha256:f6ee4284bafc46bc0405aa25e685c0a879520302d0638331a72b9d9fb9155436
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **316.5 MB (316509843 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb24e5cc0cdef3c5c67dd98028548b60a3739f67cc7db06504495cd5a1a31701`
-	Default Command: `["perl5.39.10","-de0"]`

```dockerfile
# Wed, 24 Apr 2024 04:06:51 GMT
ADD file:b6d26ef7cfc03fe202f7a5ac219566bc37f382ffadc9acdad685f2dd318cf0e4 in / 
# Wed, 24 Apr 2024 04:06:52 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 04:50:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 04:50:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 04:51:30 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 29 Apr 2024 09:51:00 GMT
WORKDIR /usr/src/perl
# Mon, 29 Apr 2024 09:51:00 GMT
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/P/PE/PEVANS/perl-5.39.10.tar.gz -o perl-5.39.10.tar.gz     && echo '4b7ffb3e068583fa5c8413390c998b2c15214f205ce737acc485b40932b9f419 *perl-5.39.10.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.39.10.tar.gz -C /usr/src/perl     && rm perl-5.39.10.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997014/cpm -o /usr/local/bin/cpm     && echo 'ee525f2493e36c6f688eddabaf53a51c4d3b2a4ebaa81576ac8b9f78ab57f4a1 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Mon, 29 Apr 2024 09:51:00 GMT
WORKDIR /usr/src/app
# Mon, 29 Apr 2024 09:51:00 GMT
CMD ["perl5.39.10" "-de0"]
```

-	Layers:
	-	`sha256:80e84b3257949a283234599e3906626cfb4ff482d06fa4dc3eaf1dd36551dafa`  
		Last Modified: Wed, 24 Apr 2024 04:10:48 GMT  
		Size: 45.2 MB (45174994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52886721ea5a8a8bac2b197dccd42a74948b88bedcfe0fdf8b24e234c0a660d0`  
		Last Modified: Wed, 24 Apr 2024 05:02:39 GMT  
		Size: 22.0 MB (21953968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38d07170ec327fa1117b5289697e5555f4c3ba76d00200d7c7cc5c143086856f`  
		Last Modified: Wed, 24 Apr 2024 05:03:03 GMT  
		Size: 59.2 MB (59216995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2937bd8fccb438207fe0e77a48873de07dbe1fbea251206222298b72dbd2b3d8`  
		Last Modified: Wed, 24 Apr 2024 05:03:45 GMT  
		Size: 175.1 MB (175141109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e2b876007b7f32564832ccda3a889724ae59187ed3d29602ae97eb66296edd6`  
		Last Modified: Thu, 25 Apr 2024 07:58:51 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da32e8264360bc01c094499eb6ca81e91e6969e599cd54f9aab9ae46e2b85bc7`  
		Last Modified: Mon, 29 Apr 2024 19:19:47 GMT  
		Size: 15.0 MB (15022511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f851615ab6bcee2c1a8ff316eb09c00f811fddfadfebf6aef72d506045c63200`  
		Last Modified: Mon, 29 Apr 2024 19:19:46 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-threaded` - unknown; unknown

```console
$ docker pull perl@sha256:0686582e9565638b7be2a86a5b5d0ccf14489892c6f5dc4f76aaf13ff5800f30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.2 MB (15191396 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab662a550ded9b8b028182f346f81d1ead588ed328217c798ce15e5e2a029267`

```dockerfile
```

-	Layers:
	-	`sha256:74da491418617202c9c4754a913a2ddeb04d3515ae8321ed12988ff5ae267e5f`  
		Last Modified: Mon, 29 Apr 2024 19:19:46 GMT  
		Size: 15.2 MB (15175150 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3de7370a29e1a2455ebf3072089c0655803821b25108cce2e7db3df65878ae02`  
		Last Modified: Mon, 29 Apr 2024 19:19:46 GMT  
		Size: 16.2 KB (16246 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-threaded` - linux; arm64 variant v8

```console
$ docker pull perl@sha256:df8b8d67ffa1847c2ed716b2e89e8b0fc34bfdc9c464b266c0b8207fa9e50714
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **355.7 MB (355691729 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9065990013cf5663ff52bc6ca019af8d15f6f964cf72b1cc1a3caa40471fb1ba`
-	Default Command: `["perl5.39.9","-de0"]`

```dockerfile
# Thu, 21 Mar 2024 18:18:23 GMT
ADD file:07ae70ad05f39a24007b6bde4418c9934bc3865fe855dfcf62a44d8a30375739 in / 
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
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/P/PE/PEVANS/perl-5.39.9.tar.gz -o perl-5.39.9.tar.gz     && echo 'c589d2e36cbb8db30fb73f661ef2c06ffe9c680f8ebe417169ec259b48ec2119 *perl-5.39.9.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.39.9.tar.gz -C /usr/src/perl     && rm perl-5.39.9.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997014/cpm -o /usr/local/bin/cpm     && echo 'ee525f2493e36c6f688eddabaf53a51c4d3b2a4ebaa81576ac8b9f78ab57f4a1 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Thu, 21 Mar 2024 18:18:23 GMT
WORKDIR /usr/src/app
# Thu, 21 Mar 2024 18:18:23 GMT
CMD ["perl5.39.9" "-de0"]
```

-	Layers:
	-	`sha256:60bdaf986dbe787297bb85c9f6a28d13ea7b9608b95206ef7ce6cdea50cd5505`  
		Last Modified: Wed, 24 Apr 2024 04:13:43 GMT  
		Size: 49.6 MB (49613341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e100ddc6b415c632410507293430c0fe6bb4228ab320ed59548c6dc030b4e4a`  
		Last Modified: Wed, 24 Apr 2024 08:41:28 GMT  
		Size: 23.6 MB (23586795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba9a57bc3c0cb0c1ea5d28dc03fb4451ae05dc271b53941c27edf70eaf70b6e6`  
		Last Modified: Wed, 24 Apr 2024 08:41:47 GMT  
		Size: 64.0 MB (63994806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7476478a1e1450b999421118cb8f193aa62f1816e0cadd988a084385cf0a5696`  
		Last Modified: Wed, 24 Apr 2024 08:42:20 GMT  
		Size: 202.6 MB (202575289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad5be1b52bc72ba1d6b7c20ea592598946f70561b95eb10a02fca313de64587e`  
		Last Modified: Thu, 25 Apr 2024 08:12:47 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:217e2710a2bc3e0338b1b2c9ee3c2e80e7bd11391194255ead62c8d265cf3d4b`  
		Last Modified: Thu, 25 Apr 2024 13:42:08 GMT  
		Size: 15.9 MB (15921233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d74b2963dc68b54c3c9fda2980260679d5ab55a3e8363bf1bb5da1a0360847b5`  
		Last Modified: Thu, 25 Apr 2024 13:42:07 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-threaded` - unknown; unknown

```console
$ docker pull perl@sha256:caf68de8ed9889ab334f59b2030601dc231bf20965bd0e10905cffd6b4936a54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 MB (15413965 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf0c48dcd909c2f5f8c9c3bcbd499856299b631f1f66e3115fa482d283e0bd72`

```dockerfile
```

-	Layers:
	-	`sha256:855be25f007646be24236725438b4a31d8ac71443148f00c866df931450c90f5`  
		Last Modified: Thu, 25 Apr 2024 13:42:08 GMT  
		Size: 15.4 MB (15397807 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d5e87d8b6cc80394d2c96ccab80dfcbcdd8f47a0a2b680a19fa1f5e3669d7c1e`  
		Last Modified: Thu, 25 Apr 2024 13:42:07 GMT  
		Size: 16.2 KB (16158 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-threaded` - linux; 386

```console
$ docker pull perl@sha256:0e2a085ba09b29dd5913ace225b63ddc5c16805771adebd6ead571731273eabc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **367.1 MB (367112309 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7da7524af1bfcbe9c88abb29ebcdc02a24ca38eb7fbfed88e74f6693c4772879`
-	Default Command: `["perl5.39.10","-de0"]`

```dockerfile
# Wed, 24 Apr 2024 03:38:48 GMT
ADD file:f9a006425066d79ec04210dee08da23c9a68df2b7ea7e47b41cbc9d8b7545361 in / 
# Wed, 24 Apr 2024 03:38:48 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 04:28:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 04:29:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 04:30:15 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 29 Apr 2024 09:51:00 GMT
WORKDIR /usr/src/perl
# Mon, 29 Apr 2024 09:51:00 GMT
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/P/PE/PEVANS/perl-5.39.10.tar.gz -o perl-5.39.10.tar.gz     && echo '4b7ffb3e068583fa5c8413390c998b2c15214f205ce737acc485b40932b9f419 *perl-5.39.10.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.39.10.tar.gz -C /usr/src/perl     && rm perl-5.39.10.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997014/cpm -o /usr/local/bin/cpm     && echo 'ee525f2493e36c6f688eddabaf53a51c4d3b2a4ebaa81576ac8b9f78ab57f4a1 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Mon, 29 Apr 2024 09:51:00 GMT
WORKDIR /usr/src/app
# Mon, 29 Apr 2024 09:51:00 GMT
CMD ["perl5.39.10" "-de0"]
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
	-	`sha256:cd21104be0995efd31362a793c3ee741e0fdbfaa53c266867eb266d518c3feff`  
		Last Modified: Mon, 29 Apr 2024 18:20:47 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f09ee7acecc93577acf1047b5ddc6fdfeacceef5ad5c9373654698b7fdae02c7`  
		Last Modified: Mon, 29 Apr 2024 18:20:47 GMT  
		Size: 15.5 MB (15530301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae86c49f11d5192cca7e2fcd45de59de3337fe78d93b77f501c4f4e41485ec04`  
		Last Modified: Mon, 29 Apr 2024 18:20:47 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-threaded` - unknown; unknown

```console
$ docker pull perl@sha256:dc9c6a7cd8ba6f24a9c58e0856cf8da9e0a3b6de43481ae16dae966a1c2a1b65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 MB (15365140 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a6a44aa0188ba122e0115637fb3c80c2ec2d3192f7d58140e1b08d8af3dcb7e`

```dockerfile
```

-	Layers:
	-	`sha256:f0ceaa91050494dbac4071b2288f3702abce31e4012dcf077b9588e7cd812975`  
		Last Modified: Mon, 29 Apr 2024 18:20:47 GMT  
		Size: 15.3 MB (15348355 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7953c7096996b9c831231171cf80dc3f8dc3328160b4a7b0f580fc1d35806ec5`  
		Last Modified: Mon, 29 Apr 2024 18:20:47 GMT  
		Size: 16.8 KB (16785 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-threaded` - linux; mips64le

```console
$ docker pull perl@sha256:1e569a2e99a3ba32b443645cff875bb69ec18d54b275c1fe144b0b233ed986e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **340.9 MB (340934957 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d53c0bdb3a62b2c597629b2300a6f68eceb5c5e856ad372fe31c60d0f98957a7`
-	Default Command: `["perl5.39.10","-de0"]`

```dockerfile
# Wed, 24 Apr 2024 03:13:30 GMT
ADD file:bd5e48bc3973f1ba0b2958f5feb2ef619d1da33cebe3daa160741598f3a64020 in / 
# Wed, 24 Apr 2024 03:13:35 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 03:54:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 03:56:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 04:01:35 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 29 Apr 2024 09:51:00 GMT
WORKDIR /usr/src/perl
# Mon, 29 Apr 2024 09:51:00 GMT
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/P/PE/PEVANS/perl-5.39.10.tar.gz -o perl-5.39.10.tar.gz     && echo '4b7ffb3e068583fa5c8413390c998b2c15214f205ce737acc485b40932b9f419 *perl-5.39.10.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.39.10.tar.gz -C /usr/src/perl     && rm perl-5.39.10.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997014/cpm -o /usr/local/bin/cpm     && echo 'ee525f2493e36c6f688eddabaf53a51c4d3b2a4ebaa81576ac8b9f78ab57f4a1 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Mon, 29 Apr 2024 09:51:00 GMT
WORKDIR /usr/src/app
# Mon, 29 Apr 2024 09:51:00 GMT
CMD ["perl5.39.10" "-de0"]
```

-	Layers:
	-	`sha256:128b5268b494ed46f2601900fdc8201341f67542053dd84964164d230083ab26`  
		Last Modified: Wed, 24 Apr 2024 03:24:37 GMT  
		Size: 49.6 MB (49582786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1db7c75a6accf74d8a7a5baea9ca05e0af438c130a33d48ca96a5c26a8fd29ff`  
		Last Modified: Wed, 24 Apr 2024 04:30:27 GMT  
		Size: 23.4 MB (23438128 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e32516c9efb0754d31d8a9019f45fa9c88d3bdc96aca1c8a6cced34b949b6b7`  
		Last Modified: Wed, 24 Apr 2024 04:31:20 GMT  
		Size: 63.0 MB (62968465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6017c9766ed85b6acea7bb176207059bcb96d8c5056168e97cb57dd3a2b5c7e`  
		Last Modified: Wed, 24 Apr 2024 04:33:29 GMT  
		Size: 189.7 MB (189742660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c39b049e807d28a87a1ce1bef0b65108bbf7f8045118408b1714f5e80a36e205`  
		Last Modified: Mon, 29 Apr 2024 20:00:27 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbc1c3b69efe24f375e39298b80ffc4e9ccdab466a994849768971675056404d`  
		Last Modified: Mon, 29 Apr 2024 22:03:50 GMT  
		Size: 15.2 MB (15202653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:555e37f6f0947287318a792c55ce6e6d73eef8b587a7551370f0d7ba6349ead9`  
		Last Modified: Mon, 29 Apr 2024 22:03:49 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-threaded` - unknown; unknown

```console
$ docker pull perl@sha256:ebf5f79fab1a070de192617a7b22336e321833960b3ac891e3b05a68b1ddbcc7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.0 KB (16017 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f48fa3e2988ebc9dd2b5ff7615d6a0a755f02071be817b886b7850d2c5276569`

```dockerfile
```

-	Layers:
	-	`sha256:bf334eee6e388b17764fd508ee22d27cdcf84591d6cc49715858be1e0ab5e3b9`  
		Last Modified: Mon, 29 Apr 2024 22:03:48 GMT  
		Size: 16.0 KB (16017 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-threaded` - linux; ppc64le

```console
$ docker pull perl@sha256:9387f1e07ec40f444c0d6db297c4d63de6a26f44eeee9facd5649fe55a913c6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **379.1 MB (379104116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e55c023e3e1dc57fd1874d188fca01026316bdd5a47c9d939af09a9e006be0a0`
-	Default Command: `["perl5.39.10","-de0"]`

```dockerfile
# Wed, 24 Apr 2024 03:20:52 GMT
ADD file:6b48a0374d2bf17058a1ace290a29b25ef9f56d85e94d8cd33ac09dbdc5daddf in / 
# Wed, 24 Apr 2024 03:20:55 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 03:48:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 03:49:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 03:56:05 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 29 Apr 2024 09:51:00 GMT
WORKDIR /usr/src/perl
# Mon, 29 Apr 2024 09:51:00 GMT
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/P/PE/PEVANS/perl-5.39.10.tar.gz -o perl-5.39.10.tar.gz     && echo '4b7ffb3e068583fa5c8413390c998b2c15214f205ce737acc485b40932b9f419 *perl-5.39.10.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.39.10.tar.gz -C /usr/src/perl     && rm perl-5.39.10.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997014/cpm -o /usr/local/bin/cpm     && echo 'ee525f2493e36c6f688eddabaf53a51c4d3b2a4ebaa81576ac8b9f78ab57f4a1 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Mon, 29 Apr 2024 09:51:00 GMT
WORKDIR /usr/src/app
# Mon, 29 Apr 2024 09:51:00 GMT
CMD ["perl5.39.10" "-de0"]
```

-	Layers:
	-	`sha256:bf47934b0700489c27f4b1918c464037353ebec2ebc12585ceea997c9a34c71c`  
		Last Modified: Wed, 24 Apr 2024 03:25:57 GMT  
		Size: 53.6 MB (53580168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:677be8677970cb6c89d034144a91a8695625d82f32553778be503e17ab5f55b3`  
		Last Modified: Wed, 24 Apr 2024 04:22:57 GMT  
		Size: 25.7 MB (25699777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a48162777bb1b177bfa77ee29ba9552a6c899119f959faa64ef54f0a5aab3116`  
		Last Modified: Wed, 24 Apr 2024 04:23:19 GMT  
		Size: 69.6 MB (69584472 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:326e881f9e7d456fa7b2b9e91f26b48776888d7ca1975413e2554119bfef1024`  
		Last Modified: Wed, 24 Apr 2024 04:23:59 GMT  
		Size: 214.2 MB (214213767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfaff0bb0d2a5a48a70914e3b7d3f513194515bbd37798e7d1f16560093e6fe2`  
		Last Modified: Thu, 25 Apr 2024 03:53:17 GMT  
		Size: 134.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e833d0f107963839ea829573fee14164f2697533cc25b8d7adc1fb8a9cd5576`  
		Last Modified: Mon, 29 Apr 2024 19:18:19 GMT  
		Size: 16.0 MB (16025666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:304dd9e4f7cfcd209a9b2ce63c22d15208a0f14dd941dac0ee80d7bfb6156e58`  
		Last Modified: Mon, 29 Apr 2024 19:18:18 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-threaded` - unknown; unknown

```console
$ docker pull perl@sha256:f623635b42228b9dd47a294f7b309d7524503e5ca8ef81f38cfd559829b65200
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 MB (15362194 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbefbea1e489c3589085949847385056bcc035664b8683c62604414ce6171140`

```dockerfile
```

-	Layers:
	-	`sha256:9cbdb0b3c1a4f67297f2df2fb8beb6ebb12b79c512ef3904b372fd2feff1d328`  
		Last Modified: Mon, 29 Apr 2024 19:18:19 GMT  
		Size: 15.3 MB (15345984 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a7c6cb9981c9260137d4b5ff5906459438e045fe319af41abb9365394689a58f`  
		Last Modified: Mon, 29 Apr 2024 19:18:18 GMT  
		Size: 16.2 KB (16210 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:devel-threaded` - linux; s390x

```console
$ docker pull perl@sha256:2c74ea0915b85c997f243b8119a98c8eaebdbe6be3fab57048eb57649196d019
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **334.7 MB (334652088 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efe2e8cf5d00ad620cc62b3392bea69fca8eb457df603ce99d024ff2f3a5a942`
-	Default Command: `["perl5.39.10","-de0"]`

```dockerfile
# Wed, 24 Apr 2024 03:42:45 GMT
ADD file:6b0e091009ac95d80973222b4f56557fc521253f20bb18eea1c9da2b61ed5cc2 in / 
# Wed, 24 Apr 2024 03:42:53 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 04:10:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 04:11:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 04:12:30 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 29 Apr 2024 09:51:00 GMT
WORKDIR /usr/src/perl
# Mon, 29 Apr 2024 09:51:00 GMT
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/P/PE/PEVANS/perl-5.39.10.tar.gz -o perl-5.39.10.tar.gz     && echo '4b7ffb3e068583fa5c8413390c998b2c15214f205ce737acc485b40932b9f419 *perl-5.39.10.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.39.10.tar.gz -C /usr/src/perl     && rm perl-5.39.10.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local -Dusedevel -Dversiononly=undef -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997014/cpm -o /usr/local/bin/cpm     && echo 'ee525f2493e36c6f688eddabaf53a51c4d3b2a4ebaa81576ac8b9f78ab57f4a1 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Mon, 29 Apr 2024 09:51:00 GMT
WORKDIR /usr/src/app
# Mon, 29 Apr 2024 09:51:00 GMT
CMD ["perl5.39.10" "-de0"]
```

-	Layers:
	-	`sha256:ea1cd174fa855055f0cc0296260c9e987dbd4cddfc8655fe48891b91e5af95b7`  
		Last Modified: Wed, 24 Apr 2024 03:48:59 GMT  
		Size: 47.9 MB (47942206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74e212650b3684bdd95eb8c4cd55ad81ca7f992455cbcc5c126d1aac521b5399`  
		Last Modified: Wed, 24 Apr 2024 04:23:04 GMT  
		Size: 24.0 MB (24047036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17c5049d590d068e07d3557ef371a6ccc2fc96ffadeabbf0c1115204536ff84b`  
		Last Modified: Wed, 24 Apr 2024 04:23:21 GMT  
		Size: 63.1 MB (63130514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74409f156b70503c3e2227e45d964aec57dadc484e6492078584c8cad2e0884f`  
		Last Modified: Wed, 24 Apr 2024 04:23:50 GMT  
		Size: 183.2 MB (183208845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:318db2938dd1836ac7a70cfbe39692f995046b7124512857e6aa5d25414b10b9`  
		Last Modified: Thu, 25 Apr 2024 02:53:07 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74997498a2d30642d78f5a8a8e6ef8b9fe376af0214a0ae8be8dcff7dd4ae0b7`  
		Last Modified: Mon, 29 Apr 2024 18:54:47 GMT  
		Size: 16.3 MB (16323223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c8562d409f3ee8af39228c461e43fed8efb3368027910dee2e701b4328a3726`  
		Last Modified: Mon, 29 Apr 2024 18:54:47 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:devel-threaded` - unknown; unknown

```console
$ docker pull perl@sha256:75a19a75fad699072e950eb8a9c428f71adbeccdb1bdd5cb0ca256ca7c845ce3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.2 MB (15200140 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb60501608e26f70269f27817e6fe074b3572d1f286e0cf0158673ff4a922438`

```dockerfile
```

-	Layers:
	-	`sha256:0c8f91c1d799acd9b00ba1d8dc643d5e1c1ab2af8de32fd78f82e13d78607e53`  
		Last Modified: Mon, 29 Apr 2024 18:54:47 GMT  
		Size: 15.2 MB (15183980 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3347d8e8203dcf4d4a5702ecffcf1d420023b4d03a39d3b92b5813c8cce3ca8b`  
		Last Modified: Mon, 29 Apr 2024 18:54:47 GMT  
		Size: 16.2 KB (16160 bytes)  
		MIME: application/vnd.in-toto+json
