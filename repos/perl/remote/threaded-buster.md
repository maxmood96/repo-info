## `perl:threaded-buster`

```console
$ docker pull perl@sha256:86659052b0e6f3546404a4907027a0d85452b29d44ae3098652cf52b957c6d90
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `perl:threaded-buster` - linux; amd64

```console
$ docker pull perl@sha256:4c63531dc540216f2027a2a3f0f8fccdb83170b5a8c7c2bee2c90c6681b01bf0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **327.6 MB (327614971 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db3bc8a2ea454a62b7f07b96f1d78462d2476f6c57a113a5a4c7e47e13cf8e05`
-	Default Command: `["perl5.38.2","-de0"]`

```dockerfile
# Sun, 31 Dec 2023 10:01:19 GMT
ADD file:ac13007eb56f6e064fe27101dfa666f02b04f4ce9a2bcf3ade6cf6055562b7e8 in / 
# Sun, 31 Dec 2023 10:01:19 GMT
CMD ["bash"]
# Sun, 31 Dec 2023 10:01:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Sun, 31 Dec 2023 10:01:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Sun, 31 Dec 2023 10:01:19 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Sun, 31 Dec 2023 10:01:19 GMT
WORKDIR /usr/src/perl
# Sun, 31 Dec 2023 10:01:19 GMT
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/P/PE/PEVANS/perl-5.38.2.tar.gz -o perl-5.38.2.tar.gz     && echo 'a0a31534451eb7b83c7d6594a497543a54d488bc90ca00f5e34762577f40655e *perl-5.38.2.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.38.2.tar.gz -C /usr/src/perl     && rm perl-5.38.2.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997014/cpm -o /usr/local/bin/cpm     && echo 'ee525f2493e36c6f688eddabaf53a51c4d3b2a4ebaa81576ac8b9f78ab57f4a1 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Sun, 31 Dec 2023 10:01:19 GMT
WORKDIR /usr/src/app
# Sun, 31 Dec 2023 10:01:19 GMT
CMD ["perl5.38.2" "-de0"]
```

-	Layers:
	-	`sha256:7418de5ce68f67dad705c01c70a7bb811f9b886f8d7aac2b66110d376046fdcb`  
		Last Modified: Thu, 11 Jan 2024 02:43:26 GMT  
		Size: 50.5 MB (50500254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5caad11564dacebdfbe4a52e47aa5f32a8064c74da57cbd81c082761a657bd2`  
		Last Modified: Thu, 11 Jan 2024 04:46:40 GMT  
		Size: 17.6 MB (17584913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f06055ea198d6db62911c16ce4047a06d9b0be9f9682759234c61203342252fb`  
		Last Modified: Wed, 17 Jan 2024 02:02:02 GMT  
		Size: 51.9 MB (51877273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29dba922c11b20960594e74c195876d5037f2c70ff2d7cfa714f875d57a7efee`  
		Last Modified: Wed, 17 Jan 2024 02:02:35 GMT  
		Size: 191.9 MB (191932569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edaae4e8cb6c061633b47bbfc082be0bd4e2d1f56b89a91054e666a903f64056`  
		Last Modified: Wed, 17 Jan 2024 03:56:21 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c01696ac6da7ebdbda0cf7b237c6ca7ef6ff111658f171d25f7aa4b295945c7e`  
		Last Modified: Wed, 17 Jan 2024 03:56:22 GMT  
		Size: 15.7 MB (15719693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cda7428973c1c2c61084bc8c86ba73f145ba7c48e69854d18930bbe1eacb091`  
		Last Modified: Wed, 17 Jan 2024 03:56:21 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:threaded-buster` - unknown; unknown

```console
$ docker pull perl@sha256:70d41ab5c566c25a749302166e515339ccc76a029c942b2dafb7e22d8f92e605
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.6 MB (13623183 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14aa6e8b45130f5f47da4bcafeddecbdedf488f64d583689ff50444d38e746ec`

```dockerfile
```

-	Layers:
	-	`sha256:d754f5ab7919ae47d296a3964ba070d5c4b6801c951ef72bf394f085ab27ed0d`  
		Last Modified: Wed, 17 Jan 2024 03:56:21 GMT  
		Size: 13.6 MB (13606778 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:28030a6763a44a473ddfb19eb5fd698708fb8bd4740ca11034d6704ea9c207dc`  
		Last Modified: Wed, 17 Jan 2024 03:56:21 GMT  
		Size: 16.4 KB (16405 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:threaded-buster` - linux; arm variant v7

```console
$ docker pull perl@sha256:0e059a397c9a4b9da0e853910aa52bb5a0fa2afab14c360bf40d09ce88d78e99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.5 MB (292525230 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17e986b615ffb3475f5ee2dcb17a604c86d122126a516d2ea16ad65b21cfb528`
-	Default Command: `["perl5.38.2","-de0"]`

```dockerfile
# Sun, 31 Dec 2023 10:01:19 GMT
ADD file:7f9fc3dd3778509079c1f4010b0ef89a6910aa3a83b317c5134489675daccb47 in / 
# Sun, 31 Dec 2023 10:01:19 GMT
CMD ["bash"]
# Sun, 31 Dec 2023 10:01:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Sun, 31 Dec 2023 10:01:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Sun, 31 Dec 2023 10:01:19 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Sun, 31 Dec 2023 10:01:19 GMT
WORKDIR /usr/src/perl
# Sun, 31 Dec 2023 10:01:19 GMT
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/P/PE/PEVANS/perl-5.38.2.tar.gz -o perl-5.38.2.tar.gz     && echo 'a0a31534451eb7b83c7d6594a497543a54d488bc90ca00f5e34762577f40655e *perl-5.38.2.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.38.2.tar.gz -C /usr/src/perl     && rm perl-5.38.2.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997014/cpm -o /usr/local/bin/cpm     && echo 'ee525f2493e36c6f688eddabaf53a51c4d3b2a4ebaa81576ac8b9f78ab57f4a1 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Sun, 31 Dec 2023 10:01:19 GMT
WORKDIR /usr/src/app
# Sun, 31 Dec 2023 10:01:19 GMT
CMD ["perl5.38.2" "-de0"]
```

-	Layers:
	-	`sha256:c11d78fb5679ceced7c7aa83357081cad2ce04776bc24c72152ce12e6b5b8411`  
		Last Modified: Thu, 11 Jan 2024 02:49:46 GMT  
		Size: 46.0 MB (45967605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf675975f6adfaf2c5b813bb5cfaf951a864bd6c9f1cb87e7622e2381bdf947e`  
		Last Modified: Thu, 11 Jan 2024 03:31:37 GMT  
		Size: 16.2 MB (16216537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7908e6bb56f5fd563f9fd988126258215be6efb8f65248027684accc2ec7da05`  
		Last Modified: Thu, 11 Jan 2024 03:32:00 GMT  
		Size: 47.4 MB (47410050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8f4252a48a724cf42edd9fc4ee69dc65ed9d90d4f536bbcc302160dd304acec`  
		Last Modified: Thu, 11 Jan 2024 03:32:44 GMT  
		Size: 168.1 MB (168134110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d94346b2272d6b125da94fdfe4265d3c2082c69c9a479f7974c092de4677bba`  
		Last Modified: Fri, 12 Jan 2024 20:16:00 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffb25bed574e923989f8872302917096cbca88afcaf9486ed66afd310e55a053`  
		Last Modified: Fri, 12 Jan 2024 22:21:15 GMT  
		Size: 14.8 MB (14796659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ee409253c515e2edfe2c5cdc1c955f44db94bc719052207ccb44cfd09168435`  
		Last Modified: Fri, 12 Jan 2024 22:21:14 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:threaded-buster` - unknown; unknown

```console
$ docker pull perl@sha256:d622b335ee49d1e0faeab24193ef1fa88ecd34b526a6c91baad9a3e5aff33732
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.5 MB (13450196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b7047a64af5c7ce5c7d37a439c7b8d55226fc618b5776578bc695c7266bc758`

```dockerfile
```

-	Layers:
	-	`sha256:d27fc30b9209c87ca860f6ea9128c2afe6fd77057a299c2f8b3ee4e9708e66fd`  
		Last Modified: Fri, 12 Jan 2024 22:21:15 GMT  
		Size: 13.4 MB (13434376 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:674b8614dfee3807bcfc64646f2711922d86f02722bd9f8b5283ba0e154d3d99`  
		Last Modified: Fri, 12 Jan 2024 22:21:14 GMT  
		Size: 15.8 KB (15820 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:threaded-buster` - linux; arm64 variant v8

```console
$ docker pull perl@sha256:dd5a15b75e64133d056a9ac18b4d00657404b44f0c5d29799d6b34aaddda611d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **318.1 MB (318100372 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:781e0070eb18873cc7749ea453affc4d4183e52fdb7fc7cc8da0c0d2504c8779`
-	Default Command: `["perl5.38.2","-de0"]`

```dockerfile
# Sun, 31 Dec 2023 10:01:19 GMT
ADD file:e9cd54dd40d18756610852bf97172fae748b0dc8eb39d2fb1c97181382daed3b in / 
# Sun, 31 Dec 2023 10:01:19 GMT
CMD ["bash"]
# Sun, 31 Dec 2023 10:01:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Sun, 31 Dec 2023 10:01:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Sun, 31 Dec 2023 10:01:19 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Sun, 31 Dec 2023 10:01:19 GMT
WORKDIR /usr/src/perl
# Sun, 31 Dec 2023 10:01:19 GMT
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/P/PE/PEVANS/perl-5.38.2.tar.gz -o perl-5.38.2.tar.gz     && echo 'a0a31534451eb7b83c7d6594a497543a54d488bc90ca00f5e34762577f40655e *perl-5.38.2.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.38.2.tar.gz -C /usr/src/perl     && rm perl-5.38.2.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997014/cpm -o /usr/local/bin/cpm     && echo 'ee525f2493e36c6f688eddabaf53a51c4d3b2a4ebaa81576ac8b9f78ab57f4a1 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Sun, 31 Dec 2023 10:01:19 GMT
WORKDIR /usr/src/app
# Sun, 31 Dec 2023 10:01:19 GMT
CMD ["perl5.38.2" "-de0"]
```

-	Layers:
	-	`sha256:ff2e543b6a43ccfdb1731587b58c288c29eb3947f78a5877f4fd9bb8dfa918b5`  
		Last Modified: Thu, 11 Jan 2024 02:45:04 GMT  
		Size: 49.3 MB (49288871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c55c30648cccb646aaaa31c2ba4da656bdf016ad106c2cf694fc55e8c805598a`  
		Last Modified: Thu, 11 Jan 2024 09:35:54 GMT  
		Size: 17.5 MB (17455536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ee21614199544300bcc475788a9b95f2d40434d6c5f77aecbeb998ad95ba6c5`  
		Last Modified: Wed, 17 Jan 2024 03:00:51 GMT  
		Size: 52.2 MB (52225759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1191b84a5df3dd9297e0575e4387638b046ce486c3efe63387cdb65502df7b2e`  
		Last Modified: Wed, 17 Jan 2024 03:01:31 GMT  
		Size: 183.5 MB (183497324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ced95ef1ec3a044c4d8ee9fe1cc810beeb26aed35f9eebe797ee88f48e6b421`  
		Last Modified: Thu, 18 Jan 2024 04:24:45 GMT  
		Size: 136.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1a777e2ecc4f8d7b00233eaf26b9d5b50e929c1265d3484231c6f8ee7ca8d50`  
		Last Modified: Thu, 18 Jan 2024 04:41:36 GMT  
		Size: 15.6 MB (15632613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fae5715c5e1fafb68216391d332bbd47107fbf243f94bd3bde56c2932c11ed1`  
		Last Modified: Thu, 18 Jan 2024 04:41:35 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:threaded-buster` - unknown; unknown

```console
$ docker pull perl@sha256:832672aa0328aae066f6885a4c2b4ebfaec73417b00a96d03a65cff444c29e65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.6 MB (13614557 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab1126bc09fd97c76cc64fa099ce4b05611e092367c8db5d2bc624c36c6ecd79`

```dockerfile
```

-	Layers:
	-	`sha256:e6122ee2d722fa7a39233f5e3a934d4285bfc612713c700dd7276739cc2a1034`  
		Last Modified: Thu, 18 Jan 2024 04:41:36 GMT  
		Size: 13.6 MB (13598803 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bb8c7e5ce21a620cd70cab9b0d301e854729f5825701b3316e11246fb6fe9f0b`  
		Last Modified: Thu, 18 Jan 2024 04:41:35 GMT  
		Size: 15.8 KB (15754 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:threaded-buster` - linux; 386

```console
$ docker pull perl@sha256:0dfaed995e547439324701fb8bbb94409a2a1e54851d612491f26e90fddc9220
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **336.6 MB (336585056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acf085a45dd8cdab04fa31e14bd2fcaf558bfef6c1a0982e485c93e9f680a7da`
-	Default Command: `["perl5.38.2","-de0"]`

```dockerfile
# Sun, 31 Dec 2023 10:01:19 GMT
ADD file:1e68cfe2a77ca5be656fe9cf5a3e89e23630239ebc044ace148ba49124dbaf7a in / 
# Sun, 31 Dec 2023 10:01:19 GMT
CMD ["bash"]
# Sun, 31 Dec 2023 10:01:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Sun, 31 Dec 2023 10:01:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Sun, 31 Dec 2023 10:01:19 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Sun, 31 Dec 2023 10:01:19 GMT
WORKDIR /usr/src/perl
# Sun, 31 Dec 2023 10:01:19 GMT
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/P/PE/PEVANS/perl-5.38.2.tar.gz -o perl-5.38.2.tar.gz     && echo 'a0a31534451eb7b83c7d6594a497543a54d488bc90ca00f5e34762577f40655e *perl-5.38.2.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.38.2.tar.gz -C /usr/src/perl     && rm perl-5.38.2.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Dusethreads -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997014/cpm -o /usr/local/bin/cpm     && echo 'ee525f2493e36c6f688eddabaf53a51c4d3b2a4ebaa81576ac8b9f78ab57f4a1 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Sun, 31 Dec 2023 10:01:19 GMT
WORKDIR /usr/src/app
# Sun, 31 Dec 2023 10:01:19 GMT
CMD ["perl5.38.2" "-de0"]
```

-	Layers:
	-	`sha256:94764bf084b89ee796b567eb9a1b71857d957204137c0ec8781723a4b7ae71ae`  
		Last Modified: Thu, 11 Jan 2024 02:44:28 GMT  
		Size: 51.3 MB (51255203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:002489140685fac56869096dde7388de7e568f955020400561fda107e627e1aa`  
		Last Modified: Thu, 11 Jan 2024 04:44:28 GMT  
		Size: 18.1 MB (18099537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fa835d2a5a09c83165e9b25c208950833146120cc2f46949bc542839754452f`  
		Last Modified: Wed, 17 Jan 2024 01:52:47 GMT  
		Size: 53.5 MB (53491922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7109657d04599cf931790d46d75b51f77e26f5d624cf8b88ed6d0024b8d7b721`  
		Last Modified: Wed, 17 Jan 2024 01:53:32 GMT  
		Size: 198.5 MB (198470068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bceb5d3d60f9f94859e3d260d5d1cd057960893781689dd437e04ac7215ef74`  
		Last Modified: Wed, 17 Jan 2024 03:56:57 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4283e4744316a17411632850b55e1f5f34d634523aacee1ebc22126678139d1`  
		Last Modified: Wed, 17 Jan 2024 03:56:58 GMT  
		Size: 15.3 MB (15268058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63e985ac52f446d6f1486a120d392815bc44afdac0143efa3c8eeb5c8449ad2a`  
		Last Modified: Wed, 17 Jan 2024 03:56:57 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:threaded-buster` - unknown; unknown

```console
$ docker pull perl@sha256:1a351b269e2b0bbb5554285a1802b83999845ecd1c94e2a686f343e7abf83efb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.6 MB (13626611 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eff88e2d8fcc174a51547ab51fc7a76b48652fa95882a09755073fe69f62c010`

```dockerfile
```

-	Layers:
	-	`sha256:34054cd5d1ce331345b81c2980a23e8f2f5df31ad3cd38be5236a359ff487f53`  
		Last Modified: Wed, 17 Jan 2024 03:56:58 GMT  
		Size: 13.6 MB (13610240 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f1f15bb8825bb205c5598edaceb96bd167439e66a66fd48ed95ea50b6651f0db`  
		Last Modified: Wed, 17 Jan 2024 03:56:57 GMT  
		Size: 16.4 KB (16371 bytes)  
		MIME: application/vnd.in-toto+json
