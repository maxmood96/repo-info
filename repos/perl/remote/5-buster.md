## `perl:5-buster`

```console
$ docker pull perl@sha256:4a440989dd32d587817932491a5015129793b57c8d0edb2caac575c44f5512cc
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

### `perl:5-buster` - linux; amd64

```console
$ docker pull perl@sha256:2884925500cef305090ef75797593f03b80a4fef58d22bdf9dd270eb7a2cef4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **327.6 MB (327562862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5cf2206e2a40272ae237c03b8c5b7955d173eb36b80fd336b33c8a58f4fa1f49`
-	Default Command: `["perl5.38.2","-de0"]`

```dockerfile
# Sat, 20 Jan 2024 20:51:34 GMT
ADD file:dccb5d0cbcf502fb7c4135575f44ac26d665fc92f50546f3a7f9e4d433726453 in / 
# Sat, 20 Jan 2024 20:51:34 GMT
CMD ["bash"]
# Sat, 20 Jan 2024 20:51:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 20 Jan 2024 20:51:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 20 Jan 2024 20:51:34 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 20 Jan 2024 20:51:34 GMT
WORKDIR /usr/src/perl
# Sat, 20 Jan 2024 20:51:34 GMT
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/P/PE/PEVANS/perl-5.38.2.tar.gz -o perl-5.38.2.tar.gz     && echo 'a0a31534451eb7b83c7d6594a497543a54d488bc90ca00f5e34762577f40655e *perl-5.38.2.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.38.2.tar.gz -C /usr/src/perl     && rm perl-5.38.2.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997014/cpm -o /usr/local/bin/cpm     && echo 'ee525f2493e36c6f688eddabaf53a51c4d3b2a4ebaa81576ac8b9f78ab57f4a1 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Sat, 20 Jan 2024 20:51:34 GMT
WORKDIR /usr/src/app
# Sat, 20 Jan 2024 20:51:34 GMT
CMD ["perl5.38.2" "-de0"]
```

-	Layers:
	-	`sha256:544676cb5e57a1ca47f178393253edded2bd54fba92674c7384013b4ddc87226`  
		Last Modified: Tue, 13 Feb 2024 00:43:09 GMT  
		Size: 50.5 MB (50500120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:783b6a2cbfde6d2dad8afded854e09b5b1ebda2fb638638c0f16b27d412ef7e3`  
		Last Modified: Tue, 13 Feb 2024 01:32:48 GMT  
		Size: 17.6 MB (17584782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c92b93a33a64c463f31b9f608a72574ce897c145372a32153f25a2df03b3eed`  
		Last Modified: Tue, 13 Feb 2024 01:33:03 GMT  
		Size: 51.9 MB (51876546 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5506dab13b722a0a2167c56d87ab89be676de83954672d39ea7d159e992a169`  
		Last Modified: Tue, 13 Feb 2024 01:33:34 GMT  
		Size: 191.9 MB (191934438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b9761d04c092b70ad836de1a4ce0d040b734bb99bb72bcbdd7dff6d273e3e48`  
		Last Modified: Tue, 13 Feb 2024 03:05:00 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc95e554270e7c719ac111e21db3ba66446f8a3f0e5a375bff405f62ba29097e`  
		Last Modified: Tue, 13 Feb 2024 03:05:00 GMT  
		Size: 15.7 MB (15666712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8bb0b5ce66c25e0724b8ac5c1b33f3e5bc0da88f317692c0eb35e8d3371f0d2`  
		Last Modified: Tue, 13 Feb 2024 03:04:59 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:5-buster` - unknown; unknown

```console
$ docker pull perl@sha256:09069979474757d02053b55f1ca57f9a3e0e8c6b64d7cd5abc1331f73a94b819
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.6 MB (13622956 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea6ea37b3d69276ea1262c56d68edaab63159a4da088f3915b83bfd18737ab1b`

```dockerfile
```

-	Layers:
	-	`sha256:b61a9090dbb90347aa5c447ca124d10d83f28f4472f29e6bc60073f7dddb2602`  
		Last Modified: Tue, 13 Feb 2024 03:05:00 GMT  
		Size: 13.6 MB (13606688 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9e8540cc8f0d9c1549884cedf1b7a49b17a9b75ce3c0dce3b3c910ebc9d03fcb`  
		Last Modified: Tue, 13 Feb 2024 03:05:00 GMT  
		Size: 16.3 KB (16268 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:5-buster` - linux; arm variant v7

```console
$ docker pull perl@sha256:27e16966fdcfe75798c25a0060da429df857827b63e8f8e46a1870b00eb8b1e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.5 MB (292508674 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69299d2ca421d56ed62648693585ed42f160107155a126472760b7681cd5c10c`
-	Default Command: `["perl5.38.2","-de0"]`

```dockerfile
# Sat, 20 Jan 2024 20:51:34 GMT
ADD file:952ff0908ecc63aa19ee3459c5e4ffbf10a0917e72f12212cec4e26ca37e18d3 in / 
# Sat, 20 Jan 2024 20:51:34 GMT
CMD ["bash"]
# Sat, 20 Jan 2024 20:51:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 20 Jan 2024 20:51:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 20 Jan 2024 20:51:34 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 20 Jan 2024 20:51:34 GMT
WORKDIR /usr/src/perl
# Sat, 20 Jan 2024 20:51:34 GMT
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/P/PE/PEVANS/perl-5.38.2.tar.gz -o perl-5.38.2.tar.gz     && echo 'a0a31534451eb7b83c7d6594a497543a54d488bc90ca00f5e34762577f40655e *perl-5.38.2.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.38.2.tar.gz -C /usr/src/perl     && rm perl-5.38.2.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997014/cpm -o /usr/local/bin/cpm     && echo 'ee525f2493e36c6f688eddabaf53a51c4d3b2a4ebaa81576ac8b9f78ab57f4a1 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Sat, 20 Jan 2024 20:51:34 GMT
WORKDIR /usr/src/app
# Sat, 20 Jan 2024 20:51:34 GMT
CMD ["perl5.38.2" "-de0"]
```

-	Layers:
	-	`sha256:23a6e5471cecf9aa4fa6cf1fd7037e25b9e75821953151df1a9eb5cac88d5dae`  
		Last Modified: Tue, 13 Feb 2024 01:28:01 GMT  
		Size: 46.0 MB (45967625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79b8cddb6bb767facfd385a827797ee92293ab687d7a0bd51dcc3e4fdf2e5410`  
		Last Modified: Tue, 13 Feb 2024 04:29:37 GMT  
		Size: 16.2 MB (16216342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:540545321e809bdd3253dc3e501c07157ca494eeb57e88cfc5f7c5ee705676c6`  
		Last Modified: Tue, 13 Feb 2024 04:29:56 GMT  
		Size: 47.4 MB (47410097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:508c05504c73b82e0130fe371cfb5de03fef9bf8a98195962243261db202e8fb`  
		Last Modified: Tue, 13 Feb 2024 04:30:34 GMT  
		Size: 168.1 MB (168133783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2285ad574487490cbbe1ca7cc3cb0fa7f782cf5408056afe7e3075c875dd145`  
		Last Modified: Thu, 15 Feb 2024 04:00:16 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0f5c4a81b65555fcc6ebc6b4fdba04adb175999b5e8006945439589cfc6ea4d`  
		Last Modified: Thu, 15 Feb 2024 04:00:18 GMT  
		Size: 14.8 MB (14780561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4477627fc6078a7906dbab95aaac99fc993db6b49d7a7a00c2677144585a366e`  
		Last Modified: Thu, 15 Feb 2024 04:00:18 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:5-buster` - unknown; unknown

```console
$ docker pull perl@sha256:4e20b754b9d7c756b893a40c749f0491acd05cd0ce1cbf9848e6abd34bbe947e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.5 MB (13450632 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0138ce0fd19964e20718908cdb3412a5e2327d70d767ea6f70a04174c7d3682`

```dockerfile
```

-	Layers:
	-	`sha256:4d015af59cac9187a6c4debc2ce2bcf4ba579e145d288860fdae5fc7d7ef8d06`  
		Last Modified: Thu, 15 Feb 2024 04:00:17 GMT  
		Size: 13.4 MB (13434286 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5a008fb0e16b8d12c3ceb78d26d3d6e2d80f89b61768ab68fee550abeb547a14`  
		Last Modified: Thu, 15 Feb 2024 04:00:16 GMT  
		Size: 16.3 KB (16346 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:5-buster` - linux; arm64 variant v8

```console
$ docker pull perl@sha256:ed23df57380e106f710f09ca4f3c6839780f826e657f88efd45530727a03de45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **318.1 MB (318075840 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3057482dc56e32933d145adde5f5925581a52d8f7a147bb593f38972b9580944`
-	Default Command: `["perl5.38.2","-de0"]`

```dockerfile
# Sat, 20 Jan 2024 20:51:34 GMT
ADD file:d671633736a15466494172d0076cd1a54d5c7a6b2972f9e84d0fb5136ec19f80 in / 
# Sat, 20 Jan 2024 20:51:34 GMT
CMD ["bash"]
# Sat, 20 Jan 2024 20:51:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 20 Jan 2024 20:51:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 20 Jan 2024 20:51:34 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 20 Jan 2024 20:51:34 GMT
WORKDIR /usr/src/perl
# Sat, 20 Jan 2024 20:51:34 GMT
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/P/PE/PEVANS/perl-5.38.2.tar.gz -o perl-5.38.2.tar.gz     && echo 'a0a31534451eb7b83c7d6594a497543a54d488bc90ca00f5e34762577f40655e *perl-5.38.2.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.38.2.tar.gz -C /usr/src/perl     && rm perl-5.38.2.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997014/cpm -o /usr/local/bin/cpm     && echo 'ee525f2493e36c6f688eddabaf53a51c4d3b2a4ebaa81576ac8b9f78ab57f4a1 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Sat, 20 Jan 2024 20:51:34 GMT
WORKDIR /usr/src/app
# Sat, 20 Jan 2024 20:51:34 GMT
CMD ["perl5.38.2" "-de0"]
```

-	Layers:
	-	`sha256:b2f3ac0fe192916cc6604d5941f01da385bf4b3d3bad97186f040b26e521c464`  
		Last Modified: Tue, 13 Feb 2024 00:45:57 GMT  
		Size: 49.3 MB (49288763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccd719c7fe078c8b5c670b220e68b3d40297d4c2b03ce37f0f0db8c8c4243917`  
		Last Modified: Tue, 13 Feb 2024 01:48:29 GMT  
		Size: 17.5 MB (17455606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b4c6bc7c3a0dfb86749a480f02c7de49c95ed599190a22c2b030956c209624b`  
		Last Modified: Tue, 13 Feb 2024 01:48:43 GMT  
		Size: 52.2 MB (52224578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db194eb11c11aaae27c605c4494c48ff5c6fed400c810b6c101bff8d0e875459`  
		Last Modified: Tue, 13 Feb 2024 01:49:07 GMT  
		Size: 183.5 MB (183499542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d16b204fe2128f6051eadc6b5023daa97aa826bd241f9a1f893c6edd3d4bacfc`  
		Last Modified: Wed, 14 Feb 2024 01:41:39 GMT  
		Size: 135.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08e22dec357530b38d70282b17241c519ad78f38d9486be4d5662750961df7e7`  
		Last Modified: Wed, 14 Feb 2024 01:41:42 GMT  
		Size: 15.6 MB (15607085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fec2f1e081e909ce06f63411b7378c7aebbaf361f3bc8d9b2f0d83abccce9d99`  
		Last Modified: Wed, 14 Feb 2024 01:41:41 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:5-buster` - unknown; unknown

```console
$ docker pull perl@sha256:fc9b444f7ea90269918133a44b831837bda9c776cd9ba0869c1541668b914c9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.6 MB (13614993 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b035b648c1fbc1d2eced2eda8b53d381624967502e0397b8f0aa44e216eae3d`

```dockerfile
```

-	Layers:
	-	`sha256:84f36210bab4bb94251af72b8962834ced995fa3968672dbb77eec73ae54f875`  
		Last Modified: Wed, 14 Feb 2024 01:41:40 GMT  
		Size: 13.6 MB (13598713 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3dc11a728d238311fb96e05855026bffa641e001633cfb1f9d5a7fb473f56a2e`  
		Last Modified: Wed, 14 Feb 2024 01:41:39 GMT  
		Size: 16.3 KB (16280 bytes)  
		MIME: application/vnd.in-toto+json

### `perl:5-buster` - linux; 386

```console
$ docker pull perl@sha256:3bf5408cc0de625be00e63ab8e051a6f60d682f0573cedccc1ded5f6546899ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **336.5 MB (336489788 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d6deae766d21f18d0fcdf134501f4b9813e7682c501bdd0abe3ee6b412c5c77`
-	Default Command: `["perl5.38.2","-de0"]`

```dockerfile
# Sat, 20 Jan 2024 20:51:34 GMT
ADD file:654c015ee394379d17dbff41ad51721cde33b46fa1db3b0e9a7d54473d92d291 in / 
# Sat, 20 Jan 2024 20:51:34 GMT
CMD ["bash"]
# Sat, 20 Jan 2024 20:51:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 20 Jan 2024 20:51:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 20 Jan 2024 20:51:34 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 20 Jan 2024 20:51:34 GMT
WORKDIR /usr/src/perl
# Sat, 20 Jan 2024 20:51:34 GMT
RUN true     && curl -fL https://cpan.metacpan.org/authors/id/P/PE/PEVANS/perl-5.38.2.tar.gz -o perl-5.38.2.tar.gz     && echo 'a0a31534451eb7b83c7d6594a497543a54d488bc90ca00f5e34762577f40655e *perl-5.38.2.tar.gz' | sha256sum --strict --check -     && tar --strip-components=1 -xaf perl-5.38.2.tar.gz -C /usr/src/perl     && rm perl-5.38.2.tar.gz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -fLO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7047.tar.gz     && echo '963e63c6e1a8725ff2f624e9086396ae150db51dd0a337c3781d09a994af05a5 *App-cpanminus-1.7047.tar.gz' | sha256sum --strict --check -     && tar -xzf App-cpanminus-1.7047.tar.gz && cd App-cpanminus-1.7047 && perl bin/cpanm . && cd /root     && cpanm IO::Socket::SSL     && curl -fL https://raw.githubusercontent.com/skaji/cpm/0.997014/cpm -o /usr/local/bin/cpm     && echo 'ee525f2493e36c6f688eddabaf53a51c4d3b2a4ebaa81576ac8b9f78ab57f4a1 */usr/local/bin/cpm' | sha256sum --strict --check -     && chmod +x /usr/local/bin/cpm     && true     && rm -fr /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7047* /tmp/*     && cpanm --version && cpm --version # buildkit
# Sat, 20 Jan 2024 20:51:34 GMT
WORKDIR /usr/src/app
# Sat, 20 Jan 2024 20:51:34 GMT
CMD ["perl5.38.2" "-de0"]
```

-	Layers:
	-	`sha256:33a96960e66e0a13921d9c0fbd1ff84e40544f75b84b3cb7124dc858fc844dc3`  
		Last Modified: Tue, 13 Feb 2024 00:44:58 GMT  
		Size: 51.3 MB (51255359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78788b06b363de6c8e3b44276527f47f5277530dc33ff6a512c93b0b96fb288a`  
		Last Modified: Tue, 13 Feb 2024 01:32:13 GMT  
		Size: 18.1 MB (18099425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c395b259eaee16d252933b055fc10e238ccf180dd0e226f790cc4d6d05ee33a`  
		Last Modified: Tue, 13 Feb 2024 01:32:36 GMT  
		Size: 53.5 MB (53491004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5394ce220a4fdfe5a7557da33b1d28ce42579dd6401bfcece4be46f785212cb5`  
		Last Modified: Tue, 13 Feb 2024 01:33:21 GMT  
		Size: 198.5 MB (198470106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b9761d04c092b70ad836de1a4ce0d040b734bb99bb72bcbdd7dff6d273e3e48`  
		Last Modified: Tue, 13 Feb 2024 03:05:00 GMT  
		Size: 133.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40a305b58f0908701a99b83872b359ae09eb5431c5058492581d1c81003df7fa`  
		Last Modified: Tue, 13 Feb 2024 03:05:48 GMT  
		Size: 15.2 MB (15173632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:250b67e2f4786ff06428c6114c07ee0fa54e3af10db3766ad59745e5d7fd52ea`  
		Last Modified: Tue, 13 Feb 2024 03:05:47 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `perl:5-buster` - unknown; unknown

```console
$ docker pull perl@sha256:c2e1ccde69777309936721a238175d5ddaeb8cc384857ef91bee7317ffff94f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.6 MB (13626384 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6133026467f4e2bbcc177905b276914e870ffd40f37116d04d1465dc020156a5`

```dockerfile
```

-	Layers:
	-	`sha256:a7a77121fec833900a888e9236f56da0e6a52425cb3806ae73c7beb8632252e0`  
		Last Modified: Tue, 13 Feb 2024 03:05:48 GMT  
		Size: 13.6 MB (13610150 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ca9f9548186bb1ebda75a1493987fb454b20d0f374f4f65f312418736493f928`  
		Last Modified: Tue, 13 Feb 2024 03:05:47 GMT  
		Size: 16.2 KB (16234 bytes)  
		MIME: application/vnd.in-toto+json
