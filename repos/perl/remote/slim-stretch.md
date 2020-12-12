## `perl:slim-stretch`

```console
$ docker pull perl@sha256:b69c1161781c6403673f489a3168c9885e151cae32e27613d540a190e4b852d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `perl:slim-stretch` - linux; amd64

```console
$ docker pull perl@sha256:d6b79fea33aa6c484379f4dd52d88e2e83d2ab806801e00a7ef831e478a5ef8d
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.1 MB (37119154 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ab9de9388ea35215f8d88163f87710e84817edfcc3edfe591c001890038ffa0`
-	Default Command: `["perl5.32.0","-de0"]`

```dockerfile
# Fri, 11 Dec 2020 02:08:58 GMT
ADD file:f03e68a10b84e2342cfffbb8cdec1117c7f5e5d0dd004072e84efb62cfdf157c in / 
# Fri, 11 Dec 2020 02:08:58 GMT
CMD ["bash"]
# Fri, 11 Dec 2020 17:41:18 GMT
LABEL maintainer=Peter Martini <PeterCMartini@GMail.com>, Zak B. Elep <zakame@cpan.org>
# Fri, 11 Dec 2020 17:41:19 GMT
COPY file:3744c5cc39cdbdcae10db09a1f0f399005a79f93c237b387a72ff5710cdd458c in /usr/src/perl/ 
# Fri, 11 Dec 2020 17:41:19 GMT
WORKDIR /usr/src/perl
# Fri, 11 Dec 2020 17:52:05 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        xz-utils     && curl -SL https://www.cpan.org/src/5.0/perl-5.32.0.tar.xz -o perl-5.32.0.tar.xz     && echo '6f436b447cf56d22464f980fac1916e707a040e96d52172984c5d184c09b859b *perl-5.32.0.tar.xz' | sha256sum -c -     && tar --strip-components=1 -xaf perl-5.32.0.tar.xz -C /usr/src/perl     && rm perl-5.32.0.tar.xz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -LO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7044.tar.gz     && echo '9b60767fe40752ef7a9d3f13f19060a63389a5c23acc3e9827e19b75500f81f3 *App-cpanminus-1.7044.tar.gz' | sha256sum -c -     && tar -xzf App-cpanminus-1.7044.tar.gz && cd App-cpanminus-1.7044 && perl bin/cpanm . && cd /root     && savedPackages="make netbase"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr ./cpanm /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7044* /tmp/*
# Fri, 11 Dec 2020 17:52:05 GMT
WORKDIR /
# Fri, 11 Dec 2020 17:52:05 GMT
CMD ["perl5.32.0" "-de0"]
```

-	Layers:
	-	`sha256:e50c3c9ef5a201a24959788dcbc7ebf88d95c63e132a4d7396ce541127afd88e`  
		Last Modified: Fri, 11 Dec 2020 02:15:43 GMT  
		Size: 22.5 MB (22527860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fa5f0a5fab8859009114fae61efeecd83942b3977402e19e946cc2cd1346d9f`  
		Last Modified: Fri, 11 Dec 2020 19:18:17 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d20cbced5f12d145623efa200bbf9aacf90a3e79fb0183155a9f5a702e678ce1`  
		Last Modified: Fri, 11 Dec 2020 19:18:21 GMT  
		Size: 14.6 MB (14591118 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `perl:slim-stretch` - linux; arm variant v7

```console
$ docker pull perl@sha256:322d7b83bd68efd2c81f68485e5a6d162487cdaa2711dc11d3a593394a4a1eca
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.1 MB (33052961 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18bef386fd785ce39a644573b092b090a3bfe86387ece21f9a4cc38c807dd031`
-	Default Command: `["perl5.32.0","-de0"]`

```dockerfile
# Fri, 11 Dec 2020 02:28:33 GMT
ADD file:a5ae44ff42f691e7afa1f743d1f05f6fd72d9c1737ae20b97977f9de76811260 in / 
# Fri, 11 Dec 2020 02:28:34 GMT
CMD ["bash"]
# Fri, 11 Dec 2020 17:20:37 GMT
LABEL maintainer=Peter Martini <PeterCMartini@GMail.com>, Zak B. Elep <zakame@cpan.org>
# Fri, 11 Dec 2020 17:20:37 GMT
COPY file:3744c5cc39cdbdcae10db09a1f0f399005a79f93c237b387a72ff5710cdd458c in /usr/src/perl/ 
# Fri, 11 Dec 2020 17:20:39 GMT
WORKDIR /usr/src/perl
# Fri, 11 Dec 2020 17:31:15 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        xz-utils     && curl -SL https://www.cpan.org/src/5.0/perl-5.32.0.tar.xz -o perl-5.32.0.tar.xz     && echo '6f436b447cf56d22464f980fac1916e707a040e96d52172984c5d184c09b859b *perl-5.32.0.tar.xz' | sha256sum -c -     && tar --strip-components=1 -xaf perl-5.32.0.tar.xz -C /usr/src/perl     && rm perl-5.32.0.tar.xz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -LO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7044.tar.gz     && echo '9b60767fe40752ef7a9d3f13f19060a63389a5c23acc3e9827e19b75500f81f3 *App-cpanminus-1.7044.tar.gz' | sha256sum -c -     && tar -xzf App-cpanminus-1.7044.tar.gz && cd App-cpanminus-1.7044 && perl bin/cpanm . && cd /root     && savedPackages="make netbase"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr ./cpanm /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7044* /tmp/*
# Fri, 11 Dec 2020 17:31:17 GMT
WORKDIR /
# Fri, 11 Dec 2020 17:31:18 GMT
CMD ["perl5.32.0" "-de0"]
```

-	Layers:
	-	`sha256:3844aeda5f39338d766015a56d78b18d6d4d4b95b0e6b41f8d37105ee5b91a80`  
		Last Modified: Fri, 11 Dec 2020 02:37:12 GMT  
		Size: 19.3 MB (19313560 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8af3e5093238acf1673b30d5556cdd1270714b7e3cc8684eec7589fe938c9f99`  
		Last Modified: Fri, 11 Dec 2020 20:36:17 GMT  
		Size: 202.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a09b91c59174abff32fe290ac38407f7eb092ddaa50bd78777f1ad43488da2fb`  
		Last Modified: Fri, 11 Dec 2020 20:36:22 GMT  
		Size: 13.7 MB (13739199 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `perl:slim-stretch` - linux; arm64 variant v8

```console
$ docker pull perl@sha256:b4ed7b4459fa8dd36d68bc5e3763854ae12a20377923a120dfed95e1d2350681
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.8 MB (34787452 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10b43303332bb513a041c4833044c5e2e63c251f0ccf290a249eaefc30ff5a8a`
-	Default Command: `["perl5.32.0","-de0"]`

```dockerfile
# Fri, 11 Dec 2020 02:48:42 GMT
ADD file:2efe3cccad076777e72be01a4380984d961a457c67dad3041063307ce1519c4d in / 
# Fri, 11 Dec 2020 02:48:44 GMT
CMD ["bash"]
# Fri, 11 Dec 2020 19:46:08 GMT
LABEL maintainer=Peter Martini <PeterCMartini@GMail.com>, Zak B. Elep <zakame@cpan.org>
# Fri, 11 Dec 2020 19:46:09 GMT
COPY file:3744c5cc39cdbdcae10db09a1f0f399005a79f93c237b387a72ff5710cdd458c in /usr/src/perl/ 
# Fri, 11 Dec 2020 19:46:09 GMT
WORKDIR /usr/src/perl
# Fri, 11 Dec 2020 19:56:26 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        xz-utils     && curl -SL https://www.cpan.org/src/5.0/perl-5.32.0.tar.xz -o perl-5.32.0.tar.xz     && echo '6f436b447cf56d22464f980fac1916e707a040e96d52172984c5d184c09b859b *perl-5.32.0.tar.xz' | sha256sum -c -     && tar --strip-components=1 -xaf perl-5.32.0.tar.xz -C /usr/src/perl     && rm perl-5.32.0.tar.xz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -LO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7044.tar.gz     && echo '9b60767fe40752ef7a9d3f13f19060a63389a5c23acc3e9827e19b75500f81f3 *App-cpanminus-1.7044.tar.gz' | sha256sum -c -     && tar -xzf App-cpanminus-1.7044.tar.gz && cd App-cpanminus-1.7044 && perl bin/cpanm . && cd /root     && savedPackages="make netbase"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr ./cpanm /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7044* /tmp/*
# Fri, 11 Dec 2020 19:56:28 GMT
WORKDIR /
# Fri, 11 Dec 2020 19:56:29 GMT
CMD ["perl5.32.0" "-de0"]
```

-	Layers:
	-	`sha256:15531941ccc12369b70088bb4e7b58263a2363c37d600f0ec7f4b7532efe6685`  
		Last Modified: Fri, 11 Dec 2020 02:56:00 GMT  
		Size: 20.4 MB (20387882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec05173d597354ee2bda33b26b414db1c98918fdf388a21c7af1ca20cc3d4800`  
		Last Modified: Fri, 11 Dec 2020 23:03:34 GMT  
		Size: 204.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e7ba016c2c8e8bd6095d4eeb976d3d4f88fd43693d6f06852b403e32bb3dd26`  
		Last Modified: Fri, 11 Dec 2020 23:03:40 GMT  
		Size: 14.4 MB (14399366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `perl:slim-stretch` - linux; 386

```console
$ docker pull perl@sha256:dd4a5add110e5cb4d11a6a1a7734d9276190a925930e350894d75ae9b217edc4
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.2 MB (37238168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb11ef5b7a45d568dc9b2049ec9917e4ce630912fc02f5d350fa0b2d161ac3bd`
-	Default Command: `["perl5.32.0","-de0"]`

```dockerfile
# Tue, 17 Nov 2020 20:23:25 GMT
ADD file:6d0d227a50cb77b9603ef598794fe0f583312a776daf61e7cd7e5493260354c9 in / 
# Tue, 17 Nov 2020 20:23:25 GMT
CMD ["bash"]
# Wed, 18 Nov 2020 07:51:32 GMT
LABEL maintainer=Peter Martini <PeterCMartini@GMail.com>, Zak B. Elep <zakame@cpan.org>
# Wed, 18 Nov 2020 07:51:33 GMT
COPY file:3744c5cc39cdbdcae10db09a1f0f399005a79f93c237b387a72ff5710cdd458c in /usr/src/perl/ 
# Wed, 18 Nov 2020 07:51:33 GMT
WORKDIR /usr/src/perl
# Wed, 18 Nov 2020 08:03:20 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        xz-utils     && curl -SL https://www.cpan.org/src/5.0/perl-5.32.0.tar.xz -o perl-5.32.0.tar.xz     && echo '6f436b447cf56d22464f980fac1916e707a040e96d52172984c5d184c09b859b *perl-5.32.0.tar.xz' | sha256sum -c -     && tar --strip-components=1 -xaf perl-5.32.0.tar.xz -C /usr/src/perl     && rm perl-5.32.0.tar.xz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -LO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7044.tar.gz     && echo '9b60767fe40752ef7a9d3f13f19060a63389a5c23acc3e9827e19b75500f81f3 *App-cpanminus-1.7044.tar.gz' | sha256sum -c -     && tar -xzf App-cpanminus-1.7044.tar.gz && cd App-cpanminus-1.7044 && perl bin/cpanm . && cd /root     && savedPackages="make netbase"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr ./cpanm /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7044* /tmp/*
# Wed, 18 Nov 2020 08:03:21 GMT
WORKDIR /
# Wed, 18 Nov 2020 08:03:21 GMT
CMD ["perl5.32.0" "-de0"]
```

-	Layers:
	-	`sha256:657537e4548aa71eaa79344d36c62360306a66e11486f3d90ce21ecef49a62cb`  
		Last Modified: Tue, 17 Nov 2020 20:30:22 GMT  
		Size: 23.2 MB (23154739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f64b77b89bcb46f661c77301eaa530b6e783fe07d3bb2413ed1f41906305c316`  
		Last Modified: Wed, 18 Nov 2020 12:33:02 GMT  
		Size: 177.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:694ac0c6290fa4c0e5cadc8c5adfe18c29853a8bf9fdd0ac7342df2b7f85f4b0`  
		Last Modified: Wed, 18 Nov 2020 12:33:07 GMT  
		Size: 14.1 MB (14083252 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `perl:slim-stretch` - linux; ppc64le

```console
$ docker pull perl@sha256:ef09d2eb473c046e6c9f8098b3a7fef9875dfbba0740aa4ed68e13433e884eb6
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.2 MB (37221053 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc6939da09b4685b49a0814e877fbcf985bc2a23ba434c4e52ba6c01c6c5c0f2`
-	Default Command: `["perl5.32.0","-de0"]`

```dockerfile
# Tue, 09 Jun 2020 01:25:38 GMT
ADD file:41ec53d65aa183c2835f73989c9e4922f818e59774811eaa6e7395e5a36d5eab in / 
# Tue, 09 Jun 2020 01:25:42 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 14:27:23 GMT
LABEL maintainer=Peter Martini <PeterCMartini@GMail.com>, Zak B. Elep <zakame@cpan.org>
# Mon, 22 Jun 2020 15:40:21 GMT
COPY file:3744c5cc39cdbdcae10db09a1f0f399005a79f93c237b387a72ff5710cdd458c in /usr/src/perl/ 
# Mon, 22 Jun 2020 15:40:24 GMT
WORKDIR /usr/src/perl
# Mon, 22 Jun 2020 15:49:42 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        xz-utils     && curl -SL https://www.cpan.org/src/5.0/perl-5.32.0.tar.xz -o perl-5.32.0.tar.xz     && echo '6f436b447cf56d22464f980fac1916e707a040e96d52172984c5d184c09b859b *perl-5.32.0.tar.xz' | sha256sum -c -     && tar --strip-components=1 -xaf perl-5.32.0.tar.xz -C /usr/src/perl     && rm perl-5.32.0.tar.xz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -LO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7044.tar.gz     && echo '9b60767fe40752ef7a9d3f13f19060a63389a5c23acc3e9827e19b75500f81f3 *App-cpanminus-1.7044.tar.gz' | sha256sum -c -     && tar -xzf App-cpanminus-1.7044.tar.gz && cd App-cpanminus-1.7044 && perl bin/cpanm . && cd /root     && savedPackages="make netbase"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr ./cpanm /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7044* /tmp/*
# Mon, 22 Jun 2020 15:49:49 GMT
WORKDIR /
# Mon, 22 Jun 2020 15:49:52 GMT
CMD ["perl5.32.0" "-de0"]
```

-	Layers:
	-	`sha256:a29e28607c9b96acae7ff89e56214e4339a87c59e40a6f030fa4cbcaab753f2c`  
		Last Modified: Tue, 09 Jun 2020 01:37:25 GMT  
		Size: 22.8 MB (22791269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0789a92ac122eecdf7b0bd168e70ec21062493b4fa3617f62eb7fd387e9d6780`  
		Last Modified: Mon, 22 Jun 2020 16:28:33 GMT  
		Size: 202.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b51e098d1488dc904c2ad47c4125a22de29c445c6aaad9ad48c920949933f27`  
		Last Modified: Mon, 22 Jun 2020 16:28:38 GMT  
		Size: 14.4 MB (14429582 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `perl:slim-stretch` - linux; s390x

```console
$ docker pull perl@sha256:7146bba14d71cdce8bd1c0461d2c192371c8bab9d849016c1aa3c3ed830cdff4
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.4 MB (37421460 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba2901811c2c8c82b4620055bacd2a71b4b7ceeba35e57cc4a5d216e4ef95038`
-	Default Command: `["perl5.32.0","-de0"]`

```dockerfile
# Tue, 09 Jun 2020 01:44:20 GMT
ADD file:b3e01a52177029e9c3ba14a708f5dd33a38777f05d0e43656aca742b2991b13c in / 
# Tue, 09 Jun 2020 01:44:22 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 04:04:12 GMT
LABEL maintainer=Peter Martini <PeterCMartini@GMail.com>, Zak B. Elep <zakame@cpan.org>
# Mon, 22 Jun 2020 16:00:38 GMT
COPY file:3744c5cc39cdbdcae10db09a1f0f399005a79f93c237b387a72ff5710cdd458c in /usr/src/perl/ 
# Mon, 22 Jun 2020 16:00:39 GMT
WORKDIR /usr/src/perl
# Mon, 22 Jun 2020 16:07:17 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends        bzip2        ca-certificates        curl        dpkg-dev        gcc        libc6-dev        make        netbase        patch        xz-utils     && curl -SL https://www.cpan.org/src/5.0/perl-5.32.0.tar.xz -o perl-5.32.0.tar.xz     && echo '6f436b447cf56d22464f980fac1916e707a040e96d52172984c5d184c09b859b *perl-5.32.0.tar.xz' | sha256sum -c -     && tar --strip-components=1 -xaf perl-5.32.0.tar.xz -C /usr/src/perl     && rm perl-5.32.0.tar.xz     && cat *.patch | patch -p1     && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"     && archBits="$(dpkg-architecture --query DEB_BUILD_ARCH_BITS)"     && archFlag="$([ "$archBits" = '64' ] && echo '-Duse64bitall' || echo '-Duse64bitint')"     && ./Configure -Darchname="$gnuArch" "$archFlag" -Duseshrplib -Dvendorprefix=/usr/local  -des     && make -j$(nproc)     && TEST_JOBS=$(nproc) make test_harness     && make install     && cd /usr/src     && curl -LO https://www.cpan.org/authors/id/M/MI/MIYAGAWA/App-cpanminus-1.7044.tar.gz     && echo '9b60767fe40752ef7a9d3f13f19060a63389a5c23acc3e9827e19b75500f81f3 *App-cpanminus-1.7044.tar.gz' | sha256sum -c -     && tar -xzf App-cpanminus-1.7044.tar.gz && cd App-cpanminus-1.7044 && perl bin/cpanm . && cd /root     && savedPackages="make netbase"     && apt-mark auto '.*' > /dev/null     && apt-mark manual $savedPackages     && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false     && rm -fr /var/cache/apt/* /var/lib/apt/lists/*     && rm -fr ./cpanm /root/.cpanm /usr/src/perl /usr/src/App-cpanminus-1.7044* /tmp/*
# Mon, 22 Jun 2020 16:07:18 GMT
WORKDIR /
# Mon, 22 Jun 2020 16:07:19 GMT
CMD ["perl5.32.0" "-de0"]
```

-	Layers:
	-	`sha256:428ea12d5f095d89f941ce335d5f799da515abfd0c161e7ee85e12cd3d97fd4e`  
		Last Modified: Tue, 09 Jun 2020 01:48:04 GMT  
		Size: 22.4 MB (22371004 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bda422b0ebe5506ce35e51f433e6f95412877201e00691a90070ae6509418a6`  
		Last Modified: Mon, 22 Jun 2020 16:32:54 GMT  
		Size: 202.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20d20fd97473b0068f2b823519fb8126c13e9f5b7477ff0785d497bb4d1e37bb`  
		Last Modified: Mon, 22 Jun 2020 16:32:56 GMT  
		Size: 15.1 MB (15050254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
